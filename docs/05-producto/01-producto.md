# Definición de Producto

---

## 1. Declaración del problema

> **Problema.** El comprador de vivienda o lote en Arequipa no puede verificar, antes de transferir dinero, si una ubicación es legalmente transferible, urbanísticamente habilitable, físicamente segura, servible con agua y desagüe, y tolerable en términos de exposición delictiva.
>
> **Causa raíz.** El Estado organiza la información por institución; el ciudadano la necesita organizada por predio. Cinco entidades soberanas custodian cinco capas y ninguna tiene el mandato de responder la única pregunta relevante para la decisión.
>
> **Consecuencia medida.** Más de 1 000 denuncias por estafa en compraventa de terrenos en Arequipa al cierre de 2024, sobre un universo nacional donde el 61,7 % de las viviendas urbanas es informal y el 93 % de la expansión urbana ocurre fuera del marco formal.

---

## 2. Qué es el producto

Una **capa de agregación y estandarización de información predial** que entrega, a partir de una ubicación, un veredicto consolidado con la fuente citada y fechada en cada afirmación.

### Entrada

Coordenada en mapa, dirección, o enlace de un aviso publicado.

### Salida

| Componente | Contenido |
|---|---|
| Semáforo por capa | Verde, ámbar o rojo en cada uno de los cinco verticales |
| Informe descargable | Un hallazgo por línea, con institución fuente, fecha del dato y nivel de confianza |
| Alertas críticas | Ausencia de partida registral, suelo no habilitable, zona de peligro alto |
| Declaración de límites | Qué no pudo verificarse y por qué |

### Las cinco capas

| # | Capa | Fuente | Nivel de certeza |
|---|---|---|---|
| 1 | Registral | SUNARP — Visor BGR, SPRL | Alto |
| 2 | Urbanística | Capa de zonificación digitalizada sobre PDM vigente | Alto en distrito piloto |
| 3 | Peligro físico | SIGRID — CENEPRED, ANA, GEOIDEP | Variable según cobertura |
| 4 | Servicios | **Proxy declarado** — proximidad a red, habilitación, historial de cortes | **Bajo, etiquetado** |
| 5 | Exposición delictiva | MININTER, calibrado con victimización INEI/UCSP | Medio |

---

## 3. Lo que el producto NO es

Esta sección es tan importante como la anterior, y responde directamente a la lección del caso Zillow.

| No es | Por qué |
|---|---|
| Un certificado | **Informa, no certifica.** No sustituye la publicidad registral ni el certificado de parámetros ni la factibilidad del prestador |
| Un juicio de titularidad | No declara quién es el propietario; reporta lo que el registro consigna, con su fecha |
| Una calificación de predio individual | Trabaja por zona agregada para evitar el conflicto que llevó al retiro de First Street en Zillow |
| Un directorio de propietarios | Aplica el criterio español: geometría y atributos públicos, identidad del titular protegida |
| Una tasación | No estima valor comercial |

---

## 4. Modelo de negocio

| Campo | Definición |
|---|---|
| **Propuesta de valor** | «Antes de firmar, sepa si ese terreno le va a dar problemas — en minutos y con la fuente oficial al lado.» |
| **Segmento primario** | Comprador de primera vivienda o lote en el borde de expansión de Arequipa Metropolitana |
| **Segmento secundario** | Notarías, tasadores, analistas de crédito de cajas municipales |
| **Canales** | Grupos de compraventa en redes sociales — el mismo canal donde hoy se publican las ofertas fraudulentas; alianza con el Colegio de Arquitectos filial Arequipa; referidos de afectados |
| **Modelo de ingresos** | Consulta básica gratuita como captación; reporte consolidado de pago; suscripción por volumen en el segmento institucional. Estructura tomada del modelo híbrido del Kadaster neerlandés |
| **Estructura de costos** | Concentrada en la **digitalización y mantenimiento de la capa de zonificación**. La infraestructura de cómputo es marginal |
| **Ventaja injusta** | Esa misma capa. La zonificación de Arequipa no está expuesta como servicio geoespacial: exige ingesta, georreferenciación, vectorización y mantenimiento normativo. Es una barrera **local**, no replicable desde otra ciudad |

---

## 5. Arquitectura funcional

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

| # | Restricción | Consecuencia de diseño |
|---|---|---|
| A1 | SUNARP no expone API pública documentada | Consumo asistido, no automatizado |
| A2 | No existe identificador único de predio compartido entre instituciones | Vinculación por coincidencia geográfica, con error declarado |
| A3 | `gob.pe` bloquea acceso programático (HTTP 418); `muniarequipa.gob.pe` responde 403 | Los conectores no pueden asumir acceso libre |
| A4 | SEDAPAR no ofrece consulta de factibilidad por ubicación | La capa 4 opera con proxy etiquetado |
| A5 | La zonificación vive en PDF | Requiere construcción y mantenimiento de capa propia |

---

## 6. Alcance del piloto

**Distrito piloto: José Luis Bustamante y Rivero.**

| Criterio | Fundamento |
|---|---|
| Materia prima | Único distrito analizado con plano de zonificación, catastral y vial descargables |
| Estabilidad normativa | Distrito consolidado; zonificación estable durante el ciclo del proyecto |
| Señal en capa delictiva | 10,12 % de hechos delictivos reportados |
| Estado actual modelable | TUPA publicado |

**Paucarpata:** caso de contraste, no piloto — su PDU distrital está en elaboración.
**Miraflores:** segunda fase de expansión.

---

## 7. Gestión de riesgos

| # | Riesgo | Severidad | Mitigación |
|---|---|---|---|
| R1 | El PDF de zonificación podría ser raster escaneado | **Alta** | Verificación en QGIS antes de comprometer cronograma; si es raster, reducir alcance a sector piloto declarado |
| R2 | Transición PDM 2016–2025 → 2025–2045 | Media | Versionado de la capa normativa con fecha de vigencia |
| R3 | Ausencia de API en SUNARP | Media | Arquitectura de consumo asistido, declarada |
| R4 | Responsabilidad legal por calificar un predio | **Alta** | Informa, no certifica; fuente y fecha por dato; zona agregada; sin juicio de titularidad |
| R5 | Fuga de datos convertiría el sistema en catálogo de objetivos para el crimen organizado | **Crítica** | Control de acceso, minimización de dato personal, registro de auditoría — ver mapeo OWASP |
| R6 | Resistencia gremial del sector inmobiliario | Media | Metodología pública y auditable; el ataque a First Street fue por exactitud, no por la idea |
| R7 | El Estado cierra el vacío | Baja en el corto plazo | Declarado como horizonte de obsolescencia. La evidencia comparada —3 144 jurisdicciones sin estandarizar en 150 años— sugiere que el vacío municipal es estructural |

---

## 8. Horizonte de obsolescencia — declaración explícita

Si el Perú avanza al **Modelo 1** (obligación de divulgación del vendedor, como Victoria o California) o completa el **Modelo 3** (bien público digital, como Países Bajos o España), este producto deja de tener razón comercial de existir y se convierte en infraestructura pública.

**Ese desenlace es socialmente preferible y el proyecto lo declara.** La evidencia comparada indica que la capa municipal es la última en resolverse, lo que otorga una ventana de años, no de meses.
