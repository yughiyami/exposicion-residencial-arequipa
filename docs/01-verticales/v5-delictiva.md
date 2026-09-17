# Vertical 5 — Exposición Delictiva

**Pregunta que responde:** ¿cuál es la incidencia delictiva real en esta zona, y cómo se compara con otras?

> Vertical de origen del proyecto. Tras el análisis comparado se reubica como **componente**, no como producto — pero es el único vertical con **metodología estadística propia**, y por eso se promueve a **función clave**.
>
> **La especificación completa —fórmula, corrección de subregistro, bandas de semáforo adoptadas del INEI, variables precisas— vive en [`docs/05-producto/03-funcion-clave-indice-incidencia.md`](../05-producto/03-funcion-clave-indice-incidencia.md).** Esta ficha se conserva como diagnóstico de fuentes y contexto regional; no se duplica la metodología aquí.

---

## Fuentes en el Perú

| Recurso | Entidad | Contenido |
|---|---|---|
| [Mapa del Delito Georreferenciado](https://observatorio.mininter.gob.pe/MapaDelDelitoGeorreferenciado) | Observatorio Nacional de Seguridad Ciudadana — MININTER | Robo, hurto, homicidio, feminicidio, estafa, extorsión, violación, TID; comisarías, centros de emergencia y establecimientos penitenciarios |
| [GEOMININTER](https://geoportal.mininter.gob.pe/) | MININTER | Geoportal sectorial |
| **Data-Crim** | INEI | Victimización, percepción de inseguridad, número de denuncias, procesos judiciales |
| **ENAPRES** | INEI | Encuesta nacional de victimización |
| **SIDPOL** | PNP | Sistema de denuncias policiales — fuente primaria |
| [Encuesta de Victimización Arequipa 2025](https://ucsp.edu.pe/archivos/publicaciones/cegob/Encuesta-Victimizacion-Percepcion-Seguridad-Ciudadana.pdf) | UCSP | Victimización y percepción a nivel metropolitano |

---

## Datos de Arequipa

| Indicador | Valor |
|---|---|
| Victimización urbana | **33,5 %** — la mayor del país *(cifra 2025, UCSP/prensa; ver nota de discrepancia abajo)* |
| Victimización según UCSP 2025 | 30,90 %, seis puntos más que en 2024 |
| Percepción de inseguridad | 88 % |
| Extorsión | De 6,8 a 30,6 denuncias por 100 mil habitantes entre 2019 y 2025 |

| Distrito | Participación | | Delito | Participación |
|---|---|---|---|---|
| Cerro Colorado | 16,60 % | | Robo en transporte público | 33,20 % |
| Paucarpata | 14,98 % | | Robo al paso | 21,05 % |
| José Luis Bustamante y Rivero | 10,12 % | | **Hurto a viviendas** | **19,03 %** |

---

## Los dos problemas metodológicos que deben resolverse

### 1. La cifra negra

El mapa del delito se alimenta de **denuncias**, no de delitos. Arequipa registra 33,5 % de victimización, pero solo una fracción denuncia. La propia fuente policial reconoce que la extorsión está subregistrada por temor a represalias.

> **Nota de discrepancia entre fuentes, declarada explícitamente.** El índice administrativo del INEI (IIC, 2023) ubica al departamento Arequipa **por debajo** del promedio nacional de inseguridad (0,357 vs. 0,37), y a Charcana (provincia La Unión) como **el distrito con menor inseguridad de todo el Perú**. El reporte Qawaq del MININTER (2019) ubica a la ciudad de Arequipa en posición **media** entre ciudades grandes (33,0 %, por debajo de Juliaca, Puno, Cusco y Tacna). La cifra de 33,5 % citada arriba proviene de encuesta directa de 2025. Tres metodologías, tres resultados. Detalle completo y fuentes en [`docs/00-evaluacion/04-referencias-academicas.md`](../00-evaluacion/04-referencias-academicas.md). **Esta discrepancia es el fundamento empírico de por qué el índice propuesto combina fuente oficial y reporte ciudadano — ver la función clave.**

> Sin corrección, el índice mediría **propensión a denunciar**, no **riesgo real**.

**Solución metodológica:** calibrar denuncias con encuesta de victimización, siguiendo el procedimiento del estudio de Barcelona, que combinó datos del mercado inmobiliario con datos de encuesta de victimización para estimar el efecto de la percepción de delito sobre los precios de vivienda. Fuente: [Empirical Economics](https://link.springer.com/article/10.1007/s00181-012-0624-y)

### 2. Resolución espacial

Numerosas denuncias se registran en la comisaría y no en el punto del hecho. Sin validación, el mapa indicaría que el lugar de mayor incidencia de Arequipa es la propia comisaría.

**Solución:** validación de geocodificación y exclusión o marcado de registros con coordenada institucional.

---

## Fundamento académico del efecto sobre el precio

El **modelo de precios hedónicos** regresiona el precio del inmueble contra un vector de características. Su justificación teórica: la valoración que las personas asignan a la seguridad se refleja en lo que están dispuestas a pagar por vivir en una zona de bajo delito.

| Estudio | Hallazgo |
|---|---|
| Allen y Rasmussen — Jacksonville, Florida | 2 880 observaciones; efecto negativo significativo del delito sobre el precio |
| [Barcelona, 2004–2006](https://link.springer.com/article/10.1007/s00181-012-0624-y) | Mercado inmobiliario cruzado con victimización; OLS y regresiones cuantílicas |
| [Acapulco, 2015–2016](https://link.springer.com/article/10.1007/s00181-019-01804-3) | La violencia criminal es factor significativo del precio |
| [Guanajuato, México](https://www.redalyc.org/journal/674/67472343006/html/) | Enfoque hedónico en contexto latinoamericano |
| [Panel por tipo de delito](https://www.sciencedirect.com/science/article/abs/pii/S0166046210000086) | No todos los delitos pesan igual |
| [BCRP — mercado de Lima](https://www.bcrp.gob.pe/docs/Publicaciones/Revista-Estudios-Economicos/36/ree-36-mundaca-sanchez.pdf) | Agenda hedónica peruana con tres variantes metodológicas |

**Advertencia metodológica obligatoria:** existe **endogeneidad**. ¿El delito reduce el precio, o los barrios de menor precio atraen delito? Sin tratamiento del problema, las estimaciones no son consistentes. Debe declararse y abordarse.

---

## Comparable internacional y su magnitud

**SpotCrime** — mayor base de datos de criminalidad de Estados Unidos:

| Indicador | Valor |
|---|---|
| Registros | Más de 500 millones |
| Ciudades cubiertas | Más de 22 000 |
| Agencias policiales | Más de 1 000 |
| Alertas anuales enviadas | 300 millones |
| **Ingresos anuales aproximados** | **USD 7 millones** — publicidad y acceso premium a datos |

Fuente: [SpotCrime](https://spotcrime.io/about)

> **El contraste decisivo.** SpotCrime opera a escala nacional estadounidense, con la mayor base del país, y factura USD 7 millones al año. La industria de seguro de título —vertical registral— factura USD 16 200 millones.
>
> La diferencia es de tres órdenes de magnitud. La capa delictiva construye tráfico y confianza; la capa registral-urbanística construye ingresos.

---

## Rol correcto dentro del producto

| Función | Justificación |
|---|---|
| **Gancho de captación** | Es la capa que el usuario entiende sin explicación y la que genera consulta espontánea |
| **Componente del reporte** | Aporta contexto de habitabilidad |
| **No es el producto** | La evidencia económica comparada lo desaconseja |

---

## Dificultad técnica: **media**

Dato público y georreferenciado, pero requiere corrección estadística —calibración con victimización— y validación de geocodificación. La dificultad es metodológica, no de acceso.

---

## Indicador de cuadro de mando asociado

- Densidad delictiva calibrada por zona, con intervalo de confianza declarado
- Brecha entre denuncias registradas y victimización estimada por distrito
- Porcentaje de registros descartados por coordenada institucional
