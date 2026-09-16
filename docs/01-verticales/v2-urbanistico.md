# Vertical 2 — Urbanístico

**Pregunta que responde:** ¿se puede construir aquí, con qué parámetros, y este suelo llegará a ser habilitable?

> **Este es el vertical crítico del proyecto.** Concentra la brecha más grande, el mayor costo de construcción y, por lo mismo, la única ventaja competitiva defendible.

---

## Fuentes en Arequipa

| Recurso | Formato | Acceso |
|---|---|---|
| PDM Arequipa 2016–2025, Ordenanza Municipal N.º 975 | PDF y almacenamiento en la nube, vía IMPLA | Descarga pública |
| PDM 2025–2045 | En exhibición pública | Consulta |
| [Plano de zonificación JLByR](https://www.munibustamante.gob.pe/archivos/gdu/planos/001_plano_de_zonificacion.pdf) | **PDF** | Descarga pública |
| [Plan Urbano Distrital JLByR](https://www.munibustamante.gob.pe/archivos/gdu/planos/plan_urbano.pdf) | PDF | Descarga pública |
| Certificado de Parámetros Urbanísticos y Edificatorios | Documento en papel | Presencial, vigencia 36 meses |
| PDU distrital de Paucarpata | **En elaboración** | No disponible |

---

## Qué se puede detectar con este vertical

- Predio rústico comercializado como lote urbano — **el mecanismo de fraude señalado por el Colegio de Arquitectos**
- Zonificación incompatible con el uso pretendido
- Suelo no habilitable, sobre el cual la formalización nunca procederá
- Parámetros edificatorios: altura máxima, coeficiente, área libre, retiros, estacionamientos
- Terrenos reservados para proyectos públicos

---

## La brecha

| Dimensión | Estado verificado |
|---|---|
| Geoportal municipal | **No existe** en la Municipalidad Provincial de Arequipa |
| Visor de zonificación | **No existe** en ninguno de los tres distritos analizados |
| Shapefile o servicio geoespacial | **No publicado** |
| Formato real del dato | **PDF** |
| Trámite del certificado | **Presencial** |

El dato **existe y es público**. No es interoperable.

---

## Por qué esta brecha no se cierra sola

| Estados Unidos | Perú |
|---|---|
| Más de 3 000 condados con sistema propio | Más de 1 800 municipalidades distritales |
| Sin estandarizar en más de 150 años | Sin estandarizar |
| Resultado: industria privada de USD 16 200 M | Resultado: vacío de mercado |

Cada municipalidad es soberana, tiene presupuesto y capacidad técnica distintos, y **ningún incentivo para estandarizarse con las demás**. El vacío es estructural.

---

## Trabajo técnico requerido

1. Georreferenciar el PDF del plano de zonificación en QGIS con puntos de control sobre el catastro
2. Vectorizar los polígonos de zona
3. Atribuir cada polígono según el Reglamento del PDM (Ordenanza N.º 975)
4. Versionar la capa con fecha de vigencia ante la transición al PDM 2025–2045

**Riesgo abierto R1:** no se ha determinado si el PDF es vectorial o raster escaneado. Si es raster, la vectorización es manual y el alcance debe reducirse a un sector piloto declarado desde el inicio.

---

## Comparables internacionales

| País | Cómo lo resuelven |
|---|---|
| Reino Unido | CON29: decisiones de planeamiento e infracciones, obligatorio en la transacción |
| Victoria (Australia) | Section 32: **controles de planeamiento y zonificación son divulgación obligatoria previa a la firma** |
| Países Bajos | BAG publicado como API REST, OGC y Linked Data |
| Estonia | **Uso permitido del suelo incorporado al mismo registro que la titularidad** |
| España | Cartografía catastral de consulta libre, formatos INSPIRE |

---

## Dificultad técnica: **alta**

Y precisamente por eso constituye la ventaja competitiva. Si la zonificación estuviera expuesta como servicio geoespacial, cualquier actor replicaría el producto en días. El costo de estructurar este vertical es la barrera de entrada, y es **local**: no se reproduce sin presencia en Arequipa.

---

## Indicador de cuadro de mando asociado

- Superficie y número de polígonos de zonificación digitalizados y vigentes
- Porcentaje de consultas en las que se detecta incompatibilidad de uso
- Porcentaje de consultas sobre suelo no habilitable
- Antigüedad de la capa normativa respecto de la ordenanza vigente
