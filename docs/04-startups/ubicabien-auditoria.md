# UbicaBien — Auditoría del producto autenticado

> Verificaciones **V1–V4** ejecutadas el 16 de septiembre de 2026 sobre una sesión autenticada propia, consumiendo 1 crédito del plan gratuito. Se documenta lo que el producto entrega, no se extrajeron sus conjuntos de datos.
>
> **Caso de prueba:** Terreno · 200 m² · Yura, Arequipa — es decir, el borde de expansión informal, que es el segmento objetivo de este proyecto.

---

## 1. Estructura de la aplicación

| Ruta | Función |
|---|---|
| `/mapa` | Buscador geográfico con avisos y capa «Riesgo» |
| `/verificador` | **Producto central** — consume 1 crédito por consulta |
| `/favoritos` | Propiedades guardadas |
| `/perfil` | Cuenta y créditos |

Navegación inferior: **Buscar · Verificar · Favoritos · Perfil**. Modelo de consumo por **créditos**, con botón «Comprar más créditos».

**Título literal del producto central:** «Verificar **el valor** de tu propiedad».

> El verificador es, por definición propia, un motor de valorización. No es un verificador de condición legal.

### Parámetros de entrada

Tipo (Departamento · Terreno · Casa), área en m², y ubicación por dirección, GPS o pin. Nada más. **No se solicita ni el nombre del vendedor, ni el número de partida registral, ni el nombre de la asociación.**

---

## 2. Arquitectura de datos observada

Esto es lo más revelador del ejercicio. Las capas se sirven como **archivos GeoJSON estáticos desde su propio origen**, con el análisis espacial resuelto en el navegador sobre Leaflet. No se observó ninguna llamada a un API de backend geoespacial.

### Capas cargadas

| Categoría | Archivo servido |
|---|---|
| Riesgos climáticos | `Puntos Inundación.geojson` |
| Riesgos climáticos | `Huayco.geojson` |
| Riesgos climáticos | `Vulcanismo Arequipa Moquegua.geojson` |
| Riesgos climáticos | `Tsunami.geojson` |
| Riesgos climáticos | `Quebradas.geojson` |
| Riesgos geológicos | `Fajas Marginales.geojson` |
| Riesgos geológicos | `Sismo.geojson` |
| Riesgos geológicos | `Suelo Inestable.geojson` |
| Riesgos geológicos | `Peligros Geológicos.geojson` |
| Riesgos geológicos | `Restos Arqueológicos.geojson` |
| Riesgos geológicos | `Catastro Minero` — `catastro1`, `catastro2`, `catastro3` |
| Habilitación urbana | `tiles/agua/` e `tiles/luz/` — **teselados**, con `index.json` y tesela por coordenada |

### Lectura técnica

1. **No hay API pública ni privada de terceros en juego.** Las capas son estáticas y propias.
2. **El teselado de las capas de agua y luz** indica que ya golpearon el límite de tamaño del enfoque cliente-pesado y tuvieron que partir esas capas.
3. **La capa de zonificación no aparece entre los archivos cargados.** Coherente con lo que el reporte declara (ver sección 4).

---

## 3. Lo que el reporte SÍ entrega

### 3.1 Valorizador

Tres precios derivados de comparables activos:

| Métrica | Valor devuelto |
|---|---|
| Precio de Lista | $ 1 278 /m² · $ 255 600 total · «+10 % sobre el precio de cierre» |
| Precio de Mercado | $ 1 220 /m² · $ 244 000 total · «Mediana de comparables activos» |
| Precio de Cierre | $ 1 162 /m² · $ 232 400 total |

Con desglose: rango del m² ($ 918 – $ 2 334), mediana y valor total, más la advertencia **«Muestra intermedia (5 a 9). Conviene contrastar con más avisos de la zona.»**

### 3.2 Diagnóstico del Suelo y Viabilidad

| Bloque | Resultado devuelto | Fuente declarada |
|---|---|---|
| **Concesión minera** | **«El pin se superpone a un derecho minero: Concesiones Mineras · TITULADO»** | **INGEMMET** |
| Población | 6 viviendas y 27 personas en la cuadra | INEI 2017 |
| Alumbrado público | Óptimo (100 %) · «Hay conexión eléctrica en esta cuadra · 1 m» | INEI 2017 |
| Acceso a agua potable | **Cobertura Bajo (0 %)** · «A 55 metros tienes una red de agua potable» | INEI 2017 |

