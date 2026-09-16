# Exposición Residencial Arequipa

Investigación aplicada y definición de producto sobre la **imposibilidad de verificar, antes de pagar, el estado legal‑urbanístico, de servicios y de peligro de una ubicación residencial en Arequipa, Perú.**

Repositorio de trabajo para el curso de Gestión Estratégica de Tecnologías de Información.

---

## Tesis del repositorio

> El problema no es la ausencia de datos. Es que **el Estado organiza la información por institución y el ciudadano la necesita organizada por predio.**

Cinco capas de información existen y son públicas. Ninguna está integrada a nivel de ubicación, y ninguna está orientada a la decisión residencial.

---

## Estructura

| Ruta | Contenido |
|---|---|
| [`MEGA-DOCUMENTO.md`](MEGA-DOCUMENTO.md) | Documento único consolidado. Punto de entrada recomendado. |
| [`docs/00-evaluacion/`](docs/00-evaluacion/) | Evaluación metodológica del problema: causa raíz, dossier de evidencia, ajuste solución‑mercado |
| [`docs/01-verticales/`](docs/01-verticales/) | Análisis de los 5 verticales de información predial |
| [`docs/02-paises/`](docs/02-paises/) | Benchmark internacional, un archivo por país |
| [`docs/03-region/`](docs/03-region/) | Situación de Perú y de la región Arequipa |
| [`docs/04-startups/`](docs/04-startups/) | Panorama competitivo global y regional |
| [`docs/05-producto/`](docs/05-producto/) | Definición de producto, plan de validación y mapeo al curso |
| [`data/fuentes.csv`](data/fuentes.csv) | Catálogo de fuentes de datos con formato, acceso y viabilidad técnica |
| [`slides/index.html`](slides/index.html) | Presentación ejecutiva (abrir en navegador) |

---

## Los cinco verticales

| # | Vertical | Fuente principal en Perú | Estado digital |
|---|---|---|---|
| 1 | Legal / registral | SUNARP — Visor BGR, SPRL | Digital y georreferenciado |
| 2 | Urbanístico | Municipalidades (PDM, zonificación) | PDF por municipalidad |
| 3 | Peligro físico | SIGRID — CENEPRED, ANA | Digital, visor público |
| 4 | Servicios básicos | SEDAPAR, SEAL | Presencial |
| 5 | Exposición delictiva | MININTER, INEI | Digital, visor público |

---

## Hallazgo central del benchmark

En el mundo el problema se resuelve con **tres modelos**, y el Perú no tiene ninguno completo:

1. **Obligación legal de divulgación** — Reino Unido, Victoria (Australia), California
2. **Transferencia de riesgo vía seguro** — Estados Unidos
3. **Bien público digital** — Países Bajos, España, Estonia

Detalle en [`docs/02-paises/`](docs/02-paises/).

---

## Estado del trabajo

- [x] Definición y validación metodológica del problema
- [x] Benchmark internacional por país
- [x] Diagnóstico de fuentes de datos en Arequipa
- [x] Panorama competitivo
- [x] Definición de producto y plan de validación
- [ ] Verificación de campo: naturaleza vectorial o raster del plano de zonificación de JLByR
- [ ] Entrevistas de desarrollo de clientes (n=15)
- [ ] Prueba de humo con umbral precomprometido

---

## Licencia

MIT. Las fuentes citadas conservan sus propios términos.
