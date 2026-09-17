# 04 — Referencias Académicas Q1–Q4

> Catálogo de literatura académica indexada consultada para fundamentar la función clave del producto. Cuartil según **SCImago Journal Rank (SJR)**, verificado el 17 de septiembre de 2026. Los artículos de acceso abierto fueron **descargados** a [`referencias/pdf/`](../../referencias/pdf/); su texto extraído está en [`referencias/texto/`](../../referencias/texto/) para cita verificable.

---

## Tabla maestra

| # | Referencia | Journal / Editor | Cuartil SJR | Tema | Descargado |
|---|---|---|---|---|---|
| A1 | INEI (2023). *La inseguridad ciudadana en el Perú: una propuesta de índice a nivel subnacional desde datos administrativos* | INEI — investigación institucional | N/A (fuente oficial) | Metodología de índice, bandas categóricas, corrección de subregistro | ✅ `INEI_propuesta_indice_inseguridad.pdf` (84 pp.) |
| A2 | Riascos Villegas, A. J., Ñungo, J. S., Gómez Tobón, L., Dulce Rubio, M., Gómez, F. (2023). *Modelling underreported spatio-temporal crime events*. PLOS ONE, 18(7) | PLOS ONE | **Q1** (Multidisciplinary) | Corrección de subregistro con datos de Bogotá, Colombia | ✅ `PLOS_ONE_Modelling_Underreported_Crime.pdf` (22 pp.) |
| A3 | Ihlanfeldt, K., Mayock, T. (2010). *Panel data estimates of the effects of different types of crime on housing prices*. Regional Science and Urban Economics, 40(2-3), 161–172 | Regional Science and Urban Economics (Elsevier) | **Q1** (SJR 1.472) | Efecto del delito sobre el precio de vivienda, por tipo de delito | ✅ `FSU_Ihlanfeldt_Mayock_Crime_Housing_Prices.pdf` (50 pp., preprint institucional) |
| A4 | Andersen, H. A., Mueller-Johnson, K. (2018). *The Danish Crime Harm Index: How It Works and Why It Matters*. Cambridge Journal of Evidence-Based Policing, 2, 52–69 | Cambridge J. Evidence-Based Policing (Springer) | No indexado en SJR (revista joven) | Ponderación de delitos por gravedad, no por conteo simple | ✅ `Danish_Crime_Harm_Index_Springer.pdf` (30 pp.) |
| A5 | Sherman, L. W., Neyroud, P. W., Neyroud, E. (2016). *The Cambridge Crime Harm Index: Measuring Total Harm From Crime Based On Sentencing Guidelines*. Policing: A Journal of Policy and Practice, 10(3), 171–183 | Policing (Oxford Academic) | Q2 (Sociology and Political Science) | Metodología original de ponderación por daño | Citado vía A4; PDF directo no accesible en acceso abierto |
| A6 | Barcelona (2004–2006): *Housing prices and crime perception*. Empirical Economics | Empirical Economics (Springer) | **Q1** (SJR 0.76) | Precios hedónicos calibrados con encuesta de victimización | Referencia bibliográfica — ver `docs/01-verticales/v5-delictiva.md` |
| A7 | Acapulco (2015–2016): *A hedonic approach to the valuation of the effect of criminal violence on housing prices*. Empirical Economics | Empirical Economics (Springer) | **Q1** (SJR 0.76) | Violencia criminal y precio de vivienda, contexto latinoamericano | Referencia bibliográfica |
| A8 | Mundaca, Sánchez. *Precios hedónicos del mercado inmobiliario de Lima*. Revista de Estudios Económicos, BCRP | BCRP (banco central) | N/A (fuente oficial) | Agenda hedónica peruana | Referencia bibliográfica — descarga bloqueada por el servidor del BCRP |
| A9 | Willingness to pay for piped water — Sri Lanka. *Letters in Spatial and Resource Sciences* | Springer | **Q2** (SJR 0.336) | Disposición a pagar por agua potable, análisis hedónico | Referencia bibliográfica |
| A10 | Willingness to pay for water — Mexico City, Indonesia (revisión) | Environment and Development Economics / diversos | Q1–Q2 según fuente | Servicios básicos y valorización de vivienda en economías en desarrollo | Referencia bibliográfica |

