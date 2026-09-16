# 03 — Ajuste Solución–Mercado

> Método: `solution-market-fit`. Cada concepto se puntúa contra el dossier de evidencia, no contra el entusiasmo del equipo. El ajuste con la evidencia **no equivale a viabilidad probada**.

---

## Insumos consumidos

| Artefacto | Contenido |
|---|---|
| Causa raíz | El Estado organiza el dato por institución; el ciudadano lo necesita por predio |
| Segmento | Comprador de primera vivienda o lote en el borde de expansión de Arequipa |
| Workaround | 4–5 consultas desacopladas, semanas de duración, sin veredicto único |
| Veredicto del dossier | `PENDIENTE` — problema documentado, demanda pagada no medida |

> **Advertencia metodológica.** Con veredicto `PENDIENTE`, ningún concepto puede declararse viable. Los puntajes que siguen miden **coherencia con la evidencia disponible**, no validación de mercado.

---

## Concepto A — Reporte de Due Diligence Predial

Central de riesgo del predio. El usuario indica una ubicación y recibe un veredicto en semáforo más un informe descargable con la fuente citada y fechada línea por línea, sobre cinco capas: registral, urbanística, peligro físico, servicios y exposición delictiva.

| Campo del canvas | Definición |
|---|---|
| **Propuesta de valor** | «Antes de firmar, sepa si ese terreno le va a dar problemas — en minutos y con la fuente oficial al lado.» |
| **Segmento** | Comprador de primera vivienda o lote en el borde de expansión de Arequipa. Secundario: notarías, tasadores, analistas de crédito de cajas municipales. |
| **Canales** | Grupos de compraventa en Facebook Marketplace (el mismo canal donde hoy se publican las ofertas fraudulentas); alianza con notarías y con el Colegio de Arquitectos filial Arequipa; referidos de afectados. |
| **Modelo de ingresos** | Pago por reporte (B2C) y suscripción por volumen (B2B). |
| **Estructura de costos** | **Digitalización y normalización del dato municipal** — concentra el costo real. La infraestructura de cómputo es marginal. |
| **Ventaja injusta** | Precisamente ese costo. La zonificación de Arequipa no está expuesta como servicio geoespacial: requiere ingesta, georreferenciación, vectorización y mantenimiento. Es una barrera **local**: no se replica desde Lima sin presencia en campo. |

**Ajuste con la evidencia: `PARCIALMENTE SOPORTADO`**

- *Soportado por:* A1–A4 (daño cuantificado), B1–B5 (universo dimensionado), C2–C4 (fragmentación verificada), D1–D3 (precedente del *title plant* con causa raíz idéntica), D6 (modelo de agregación validado).
- *No soportado:* E1 — no existe evidencia de que un comprador arequipeño pague por este reporte. E3 — no hay base para fijar precio.
- *Perfil de riesgo:* **extiende un workaround observado**. Riesgo bajo, techo alto.

---

## Concepto B — Índice de Exposición Residencial sobre portales

Puntaje 0–100 por ubicación, integrado como capa en portales inmobiliarios.

| Campo del canvas | Definición |
|---|---|
| **Propuesta de valor** | «Compare barrios con un número.» |
| **Segmento** | Usuario de portal inmobiliario. El **cliente pagador es el portal**, no el comprador. |
| **Canales** | Integración vía API con Urbania, Adondevivir o Properati. |
| **Modelo de ingresos** | Licencia al portal. |
| **Estructura de costos** | Modelado y mantenimiento del índice. |
| **Ventaja injusta** | Débil. El algoritmo de puntuación es replicable en tiempo corto. |

**Ajuste con la evidencia: `NO SOPORTADO` en esta forma**

