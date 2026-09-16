# Vertical 3 — Peligro Físico

**Pregunta que responde:** ¿este suelo es físicamente seguro frente a huaicos, inundación, sismo o deslizamiento?

---

## Fuentes en Arequipa

| Recurso | Entidad | Enlace |
|---|---|---|
| Mapa de peligro de la ciudad de Arequipa | INDECI–PNUD, vía SIGRID | [SIGRID 3546](https://sigrid.cenepred.gob.pe/sigridv3/documento/3546) |
| Evaluación de riesgos en torrenteras, distrito de Yura | Municipalidad de Yura, vía SIGRID | [SIGRID 6076](https://sigrid.cenepred.gob.pe/sigridv3/documento/6076) |
| Mapa de peligro por inundación, ciudad de Camaná | INDECI, vía SIGRID | [SIGRID 3555](https://sigrid.cenepred.gob.pe/sigridv3/documento/3555) |
| Puntos críticos con riesgo a inundaciones en ríos y quebradas del departamento (2019) | ANA, vía SIGRID | [SIGRID 8814](http://sigrid.cenepred.gob.pe/sigridv3/documento/8814) |
| Mapa de Zonificación Sísmica–Geotécnica de Suelos: Arequipa | GEOIDEP | [Catálogo IDEP](https://catalogo.geoidep.gob.pe/metadatos/srv/api/records/26f6f0eb-8bc4-4427-b2a0-f5c33b479752) |
| Zonas con peligro potencial de inundación — Perú | PCM, vía SIGRID | [SIGRID 843](https://sigrid.cenepred.gob.pe/sigridv3/documento/843) |

**SIGRID** es una plataforma geoespacial web de libre acceso para consultar, compartir, analizar y monitorear información sobre peligros, vulnerabilidades y riesgos de origen natural a nivel nacional.

---

## Qué se puede detectar con este vertical

- Predio ubicado en torrentera o en su faja marginal
- Zona de inundación por desborde de río o quebrada
- Zona de peligro sísmico por tipo de suelo — relevante para una ciudad con la sismicidad de Arequipa
- Terreno sobre el cual **la formalización nunca procederá** por estar en zona de alto riesgo

> Este último punto conecta directamente con COFOPRI: antes de titular, la entidad realiza informes técnicos para determinar si el titulamiento es viable **y si el asentamiento no está en zona de alto riesgo**. Un comprador que consulta esta capa *ex ante* obtiene la misma respuesta que el Estado le dará años después.

---

## Brecha

| Dimensión | Estado |
|---|---|
| Existencia del dato | Resuelta |
| Acceso público | Resuelto — plataforma libre |
| Georreferenciación | Resuelta |
| **Cobertura homogénea** | **Desigual** — algunos distritos tienen estudio de detalle, otros solo cartografía nacional |
| Actualización | Variable según el estudio |

La brecha no es de acceso sino de **granularidad desigual**: la confianza de la respuesta varía según el distrito consultado. El reporte debe comunicar ese nivel de confianza, no ocultarlo.

---

## Comparables internacionales

| País | Instrumento | Naturaleza |
|---|---|---|
| California | **Natural Hazard Disclosure Statement** — Civil Code 1103, seis zonas de peligro, obligación del vendedor | Obligación legal |
| Reino Unido | Riesgo de inundación en la Parte C de Material Information | Obligación legal condicional |
| Estados Unidos | First Street Foundation, integrada en Redfin, Realtor.com y Homes.com | Producto privado |
| Estados Unidos | Jupiter Intelligence — ClimateScore, FloodScore, HeatScore; **USD 88 M levantados** | Producto privado |
| Estados Unidos | Cape Analytics — imagen satelital y aprendizaje automático para condición y riesgo del predio | Producto privado |

---

## La advertencia del caso Zillow

Zillow retiró los puntajes de riesgo climático de más de un millón de avisos en noviembre–diciembre de 2025. El efecto medido antes del retiro: los inmuebles marcados como de alto riesgo se vendieron **aproximadamente 1 % por debajo** de su valor de mercado.

**Implicancias de diseño para este vertical:**

1. Comunicar **nivel de peligro por zona**, no una calificación de un predio individual
2. Citar el estudio fuente y su fecha en cada afirmación
3. No emitir conclusiones que la fuente no sostenga
4. Anticipar resistencia gremial: el ataque efectivo contra First Street fue por **exactitud**, no por la idea

---

## Dificultad técnica: **baja**

Es el vertical más accesible: dato público, georreferenciado, en plataforma diseñada para consulta. Debe ser el primero en integrarse en el prototipo.

---

## Indicador de cuadro de mando asociado

- Porcentaje de consultas sobre predios en zona de peligro alto o muy alto
- Cobertura de estudios de detalle disponibles por distrito
- Antigüedad media del estudio utilizado en cada respuesta
