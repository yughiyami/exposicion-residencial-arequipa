# Mapeo al Curso de Gestión Estratégica de TI

Correspondencia entre los componentes exigidos por el sílabo y el contenido de esta investigación.

---

## 1. PETI — Plan Estratégico de Tecnologías de Información

### Alineamiento institucional

| Instrumento | Vínculo |
|---|---|
| Política Nacional de Gobierno Digital | Marco de alineamiento del plan |
| Ley de Gobierno Digital e interoperabilidad del Estado | Fundamento normativo de la integración propuesta |
| Catálogo de aplicaciones con IA en el Estado peruano — PCM | Referencia institucional de iniciativas comparables |
| PDM Arequipa, Ordenanza Municipal N.º 975 | Marco normativo de la capa urbanística |

### Argumento central del PETI

> **No se propone crear información nueva. Se propone integrar información existente.**

Cuatro de las cinco capas ya son públicas y están digitalizadas. El costo del proyecto se concentra en estructurar una sola capa —la zonificación— y en vincular las cinco. Este argumento es económicamente defendible y distingue la propuesta de proyectos que exigen levantamiento de información desde cero.

### Análisis de cadena de valor

Cadena de valor del proceso de adquisición de vivienda, desde la búsqueda hasta la inscripción registral. El producto interviene en la actividad de **verificación previa a la decisión**, hoy inexistente como eslabón formal.

### Marco de diagnóstico

**Índice de Calidad de la Administración de Tierras** del Banco Mundial, con cinco dimensiones aplicadas a Arequipa:

1. Confiabilidad de la infraestructura
2. Transparencia de la información
3. Cobertura geográfica
4. Resolución de disputas de tierras
5. Acceso equitativo a derechos de propiedad

Usar un marco de organismo internacional en lugar de una estructura propia eleva el rigor del diagnóstico.

---

## 2. BPMN — Estado actual y estado objetivo

### Estado actual (As-Is)

Proceso verificado documentalmente, no supuesto:

| Paso | Entidad | Canal | Duración | Requisito previo |
|---|---|---|---|---|
| 1 | SUNARP | En línea | Horas | Ninguno |
| 2 | Municipalidad distrital | **Presencial** | 5 días hábiles | Solicitud dirigida al alcalde |
| 3 | CENEPRED / SIGRID | En línea | Horas | Interpretación técnica |
| 4 | **SEDAPAR** | **Presencial** | Variable | **Memoria descriptiva firmada por profesional colegiado + ficha registral de antigüedad menor a 60 días** |
| 5 | MININTER | En línea | Horas | Interpretación espacial |

**Características del estado actual:** cinco consultas desacopladas, dos de ellas presenciales, una con requisito profesional previo, sin trazabilidad entre sí y **sin veredicto consolidado**.

> El paso 4 es el hallazgo más potente para la sustentación: para saber si un terreno tendrá agua, el ciudadano debe contratar a un profesional colegiado **antes de comprarlo**.

### Estado objetivo (To-Be)

Consulta única orquestada. Una entrada —la ubicación—, resolución espacial, consulta paralela a las cinco capas, motor de reglas, y salida consolidada con fuente, fecha y nivel de confianza por línea.

### Fuentes documentales para el modelado

- TUPA de José Luis Bustamante y Rivero
- TUPA de Paucarpata
- Ficha de trámite de factibilidad de SEDAPAR en gob.pe
- Fichas informativas de parámetros urbanísticos de Miraflores

---

## 3. Curva de Gartner — Tecnologías aplicadas

| Tecnología | Aplicación en el proyecto |
|---|---|
| Interoperabilidad de datos gubernamentales | Núcleo de la propuesta |
| *Composable government* | Marco conceptual de la integración |
| SIG analítico | Vectorización, resolución espacial, intersección de capas |
| Puntuación multicriterio | Motor de semáforo por capa |
| Analítica geoespacial | Calibración de la capa delictiva |