---

## Fuentes oficiales complementarias (no arbitradas, valor probatorio directo)

| # | Documento | Institución | Uso en el proyecto | Descargado |
|---|---|---|---|---|
| B1 | *Victimización en el Perú 2024* | INEI | Estadística nacional de victimización | ✅ `INEI_Victimizacion_Peru_2024.pdf` |
| B2 | *Estadísticas de Seguridad Ciudadana, enero–junio 2024* | INEI | Boletín estadístico semestral, 107 pp. | ✅ `INEI_Boletin_Seguridad_Ciudadana_2024.pdf` |
| B3 | *Reporte Qawaq 1 — La victimización en Perú: cifras esenciales* | Observatorio MININTER | Ranking de ciudades por victimización, 2018–2020 | ✅ `MININTER_Qawaq_Victimizacion_Cifras_Esenciales.pdf` (18 pp.) |

---

## Hallazgo metodológico central (A1 — INEI)

Este documento no es literatura externa: es la **propuesta oficial peruana** de un índice de inseguridad ciudadana subnacional, y se convirtió en la columna vertebral de la función clave del producto. Extractos verificados:

### Fórmula del índice

> El cálculo final del IIC se obtendrá al realizar un **promedio geométrico** de tres componentes [...] debido a que los tres elementos tienen una alta correlación entre sí.
>
> IIC = (Victimización × Vigilancia_y_Prevención × Percepción)^(1/3)

*(`INEI_propuesta_indice_inseguridad.pdf`, p. 31)*

### Normalización

> ,  =  (x_{i,c} − min_c) / (max_c − min_c)

Min-max sobre el total de distritos; las variables que ya son tasas (naturalmente entre 0 y 1) no se normalizan. Los indicadores inversos —donde un valor mayor implica **menos** inseguridad— se invierten como (1 − indicador normalizado). *(p. 33)*

### Bandas categóricas (CUADRO N° 6)

| Puntaje | Categoría |
|---|---|
| 0,00 – 0,20 | Muy baja |
| 0,21 – 0,40 | Baja |
| 0,41 – 0,60 | Media |
| 0,61 – 0,80 | Alta |
| 0,81 – 1,00 | Muy alta |

*(p. 42)* — **Esta es la tabla que este proyecto adopta como base del semáforo.** No se inventa una escala nueva: se usa la clasificación de la propia entidad estadística nacional del Perú.

### Corrección de subregistro (cifra negra)

> Se desarrolla un enfoque de modelización de la **frontera de producción estocástica** [...] para calcular el porcentaje máximo de denuncias dentro del distrito [...]. Así, se resuelve el tema de subreporte de crímenes, ya que se utiliza una regla de tres simple para estimar el número de delitos denunciados corregido a partir del número de delitos observado y el porcentaje anteriormente mencionado.

*(p. 33)* — Metodología de Chaudhuri et al. (2014) para el índice de delitos violentos en India, adaptada por el INEI. Para los distritos sin observaciones, se predice el valor mediante regresión lineal usando **nivel de pobreza distrital y su término cuadrático**, con efectos fijos departamentales. *(p. 34)*

### Resultado nacional citable

> El promedio general del IIC es de 0,37 puntos [...]. Aquel del pilar de victimización, 0,10 puntos; de vigilancia y prevención comunitaria, 0,64 puntos; y, del pilar de percepción, 0,72 puntos.

*(p. 42)*

### Dato específico de Arequipa — con una tensión que se declara, no se oculta

| Fuente | Métrica | Valor | Lectura |
|---|---|---|---|
| INEI IIC (A1), departamento Arequipa | Promedio del índice | **0,357** | Por debajo del promedio nacional (0,37); posición relativamente favorable |
| INEI IIC (A1), distrito Charcana (provincia La Unión, Arequipa) | IIC | **0,171** | **El distrito con MENOR inseguridad de todo el Perú** |
| INEI IIC (A1), distrito Madrigal (Arequipa) | IIC | 0,253 | 4.º distrito con menor inseguridad del país |
| INEI IIC (A1), distritos de Arequipa Metropolitana | IIC | 0,329 – 0,406 | Characato el más alto (0,406) de la muestra citada; Alto Selva Alegre el más bajo (0,329) |
| MININTER Qawaq (B3), ciudad de Arequipa, 2019 | % victimización | **33,0 %** | Arequipa ocupa una posición **media**, no la más alta: por debajo de Juliaca (46,2 %), Puno (40,8 %), Cusco, Tacna |
| UCSP / El Búho, 2025 | % victimización urbana | **33,5 %** — citada como la más alta del país | Discrepancia frente a B3 |

