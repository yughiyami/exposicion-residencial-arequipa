# Los Cinco Verticales de Información Predial

Toda decisión residencial informada requiere responder cinco preguntas. Cada una corresponde a un vertical, con su institución soberana, su formato y su brecha específica.

---

## Tabla maestra

| # | Vertical | Pregunta del ciudadano | Institución soberana | Formato actual | Brecha | Dificultad técnica |
|---|---|---|---|---|---|---|
| [1](v1-registral.md) | Legal / registral | ¿Es legalmente transferible? | SUNARP | Geovisor web, sin API | Acceso automatizado | Media |
| [2](v2-urbanistico.md) | Urbanístico | ¿Se puede construir y habilitar? | Municipalidad distrital | PDF | **Estructuración del dato** | **Alta** |
| [3](v3-peligro.md) | Peligro físico | ¿Es físicamente seguro? | CENEPRED / ANA / IGP | Plataforma geoespacial | Cobertura desigual | Baja |
| [4](v4-servicios.md) | Servicios básicos | ¿Tendrá agua y desagüe? | EPS (SEDAPAR) / SEAL | Expediente presencial | **Inexistencia de canal digital** | **Muy alta** |
| [5](v5-delictiva.md) | Exposición delictiva | ¿Es tolerable vivir ahí? | MININTER / INEI | Geovisor y estadística | Subregistro y resolución espacial | Media |

---

## Ordenamiento por consecuencia económica

No todos los verticales pesan igual. Ordenados por magnitud e irreversibilidad de la pérdida:

| Posición | Vertical | Pérdida máxima | Reversible | Comparable internacional | Magnitud del comparable |
|---|---|---|---|---|---|
| 1 | Legal / registral | **Capital total** | No | Seguro de título EE. UU. | **USD 16 200 M anuales** |
| 2 | Urbanístico | Capital total o inmovilización por años | Muy difícil | Local Authority Search (Reino Unido) | Obligatorio por ley |
| 3 | Servicios básicos | Habitabilidad; costo recurrente de cisterna | Parcial | Factibilidad como requisito de licencia | — |
| 4 | Peligro físico | Vida e integridad; pérdida total del inmueble | No | NHD California; First Street | Jupiter Intelligence: **USD 88 M levantados** |
| 5 | Exposición delictiva | ~1 % del valor; calidad de vida | Sí | SpotCrime | **~USD 7 M anuales** |

> **La conclusión que reordena el proyecto.** El vertical con el que se planteó originalmente el problema —exposición delictiva— es el **último** en consecuencia económica. Su comparable internacional maduro factura tres órdenes de magnitud menos que el comparable del vertical registral.
>
> Esto no invalida la capa delictiva: la reubica como **componente de un producto**, no como el producto.

---

## Estado de integración

```
Vertical 1 — Registral      ████████░░  Digital, georreferenciado, sin API
Vertical 2 — Urbanístico    ██░░░░░░░░  PDF por municipalidad
Vertical 3 — Peligro        ███████░░░  Plataforma pública, cobertura desigual
Vertical 4 — Servicios      █░░░░░░░░░  Presencial, requiere profesional colegiado
Vertical 5 — Delictiva      ███████░░░  Geovisor público, con subregistro
```

**Ninguno de los cinco está vinculado a otro por un identificador común.** Esa es la causa raíz expresada en términos técnicos.

---

## El problema del identificador único

Países Bajos y Estonia resolvieron la integración con una regla simple: **el mismo identificador único para el mismo predio en todos los registros**. España cumple la misma función con la referencia catastral.

En el Perú no existe una clave universal de predio compartida entre SUNARP, las municipalidades y los prestadores de servicios.

**Consecuencia para la arquitectura del producto:** la vinculación entre capas debe resolverse por **coincidencia geográfica** (intersección espacial de coordenadas y polígonos), lo cual introduce error de asignación. Esta limitación debe declararse explícitamente en la documentación técnica y reflejarse en el nivel de confianza que el reporte comunica al usuario.

---

## Criterio de privacidad transversal

Adoptado del modelo español y aplicable a los cinco verticales:

| Categoría | Tratamiento |
|---|---|
| Geometría, superficie, uso, zonificación, peligro, incidencia agregada | **Público** |
| Identidad del titular, valor del predio, domicilio de personas | **Protegido** |

Este criterio no es una preferencia del equipo: es la solución normativa de un país que ya enfrentó la misma disyuntiva.
