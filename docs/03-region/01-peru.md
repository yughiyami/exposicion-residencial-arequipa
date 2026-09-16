# Perú — Situación Nacional

---

## 1. La dimensión del universo afectado

| Indicador | Valor | Fuente |
|---|---|---|
| Viviendas urbanas informales al cierre de 2025 | **61,7 %** — más de 4,1 millones de hogares, más de 14 millones de personas | [PQS](https://pqs.pe/actualidad/mas-de-14-millones-de-personas-habitan-viviendas-informales-2/) |
| Viviendas nuevas construidas informalmente en 17 años | **1,6 millones (63 %)**, sin título de propiedad o sin conexión a servicios básicos | [La República](https://larepublica.pe/economia/2025/07/25/un-peru-construido-por-maestros-de-obra-63-de-las-viviendas-son-informales-porque-peruanos-no-pueden-acreditar-ingresos-formales-hnews-1625150) |
| Expansión urbana informal | **93 %** | [ASPAI](https://aspai.pe/2026/01/26/radiografia-de-la-vivienda-en-el-peru-principales-indicadores-problematica-y-oportunidades/) |
| Viviendas urbanas autoconstruidas | 7 de cada 10 | [ASPAI](https://aspai.pe/2026/01/26/radiografia-de-la-vivienda-en-el-peru-principales-indicadores-problematica-y-oportunidades/) |
| Viviendas informales levantadas con asistencia de ingeniero o arquitecto (2024) | **13,8 %** | [ASPAI](https://aspai.pe/2026/01/26/radiografia-de-la-vivienda-en-el-peru-principales-indicadores-problematica-y-oportunidades/) |
| Déficit habitacional total | **1,9 millones de viviendas** — 587 mil cuantitativo, 1,3 millones cualitativo | [Vigilante](https://vigilante.pe/2025/02/17/vivienda-de-interes-social-la-clave-para-cerrar-el-deficit-habitacional-en-peru/) |

### Composición de la producción anual de vivienda

De aproximadamente 128 mil viviendas construidas por año:

| Segmento | Participación |
|---|---|
| Vivienda convencional | 23 % |
| Nuevo Crédito Mivivienda | 7 % |
| Techo Propio | 4 % |
| **Producción informal / autoconstrucción** | **~66 %** |

**Lectura para el proyecto.** El segmento objetivo —comprador sin asesoría profesional en el borde de expansión— **no es un nicho: es la mayoría del mercado peruano de vivienda.** Dos tercios de la producción anual y el 93 % de la expansión urbana ocurren exactamente donde la información predial es más opaca.

---

## 2. Estado de digitalización por capa

| Capa | Institución | Estado | Formato | Evaluación |
|---|---|---|---|---|
| Registral | SUNARP | **Digital y georreferenciado** | Geovisor web; sin API pública documentada | Modelo 3 casi completo |
| Urbanística | +1 800 municipalidades distritales | **No digital** | PDF por municipalidad | Sin modelo |
| Peligro físico | CENEPRED / ANA | **Digital** | Plataforma geoespacial SIGRID | Modelo 3 parcial |
| Servicios básicos | EPS regionales | **Presencial** | Expediente físico | Sin modelo |
| Exposición delictiva | MININTER / INEI | **Digital** | Geovisor y estadística | Modelo 3 parcial |
| Divulgación obligatoria del vendedor | — | **Inexistente** | — | Sin modelo |

---

## 3. Lo que sí funciona: SUNARP

### Visor de Base Gráfica Registral (BGR)

- Geovisor **gratuito y georreferenciado**: [visor-bgr.sunarp.gob.pe](https://www.gob.pe/63173-acceder-al-visor-de-la-base-grafica-registral)
- Navega **más de 6 millones de imágenes de predios**, superponiendo polígonos sobre imagen satelital
- Superó **3 millones de consultas de más de 360 mil ciudadanos**
- [Manual de usuario oficial](https://www.sunarp.gob.pe/pdfs/visorbgr/MANUAL_DEL_USUARIO_VISOR_BGR.pdf)

> Las 3 millones de consultas constituyen **la evidencia conductual más fuerte disponible** de que existe demanda ciudadana de verificación predial. Su limitación como evidencia: el servicio es gratuito, por lo que no acredita disposición a pagar.

### Servicio de Publicidad Registral en Línea (SPRL)

[sprl.sunarp.gob.pe](https://sprl.sunarp.gob.pe/sprl/ingreso) — acceso a índices, repositorio centralizado de imágenes de partidas y títulos en formato digital. Servicios gratuitos y de pago, con descarga 24/7 y firma electrónica.

**Restricción arquitectónica verificada:** no se identificó API pública documentada. El consumo debe diseñarse como asistido, no automatizado.

---

## 4. Lo que no funciona: la capa municipal

La zonificación y la habilitación urbana son competencia de más de 1 800 municipalidades distritales, cada una con:

- Su propio Texto Único de Procedimientos Administrativos
- Su propio Plan de Desarrollo Urbano, cuando lo tiene
- Su propio presupuesto y capacidad técnica
- **Ningún incentivo para estandarizarse con las demás**

### El paralelo estructural

| Estados Unidos | Perú |
|---|---|
| Más de 3 000 condados con sistema propio | Más de 1 800 municipalidades distritales |
| Taxonomía de instrumentos distinta en 3 144 jurisdicciones | Zonificación en PDF con nomenclatura propia por municipalidad |
| No estandarizado en más de 150 años | No estandarizado |
| Consecuencia: industria privada de USD 16 200 millones anuales | Consecuencia: vacío de mercado |

**Conclusión.** El vacío en la capa municipal peruana no es coyuntural sino **estructural**. La evidencia comparada indica que no se cierra por evolución natural.

---

## 5. Marco de política pública aplicable

| Instrumento | Relevancia |
|---|---|
| Política Nacional de Gobierno Digital | Marco de alineamiento del PETI |
| Ley de Gobierno Digital e interoperabilidad del Estado | Fundamento normativo de la integración propuesta |
| [Catálogo de aplicaciones con IA en el Estado peruano — PCM](https://www.gob.pe/institucion/pcm/informes-publicaciones/6879780-catalogo-de-aplicaciones-con-inteligencia-artificial-en-el-estado-peruano) | Referencia institucional de iniciativas comparables |
| Ley N.º 31056 | Restringe la venta o transferencia de lotes formalizados durante los primeros cinco años |
| COFOPRI | Formalización predial; realiza informes técnicos previos para determinar si el titulamiento es viable **y si el asentamiento no está en zona de alto riesgo** |

Sobre COFOPRI en Arequipa: 5 000 lotes ingresaron a evaluación técnico-legal para formalización futura, y se entregaron 2 840 títulos que beneficiaron a más de 11 000 ciudadanos, la mayoría tras más de 15 años de espera. Fuentes: [TVPerú](https://www.tvperu.gob.pe/noticias/nacionales/cofopri-evalua-5000-lotes-en-arequipa-para-avanzar-en-su-formalizacion-predial) · [MVCS](https://www.gob.pe/institucion/vivienda/noticias/1400702-arequipa-ministerio-de-vivienda-entrega-2840-titulos-de-propiedad-a-familias-e-instituciones-de-ocho-provincias-de-la-region)

> El dato de «más de 15 años de espera» cuantifica el costo temporal de la fragmentación institucional mejor que cualquier argumento del equipo.

---

## 6. Nota operativa sobre acceso automatizado

Verificado durante esta investigación:

| Portal | Comportamiento ante acceso programático |
|---|---|
| `gob.pe` | Bloquea — devuelve HTTP 418 y página de acceso restringido |
| `muniarequipa.gob.pe` | Devuelve HTTP 403 a solicitudes programáticas; carga correctamente en navegador |

Estas restricciones deben incorporarse al análisis de riesgo técnico del proyecto y al diseño de los conectores.