- *Soportado únicamente el problema general*, no esta forma de solución.
- *Contraevidencia documentada:* Zillow retiró los puntajes de riesgo climático de First Street de más de un millón de avisos en noviembre–diciembre de 2025 tras presión de la industria. El efecto medido fue que los inmuebles marcados como de alto riesgo se vendieron aproximadamente **1 % por debajo** de su valor de mercado. Ver [CNN](https://www.cnn.com/2025/12/02/climate/zillow-climate-data-extreme-weather-first-street-redfin).
- **Fallo estructural del concepto:** el pagador propuesto es el actor cuyo incentivo económico se perjudica si el producto funciona. Un portal no financia sostenidamente una función que reduce el precio de su inventario.
- *Decisión:* **no se descarta la funcionalidad, se descarta el canal.** El índice se absorbe como componente del Concepto A, donde el equipo controla la relación con el usuario final.

---

## Concepto C — API de riesgo de garantía para entidades financieras

Verificación vendida a quien otorga crédito hipotecario: una garantía sobre predio no habilitable o en zona de riesgo es una garantía de ejecución dudosa.

| Campo del canvas | Definición |
|---|---|
| **Propuesta de valor** | «Reduzca la pérdida esperada de su cartera hipotecaria verificando la garantía antes del desembolso.» |
| **Segmento** | Cajas municipales, Edpymes y bancos con cartera hipotecaria en Arequipa. |
| **Canales** | Venta institucional directa; relación con áreas de riesgos. |
| **Modelo de ingresos** | Contrato anual más precio por consulta. |
| **Estructura de costos** | Ciclo de venta institucional largo; exigencias de cumplimiento y auditoría. |
| **Ventaja injusta** | La misma capa de dato del Concepto A, con mayor valor por consulta. |

**Ajuste con la evidencia: `PARCIALMENTE SOPORTADO`**

- *Soportado por:* la lógica económica es sólida y D1 demuestra que el sector financiero de EE. UU. sostiene una industria de USD 16 200 M sobre exactamente este riesgo.
- *No soportado:* E4 — no existe evidencia de que una entidad financiera arequipeña haya manifestado esta necesidad. Ninguna entrevista institucional ha sido realizada.
- *Perfil de riesgo:* ciclo de venta largo, dependiente de relación institucional. **Inadecuado como primer producto en un ciclo académico.** Adecuado como segunda línea de ingresos una vez normalizada la capa de dato.

---

## Verificación anti-«solución en busca de problema»

| Pregunta de control | A | B | C |
|---|---|---|---|
| ¿Mapea directamente a la causa raíz declarada? | Sí | Parcial — atiende comparación, no verificación | Sí |
| ¿La evidencia respalda **esta forma** de solución? | Parcial | No | Parcial |
| ¿Extiende conducta observada o inventa necesidad latente? | Extiende | Extiende | Extiende |
| ¿Requiere crear una necesidad nueva? | No | No | No |

Ninguno de los tres exige crear una necesidad latente. Es un perfil de riesgo conservador, con techo acotado pero fundamento sólido.

---

## Recomendación

> **Concepto A**, posicionado explícitamente como **capa de agregación y estandarización de información predial** — el equivalente arequipeño de un *title plant*.

**Fundamento.** Gana por cuatro razones verificables, no por preferencia. Primero, resuelve la causa raíz —fragmentación institucional— mientras B atiende únicamente el síntoma de comparación. Segundo, extiende un workaround observado en lugar de inventar una necesidad latente, lo que lo ubica en el perfil de riesgo conservador que corresponde a un equipo sin capital. Tercero, el usuario y el pagador son la misma persona, con incentivos alineados; en B el pagador propuesto pierde dinero si el producto funciona, y la retirada de Zillow demuestra que ese conflicto no es teórico. Cuarto, la ventaja competitiva no reside en el algoritmo —replicable en días— sino en la capa de zonificación digitalizada y mantenida, que constituye una barrera local y costosa de reproducir.

**Condición de la recomendación.** Es una recomendación de **diseño**, no una declaración de viabilidad. Con veredicto del dossier en `PENDIENTE`, el Concepto A debe superar los umbrales precomprometidos de F.1 y F.2 antes de comprometer esfuerzo de construcción.

---

## Riesgos abiertos del concepto recomendado

| # | Riesgo | Mitigación de diseño |
|---|---|---|
| R1 | El plano de zonificación de JLByR podría ser raster escaneado y no vectorial | Verificación en QGIS antes de comprometer cronograma. Si es raster, el alcance se reduce a un sector piloto y se declara desde el inicio. |
| R2 | Transición normativa del PDM 2016–2025 al PDM 2025–2045 | Versionado de la capa normativa por diseño, con fecha de vigencia en cada consulta |
| R3 | SUNARP no expone API pública documentada | Arquitectura de consumo asistido, no automatizado. Declarado como restricción, no ocultado. |
| R4 | Riesgo legal y reputacional por calificar un predio individual | El producto **informa, no certifica**. Cita fuente y fecha por dato; no emite juicio de titularidad; trabaja por zona agregada. Criterio de privacidad adoptado del Catastro español: geometría y atributos públicos, identidad del titular protegida. |
| R5 | Fuga de datos convertiría el sistema en catálogo de objetivos para el crimen organizado | Control de acceso, minimización de dato personal, registro de auditoría. Desarrollado en el mapeo OWASP. |
| R6 | El Estado podría cerrar el vacío avanzando al Modelo 1 o completando el Modelo 3 | Declarado explícitamente como horizonte de obsolescencia. La evidencia comparada (3 144 jurisdicciones en EE. UU. sin estandarizar en 150 años) sugiere que el vacío municipal es estructural. |
