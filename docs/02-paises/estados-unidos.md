# Estados Unidos — Modelo 2: Transferencia de riesgo vía seguro

El caso más importante del benchmark para este proyecto, porque **su causa raíz es idéntica a la peruana** y el mercado ya demostró qué ocurre cuando el Estado no se estandariza.

---

## La fragmentación

| Dato | Valor |
|---|---|
| Condados con sistema propio de registro | Más de 3 000 |
| Jurisdicciones con taxonomía de instrumentos distinta | 3 144 |

> El mismo evento legal —una transferencia, un gravamen, una ejecución hipotecaria— se registra bajo **nombres, formatos y convenciones de indexación diferentes** en 3 144 jurisdicciones.

Esta frase describe, con cambio de escala, exactamente lo que ocurre entre las más de 1 800 municipalidades distritales del Perú.

---

## La consecuencia: una industria de USD 16 200 millones

| Indicador | Valor |
|---|---|
| Volumen de negocio 2023 | USD 16 500 millones |
| Primas suscritas 2024 | USD 16 200 millones |
| Concentración | Ninguna empresa supera el 5 % de participación |

**Fuentes:** [IBISWorld](https://www.ibisworld.com/united-states/industry/title-insurance/4784/) · [ALTA](https://www.alta.org/press/TitleInsuranceOverview.pdf)

---

## El *title plant* — precedente directo del producto propuesto

Este es el hallazgo operativo central del benchmark:

> Debido a las ineficiencias de las oficinas de registro de los condados, las compañías de título construyeron sus propios **«title plants»**: sistemas que **replican la información de los registros públicos pero reindexada de forma consistente** —por nombre o por lote— de modo que las búsquedas puedan ejecutarse con mayor rapidez y precisión.

**Traducción al caso Arequipa:** cuando el Estado no unifica el dato, el mercado construye un espejo privado, lo estandariza y cobra por consultarlo. No es una hipótesis de negocio: es historia económica documentada de un sector que mueve USD 16 200 millones al año.

El producto propuesto en este repositorio es un *title plant* aplicado a la capa de zonificación y habilitación urbana.

---

## California — Natural Hazard Disclosure

California es el **único estado de la Unión** que obliga al vendedor a entregar una Declaración de Peligros Naturales (NHD).

### Base legal

**California Civil Code, Sec. 1103.** El vendedor y el corredor están legalmente obligados a declarar si el predio se ubica en una o más zonas de peligro mapeadas por el estado o por la autoridad local.

### Las seis zonas de declaración obligatoria

1. Área de peligro especial de inundación (*Special Flood Hazard Area*)
2. Zona de inundación por falla de represa (*Dam Inundation Zone*)
3. Zona de severidad muy alta de peligro de incendio
4. Área de incendio forestal (*Wildland Fire Area*)
5. Zona de falla sísmica (*Earthquake Fault Zone*)
6. Zona de peligro sísmico — licuefacción o deslizamiento

### Mecánica y consecuencias

- Debe entregarse **antes de la aceptación del contrato**.
- Si se entrega después, el comprador dispone de 3 días para terminar la operación (5 si fue enviada por correo).
- El incumplimiento doloso o negligente genera **responsabilidad por daños reales** (Civil Code 1102.13).

**Fuente:** [Standardized Natural Hazards Disclosure Statement](https://en.wikipedia.org/wiki/Standardized_Natural_Hazards_Disclosure_Statement)

Esta es, literalmente, la capa de peligro físico del producto propuesto, convertida en obligación legal.

---

## El caso Zillow — la advertencia más valiosa del benchmark

Entre septiembre de 2024 y noviembre de 2025 Zillow mostró puntajes de riesgo climático de First Street Foundation en sus avisos. En noviembre–diciembre de 2025 **los retiró de más de un millón de avisos**.

### Por qué los retiró

El detonante formal fue el reclamo del California Regional MLS por evaluaciones de inundación consideradas inexactas. El motivo económico de fondo fue otro:

> Cuando las estimaciones de riesgo de inundación se mostraron a millones de usuarios, los compradores comenzaron a buscar propiedades de menor riesgo, y **los inmuebles marcados como de alto riesgo se vendieron aproximadamente 1 % por debajo de su valor de mercado**.

### Estado actual

Zillow retiró los puntajes pero mantuvo enlaces a First Street. Redfin, Realtor.com y Homes.com continúan mostrando los datos, aunque el mismo grupo californiano les solicitó retirarlos.

**Fuentes:** [CNN](https://www.cnn.com/2025/12/02/climate/zillow-climate-data-extreme-weather-first-street-redfin) · [The Real Deal](https://therealdeal.com/national/2025/12/01/zillow-drops-climate-risk-scores-after-industry-pushback/)

### Implicancias de diseño

1. **El índice funciona.** Movió precios de mercado de forma medible. Eso es prueba de eficacia, no de fracaso.
2. **Precisamente por funcionar, genera resistencia gremial.** El producto debe anticiparla.
3. **No vender al actor con incentivo invertido.** Un portal inmobiliario no financia sostenidamente una función que reduce el precio de su inventario.
4. **Metodología pública y auditable.** El ataque efectivo fue contra la exactitud, no contra la idea.

---

## Capa de mercado estadounidense

| Empresa | Qué hace | Señal |
|---|---|---|
| **Cape Analytics** | Imagen satelital y aérea más aprendizaje automático para evaluar condición del predio, densidad de vegetación, material del techo y riesgo de incendio, viento y granizo | Capa de peligro físico con capital institucional — [sitio](https://capeanalytics.com/real-estate-property-intelligence/) |
| **Jupiter Intelligence** | Analítica de riesgo climático con productos ClimateScore, FloodScore y HeatScore | **USD 88 millones** levantados — [Crunchbase](https://www.crunchbase.com/organization/jupiter-intelligence) |
| **Regrid** | Geometría parcelaria a escala nacional | Capa base de agregación |
| **SpotCrime** | Mayor base de criminalidad de EE. UU.: 500 M+ registros, 22 000+ ciudades, 1 000+ agencias policiales, 300 M de alertas anuales | Ingresos aproximados de **USD 7 millones anuales** vía publicidad y acceso premium a datos — [sitio](https://spotcrime.io/about) |

### El contraste que define la estrategia del producto

| Vertical | Comparable | Magnitud económica |
|---|---|---|
| Exposición delictiva | SpotCrime | ~USD 7 millones anuales |
| Condición registral | Industria de seguro de título | USD 16 200 millones anuales |

La diferencia es de tres órdenes de magnitud. **La capa delictiva sostiene un negocio pequeño; la capa registral-urbanística sostiene una industria.** Esta evidencia fundamenta el reencuadre del problema original.
