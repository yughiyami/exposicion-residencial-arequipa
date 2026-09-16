# Reino Unido — Modelo 1: Obligación legal de divulgación

El sistema más completo del benchmark. Opera en **dos niveles simultáneos**: verificación obligatoria durante la transacción, y divulgación obligatoria en el aviso publicitario.

---

## Nivel 1 — Local Authority Search (durante la transacción)

En Inglaterra y Gales la búsqueda ante la autoridad local es parte obligatoria del proceso de *conveyancing*. Es **exigida por los prestamistas hipotecarios** y fuertemente recomendada incluso en compras al contado.

Se compone de dos documentos:

### LLC1 — Local Land Charges Register

Revela cargas y obligaciones inscritas contra el título del predio:

- Cargas financieras
- Condiciones y acuerdos de planeamiento urbano
- Órdenes de protección de árboles (*Tree Preservation Orders*)
- Designación de área de conservación
- Condición de edificio protegido (*listed building*)
- Notificaciones de ejecución
- Obligación por *Community Infrastructure Levy*

### CON29 — Consultas a la autoridad local

Cubre información relativa a:

- Vías públicas y propuestas de nuevas carreteras o proyectos ferroviarios
- Decisiones de planeamiento que puedan afectar al predio
- Notificaciones estatutarias pendientes
- Infracciones de planeamiento o de reglamento de edificación
- **Existencia de orden de expropiación forzosa**

### El principio jurídico que importa

> Todas las inscripciones del LLC1 son **legalmente vinculantes para los propietarios sucesivos**. Si la información estaba disponible en el registro, obliga al comprador **aunque no haya realizado la búsqueda**.

El desconocimiento no exime. Esto invierte por completo el incentivo: verificar deja de ser opcional.

**Fuentes:** [HomeOwners Alliance](https://hoa.org.uk/advice/guides-for-homeowners/i-am-buying/local-authority-searches-explained/) · [GlobalX](https://www.globalx.co/news-resources/knowledge-hub/local-authority-and-llc1-and-con29-searches-explained/)

---

## Nivel 2 — Material Information (en el aviso publicitario)

Régimen definido por **National Trading Standards** sobre qué debe mostrar obligatoriamente todo aviso inmobiliario. Es el análogo más cercano al producto propuesto en este repositorio.

| Parte | Contenido | Aplicación |
|---|---|---|
| **A** | Banda de *council tax* o tarifa, precio o renta, tipo de tenencia | Todos los avisos |
| **B** | Tipo de propiedad, materiales de construcción, número de ambientes, servicios públicos, estacionamiento | Todos los avisos |
| **C** | **Riesgo de inundación**, restricciones registrales y demás afectaciones | Solo si el predio está afectado |

### Exigibilidad

Las obligaciones de Material Information son exigibles bajo el **DMCC Act 2024**.

La regla operativa clave:

> El agente debe **tomar pasos razonables para establecer** la información, no simplemente repetir lo que declara el vendedor.

### Evolución normativa

- 2022 — introducción de la Parte A
- Noviembre de 2023 — publicación de las Partes B y C
- 2024 — se consolida como guía estándar para avisos inmobiliarios

**Fuentes:** [National Trading Standards](https://www.nationaltradingstandards.uk/news/material-information-for-property-listings-announced/) · [Open Property Data Association](https://openpropdata.org.uk/national-trading-standards-material-info/)

---

## Ecosistema de datos

El Reino Unido desarrolló un estándar sectorial de datos prediales a través de la **Open Property Data Association**, y una capa comercial de agregadores. El caso más relevante es **Sprift**: entrega más de 300 puntos de dato sobre más de 30 millones de propiedades residenciales vía API REST o paquetes a medida, **sin producir dato primario**.

**Fuente:** [Sprift](https://sprift.com/home)

---

## Lecciones transferibles al caso Arequipa

| # | Lección | Aplicación |
|---|---|---|
| 1 | La información puede obligarse a viajar **con el inmueble**, no con el comprador | Referente normativo para una propuesta de política pública regional |
| 2 | La estructura A/B/C separa lo universal de lo condicional | Modelo directo para estructurar el reporte: capas siempre presentes vs. capas que solo aplican si el predio está afectado |
| 3 | «Tomar pasos razonables para establecer» es un estándar de diligencia auditable | Define el nivel de responsabilidad que el producto debe asumir sin llegar a certificar |
| 4 | El agregador no produce dato: lo estandariza | Confirma la arquitectura propuesta |