Se descarta deliberadamente la incorporación de tecnologías sin función en el problema. La sobrecarga tecnológica es un error frecuente en este tipo de propuestas.

---

## 4. Cuadro de Mando Integral

| Perspectiva | Indicador | Línea base | Meta |
|---|---|---|---|
| **Ciudadano** | Tiempo de verificación integral | Semanas | Minutos |
| **Ciudadano** | Número de entidades que el ciudadano debe consultar | 5 | 1 |
| **Ciudadano** | Trámites presenciales requeridos | 2 | 0 en la consulta preliminar |
| **Proceso interno** | Polígonos de zonificación digitalizados y vigentes | 0 | Cobertura del distrito piloto |
| **Proceso interno** | Antigüedad de la capa normativa respecto de la ordenanza vigente | — | Menor a 30 días |
| **Proceso interno** | Porcentaje de reportes con fuente y fecha en el 100 % de las líneas | — | 100 % |
| **Impacto** | Consultas en las que se detecta suelo no habilitable | — | Medición y publicación |
| **Impacto** | Consultas en las que se detecta ausencia de partida registral | — | Medición y publicación |
| **Financiera** | Costo por reporte emitido | — | Descendente por efecto de la capa reutilizable |

---

## 5. OWASP y análisis de riesgo

Este proyecto tiene una particularidad que eleva la exigencia del análisis de seguridad por encima de lo habitual en un trabajo académico.

> El sistema procesa información de **titularidad y ubicación de domicilios**. Una fuga no produce una molestia: produce un **catálogo de objetivos para el crimen organizado**, en una región donde las denuncias por extorsión pasaron de 6,8 a 30,6 por cada 100 mil habitantes entre 2019 y 2025.

### Controles derivados

| Riesgo | Control |
|---|---|
| Exposición de datos sensibles | Minimización: adoptar el criterio español — geometría y atributos públicos, identidad del titular protegida |
| Control de acceso roto | Autorización por rol; el reporte completo no se expone sin autenticación |
| Fallas de registro y monitoreo | Registro de auditoría de toda consulta, con retención definida |
| Falsificación de identidad de fuente | Cada dato del reporte conserva trazabilidad de origen y fecha |
| Uso automatizado abusivo | Limitación de tasa; el sistema no debe permitir barrido masivo del territorio |

### Riesgo legal y reputacional

Control derivado del caso Zillow: **informa, no certifica**; zona agregada en lugar de predio individual; metodología publicada; sin juicio de titularidad.

---

## 6. Infraestructura y continuidad

El proyecto **no requiere** un centro de datos de alta categoría. Declararlo así es más riguroso que sobredimensionar:

| Componente | Requerimiento real |
|---|---|
| Capa de zonificación | Almacenamiento geoespacial con respaldo y versionado |
| Consulta a fuentes externas | Dependencia de disponibilidad de terceros — riesgo declarado, no controlable |
| Continuidad | El servicio es consultivo, no crítico: una interrupción no genera daño a terceros |

El riesgo de continuidad relevante **no es de infraestructura propia**, sino de **disponibilidad de las fuentes del Estado**, verificada durante esta investigación: `gob.pe` bloquea acceso programático y `muniarequipa.gob.pe` responde 403 a solicitudes automatizadas.

---

## 7. Proyecto de Responsabilidad Social

| Elemento | Contenido |
|---|---|
| Población beneficiaria | Compradores de primera vivienda en el borde de expansión, segmento sin acceso a asesoría profesional — recuérdese que solo el 13,8 % de las viviendas informales contó con asistencia de ingeniero o arquitecto |
| Daño evitado | Pérdida total e irreversible del ahorro familiar |
| Escala del problema | 61,7 % de viviendas urbanas informales; 93 % de la expansión urbana fuera del marco formal |
| Entregable social | Consulta básica gratuita y metodología pública |
| Sostenibilidad | El componente gratuito se financia con el segmento institucional, siguiendo el modelo híbrido del Kadaster neerlandés |