### 3.3 Conectividad

Índice «Media», con distancia caminando a: centros de salud (1, a 3 min), centros educativos (3, a 2 min), paradas (2, a 1 min). Parques, restaurantes, bancos y centros comerciales: «sin datos en 600 m».

### 3.4 Comparables

Hasta 10 predios similares, con precio, área, precio por m², habitaciones, baños, estacionamientos y etiqueta de zonificación tomada del aviso.

---

## 4. Lo que el reporte NO entrega — verificado

### 4.1 Zonificación: **«Próximamente»** en su totalidad

Esta es la conclusión más importante de toda la auditoría.

| Campo | Estado devuelto |
|---|---|
| Zonificación | **Próximamente** |
| N.º máximo de pisos | **Próximamente** |
| Porcentaje de edificación | **Próximamente** |
| Área mínima del lote | **Próximamente** |
| Áreas libres · área construible · frente mínimo · coeficiente de edificación · estacionamientos | **Próximamente** |

> **El riesgo R9 queda resuelto a favor del proyecto. UbicaBien NO ha digitalizado la zonificación del PDM de Arequipa.** La ventaja competitiva que este repositorio había dado por disputada **sigue disponible**.
>
> Y hay una segunda lectura: un equipo financiado, con un CTO dedicado y una CEO especialista en planificación territorial, **no lo ha resuelto en un año**. Eso confirma que la barrera es real y alta — exactamente lo que este repositorio sostenía en `docs/01-verticales/v2-urbanistico.md`.

### 4.2 Riesgo de desastre: encabezado sin contenido

El bloque devuelve «Riesgo de Desastre: **Sí**», y todos sus componentes en **Próximamente**: riesgo de inundación, riesgo sísmico, vulcanismo, quebrada, suelo inestable, huayco.

Los archivos GeoJSON correspondientes **sí se cargan en el navegador**, pero el análisis por punto no está conectado al reporte. La capacidad está a medio construir.

### 4.3 Capa registral: **ausente y no anunciada**

No hay partida registral, ni titularidad, ni cargas, ni gravámenes, ni habilitación urbana como condición jurídica. Tampoco figura como «Próximamente» — **no está en su hoja de ruta visible**.

### 4.4 Exposición delictiva: ausente

No aparece en ninguna forma.

### 4.5 Otros pendientes

- «Vía principal más cercana» — Próximamente
- «Datos para una tasación reglamentaria» — Próximamente

---

## 5. El hallazgo decisivo: el valorizador se rompe en el borde informal

La consulta fue por un **Terreno en Yura**. Estos son los 9 comparables que el sistema utilizó para calcular el precio:

| # | Tipo | Distrito | Área | Precio/m² |
|---|---|---|---|---|
| 1 | Terreno | **Cerro Colorado** | 11 673 m² | **$ 103 910** |
| 2 | **Casa** | **Cayma** | 471 m² | $ 1 597 |
| 3 | Terreno | **Cerro Colorado** | 6 650 m² | **$ 90** |
| 4 | Terreno | **Uchumayo** | 4 206 m² | $ 855 |
| 5 | **Casa** | **Cercado** | 477 m² | $ 1 030 |
| 6 | **Casa** | **Cayma** | 500 m² | $ 3 070 |
| 7 | Terreno | **Sachaca** | 245 m² | $ 1 306 |
| 8 | Terreno | **Cercado** | 1 802 m² | $ 981 |
| 9 | Terreno | **Arequipa — El Filtro** | 638 m² | $ 1 220 |

### Tres fallas simultáneas

**1. Ningún comparable está en Yura.** Todos provienen de Cerro Colorado, Cayma, Uchumayo, Sachaca y el Cercado — mercados distintos, a kilómetros de distancia.

**2. Se consultó «Terreno» y tres de los nueve comparables son casas.** El filtro de tipo no se respeta cuando falta muestra.

**3. El rango de precio por m² va de $ 90 a $ 103 910 —un factor de 1 154×— y aun así el sistema reporta una mediana de $ 1 220/m² y un total de $ 244 000** para un lote de 200 m² en Yura.

El comparable #1 es además un dato manifiestamente erróneo: $ 1 212 946 657 por un terreno.