> **Esta discrepancia es, en sí misma, el argumento más fuerte a favor del producto.** El IIC del INEI (2023, con datos hasta ~2021) es un índice **administrativo**: pondera fuertemente infraestructura de vigilancia y percepción medida en comisarías, no victimización vivida. El reporte Qawaq de 2019 muestra a Arequipa en posición media entre ciudades grandes. Las fuentes de 2025 (UCSP, El Búho) —más recientes y basadas en encuesta directa a la población— reportan a Arequipa como la de mayor victimización urbana del país.
>
> Tres fuentes serias, tres metodologías distintas (índice administrativo compuesto vs. ranking de denuncias vs. encuesta de victimización directa), **tres resultados que no coinciden**. Eso no es un error de esta investigación: es la prueba empírica de que **ninguna fuente única —ni denuncias, ni percepción administrativa, ni encuesta puntual— captura la incidencia real por sí sola.** Justifica precisamente el diseño híbrido que se propone en la sección siguiente.

---

## Hallazgo metodológico complementario (A2 — PLOS ONE, Bogotá)

> Este trabajo estudia la posibilidad de recuperar tasas "verdaderas" de criminalidad y de subregistro a lo largo del tiempo usando datos diarios secuencialmente disponibles [...]. Los datos de criminalidad de una gran ciudad, Bogotá (Colombia), fueron usados para estimar las tasas "verdaderas" de criminalidad y de subregistro.

*(Abstract, `PLOS_ONE_Modelling_Underreported_Crime.pdf`)*

Autores de **Quantil**, la **Universidad de los Andes** y la **Universidad Nacional de Colombia**. Es el precedente académico más cercano geográfica y metodológicamente: aborda el mismo problema —el subregistro delictivo— en una ciudad latinoamericana comparable, con instrumentos de política pública como objetivo declarado. Confirma que el problema de la cifra negra es tratable con metodología rigurosa **sin depender de una encuesta nacional cara**, usando la estructura temporal de los propios reportes.

---

## Hallazgo complementario (A3, A4 — ponderación y magnitud del efecto)

- **Ihlanfeldt & Mayock (2010):** de siete categorías de delito analizadas, solo **robo y agresión agravada** (por acre) ejercen influencia significativa sobre el valor de vivienda; el delito contra la propiedad, no. El crimen violento en el quintil de mayor densidad es **32 veces mayor** que en el de menor densidad. *(RSUE, Q1)*
- **Danish Crime Harm Index (Andersen & Mueller-Johnson, 2018):** entre 2011 y 2016 el **conteo** de delitos cayó 14 %, mientras el índice **ponderado por gravedad** subió 0,5–6 % según el criterio. Un índice que no pondera por gravedad puede mostrar la tendencia **opuesta** a la real.

> **Implicancia de diseño directa:** el índice de incidencia de este proyecto no puede tratar todos los delitos como equivalentes ni depender solo del conteo. Debe ponderar por severidad (siguiendo A4/A5) y, siguiendo a A3, distinguir explícitamente robo/agresión de otras categorías, porque son las que efectivamente correlacionan con el valor y la decisión residencial.

---

## Nota de método

- Los artículos B1–B3 y A1 son fuentes oficiales/institucionales, no arbitradas por pares; se usan como evidencia primaria, no como literatura científica.
- A5, A6, A7, A8, A9, A10 se citan bibliográficamente porque el acceso a su PDF completo está bloqueado por el editor (paywall) o por el servidor de origen (BCRP); su cuartil fue verificado de forma independiente vía SCImago.
- Todo archivo en `referencias/pdf/` fue descargado de un enlace público, sin autenticación ni elusión de control de acceso.
