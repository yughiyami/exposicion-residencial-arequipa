# Exposición Residencial en Arequipa
## Investigación aplicada, definición de problema y propuesta de producto

**Curso:** Gestión Estratégica de Tecnologías de Información
**Ámbito:** Arequipa Metropolitana, Perú
**Fecha de verificación de fuentes:** 16 de septiembre de 2026

---

## Índice

1. [Resumen ejecutivo](#1-resumen-ejecutivo)
2. [Definición del problema](#2-definición-del-problema)
3. [Evaluación metodológica](#3-evaluación-metodológica)
4. [Los cinco verticales](#4-los-cinco-verticales)
5. [Benchmark internacional](#5-benchmark-internacional)
6. [Situación del Perú](#6-situación-del-perú)
7. [Situación de Arequipa](#7-situación-de-arequipa)
8. [Panorama competitivo](#8-panorama-competitivo)
9. [Propuesta de producto](#9-propuesta-de-producto)
10. [Plan de validación](#10-plan-de-validación)
11. [Mapeo al curso](#11-mapeo-al-curso)
12. [Limitaciones declaradas](#12-limitaciones-declaradas)
13. [Bibliografía](#13-bibliografía)

---

# 1. Resumen ejecutivo

## El problema

El comprador de vivienda o lote en Arequipa **no puede verificar, antes de transferir dinero**, si una ubicación es legalmente transferible, urbanísticamente habilitable, físicamente segura, servible con agua y desagüe, y tolerable en términos de exposición delictiva.

## La causa raíz

> **El Estado organiza la información por institución. El ciudadano la necesita organizada por predio.**

Cinco entidades soberanas custodian cinco capas de información. Ninguna tiene el mandato de responder la única pregunta que determina la decisión: *¿me conviene comprar en esta ubicación?*

El problema **no es de disponibilidad de datos**. Es de **integración orientada a la decisión**.

## La magnitud

| Indicador | Valor |
|---|---|
| Denuncias por estafa en compraventa de terrenos en Arequipa, cierre de 2024 | **Más de 1 000** |
| Viviendas urbanas informales en el Perú, cierre de 2025 | **61,7 %** — 4,1 millones de hogares, 14 millones de personas |
| Expansión urbana informal | **93 %** |
| Viviendas informales con asistencia de ingeniero o arquitecto | **13,8 %** |
| Victimización urbana en Arequipa | **33,5 %** — la mayor del país |

## El hallazgo que reordena el proyecto

El planteamiento original se centraba en la **exposición delictiva**. El análisis comparado demuestra que es el vertical de **menor consecuencia económica** de los cinco:

| Vertical | Comparable internacional maduro | Magnitud |
|---|---|---|
| Registral | Industria de seguro de título, EE. UU. | **USD 16 200 millones anuales** |
| Delictiva | SpotCrime, EE. UU. | **~USD 7 millones anuales** |

Tres órdenes de magnitud. La capa delictiva construye tráfico y confianza; la capa registral-urbanística construye ingresos.

## El benchmark

En el mundo el problema se resuelve con **tres modelos**, y el Perú no tiene ninguno completo:

| Modelo | Países | Mecanismo |
|---|---|---|
| **1. Obligación legal** | Reino Unido, Victoria, California | El Estado obliga a que la información viaje con el inmueble |
| **2. Seguro** | Estados Unidos | Una industria privada asume el riesgo por una prima |
| **3. Bien público digital** | Países Bajos, España, Estonia | El Estado publica el dato como servicio gratuito |

## La propuesta

> Una **capa de agregación y estandarización de información predial** para Arequipa: el equivalente local de un *title plant* norteamericano, aplicado a la capa de zonificación y habilitación urbana.

## El veredicto honesto

**El problema está documentado. La demanda pagada no está medida.** El veredicto del dossier de evidencia permanece en `PENDIENTE` hasta ejecutar el experimento con umbral precomprometido. Este documento **no declara viabilidad**: declara coherencia entre problema, evidencia y diseño.

---

# 2. Definición del problema

## 2.1 Planteamiento original

> «Las personas que buscan comprar o alquilar una vivienda en Arequipa tienen dificultades para evaluar objetivamente la exposición delictiva de una ubicación específica, debido a que la información sobre hechos delictivos, aunque disponible mediante plataformas y bases de datos oficiales, requiere procesos de consulta, interpretación y comparación espacial que no están orientados directamente a la decisión residencial.»

## 2.2 Por qué se amplía

El planteamiento es correcto en su mecánica —dato disponible pero no accionable— y estrecho en su alcance.

| Dimensión | Exposición delictiva | Condición legal-urbanística |
|---|---|---|
| Magnitud de la pérdida | Incomodidad; ~1 % del valor | **Pérdida total del capital** |
| Reversibilidad | Alta — mudarse | **Nula** |
| Ventana de decisión | Permanente | **Solo antes de la firma** |
| Gasto observable hoy | No documentado | Búsqueda registral, honorarios, tasación |

## 2.3 Problema reformulado

> El comprador de vivienda o lote en Arequipa no dispone de ningún mecanismo que le permita obtener, **antes de transferir dinero y en un solo acto**, un veredicto verificable sobre las cinco condiciones que determinan si una ubicación es adquirible sin riesgo patrimonial: situación registral, condición urbanística, peligro físico, factibilidad de servicios y exposición delictiva.

## 2.4 A quién afecta

Comprador de primera vivienda o lote en el borde de expansión de Arequipa Metropolitana: **Cerro Colorado, Yura, Characato, La Joya, eje Majes–Pedregal**.

Perfil conductual: compra una sola vez en su vida, financia con ahorro familiar o crédito de caja municipal, no contrata asesoría profesional, y opera bajo presión de escasez inducida por el vendedor.

**No es un nicho.** Dos tercios de la producción anual de vivienda del Perú y el 93 % de la expansión urbana ocurren exactamente en ese segmento.

## 2.5 Qué hacen hoy

1. Solicitud de partida registral en SUNARP
2. Consulta informal a un abogado conocido
3. Confianza en el dirigente de la asociación o en el vendedor
4. Consulta presencial no vinculante en la municipalidad

Resultado: cuatro a cinco consultas desacopladas, semanas de duración, respuestas parciales, **ningún veredicto único**.

## 2.6 Mecánica documentada del fraude en Arequipa

1. Publicación en redes sociales de lotes a precios accesibles
2. Entrega de recibos o documentos falsos
3. Venta de predios de propiedad del Estado por seudodirigentes
4. Comercialización de predios rústicos como lotes urbanos

> **Los cuatro mecanismos son detectables *ex ante* cruzando SUNARP con la zonificación municipal y el mapa de peligro. Ninguno requiere información privilegiada.**

---

# 3. Evaluación metodológica

Aplicación de tres marcos secuenciales. Detalle completo en [`docs/00-evaluacion/`](docs/00-evaluacion/).

## 3.1 Análisis de causa raíz

### TRIZ — Contradicción

| Para lograr | El sistema debe ser | Pero eso impide |
|---|---|---|
| Validez jurídica del dato | Custodiado por la institución soberana | Consolidación en un punto |
| Utilidad en la decisión | Consolidado en un punto y un instante | Soberanía institucional |

La contradicción **no la resuelve nadie: se traslada al ciudadano**. Esa transferencia de carga es la causa raíz.

### Jobs-to-be-Done

El trabajo contratado no es «ver un mapa». Es **«no arruinarme»**. El producto compite contra la incertidumbre, no contra otros mapas.

### Marketing Myopia

Definir el negocio como «plataforma de mapas de seguridad» es miopía de categoría. La definición correcta es **due diligence residencial**: el equivalente predial de una central de riesgo crediticio.

> En el Perú cualquiera comprende la consulta del historial crediticio de una persona. **No existe el equivalente para un predio.**

### Progress-Making Forces

| Fuerza | Contenido | Intensidad |
|---|---|---|
| Push | 1 000+ denuncias por estafa; 33,5 % de victimización | Alta |
| Pull | Veredicto en minutos frente a semanas | Alta |
| Anxiety | «¿Puedo confiar en este dato?» | Media — mitigable con fuente y fecha |
| Habit | «Le pregunto a un conocido» | Media |

## 3.2 Predicción falsable

> Si la causa raíz es la fragmentación institucional y no la ausencia de datos, debe observarse que **(a)** los compradores ya incurren en gasto y tiempo en consultas separadas; **(b)** las denuncias por estafa se concentran en el borde periurbano; **(c)** notarios y analistas de crédito ejecutan hoy un checklist manual multi-fuente.

**Qué la falsaría:** si en una muestra de compradores recientes la mayoría no realizó más de una consulta, no incurrió en gasto y no percibe el asunto como relevante.

## 3.3 Condición de parada

Se detiene el análisis en este nivel porque la hipótesis es falsable y está anclada en conducta y gasto observables. Descender a «¿por qué el Estado peruano está fragmentado?» conduciría a reforma institucional, fuera de la capacidad de intervención del equipo — el error de capa del caso Segway.

---

# 4. Los cinco verticales

| # | Vertical | Pregunta | Institución | Formato | Brecha | Dificultad |
|---|---|---|---|---|---|---|
| 1 | Legal / registral | ¿Es transferible? | SUNARP | Geovisor, sin API | Acceso automatizado | Media |
| 2 | Urbanístico | ¿Se puede construir? | Municipalidad | **PDF** | **Estructuración** | **Alta** |
| 3 | Peligro físico | ¿Es seguro? | CENEPRED / ANA | Plataforma geoespacial | Cobertura desigual | Baja |
| 4 | Servicios | ¿Tendrá agua? | SEDAPAR / SEAL | **Presencial** | **Sin canal digital** | **Muy alta** |
| 5 | Exposición delictiva | ¿Es tolerable? | MININTER / INEI | Geovisor | Subregistro | Media |

## Estado de integración

```
Vertical 1 — Registral      ████████░░  Digital, georreferenciado, sin API
Vertical 2 — Urbanístico    ██░░░░░░░░  PDF por municipalidad
Vertical 3 — Peligro        ███████░░░  Plataforma pública, cobertura desigual
Vertical 4 — Servicios      █░░░░░░░░░  Presencial, requiere profesional colegiado
Vertical 5 — Delictiva      ███████░░░  Geovisor público, con subregistro
```

**Ninguno está vinculado a otro por un identificador común.** Es la causa raíz expresada técnicamente.

## El problema del identificador único

Países Bajos y Estonia resolvieron la integración con la misma regla: **el mismo identificador único de predio en todos los registros**. España cumple igual función con la referencia catastral.

En el Perú **no existe** esa clave universal. La vinculación debe resolverse por coincidencia geográfica, lo que introduce error. **Debe declararse, no ocultarse.**

Detalle por vertical en [`docs/01-verticales/`](docs/01-verticales/).

---

# 5. Benchmark internacional

Detalle por país en [`docs/02-paises/`](docs/02-paises/).

## 5.1 Modelo 1 — Obligación legal de divulgación

### Reino Unido

**Local Authority Search**, obligatoria en *conveyancing* y exigida por los prestamistas hipotecarios:

- **LLC1** — cargas financieras, condiciones de planeamiento, órdenes de protección de árboles, área de conservación, edificio protegido, notificaciones de ejecución.
- **CON29** — vías públicas, proyectos viales y ferroviarios, decisiones de planeamiento, notificaciones estatutarias, infracciones, **orden de expropiación**.

> Las inscripciones del LLC1 son **legalmente vinculantes para los propietarios sucesivos**. Obligan **aunque no se haya hecho la búsqueda**.

**Material Information** — National Trading Standards, exigible bajo el **DMCC Act 2024**:

| Parte | Contenido |
|---|---|
| A | Council tax, precio, tenencia |
| B | Tipo, materiales, ambientes, servicios, estacionamiento |
| C | **Riesgo de inundación**, restricciones registrales — solo si aplica |

Regla operativa: el agente debe **tomar pasos razonables para establecer** la información, no repetir al vendedor.

### Victoria, Australia

**Section 32 Vendor's Statement** — *Sale of Land Act 1962*, secciones 32 a 32I. Entrega obligatoria **antes de la firma**. Incluye título, gravámenes, **controles de planeamiento y zonificación**, tributos.

- **No se puede pactar en contra.**
- Si es incompleta o inexacta, el comprador **puede rescindir antes del cierre**.

### California

**Natural Hazard Disclosure Statement** — Civil Code Sec. 1103. Único estado de la Unión que lo exige. Seis zonas: inundación especial, inundación por represa, severidad muy alta de incendio, área forestal, falla sísmica, peligro sísmico. Entrega previa a la aceptación del contrato; el incumplimiento doloso o negligente genera **responsabilidad por daños**.

## 5.2 Modelo 2 — Estados Unidos: la industria que nace del desorden

| Dato | Valor |
|---|---|
| Condados con sistema propio | Más de 3 000 |
| Jurisdicciones con taxonomía distinta | 3 144 |
| Primas de seguro de título 2024 | **USD 16 200 millones** |
| Concentración | Ninguna empresa supera el 5 % |

### El *title plant* — precedente directo

> Debido a las ineficiencias de las oficinas de registro de los condados, las compañías de título construyeron sus propios **title plants**: sistemas que replican la información de los registros públicos **reindexada de forma consistente**, para ejecutar búsquedas con mayor rapidez y precisión.

**Cuando el Estado no unifica, el mercado construye el espejo y cobra por consultarlo.** No es hipótesis: es historia económica de un sector de USD 16 200 millones anuales.

### El caso Zillow — la advertencia

Zillow retiró los puntajes de riesgo climático de First Street de **más de un millón de avisos** en noviembre–diciembre de 2025, tras reclamo del California Regional MLS. El motivo económico de fondo:

> Los inmuebles marcados como de alto riesgo se vendieron **~1 % por debajo** de su valor de mercado.

**Cuatro implicancias de diseño:**

1. El índice funciona — movió precios de forma medible.
2. Precisamente por funcionar, genera resistencia gremial.
3. No vender al actor con incentivo invertido.
4. Metodología pública y auditable: el ataque efectivo fue por **exactitud**, no por la idea.

## 5.3 Modelo 3 — Bien público digital

### Países Bajos

**Kadaster** opera **PDOK**, gratuita para todos. El **BAG** cubre edificaciones, unidades residenciales, numeración y espacios públicos con geometría, coordenadas, año de construcción y uso.

Entregado como **API REST, OGC API, Linked Data y SPARQL**; visor con más de **235 conjuntos de datos**. Modelo híbrido: **capa base gratuita, capa de valor agregado paga** (precio de compra ~EUR 0,45 por consulta).

### España

**Sede Electrónica del Catastro**. Consulta **libre y gratuita** de datos no protegidos, incluida la cartografía; formatos INSPIRE.

| Categoría | Acceso |
|---|---|
| Geometría, superficie, uso, croquis, certificaciones | **Público** |
| Nombre, domicilio del titular, **valor catastral** | **Protegido** |

> Este criterio resuelve de antemano la principal objeción ética al producto, con fundamento normativo comparado.

### Estonia

**e-Land Register**: cualquiera consulta superficie, propietarios, restricciones, hipotecas y **uso permitido del suelo** —el equivalente de la zonificación— en el **mismo registro** que la titularidad.

> Los registros estonios se referencian entre sí, evitando la doble recolección, y **usan los mismos identificadores únicos en todos los registros**, incluidas las parcelas.

### Latinoamérica

**Colombia** — Ventanilla Única de Registro (VUR), liderada por la Superintendencia de Notariado y Registro, coordinando alcaldías, gobernaciones, entidades financieras y notarías.

**Chile** — Conservador de Bienes Raíces digital, con Certificado de Hipotecas, Gravámenes y Prohibiciones en línea.

Ambos resuelven la capa registral. **Ninguno resuelve la capa urbanística municipal.**

## 5.4 Tabla comparativa

| País | Modelo | Instrumento | Obligatorio | Formato | Costo ciudadano |
|---|---|---|---|---|---|
| Reino Unido | 1 | LLC1 + CON29; Material Information | Sí con hipoteca | Informe estructurado | Comprador |
| Victoria | 1 | Section 32 | Sí, no pactable en contra | Documento legal | Vendedor |
| California | 1 | NHD Statement | Sí, Civil Code 1103 | Formulario estatutario | Vendedor |
| EE. UU. federal | 2 | Seguro de título | De facto | Base privada | Prima |
| Países Bajos | 3 | Kadaster / PDOK / BAG | — | API REST, OGC, SPARQL | Gratuito |
| España | 3 | Sede Electrónica del Catastro | — | INSPIRE, servicios web | Gratuito |
| Estonia | 3 | e-Land Register | — | Registros interconectados | Público |
| Colombia | 3 parcial | VUR | — | Portal integrado | En línea |
| Chile | 3 parcial | CBR digital | — | Certificados en línea | Por certificado |
| **Perú** | **Ninguno** | Visor BGR (solo registral) | No | Geovisor; municipal en PDF | Gratuito en lo nacional |

## 5.5 Marco de evaluación

**Índice de Calidad de la Administración de Tierras** — Banco Mundial. Cinco dimensiones: confiabilidad de la infraestructura, transparencia de la información, cobertura geográfica, resolución de disputas, acceso equitativo a derechos de propiedad. Última recolección: mayo de 2019. Doing Business fue archivado; **B-READY** mide hoy el tiempo y costo *de facto* de transferir propiedad.

---

# 6. Situación del Perú

## 6.1 El universo afectado

| Indicador | Valor |
|---|---|
| Viviendas urbanas informales, cierre de 2025 | **61,7 %** — 4,1 M de hogares, 14 M de personas |
| Viviendas nuevas informales en 17 años | **1,6 millones (63 %)** sin título o sin servicios básicos |
| Expansión urbana informal | **93 %** |
| Viviendas urbanas autoconstruidas | 7 de cada 10 |
| Con asistencia de ingeniero o arquitecto (2024) | **13,8 %** |
| Déficit habitacional | **1,9 M** — 587 mil cuantitativo, 1,3 M cualitativo |

### Producción anual de vivienda (~128 mil unidades)

| Segmento | Participación |
|---|---|
| Convencional | 23 % |
| Nuevo Crédito Mivivienda | 7 % |
| Techo Propio | 4 % |
| **Informal / autoconstrucción** | **~66 %** |

## 6.2 Estado por capa

| Capa | Estado | Formato |
|---|---|---|
| Registral | Digital y georreferenciado | Geovisor, sin API |
| Urbanística | **No digital** | PDF por municipalidad |
| Peligro físico | Digital | SIGRID |
| Servicios | **Presencial** | Expediente |
| Delictiva | Digital | Geovisor |
| Divulgación obligatoria del vendedor | **Inexistente** | — |

## 6.3 Lo que sí funciona: SUNARP

**Visor BGR** — gratuito, georreferenciado, más de 6 millones de imágenes de predios, **más de 3 millones de consultas de más de 360 mil ciudadanos**.

> Es la evidencia conductual más fuerte disponible de demanda de verificación predial en el Perú. **Su límite:** el servicio es gratuito y no acredita disposición a pagar.

**SPRL** — publicidad registral en línea, 24/7, con firma electrónica. **Sin API pública documentada.**

## 6.4 Lo que no funciona: la capa municipal

Más de 1 800 municipalidades distritales, cada una con su TUPA, su plan urbano cuando lo tiene, su presupuesto y **ningún incentivo para estandarizarse**.

| Estados Unidos | Perú |
|---|---|
| 3 000+ condados | 1 800+ municipalidades |
| Sin estandarizar en 150 años | Sin estandarizar |
| Industria privada de USD 16 200 M | Vacío de mercado |

> **El vacío no es coyuntural. Es estructural. La evidencia comparada indica que no se cierra por evolución natural.**

## 6.5 Nota sobre acceso automatizado

| Portal | Comportamiento verificado |
|---|---|
| `gob.pe` | HTTP 418, acceso restringido |
| `muniarequipa.gob.pe` | HTTP 403 a solicitudes programáticas; carga en navegador |

---

# 7. Situación de Arequipa

## 7.1 Exposición delictiva

| Indicador | Valor |
|---|---|
| Victimización urbana | **33,5 %** — la mayor del país, frente a 26,8 % en 2019 |
| Victimización UCSP 2025 | 30,90 %, seis puntos más que 2024 |
| Percepción de inseguridad | **88 %** |
| Extorsión | De **6,8 a 30,6** denuncias por 100 mil habitantes, 2019–2025 |

| Distrito | Participación | Delito | Participación |
|---|---|---|---|
| Cerro Colorado | 16,60 % | Robo en transporte público | 33,20 % |
| Paucarpata | 14,98 % | Robo al paso | 21,05 % |
| José Luis Bustamante y Rivero | 10,12 % | **Hurto a viviendas** | **19,03 %** |

## 7.2 Fraude en compraventa

- **Más de 1 000 denuncias** por presunta estafa al cierre de 2024, según la Procuraduría adjunta del Gobierno Regional.
- El **Colegio de Arquitectos del Perú** alerta sobre predios rústicos sin habilitación urbana ni infraestructura básica comercializados como lotes urbanos.
- Muchas ventas ocurren sobre terrenos que **el Estado jamás podrá formalizar**.

## 7.3 Diagnóstico de fuentes — verificación directa

### Municipalidad Provincial de Arequipa

Servicios del portal **Muni Virtual**: pagos en línea, mesa de partes, búsqueda de expedientes, partidas virtuales, consultas de transportes, empadronamiento SIT, plaqueo, casilla electrónica.

| Recurso | Disponible |
|---|---|
| Geoportal | **No** |
| Visor de zonificación | **No** |
| Consulta catastral en línea | **No** |

PDM 2016–2025 (Ordenanza Municipal N.º 975) publicado por el **IMPLA** como PDF y enlaces en la nube. **PDM 2025–2045 en exhibición pública.**

### José Luis Bustamante y Rivero — el más avanzado

| Recurso | Estado |
|---|---|
| Plano de zonificación | **PDF** |
| Plano catastral | PDF |
| Planos viales | PDF |
| Plan Urbano Distrital | PDF |
| TUPA | PDF |
| Shapefile o servicio geoespacial | **No** |
| Visor interactivo | **No** |

Certificado de parámetros: presencial, Villa Eléctrica, 08:00–13:00.

### Miraflores

Mesa de partes virtual y TUPA en línea. **Sin visor de zonificación ni certificado en línea.**

### Paucarpata

Mesa de partes virtual y TUPA publicado. **Sin visor.** Su **Plan de Desarrollo Urbano distrital está en elaboración**: la zonificación de detalle no está consolidada.

### SEDAPAR

Factibilidad **100 % presencial**. Requisitos: DNI o vigencia de poder ≤ 30 días; **ficha registral ≤ 60 días**; **memoria descriptiva firmada por ingeniero civil, sanitario o arquitecto colegiado**.

> **Para saber si un terreno tendrá agua, el ciudadano debe contratar a un profesional colegiado antes de comprarlo.** Esta barrera explica por sí sola por qué la verificación no ocurre. Contrastar con el dato nacional: solo el 13,8 % de las viviendas informales contó con esa asistencia.

Contexto de estrés: el alcalde alertó que el 80 % de la población quedó desabastecida de un momento a otro (febrero de 2024); SEDAPAR devolvió S/ 6 147 211 al Ministerio de Vivienda tras no ejecutar el convenio de cisternas durante 2025.

## 7.4 Peligro físico documentado

Mapa de peligro de la ciudad de Arequipa (INDECI–PNUD); evaluación de riesgos en torrenteras de Yura; mapa de inundación de Camaná; puntos críticos de inundación del departamento (ANA, 2019); zonificación sísmica-geotécnica de suelos (GEOIDEP). Todos disponibles en **SIGRID — CENEPRED**.

## 7.5 Decisión de alcance

**Piloto: José Luis Bustamante y Rivero.**

| Criterio | Fundamento |
|---|---|
| Materia prima | Único con zonificación, catastro y vías descargables |
| Estabilidad normativa | Distrito consolidado |
| Señal delictiva | 10,12 % de hechos reportados |
| Estado actual modelable | TUPA publicado |

**Paucarpata:** caso de contraste — PDU en elaboración; el distrito con más territorio informal y menos zonificación de detalle presenta, por construcción, mayor exposición. **Refuerza la tesis.**

**Miraflores:** segunda fase.

---

# 8. Panorama competitivo

## 8.1 Mapa por vertical

| Vertical | Actor | País | Señal económica |
|---|---|---|---|
| Registral | Industria de seguro de título | EE. UU. | **USD 16 200 M / año** |
| Urbanístico | Sprift | Reino Unido | 300+ datos sobre 30 M+ propiedades |
| Peligro físico | Jupiter Intelligence | EE. UU. | **USD 88 M levantados** |
| Peligro físico | Cape Analytics | EE. UU. | Satélite + aprendizaje automático |
| Peligro físico | First Street Foundation | EE. UU. | Integrada en Redfin, Realtor.com, Homes.com |
| Geometría parcelaria | Regrid | EE. UU. | Capa base nacional |
| Delictiva | SpotCrime | EE. UU. | **~USD 7 M / año** |
| Livability | NeighborhoodScout, CrimeGrade, AreaVibes | EE. UU. | 45 000+ ubicaciones |
| Servicios | Walk Score | EE. UU. | API consumida por Zillow |

```
Seguro de título (registral)     ████████████████████████████████  USD 16 200 M / año
Jupiter Intelligence (peligro)   ▌                                  USD 88 M levantados
SpotCrime (delictiva)            ▏                                  USD 7 M / año
```

## 8.2 Arquetipos

| Arquetipo | Ejemplo | Aplicable |
|---|---|---|
| **A. Agregador puro** | Sprift, Regrid | **Sí — modelo recomendado** |
| B. Productor de dato propio | Cape Analytics, Jupiter | Segunda fase; exige capital |
| C. Transferencia de riesgo | Seguro de título | Techo del sector; exige licencia |
| D. Capa sobre portales | First Street en Zillow | **Descartado — conflicto de incentivos** |

## 8.3 Latinoamérica

| Empresa | País | Foco | ¿Verifica riesgo de ubicación? |
|---|---|---|---|
| **UbicaBien** | **Perú — Arequipa** | **Geoverificación: valorización, zonificación, conectividad, desastres** | **Sí — competidor directo** |
| Houm | Chile | Arriendo digital | No |
| Homie | México | Renta sin aval | No |
| La Haus | Colombia | Venta de vivienda nueva | No |
| Gojom | Perú | Transacción | No |
| Valia | Perú | Agente–cliente | No |
| Urbania / Adondevivir / Properati | Perú | Portales de avisos | No |

| Indicador | Valor |
|---|---|
| Mercado global proptech 2026 | USD 44 590 M → USD 104 570 M en 2034 (TCAC 11,9 %) |
| Mercado inmobiliario latinoamericano 2026 | Podría superar USD 1,1 billones |
| Startups proptech en el Perú | Más de 15 (Perú PropTech) |

Según el **BID**, las proptech regionales atacan **falta de transparencia** e **ineficiencia de procesos**. Este proyecto se ubica en el primero.

## 8.4 UbicaBien — competidor directo en Arequipa

> **Corrección.** Una versión previa de este documento afirmaba que ningún actor latinoamericano ofrecía verificación integral de una ubicación residencial. **Era falso.** Ficha completa en [`docs/04-startups/ubicabien.md`](docs/04-startups/ubicabien.md).

| Campo | Dato |
|---|---|
| Posicionamiento | «El primer verificador inmobiliario del Perú» · lema **Decide Bien** |
| Origen | **Nace en Arequipa** |
| Lanzamiento | Agosto de 2026 |
| Respaldo | **StartUp Perú · ProInnóvate · Innicia (UCSM)** |
| Equipo | CEO con perfil en gestión de riesgos de desastres y planificación territorial; CTO full stack y cloud; CDO en diseño de servicios |
| Capas | Valorización · Zonificación · Conectividad · Desastres |
| Producto adicional | ACM para corredores, con firma y logo de agencia en el reporte |
| Precios | Gratuito (3 verificaciones) · S/ 10/mes · S/ 49/mes · S/ 150/3 meses |
| Postura legal | «Información referencial, no constituye asesoría profesional» |

### Comparación de cobertura

| Capa | UbicaBien | Propuesta |
|---|---|---|
| Valorización / precio | **Sí — capa central** | **No** — fuera de alcance |
| Zonificación | Sí | Sí |
| Conectividad a amenidades | Sí | Parcial, propósito distinto |
| Riesgo de desastres | Sí | Sí |
| **Registral (SUNARP)** | **No visible en el sitio público** | **Sí — capa central** |
| **Habilitación urbana** | No declarado | **Sí — capa central** |
| **Factibilidad de agua y desagüe** | No | Sí, como proxy declarado |
| **Exposición delictiva** | No | Sí |
| ACM para corredores | Sí | No |

## 8.5 Conclusión competitiva revisada

**Validación del problema.** Un equipo con financiamiento público apostó a este problema en esta misma ciudad. Es evidencia externa más fuerte que cualquier argumento propio, y levanta la advertencia previa de «si nadie lo construyó, quizá no hay demanda».

**Amenaza competitiva.** Están lanzados, con planes de pago activos y respaldo institucional local. **Si ya digitalizaron la zonificación de Arequipa, la ventaja competitiva propuesta está tomada.**

### Diferenciación defendible

| Eje | UbicaBien | Propuesta |
|---|---|---|
| Pregunta central | **«¿Es buena inversión?»** | **«¿Me van a estafar?»** |
| Usuario | Inversionista, corredor, agencia | Comprador de **primera vivienda** en el borde de expansión |
| Frecuencia | Recurrente | **Una vez en la vida** |
| Cobro | Suscripción mensual | **Pago por evento** |
| Mercado | Formal y consolidado | **Informal y periurbano — 61,7 % del parque urbano** |
| Capa de diferenciación | — | **Registral y habilitación urbana** |

Fundamento económico: el comparable internacional de la capa registral mueve **USD 16 200 millones anuales**, y los cuatro mecanismos de fraude documentados en Arequipa se detectan con partida registral y habilitación urbana, **no con valorización**.

> Una valorización precisa de un terreno que el vendedor no puede transferir es información exacta e inútil.

### Posicionamiento revisado

> **Verificación registral y de habilitación urbana orientada a la prevención de fraude, para el comprador de primera vivienda en el borde de expansión informal de Arequipa — con cobro por evento, no por suscripción.**

---

# 9. Propuesta de producto

## 9.1 Qué es

Una **capa de agregación y estandarización de información predial** que entrega, a partir de una ubicación, un veredicto consolidado con fuente citada y fechada en cada afirmación.

**Posicionamiento:** un *title plant* aplicado a la capa de zonificación y habilitación urbana de Arequipa.

## 9.2 Entrada y salida

**Entrada:** coordenada, dirección o enlace de un aviso.

**Salida:**

| Componente | Contenido |
|---|---|
| Semáforo por capa | Verde, ámbar o rojo en los cinco verticales |
| Informe descargable | Un hallazgo por línea con institución fuente, fecha y nivel de confianza |
| Alertas críticas | Sin partida registral; suelo no habilitable; zona de peligro alto |
| Declaración de límites | Qué no pudo verificarse y por qué |

## 9.3 Lo que NO es

| No es | Por qué |
|---|---|
| Un certificado | **Informa, no certifica** |
| Un juicio de titularidad | Reporta lo que el registro consigna, con su fecha |
| Calificación de predio individual | Trabaja por zona agregada — lección Zillow |
| Un directorio de propietarios | Criterio español: identidad protegida |
| Una tasación | No estima valor comercial |

## 9.4 Modelo de negocio

| Campo | Definición |
|---|---|
| Propuesta de valor | «Antes de firmar, sepa si ese terreno le va a dar problemas — en minutos y con la fuente oficial al lado.» |
| Segmento primario | Comprador de primera vivienda o lote en el borde de expansión |
| Segmento secundario | Notarías, tasadores, analistas de crédito |
| Canales | Grupos de compraventa en redes sociales; Colegio de Arquitectos filial Arequipa; referidos |
| Ingresos | Consulta básica gratuita; reporte de pago; suscripción institucional — modelo híbrido Kadaster |
| Costos | **Digitalización y mantenimiento de la capa de zonificación** |
| Ventaja injusta | **Revisada.** La zonificación digitalizada ya no es foso exclusivo: UbicaBien la ofrece. La barrera defendible es la **capa registral más el conocimiento del mecanismo de fraude local** |

## 9.5 Arquitectura funcional

```
                    ENTRADA: ubicación
                           │
              ┌────────────┴────────────┐
              │   Resolución espacial   │
              │  (coincidencia geo —    │
              │  sin identificador      │
              │  único de predio)       │
              └────────────┬────────────┘
                           │
   ┌──────────┬────────────┼────────────┬──────────┐
   ▼          ▼            ▼            ▼          ▼
Registral  Urbanística  Peligro     Servicios  Delictiva
SUNARP     Capa propia  SIGRID      Proxy      MININTER
(asistido) (interna)    (público)   (derivado) (calibrado)
   │          │            │            │          │
   └──────────┴────────────┼────────────┴──────────┘
                           ▼
              ┌─────────────────────────┐
              │  Motor de reglas y      │
              │  nivel de confianza     │
              └────────────┬────────────┘
                           ▼
              SALIDA: semáforo + informe
              con fuente y fecha por línea
```

### Restricciones arquitectónicas declaradas

| # | Restricción | Consecuencia |
|---|---|---|
| A1 | SUNARP sin API pública | Consumo asistido |
| A2 | Sin identificador único de predio | Vinculación geográfica con error declarado |
| A3 | `gob.pe` 418; `muniarequipa.gob.pe` 403 | Conectores no pueden asumir acceso libre |
| A4 | SEDAPAR sin consulta por ubicación | Capa 4 con proxy etiquetado |
| A5 | Zonificación en PDF | Capa propia construida y mantenida |

## 9.6 Gestión de riesgos

| # | Riesgo | Severidad | Mitigación |
|---|---|---|---|
| R1 | PDF de zonificación podría ser raster | **Alta** | Verificación en QGIS antes de comprometer cronograma |
| R2 | Transición PDM 2016–2025 → 2025–2045 | Media | Versionado con fecha de vigencia |
| R3 | Sin API en SUNARP | Media | Consumo asistido declarado |
| R4 | Responsabilidad legal | **Alta** | Informa, no certifica; fuente y fecha; zona agregada |
| R5 | Fuga de datos → catálogo de objetivos para el crimen organizado | **Crítica** | Control de acceso, minimización, auditoría |
| R6 | Resistencia gremial | Media | Metodología pública y auditable |
| R7 | El Estado cierra el vacío | Baja a corto plazo | Declarado como horizonte de obsolescencia |

## 9.7 Horizonte de obsolescencia

Si el Perú avanza al Modelo 1 o completa el Modelo 3, este producto se convierte en infraestructura pública y deja de tener razón comercial.

**Ese desenlace es socialmente preferible y el proyecto lo declara.** La evidencia comparada indica que la capa municipal es la última en resolverse.

---

# 10. Plan de validación

Detalle en [`docs/00-evaluacion/02-dossier-evidencia.md`](docs/00-evaluacion/02-dossier-evidencia.md).

## 10.1 Prueba de humo

| Campo | Definición |
|---|---|
| Método | Página única con CTA real: «Verificar mi terreno — dejar correo» |
| Tráfico | Grupos de compraventa de Cerro Colorado, Yura y Characato; gasto publicitario mínimo segmentado |
| Costo | Menor a USD 50 |
| Duración | 7 días |
| **Umbral de aprobación** | **≥ 4 %** de 300 visitantes segmentados |
| **Umbral de refutación** | **< 2 %** de 300 visitantes |
| Zona gris | 2 %–4 % → señal débil; repetir con propuesta reformulada |

*Justificación del umbral:* se fija por encima de la conversión típica de una landing fría de servicio profesional (1–2 %) porque el dolor declarado es catastrófico e irreversible.

## 10.2 MVP conserje

| Campo | Definición |
|---|---|
| Método | Entrega manual del reporte de cinco capas. Sin software |
| Muestra | 10 compradores reales captados por la prueba de humo |
| Costo | Tiempo — ~3 horas por reporte inicialmente |
| **Umbral de aprobación** | **≥ 4 de 10** volverían a pagar, y ≥ 2 recomiendan espontáneamente |
| **Umbral de refutación** | **≤ 2 de 10** |

## 10.3 Entrevistas

15 compradores que cerraron operación en los últimos 24 meses. **Solo conducta pasada:**

- ¿Qué verificó antes de firmar? Paso por paso.
- ¿Cuánto gastó? ¿Cuánto tiempo le tomó?
- ¿Qué no pudo averiguar aunque lo intentó?
- ¿Se enteró de algo después de firmar que hubiera querido saber antes?

**Prohibido:** «¿Usaría usted una plataforma que…?» — es intención hipotética, no evidencia.

## 10.4 Verificación técnica bloqueante

**Abrir el PDF de zonificación de JLByR en QGIS y determinar si es vectorial o raster escaneado.** Es la única verificación que aún puede alterar el cronograma del proyecto.

## 10.5 Veredicto actual

> ## `PENDIENTE`

La evidencia publicada sobre **existencia y magnitud del problema** es sólida. La evidencia sobre **demanda pagada en Arequipa** es **inexistente**. El único indicio conductual —3 millones de consultas al Visor BGR— prueba interés en verificar sobre un servicio **gratuito**.

**La investigación documental no sustituye al experimento.**

---

# 11. Mapeo al curso

Detalle en [`docs/05-producto/02-mapeo-gsti.md`](docs/05-producto/02-mapeo-gsti.md).

## 11.1 PETI

**Argumento central:** no se propone crear información nueva, sino **integrar información existente**. Cuatro de cinco capas ya son públicas y digitales.

Alineamiento: Política Nacional de Gobierno Digital, Ley de Gobierno Digital e interoperabilidad, PDM (Ordenanza N.º 975).

Marco de diagnóstico: **Índice de Calidad de la Administración de Tierras** del Banco Mundial, cinco dimensiones aplicadas a Arequipa.

## 11.2 BPMN

### Estado actual — verificado documentalmente

| Paso | Entidad | Canal | Duración | Requisito previo |
|---|---|---|---|---|
| 1 | SUNARP | En línea | Horas | Ninguno |
| 2 | Municipalidad | **Presencial** | 5 días hábiles | Solicitud al alcalde |
| 3 | CENEPRED | En línea | Horas | Interpretación técnica |
| 4 | **SEDAPAR** | **Presencial** | Variable | **Memoria descriptiva de profesional colegiado + ficha registral ≤ 60 días** |
| 5 | MININTER | En línea | Horas | Interpretación espacial |

Cinco consultas desacopladas, dos presenciales, una con requisito profesional previo, sin trazabilidad, **sin veredicto consolidado**.

### Estado objetivo

Consulta única orquestada: una entrada, resolución espacial, consulta paralela a cinco capas, motor de reglas, salida consolidada con fuente, fecha y nivel de confianza.

## 11.3 Curva de Gartner

Interoperabilidad de datos gubernamentales · *composable government* · SIG analítico · puntuación multicriterio · analítica geoespacial.

Se descarta deliberadamente incorporar tecnologías sin función en el problema.

## 11.4 Cuadro de Mando Integral

| Perspectiva | Indicador | Línea base | Meta |
|---|---|---|---|
| Ciudadano | Tiempo de verificación integral | Semanas | Minutos |
| Ciudadano | Entidades a consultar | 5 | 1 |
| Ciudadano | Trámites presenciales | 2 | 0 en consulta preliminar |
| Proceso | Polígonos de zonificación vigentes | 0 | Cobertura del piloto |
| Proceso | Antigüedad de la capa normativa | — | < 30 días |
| Proceso | Reportes con fuente y fecha en el 100 % de líneas | — | 100 % |
| Impacto | Detección de suelo no habilitable | — | Medición y publicación |
| Impacto | Detección de ausencia de partida registral | — | Medición y publicación |
| Financiera | Costo por reporte emitido | — | Descendente |

## 11.5 OWASP y riesgo

> El sistema procesa información de **titularidad y ubicación de domicilios**. Una fuga produce un **catálogo de objetivos para el crimen organizado**, en una región donde la extorsión pasó de 6,8 a 30,6 denuncias por 100 mil habitantes entre 2019 y 2025.

| Riesgo | Control |
|---|---|
| Exposición de datos sensibles | Minimización; criterio español de dato protegido |
| Control de acceso roto | Autorización por rol |
| Fallas de registro y monitoreo | Auditoría de toda consulta |
| Falsificación de fuente | Trazabilidad de origen y fecha por dato |
| Uso automatizado abusivo | Limitación de tasa; sin barrido masivo del territorio |

## 11.6 Responsabilidad social

| Elemento | Contenido |
|---|---|
| Beneficiarios | Compradores de primera vivienda sin acceso a asesoría — solo 13,8 % contó con ingeniero o arquitecto |
| Daño evitado | Pérdida total e irreversible del ahorro familiar |
| Escala | 61,7 % de viviendas urbanas informales; 93 % de expansión informal |
| Entregable social | Consulta básica gratuita y metodología pública |
| Sostenibilidad | Financiada por el segmento institucional — modelo híbrido Kadaster |

---

# 12. Limitaciones declaradas

Esta sección existe porque un trabajo que no declara sus límites no es investigación.

| # | Limitación | Efecto |
|---|---|---|
| L1 | **La demanda pagada no ha sido medida.** El veredicto es `PENDIENTE` | Ninguna afirmación de viabilidad comercial está respaldada |
| L2 | No se ha determinado si el PDF de zonificación de JLByR es vectorial o raster | El cronograma puede alterarse |
| L3 | No se realizaron entrevistas de desarrollo de clientes | El gasto actual del comprador es supuesto, no dato |
| L4 | No se accedió al registro de la Procuraduría regional | La distribución geográfica de las denuncias es desconocida |
| L5 | No se consultó a notarías ni a cajas municipales | El canal B2B es hipótesis |
| L6 | No existe identificador único de predio | Toda vinculación entre capas es aproximada |
| L7 | La capa de servicios opera con proxy | No sustituye la factibilidad del prestador |
| L8 | La capa delictiva tiene cifra negra y problema de resolución espacial | Requiere calibración con victimización y validación de geocodificación |
| L9 | El modelo hedónico presenta endogeneidad | ¿El delito reduce el precio o los barrios baratos atraen delito? Debe tratarse |
| L10 | Datos de mercado inmobiliario de Arequipa 2025–2026 no obtenidos con detalle | El TAM local no está dimensionado |
| L11 | **La cobertura real de UbicaBien no fue verificada dentro del producto autenticado** | Toda afirmación sobre lo que **no** cubre es inferencia a partir de su sitio público. Debe ejecutarse V1–V4 de `docs/04-startups/ubicabien.md` |
| L12 | **No se determinó si UbicaBien ya digitalizó la zonificación de Arequipa** | Si lo hizo, la ventaja competitiva declarada en la sección 9 está tomada o compartida |

---

# 13. Bibliografía

## Benchmark internacional

1. [Local Authority Searches: LLC1 y CON29 — HomeOwners Alliance](https://hoa.org.uk/advice/guides-for-homeowners/i-am-buying/local-authority-searches-explained/)
2. [Local authority searches explained — GlobalX](https://www.globalx.co/news-resources/knowledge-hub/local-authority-and-llc1-and-con29-searches-explained/)
3. [Material Information for property listings — National Trading Standards](https://www.nationaltradingstandards.uk/news/material-information-for-property-listings-announced/)
4. [NTS Material Information — Open Property Data Association](https://openpropdata.org.uk/national-trading-standards-material-info/)
5. [Section 32 explained — RACV (Victoria)](https://www.racv.com.au/royalauto/property/buying/what-is-section-32.html)
6. [Section 32 Vendor Statements — Parke Lawyers](https://pl.com.au/information-centre/section-32-vendor-statements-victoria-explained)
7. [Standardized Natural Hazards Disclosure Statement — California](https://en.wikipedia.org/wiki/Standardized_Natural_Hazards_Disclosure_Statement)
8. [Title Insurance Industry Analysis 2025 — IBISWorld](https://www.ibisworld.com/united-states/industry/title-insurance/4784/)
9. [Title Insurance: A Comprehensive Overview — ALTA](https://www.alta.org/press/TitleInsuranceOverview.pdf)
10. [Zillow retira climate risk scores — CNN](https://www.cnn.com/2025/12/02/climate/zillow-climate-data-extreme-weather-first-street-redfin)
11. [Zillow drops climate risk scores — The Real Deal](https://therealdeal.com/national/2025/12/01/zillow-drops-climate-risk-scores-after-industry-pushback/)
12. [Open datasets — Kadaster, Países Bajos](https://www.kadaster.nl/zakelijk/datasets/open-datasets)
13. [BAG OGC API — PDOK](https://api.pdok.nl/kadaster/bag/ogc/v2?f=html&lang=en)
14. [Servicios de acceso libre — Sede Electrónica del Catastro, España](https://www.catastro.hacienda.gob.es/ayuda/ayuda_cl.htm)
15. [e-Land Register — Estonia (RIK)](https://www.rik.ee/en/e-land-register/e-land-register-portal)
16. [e-Services & registries — e-Estonia](https://e-estonia.com/solutions/e-governance/e-services-registries/)
17. [Ventanilla Única de Registro — Colombia](https://www.vur.gov.co/)
18. [Consultas en línea — Conservador de Bienes Raíces, Chile](https://www.conservador.cl/portal/consultas_en_linea)
19. [Quality of Land Administration Index — Banco Mundial](https://govdata360.worldbank.org/indicators/h4620451e)
20. [Walk Score Methodology](https://www.walkscore.com/methodology.shtml)
21. [Validation of Walk Score — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC4845899/)

## Panorama competitivo

22. [Sprift — UK Property Data](https://sprift.com/home)
23. [Cape Analytics — Real Estate Property Intelligence](https://capeanalytics.com/real-estate-property-intelligence/)
24. [Jupiter Intelligence — Crunchbase](https://www.crunchbase.com/organization/jupiter-intelligence)
25. [SpotCrime — About](https://spotcrime.io/about)
26. [NeighborhoodScout](https://www.neighborhoodscout.com/)
27. [CrimeGrade](https://crimegrade.org/)
28. [AreaVibes — Neighborhood Crime Statistics](https://www.areavibes.com/library/neighborhood-crime-statistics/)
29. [Proptech en Latinoamérica: Guía Definitiva — Startupeable](https://startupeable.com/proptech/)
30. [Proptech en Latinoamérica 2026 — Houm](https://blog.houm.com/proptech-en-latinoamerica-2026-como-la-tecnologia-esta-transformando-el-mercado-inmobiliario/)

## Perú — situación nacional

31. [Más de 14 millones de personas habitan viviendas informales — PQS](https://pqs.pe/actualidad/mas-de-14-millones-de-personas-habitan-viviendas-informales-2/)
32. [63 % de las viviendas son informales — La República](https://larepublica.pe/economia/2025/07/25/un-peru-construido-por-maestros-de-obra-63-de-las-viviendas-son-informales-porque-peruanos-no-pueden-acreditar-ingresos-formales-hnews-1625150)
33. [Radiografía de la vivienda en el Perú — ASPAI](https://aspai.pe/2026/01/26/radiografia-de-la-vivienda-en-el-peru-principales-indicadores-problematica-y-oportunidades/)
34. [Vivienda de Interés Social y déficit habitacional — Vigilante](https://vigilante.pe/2025/02/17/vivienda-de-interes-social-la-clave-para-cerrar-el-deficit-habitacional-en-peru/)
35. [Housing in Peru — Banco Mundial](https://documents1.worldbank.org/curated/en/214201645586293949/pdf/Housing-in-Peru-An-Instrument-for-Inclusive-and-Resilient-Economic-Recovery.pdf)
36. [Autoconstrucción en el Perú — SENCICO](https://www.gob.pe/institucion/sencico/noticias/1420547-articulo-autoconstruccion-en-el-peru-una-tarea-pendiente)

## Perú — fuentes de datos

37. [Visor de la Base Gráfica Registral — SUNARP](https://www.gob.pe/63173-acceder-al-visor-de-la-base-grafica-registral)
38. [Visor BGR supera 3 millones de consultas — SUNARP](https://www.gob.pe/institucion/sunarp/noticias/1359152-visor-bgr-sunarp-supera-los-3-millones-de-consultas-de-mas-de-360-mil-ciudadanos)
39. [Manual del Usuario Visor BGR — SUNARP](https://www.sunarp.gob.pe/pdfs/visorbgr/MANUAL_DEL_USUARIO_VISOR_BGR.pdf)
40. [SPRL — Extranet SUNARP](https://sprl.sunarp.gob.pe/sprl/ingreso)
41. [Mapa del Delito Georreferenciado — MININTER](https://observatorio.mininter.gob.pe/MapaDelDelitoGeorreferenciado)
42. [GEOMININTER](https://geoportal.mininter.gob.pe/)
43. [Solicitar certificado de factibilidad de agua y alcantarillado — gob.pe](https://www.gob.pe/25043-solicitar-certificado-de-factibilidad-para-servicio-de-agua-potable-y-alcantarillado?child=65539)
44. [Catálogo de aplicaciones con IA en el Estado peruano — PCM](https://www.gob.pe/institucion/pcm/informes-publicaciones/6879780-catalogo-de-aplicaciones-con-inteligencia-artificial-en-el-estado-peruano)

## Arequipa

45. [Arequipa 2025: extorsión, robos armados y sicariato — El Búho](https://elbuho.pe/2026/01/arequipa-2025-extorsion-robos-armados-y-sicariato-marcan-el-avance-del-crimen-organizado/)
46. [Encuesta de Victimización y Percepción de Seguridad — UCSP](https://ucsp.edu.pe/archivos/publicaciones/cegob/Encuesta-Victimizacion-Percepcion-Seguridad-Ciudadana.pdf)
47. [Tres de cada diez arequipeños víctimas de delito — UCSP](https://ucsp.edu.pe/noticias/tres-de-cada-diez-arequipenos-victimas-delito-ultimo-ano/)
48. [El 88 % de la población percibe inseguridad — Diario Correo](https://diariocorreo.pe/edicion/arequipa/arequipa-el-88-de-la-poblacion-percibe-inseguridad-noticia/)
49. [Procuraduría tiene mil denuncias por estafas en compra y venta de terrenos — Diario Viral](https://diarioviral.pe/arequipa/43/cercado/procuraduria-tiene-mil-denuncias-por-estafas-en-la-compra-y-venta-de-terrenos-35360)
50. [Alertan sobre venta irregular de lotes — El Búho](https://elbuho.pe/2026/09/alertan-sobre-venta-irregular-de-lotes-turisticos-como-terrenos-urbanos-en-la-libertad/)
51. [El millonario negocio detrás de la venta irregular de terrenos agrícolas — Revista Economía](https://www.revistaeconomia.com/arequipa-el-millonario-negocio-detras-de-la-venta-irregular-de-terrenos-agricolas/)
52. [Traficantes de terreno estafaron a 20 mil familias — Diario Correo](https://diariocorreo.pe/edicion/arequipa/arequipa-traficantes-de-terreno-estafaron-a-20-mil-familias-594466/)
53. [Plano de zonificación PDM — Municipalidad de JLByR](https://www.munibustamante.gob.pe/archivos/gdu/planos/001_plano_de_zonificacion.pdf)
54. [Plan Urbano Distrital — JLByR](https://www.munibustamante.gob.pe/archivos/gdu/planos/plan_urbano.pdf)
55. [Muni Virtual — Municipalidad Provincial de Arequipa](https://www.muniarequipa.gob.pe/muni-virtual-4/)
56. [Mesa de partes virtual — Municipalidad de Paucarpata](https://mpv.munipaucarpata.gob.pe/)
57. [Mapa de peligro de la ciudad de Arequipa — SIGRID/CENEPRED](https://sigrid.cenepred.gob.pe/sigridv3/documento/3546)
58. [Evaluación de riesgos en torrenteras, Yura — SIGRID](https://sigrid.cenepred.gob.pe/sigridv3/documento/6076)
59. [Puntos críticos de inundación en Arequipa, ANA — SIGRID](http://sigrid.cenepred.gob.pe/sigridv3/documento/8814)
60. [Zonificación sísmica-geotécnica de suelos: Arequipa — GEOIDEP](https://catalogo.geoidep.gob.pe/metadatos/srv/api/records/26f6f0eb-8bc4-4427-b2a0-f5c33b479752)
61. [Sedapar devolvió S/ 6 millones al Ministerio de Vivienda — La República](https://larepublica.pe/sociedad/2026/05/11/sedapar-no-entrego-agua-gratuita-a-poblacion-vulnerable-de-arequipa-y-devolvio-s6-millones-al-ministerio-de-vivienda-855195)
62. [80 % de la población desabastecida de agua — Infobae](https://www.infobae.com/peru/2024/02/08/arequipa-sigue-sin-agua-80-de-la-poblacion-se-ha-desabastecido-de-un-momento-a-otro-alerta-alcalde/)
63. [Cofopri evalúa 5 000 lotes en Arequipa — TVPerú](https://www.tvperu.gob.pe/noticias/nacionales/cofopri-evalua-5000-lotes-en-arequipa-para-avanzar-en-su-formalizacion-predial)
64. [Ministerio de Vivienda entrega 2 840 títulos en Arequipa](https://www.gob.pe/institucion/vivienda/noticias/1400702-arequipa-ministerio-de-vivienda-entrega-2840-titulos-de-propiedad-a-familias-e-instituciones-de-ocho-provincias-de-la-region)

## Fundamento académico

65. [Housing prices and crime perception (Barcelona) — Empirical Economics](https://link.springer.com/article/10.1007/s00181-012-0624-y)
66. [Hedonic valuation of criminal violence (Acapulco) — Empirical Economics](https://link.springer.com/article/10.1007/s00181-019-01804-3)
67. [Panel data estimates: types of crime and housing prices — ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0166046210000086)
68. [Impacto de la inseguridad en el precio de las viviendas, Guanajuato — Redalyc](https://www.redalyc.org/journal/674/67472343006/html/)
69. [Precios hedónicos del mercado inmobiliario de Lima — BCRP](https://www.bcrp.gob.pe/docs/Publicaciones/Revista-Estudios-Economicos/36/ree-36-mundaca-sanchez.pdf)
70. [Crime and Housing Prices — Ihlanfeldt & Mayock, FSU](https://cosspp.fsu.edu/dmi/wp-content/uploads/sites/8/2020/09/02.2009-Crime-and-Housing-Prices.pdf)

---

*Documento generado como entregable del curso de Gestión Estratégica de Tecnologías de Información. Todas las fuentes fueron verificadas el 16 de septiembre de 2026. Las afirmaciones no verificadas están explícitamente marcadas como supuestos en la sección 12.*
