# 03 — Función Clave: Índice de Incidencia con Semáforo

> Esta es la función central del producto. Una sola cosa, bien hecha, con variables precisas y metodología citable — no cinco capas genéricas. Todo lo demás (registral, urbanístico, catastral, servicios) es contexto de apoyo; **esta es la pieza que el usuario entiende en tres segundos y que ningún competidor identificado replica de esta forma.**

---

## 1. Qué problema resuelve, en una frase

> Ni la denuncia oficial ni el reporte vecinal, por separado, dicen la verdad sobre cuán insegura es una zona. **Un índice que combine ambos, con la misma metodología de bandas que usa el INEI para todo el país, sí.**

## 2. Por qué no es lo que ya existe — verificado, no supuesto

| Fuente existente | Qué hace | Qué le falta |
|---|---|---|
| **Mapa del Delito — MININTER** | Puntos de denuncia georreferenciados | Sin corrección de subregistro, sin índice, sin bandas, sin reportes ciudadanos |
| **IIC — INEI** (ver [`04-referencias-academicas.md`](../00-evaluacion/04-referencias-academicas.md)) | Índice compuesto con corrección estadística de subregistro y bandas oficiales | Es un producto **académico/administrativo**, a nivel distrital, publicado como investigación — no es un servicio de consulta en tiempo real, no incorpora reportes ciudadanos, no está embebido en una decisión de compra |
| **UbicaBien** (auditoría verificada, ver [`../04-startups/ubicabien-auditoria.md`](../04-startups/ubicabien-auditoria.md)) | Valorización, zonificación (sin digitalizar), conectividad, desastres | **Cero capa delictiva. Ausente por completo, en cualquier forma.** |
| **SpotCrime** | Híbrido denuncia + reporte, con app y API | Existe únicamente en Estados Unidos; no opera en el Perú ni está integrado a una decisión inmobiliaria |

**Ningún actor identificado combina las tres cosas a la vez: (a) fuente oficial corregida por subregistro, (b) reporte ciudadano verificado, (c) embebido en una decisión de compra de vivienda en Arequipa.** Esa combinación es la función clave.

---

## 3. Las dos fuentes de dato — y por qué ninguna alcanza sola

### 3.1 Denuncias oficiales — MININTER / SIDPOL, vía INEI

Miden lo que la policía registró. Su defecto conocido, documentado en la literatura:

> La disparidad entre las tasas sugeridas por las encuestas de victimización y las sugeridas por las estadísticas oficiales es consecuencia principalmente del **subreporte por parte de las víctimas** y del **subregistro por parte de la policía** — el fenómeno conocido como la **cifra negra del delito**.

*(Fundamento: A2 y B1–B3 en el catálogo de referencias; en Arequipa, la propia PNP reconoce subregistro de extorsión por temor a represalias.)*

### 3.2 Reportes ciudadanos — capa nueva, generada por el propio producto

Cada usuario que consulta una zona puede dejar un reporte breve, geolocalizado, con categoría de hecho y fecha. **No sustituye a la denuncia formal** —se le indica explícitamente al usuario que reporte también a la PNP— pero captura lo que la cifra negra esconde: el hecho que ocurrió y nunca se denunció.

Precedente directo: la literatura de *crowdsourcing* de seguridad en Latinoamérica confirma que sitios de reporte ciudadano ya **pasan información a las autoridades pertinentes** y **conectan al ciudadano con el gobierno y los medios** en varios países de la región — el mecanismo existe y funciona; no está aplicado a decisión inmobiliaria en Arequipa.

### 3.3 Por qué ninguna basta sola — evidencia de la tensión real

Se documentó una discrepancia real entre tres fuentes serias sobre la victimización de Arequipa (detalle completo en `04-referencias-academicas.md`):

| Fuente | Año del dato | Resultado |
|---|---|---|
| INEI — índice administrativo (IIC) | ~2021 | Arequipa **por debajo** del promedio nacional (0,357 vs. 0,37) |
| MININTER Qawaq — ranking de denuncias | 2019 | Arequipa en posición **media** entre ciudades grandes (33,0 %) |
| UCSP / prensa — encuesta directa | 2025 | Arequipa la **más alta** del país (33,5 %) |