### Por qué esto importa

> **Su capacidad central deja de funcionar exactamente donde ocurre el daño que este proyecto quiere prevenir.**

No es un defecto de implementación que se corrija con un parche. Es estructural: la valorización por comparables **requiere comparables**, y el borde de expansión informal —donde el 93 % de la expansión urbana peruana ocurre— no los tiene, porque esos lotes no se publican en portales.

El sistema no responde «no tengo datos suficientes para esta zona». Responde **un número preciso y equivocado**, con tres decimales de falsa confianza.

---

## 6. Lo que tienen y este proyecto no había considerado

Corresponde reconocerlo con la misma franqueza:

| Capacidad | Valor | Acción recomendada |
|---|---|---|
| **Concesiones mineras de INGEMMET** | Detectó que el pin se superpone a un derecho minero titulado. Es una causa real de imposibilidad de habilitar, y no estaba en los cinco verticales de este repositorio | **Incorporar como sexto vertical** |
| **INEI 2017 a nivel de cuadra** | Viviendas y personas por cuadra, cobertura de alumbrado y de agua. Proxy inteligente y barato | **Adoptar** — resuelve parcialmente el Vertical 4 sin convenio con SEDAPAR |
| **Distancia a la red de agua** | «A 55 metros tienes una red de agua potable» | **Adoptar como proxy declarado** |
| **Biblioteca de riesgo** | Fajas marginales, quebradas, huayco, sismo, vulcanismo, suelo inestable, tsunami, restos arqueológicos, peligros geológicos | Confirma que las fuentes públicas alcanzan para construir esta capa |
| **Arquitectura GeoJSON estático** | Sin backend geoespacial. Barata, rápida, desplegable por un equipo pequeño | **Adoptar el patrón**, con teselado desde el inicio |

---

## 7. Estado de las verificaciones V1–V4

| # | Verificación | Resultado |
|---|---|---|
| **V1** | ¿Existe capa registral? | **NO.** Confirmado. Ni presente ni anunciada |
| **V2** | ¿Digitalizaron la zonificación? | **NO.** Todos los campos devuelven «Próximamente» |
| **V3** | ¿Detectan suelo no habilitable? | **Parcialmente.** Detectan concesión minera, pero no condición de habilitación urbana ni distinción entre predio rústico y lote urbano |
| **V4** | ¿Cubren el borde periurbano? | **Cobertura geográfica sí; utilidad no.** El motor devuelve comparables de otros distritos y produce una valorización sin fundamento |

---

## 8. Consecuencias para el proyecto

### 8.1 Riesgos que se cierran

| Riesgo | Estado |
|---|---|
| **R9** — «Si UbicaBien ya digitalizó la zonificación, la ventaja está tomada» | **CERRADO.** No la digitalizaron. La barrera sigue abierta |
| **T1** — «El foso está tomado» | **DESCARTADO** |

### 8.2 Diferenciación confirmada con evidencia, no con inferencia

| Eje | Evidencia obtenida |
|---|---|
| **Capa registral** | Ausente y fuera de su hoja de ruta visible |
| **Habilitación urbana** | No entregan condición jurídica del suelo |
| **Zonificación operativa** | «Próximamente» en los nueve campos |
| **Segmento** | Su motor degrada precisamente en el borde informal |
| **Pregunta central** | Su producto se titula «Verificar **el valor**». La pregunta del segmento objetivo no es cuánto vale |

### 8.3 La frase que resume la diferencia

> UbicaBien responde **«¿cuánto vale y qué hay alrededor?»**
> El problema del comprador de Yura es **«¿esto existe, es suyo y se puede habilitar?»**
>
> Y cuando se le pregunta por Yura, UbicaBien responde con comparables de Cayma.

---

## 9. Nota de método

- La auditoría se realizó sobre una sesión autenticada legítima del usuario, consumiendo 1 de 3 créditos del plan gratuito.
- No se descargaron ni redistribuyeron sus conjuntos de datos; solo se registraron las rutas que la aplicación solicita al navegador, como evidencia de arquitectura.
- No se accedió a información de otros usuarios ni se eludió ningún control de acceso.
- Los estados «Próximamente» corresponden a lo que el producto declara al 16 de septiembre de 2026 y pueden cambiar. Debe reverificarse antes de la sustentación.
