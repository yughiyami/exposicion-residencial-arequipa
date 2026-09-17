# Vertical 1b — Catastral (corrección: SNCP, no SUNARP)

> **Corrección de la investigación previa.** Los documentos anteriores de este repositorio trataron la capa catastral como parte del dominio de SUNARP (Visor BGR). Es impreciso. **El catastro y el registro son dos sistemas distintos y complementarios en el Perú**, con instituciones diferentes. Esta ficha corrige la imprecisión.

---

## 1. La distinción que se había pasado por alto

| Sistema | Qué acredita | Pregunta que responde | Institución líder |
|---|---|---|---|
| **Registro** | Titularidad jurídica, cargas, gravámenes | ¿De quién es y está libre de deudas? | SUNARP |
| **Catastro** | Descripción física y técnica del predio: geometría, superficie, linderos | ¿Dónde empieza y termina exactamente, y qué tan preciso es ese dato? | **SNCP** (Sistema Nacional Integrado de Catastro) |

El Visor BGR de SUNARP, documentado en `v1-registral.md`, es un **visor gráfico sobre la base registral** — útil, gratuito, georreferenciado — pero **no es el catastro nacional**. Es la representación gráfica de lo inscrito, no el levantamiento técnico catastral.

---

## 2. Qué es el SNCP

**Sistema Nacional Integrado de Información Catastral Predial (SNCP)**, creado por la Ley N.° 28294 (Ley que crea el Sistema Nacional Integrado de Catastro). Portal: [sncp.gob.pe](https://sncp.gob.pe/).

Objetivo declarado: gestionar el **Catastro Nacional Integrado de Predios**, desarrollando mecanismos para generar, mantener, actualizar, integrar e interconectar la información catastral a través de una infraestructura de datos catastral.

### Composición institucional

El **Consejo Nacional de Catastro** —presidido por **SUNARP**— aprueba la política nacional del sistema. Lo integran:

| Institución | Rol |
|---|---|
| **SUNARP** | Preside el Consejo Nacional de Catastro |
| **COFOPRI** | **Secretaría Técnica del SNCP.** Asigna el **Código Único Catastral (CUC)** a los gobiernos locales |
| **INGEMMET** | Catastro minero |
| **ICL** (Instituto Catastral de Lima) | Catastro de Lima Metropolitana |
| **SBN** (Superintendencia de Bienes Estatales) | Predios del Estado |
| **AMPE** (Asociación de Municipalidades del Perú) | Representación municipal |
| **IGN** (Instituto Geográfico Nacional) | Referencia geodésica nacional |
| Gobiernos regionales y municipalidades provinciales, distritales y de Lima Metropolitana | Ejecución catastral local |

> **Dato operativo clave para el diseño técnico del producto:** el **Código Único Catastral (CUC)**, asignado por COFOPRI como Secretaría Técnica, es el identificador que más se aproxima al **identificador único de predio** que este repositorio identificó como ausente en el benchmark internacional (ver `docs/02-paises/estonia.md` y `docs/02-paises/espana.md`, donde Estonia y España sí cuentan con esa clave). **Su existencia formal no garantiza cobertura completa ni consistencia de uso entre municipalidades** — eso queda como riesgo abierto, no como supuesto resuelto.

---

## 3. Qué cambia para el proyecto

1. **La capa catastral no está resuelta por SUNARP.** El Visor BGR sigue siendo útil (georreferenciación gráfica, gratuita, con más de 6 millones de imágenes de predios), pero es una capa **registral con representación gráfica**, no una capa catastral técnica completa.

2. **El CUC es el candidato real a identificador único de predio en el Perú.** Si el SNCP lo aplica de forma consistente entre SUNARP, COFOPRI y las municipalidades, resuelve —al menos parcialmente— la restricción arquitectónica A2 declarada en `docs/05-producto/01-producto.md` («no existe identificador único de predio compartido entre instituciones»). **Esto debe verificarse antes de asumirlo como resuelto**: consultar si el CUC está adoptado en José Luis Bustamante y Rivero, el distrito piloto.

3. **El vertical urbanístico (`v2-urbanistico.md`) y el catastral son distintos.** La zonificación es un atributo normativo sobre un predio ya delimitado catastralmente; el catastro es la delimitación física en sí. Ambos siguen siendo brechas independientes en Arequipa: ninguna municipalidad analizada publica ni la una ni la otra como servicio geoespacial.

---

## 4. Riesgo abierto (nuevo)

| # | Riesgo | Acción de verificación |
|---|---|---|
| R10 | No se ha confirmado si José Luis Bustamante y Rivero tiene asignado y publicado el CUC de sus predios | Consultar al SNCP (sncp.gob.pe) o a la Gerencia de Desarrollo Urbano del distrito |
| R11 | El CUC podría existir formalmente pero no usarse de manera consistente en los sistemas municipales (mismo patrón que el resto de la capa urbanística: existe en papel, no en la práctica digital) | Verificar en campo junto con R1 (naturaleza vectorial o raster del plano de zonificación) |