> Tres metodologías, tres resultados distintos. Eso no invalida ninguna fuente: **demuestra que ninguna, por sí sola, captura la incidencia real.** Es el argumento empírico —no una opinión de diseño— para combinar fuente oficial y fuente ciudadana.

---

## 4. La fórmula

Se adopta, no se inventa, la lógica del INEI (promedio geométrico entre componentes correlacionados, normalización min-max, bandas categóricas oficiales), adaptada a dos fuentes por zona en lugar de tres pilares distritales:

### 4.1 Normalización de tasas

Siguiendo la convención INEI (fórmulas 3–4, p. 34 de A1): toda variable se expresa como **tasa por cada 10 000 habitantes**.

```
Tasa_por_10k = (Variable_zona / Población_zona) × 10 000
```

### 4.2 Corrección de subregistro — versión de alcance de curso

El INEI resuelve la cifra negra con un modelo de frontera de producción estocástica (máxima verosimilitud). Ese nivel de sofisticación econométrica **excede el alcance de un proyecto de curso**, y se declara así explícitamente — no se simula un rigor que no existe.

**Proxy adoptado para el prototipo:**

```
Factor_corrección_zona = Tasa_victimización_encuestada_distrito / Tasa_denuncia_oficial_distrito
D_corregida = D_observada × Factor_corrección_zona
```

El factor se calcula a nivel distrital cruzando la denuncia oficial (MININTER) contra la victimización autorreportada (UCSP/ENAPRES) del mismo distrito y período. Es una razón simple, no un modelo predictivo — **exactamente el nivel de rigor que un trabajo de pregrado puede sostener y defender**, con la ruta hacia el método completo (A1, A2) declarada como trabajo futuro.

### 4.3 Combinación de las dos fuentes

```
IIP_zona = (D_corregida^0.6 × R_ciudadana^0.4)^(1/(0.6+0.4))
```

Es un **promedio geométrico ponderado**: la fuente oficial pesa más (0.6) por su mayor validez estadística; la fuente ciudadana pesa menos (0.4) porque es nueva y su volumen crecerá con el uso, pero corrige la cifra negra que la fuente oficial no puede ver. El uso del promedio geométrico —y no una suma ponderada simple— sigue directamente la justificación del INEI: evita que una sola fuente con un valor extremo domine el resultado cuando ambas fuentes están correlacionadas.

### 4.4 Ponderación por severidad — no todo delito pesa igual

Siguiendo A3 (Ihlanfeldt & Mayock) y A4/A5 (Crime Harm Index): antes de calcular la tasa, cada hecho se pondera por categoría, no se cuenta como unidad simple.

| Categoría | Peso relativo | Fundamento |
|---|---|---|
| Robo con violencia, extorsión | Alto | A3: robo y agresión son las únicas categorías con efecto significativo comprobado sobre el valor de vivienda |
| Hurto a vivienda, robo al paso | Medio | Delitos más frecuentes en Arequipa (19,03 % y 21,05 % del total, ver `docs/03-region/02-arequipa.md`) |
| Faltas menores | Bajo | Sigue el principio de A4: contar todo por igual distorsiona la tendencia real |

*(La escala numérica exacta de pesos —como los días de prisión recomendados que usa el Danish Crime Harm Index— es una decisión de calibración posterior a validar con datos reales de Arequipa; no se fija un número arbitrario sin evidencia local.)*

---

## 5. El semáforo — adoptado del INEI, no inventado

Se colapsan las cinco bandas oficiales del **Cuadro N° 6** de A1 en tres colores, preservando la frontera exacta que usa el INEI para todo el país:

| Bandas INEI (5 niveles) | Semáforo del producto | Color |
|---|---|---|
| 0,00 – 0,20 Muy baja<br>0,21 – 0,40 Baja | **Bajo** | 🟢 Verde |
| 0,41 – 0,60 Media | **Medio** | 🟡 Ámbar |
| 0,61 – 0,80 Alta<br>0,81 – 1,00 Muy alta | **Alto** | 🔴 Rojo |

