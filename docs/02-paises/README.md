# Benchmark Internacional — Índice

Cómo resuelven otros países el problema de **verificar la condición de un predio antes de comprarlo**.

---

## Hallazgo central

No existe un sistema único. Existen **tres modelos**, y cada país eligió el suyo en función de cuán fragmentado esté su aparato estatal.

| Modelo | Quién asume el trabajo | Quién paga | Países |
|---|---|---|---|
| **1. Obligación legal de divulgación** | El vendedor y su representante legal | Vendedor o comprador | [Reino Unido](reino-unido.md), [Australia](australia.md), [California](estados-unidos.md#california--natural-hazard-disclosure) |
| **2. Transferencia de riesgo vía seguro** | Una industria privada | Comprador y prestamista | [Estados Unidos](estados-unidos.md) |
| **3. Bien público digital** | El Estado | Nadie — acceso gratuito | [Países Bajos](paises-bajos.md), [España](espana.md), [Estonia](estonia.md) |

**El Perú no tiene ninguno de los tres completo.** Ver [`../03-region/01-peru.md`](../03-region/01-peru.md).

---

## Tabla comparativa

| País | Modelo | Instrumento central | Obligatorio | Formato del dato | Costo para el ciudadano |
|---|---|---|---|---|---|
| Reino Unido | 1 | Local Authority Search (LLC1 + CON29); Material Information | Sí, si hay hipoteca | Informe estructurado | Pagado por el comprador vía solicitor |
| Australia (Victoria) | 1 | Section 32 Vendor's Statement | Sí, sin excepción pactable | Documento legal | Pagado por el vendedor |
| Estados Unidos (California) | 1 | Natural Hazard Disclosure Statement | Sí, Civil Code 1103 | Formulario estatutario | Pagado por el vendedor |
| Estados Unidos (federal) | 2 | Seguro de título sobre *title plants* privados | De facto, exigido por el prestamista | Base privada reindexada | Prima de seguro |
| Países Bajos | 3 | Kadaster / PDOK / BAG | No aplica | API REST, OGC, Linked Data, SPARQL | Gratuito |
| España | 3 | Sede Electrónica del Catastro | No aplica | Cartografía, INSPIRE, servicios web | Gratuito (datos no protegidos) |
| Estonia | 3 | e-Land Register | No aplica | Registros interconectados con identificador único | Consulta pública |
| Colombia | 3 parcial | Ventanilla Única de Registro (VUR) | No aplica | Portal integrado | Consulta en línea |
| Chile | 3 parcial | Conservador de Bienes Raíces digital | No aplica | Trámites y certificados en línea | Pagado por certificado |
| **Perú** | **Ninguno completo** | SUNARP Visor BGR (solo capa registral) | No | Geovisor nacional; municipal en PDF | Gratuito en lo nacional |

---

## Lectura para el proyecto

1. **Donde el Estado se ordena, no hay negocio — y está bien.** Países Bajos, España y Estonia eliminaron la oportunidad de mercado al convertir el dato en bien público. Es el desenlace socialmente óptimo.
2. **Donde el Estado no se ordena, aparece una industria.** Estados Unidos sostiene un mercado de USD 16 200 millones anuales construido sobre la fragmentación de 3 144 jurisdicciones.
3. **Donde el Estado legisla, el costo se traslada al vendedor.** Reino Unido, Victoria y California obligan a que la información viaje con el inmueble.
4. **El Perú resolvió la capa nacional y no resolverá la municipal.** SUNARP ya opera un geovisor gratuito. Las más de 1 800 municipalidades distritales no van a estandarizarse entre sí, por la misma razón que los 3 144 condados estadounidenses no lo hicieron en siglo y medio.

---

## Marco de evaluación aplicable

El **Índice de Calidad de la Administración de Tierras** del Banco Mundial ofrece cinco dimensiones utilizables como estructura de diagnóstico:

1. Confiabilidad de la infraestructura
2. Transparencia de la información
3. Cobertura geográfica
4. Resolución de disputas de tierras
5. Acceso equitativo a derechos de propiedad

Última recolección: mayo de 2019. Doing Business fue archivado; su sucesor **B-READY** mide, mediante encuestas a empresas, el tiempo y costo *de facto* de transferir propiedad.

Fuente: [GovData360 — Banco Mundial](https://govdata360.worldbank.org/indicators/h4620451e)
