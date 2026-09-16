# Países Bajos — Modelo 3: Bien público digital

El estándar de oro del benchmark. El Estado resolvió la fragmentación convirtiendo el dato predial en infraestructura pública abierta.

---

## Arquitectura institucional

| Componente | Función |
|---|---|
| **Kadaster** | Organismo nacional de catastro y registro |
| **PDOK** — *Publieke Dienstverlening op de Kaart* | Plataforma de servicios geoespaciales, **gratuita para cualquier persona o empresa** |
| **BAG** — *Basisregistratie Adressen en Gebouwen* | Registro base de direcciones y edificaciones |

---

## Qué contiene el BAG

Cinco tipos de objeto:

1. Edificaciones (*panden*)
2. Unidades de uso residencial (*verblijfsobjecten*)
3. Designaciones de numeración (*nummeraanduidingen*)
4. Espacios públicos
5. Lugares residenciales

Con atributos de estado, superficie, **geometría, coordenadas, año de construcción y propósito de uso**.

---

## Cómo se entrega el dato

Este es el punto que más importa para el diseño técnico del proyecto: el dato no se publica como documento, se publica como **servicio consumible**.

| Canal | Detalle |
|---|---|
| API REST | `data.pdok.nl/bag/api/v1/` |
| OGC API | [`api.pdok.nl/kadaster/bag/ogc/v2`](https://api.pdok.nl/kadaster/bag/ogc/v2?f=html&lang=en) |
| Linked Data | `bag.basisregistraties.overheid.nl` |
| SPARQL | Endpoint público sobre los grandes conjuntos espaciales nacionales |
| Visor | Más de **235 conjuntos de datos**, incluidos BAG, BGT y BRT |

**Fuentes:** [Kadaster — Open datasets](https://www.kadaster.nl/zakelijk/datasets/open-datasets) · [PDOK OGC API](https://api.pdok.nl/kadaster/bag/ogc/v2?f=html&lang=en)

---

## El modelo económico híbrido

Neerlandia no regaló todo. Separó dos capas:

| Capa | Acceso | Ejemplo |
|---|---|---|
| **Base** | Gratuita y abierta | Geometría, direcciones, edificaciones, año de construcción |
| **Valor agregado** | API comercial de pago | Precio de compra (~EUR 0,45 por consulta), descripciones WOZ, estadísticas de barrio |

**Fuente:** [Maatwerk API's Kadaster](https://www.kadaster.nl/zakelijk/datasets/maatwerk-api-s-kadaster)

---

## Lecciones transferibles al caso Arequipa

| # | Lección | Aplicación directa |
|---|---|---|
| 1 | **Capa base gratuita, capa de valor agregado paga** | Modelo de ingresos recomendado para el producto: consulta básica gratuita como captación, reporte consolidado como producto pago |
| 2 | Publicar como **servicio**, no como documento | Define el objetivo final de la capa de zonificación digitalizada: no un PDF mejor, sino un servicio geoespacial consultable |
| 3 | **Identificador único compartido entre registros** | Sin una clave común entre SUNARP, municipalidad y SEDAPAR, la integración es siempre aproximada. Es la limitación arquitectónica central del caso peruano. |
| 4 | Cuando el Estado resuelve, el negocio privado desaparece | Define el horizonte de obsolescencia del producto y obliga a declararlo con honestidad en el documento del proyecto |

---

## Contraste con el Perú

| Dimensión | Países Bajos | Perú |
|---|---|---|
| Registro predial georreferenciado | Sí, con API | Sí — Visor BGR SUNARP, sin API pública |
| Zonificación como servicio | Sí | No — PDF por municipalidad |
| Identificador único entre registros | Sí | No |
| Costo de acceso a la capa base | Gratuito | Gratuito en lo nacional, presencial en lo municipal |

El Perú está a **una capa de distancia** del modelo neerlandés en lo nacional, y a décadas en lo municipal.