**Por qué colapsar a tres y no mostrar cinco:** el usuario objetivo de este producto no es un analista de política pública —es un comprador tomando una decisión en minutos. Tres colores son procesables al instante; cinco categorías textuales no. La granularidad de cinco niveles **se conserva internamente** (para quien exporte el reporte completo) y se **simplifica en la interfaz** — no se pierde información, se prioriza la decisión.

---

## 6. Variables precisas — tabla de especificación

| Variable | Definición exacta | Fuente | Frecuencia de actualización |
|---|---|---|---|
| `D_observada` | N.° de delitos denunciados en la zona, últimos 12 meses, ponderados por severidad (tabla §4.4) | Mapa del Delito — MININTER | Según publicación del observatorio |
| `V_encuestada` | % de victimización autorreportada del distrito | ENAPRES / UCSP | Anual |
| `Factor_corrección` | `V_encuestada / (D_observada normalizada a %)` | Cálculo propio | Recalculado cuando cambia la encuesta base |
| `D_corregida` | `D_observada × Factor_corrección`, expresada como tasa por 10 000 hab. | Cálculo propio | Con cada actualización de MININTER |
| `R_ciudadana` | N.° de reportes verificados de usuarios en la zona, últimos 12 meses, tasa por 10 000 hab. | Generada por el producto | Continua |
| `Población_zona` | Habitantes de la zona de agregación | INEI (proyección censal) | Según censo/proyección vigente |
| `IIP_zona` | Resultado final, 0 a 1 | Fórmula §4.3 | Recalculado con cada actualización de cualquier insumo |

**Unidad de agregación: zona, no predio individual.** Se conserva el principio ya establecido en `docs/05-producto/01-producto.md` §3 (lección del caso Zillow): el índice nunca califica un predio específico, siempre un polígono agregado (manzana o sector censal), evitando el riesgo de difamación puntual y el conflicto que hundió los scores de First Street en Zillow.

---

## 7. Verificación de reporte ciudadano — control de calidad, no censura

Para que `R_ciudadana` no se convierta en ruido o en herramienta de manipulación (un vendedor competidor reportando falsamente contra una zona rival):

1. **Geolocalización obligatoria** en el momento del reporte — no editable después.
2. **Categoría cerrada** de hecho (no texto libre calificando personas), siguiendo el mismo principio de "hechos, no juicios" ya adoptado en `docs/05-producto/01-producto.md`.
3. **Umbral mínimo de reportes independientes** antes de que una zona muestre `R_ciudadana` distinto de cero — un solo reporte no mueve el índice.
4. **Ventana de vigencia**: un reporte pesa menos conforme envejece (declive temporal), consistente con el enfoque temporal de A2 (Bogotá).

---

## 8. Qué NO hace esta función — límites declarados

| No hace | Por qué |
|---|---|
| No sustituye la denuncia policial | El producto instruye explícitamente a denunciar; el reporte ciudadano es complementario, no un canal legal |
| No implementa el modelo de frontera estocástica del INEI en la versión de curso | Se declara como trabajo futuro (§4.2); el proxy actual es transparente y auditable |
| No pondera con pesos calibrados estadísticamente en el lanzamiento | Los pesos de §4.3 y §4.4 son de arranque, documentados, ajustables con datos reales |
| No publica el índice a nivel de predio individual | Ver §6 — es zona agregada, por diseño, no por limitación técnica |

---

## 9. Encaje con el resto del producto

Esta función es la **capa 5** de las seis definidas en `docs/01-verticales/README.md`, pero se documenta aparte porque es la única con:

- Metodología propia (no solo agregación de fuente ajena, como las capas 1, 3 y 6)
- Corrección estadística explícita
- Componente de datos generado por el propio producto (`R_ciudadana`), que crece con el uso — el único activo del proyecto con efecto de red de datos genuino.

El resto de capas (registral, urbanística, catastral/SNCP, servicios, peligro físico) son de **agregación pura**: se documentan en `docs/01-verticales/` y se apoyan en fuentes existentes sin metodología estadística propia.
