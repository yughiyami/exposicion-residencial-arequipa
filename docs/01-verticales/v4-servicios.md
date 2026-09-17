# Vertical 4 — Servicios Básicos

**Pregunta que responde:** ¿este predio tendrá agua potable y desagüe, y en qué condiciones?

> El vertical con la **mayor brecha digital** de los seis, y con la barrera de acceso más reveladora.

---

## 0. Por qué este vertical es necesario — no es un adorno

Se justifica con tres tipos de evidencia, no con intuición:

**Evidencia económica (por qué le importa al comprador).** La literatura hedónica internacional cuantifica el efecto de los servicios básicos sobre el valor de la vivienda de forma consistente en economías en desarrollo: en Indonesia, la disponibilidad de agua entubada incrementa el precio de alquiler urbano en **9,1 %**; en Ciudad de México, los hogares están dispuestos a pagar entre **5,8 % y 8,3 % del ingreso mensual** por un servicio de agua bien mantenido o mejorado (ver `docs/00-evaluacion/04-referencias-academicas.md`, A9–A10). No es una amenidad menor: es un componente medible y significativo del precio.

**Evidencia normativa (por qué es una barrera real en Arequipa).** El propio trámite de factibilidad de SEDAPAR exige una memoria descriptiva firmada por un profesional colegiado y una ficha registral de antigüedad menor a 60 días — es decir, **el Estado ya reconoce que la factibilidad de servicios es una condición habilitante de la compra**, no un dato accesorio (ver §2 más abajo).

**Evidencia de mercado (por qué el competidor lo intentó y no lo resolvió del todo).** La auditoría de UbicaBien (`docs/04-startups/ubicabien-auditoria.md`) confirma que sí incluyeron esta capa, con datos de cobertura de agua y alumbrado a nivel de cuadra — validación externa de que un equipo financiado consideró este vertical suficientemente importante como para construirlo primero, antes que la capa registral o de zonificación completa.

---

## Fuentes en Arequipa

| Prestador | Servicio | Canal |
|---|---|---|
| **SEDAPAR** | Agua potable y alcantarillado | Presencial — Av. Virgen del Pilar 1701, 07:10–12:10 y 13:00–15:30 |
| **SEAL** | Energía eléctrica | Presencial y oficina virtual para clientes existentes |

---

## El trámite de factibilidad

Requisitos para el Certificado de Factibilidad de SEDAPAR:

1. Copia simple de DNI vigente, o vigencia de poder con antigüedad no mayor a 30 días calendario
2. **Ficha registral con antigüedad no mayor a 60 días calendario**
3. **Memoria descriptiva del terreno firmada por ingeniero civil, sanitario o arquitecto colegiado**, indicando propietario, ubicación, linderos, área, perímetro, descripción del proyecto, cálculo probable de consumo y sistema de abastecimiento

Fuente: [gob.pe](https://www.gob.pe/25043-solicitar-certificado-de-factibilidad-para-servicio-de-agua-potable-y-alcantarillado?child=65539)

---

## El hallazgo central

> **Para saber si un terreno tendrá agua, el ciudadano debe contratar a un profesional colegiado antes de comprarlo.**

Esta barrera explica por sí sola por qué la verificación no ocurre en la práctica, y constituye el argumento más sólido del estado actual del proceso: el sistema exige una inversión profesional previa a una decisión que aún no se ha tomado.

Contrastar con el dato nacional: solo el **13,8 %** de las viviendas informales fue levantado con asistencia de ingeniero o arquitecto. El requisito es, para el segmento objetivo, prácticamente inalcanzable.

---

## Contexto de estrés del servicio

| Hecho | Fuente |
|---|---|
| El alcalde alertó que el 80 % de la población quedó desabastecida de agua de un momento a otro (febrero de 2024) | [Infobae](https://www.infobae.com/peru/2024/02/08/arequipa-sigue-sin-agua-80-de-la-poblacion-se-ha-desabastecido-de-un-momento-a-otro-alerta-alcalde/) |
| SEDAPAR devolvió S/ 6 147 211 al Ministerio de Vivienda tras no ejecutar durante 2025 el convenio de distribución gratuita por camión cisterna | [La República](https://larepublica.pe/sociedad/2026/05/11/sedapar-no-entrego-agua-gratuita-a-poblacion-vulnerable-de-arequipa-y-devolvio-s6-millones-al-ministerio-de-vivienda-855195) |
| Cortes programados recurrentes con abastecimiento por cisterna en distritos de Arequipa | [Infobae](https://www.infobae.com/peru/2025/04/10/sedapar-programa-corte-de-agua-en-arequipa-hasta-el-12-de-abril-conoce-los-puntos-de-abastecimiento/) |

> **Distinción necesaria para el producto:** no es lo mismo *tener factibilidad de conexión* que *tener servicio continuo*. Ambas dimensiones deben informarse por separado. Un predio puede ser factible y aun así depender de cisterna durante meses.

---

## Brecha

| Dimensión | Estado |
|---|---|
| Canal digital para factibilidad | **Inexistente** |
| Consulta por ubicación | **No disponible** — el trámite es por expediente |
| Oficina virtual | Existe, pero solo para clientes con suministro activo |
| Requisito profesional previo | **Vigente** |

---

## Estrategia de aproximación para el producto — variables precisas

Ante la imposibilidad de consultar factibilidad por ubicación, el producto opera con **información proxy declarada como tal**, con cuatro variables específicas y sus fuentes exactas:

| # | Variable precisa | Fuente exacta | Qué responde |
|---|---|---|---|
| 1 | **% de cobertura de agua potable y desagüe a nivel de manzana o cuadra** | Censo Nacional 2017 (INEI), vía REDATAM o el mismo dato que UbicaBien ya demostró viable en su auditoría | ¿La mayoría de los predios vecinos ya tienen conexión? |
| 2 | **Distancia en metros a la red de agua/desagüe más cercana** | Trazado de red del Censo 2017 o de la EPS, cuando esté disponible | ¿Qué tan lejos está la conexión más próxima? |
| 3 | **Condición de habilitación urbana** (Vertical 2) | Capa de zonificación propia | Un predio sin habilitación **no** tendrá conexión formal, sin importar la proximidad física a la red |
| 4 | **Historial de cortes y abastecimiento por cisterna** en la zona | Comunicados oficiales de SEDAPAR y prensa regional | ¿El servicio, aun si existe, es continuo o depende de cisterna? |

**Fuente de la variable 1, verificada como viable:** la auditoría de UbicaBien confirmó en campo que el Censo 2017 del INEI entrega, a nivel de cuadra, población, viviendas, cobertura de alumbrado y **cobertura de agua potable** con distancia a la red más cercana. Es un dato público, gratuito, y **ya demostrado como técnicamente accesible por un competidor real** — no es una suposición de este repositorio.

### Regla de presentación — no confundir proxy con certificado

Nunca debe presentarse una estimación proxy como si fuera un certificado de factibilidad. El reporte debe indicar explícitamente: *«Esta es una estimación basada en cobertura del entorno (Censo 2017). La factibilidad formal solo la emite SEDAPAR.»* Es un límite de diseño, no una limitación temporal.

---

## Comparables internacionales

| País | Cómo se resuelve |
|---|---|
| Reino Unido | Servicios públicos incluidos en la **Parte B** de Material Information, obligatorio en todos los avisos |
| Victoria (Australia) | Tributos y servicios incluidos en la Section 32 |
| Países Bajos | Atributos de la edificación disponibles vía API del BAG |

En los tres casos la información de servicios **acompaña al inmueble**, no exige un trámite del comprador.

---

## Dificultad técnica: **muy alta**

No es un problema de integración sino de **inexistencia de canal**. Resolverlo plenamente requiere un convenio con el prestador, lo cual excede el alcance de un ciclo académico. Debe declararse como limitación conocida y abordarse con información proxy claramente etiquetada.

---

## Indicador de cuadro de mando asociado

- Porcentaje de consultas con proxy de servicio favorable frente a desfavorable
- Cobertura de red modelada por distrito
- Brecha declarada: proporción de reportes emitidos con incertidumbre alta en este vertical
