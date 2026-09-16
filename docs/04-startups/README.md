# Panorama Competitivo

Quién está intentando resolver este problema en el mundo, con qué modelo y con qué resultado económico.

---

## 1. Mapa por vertical

| Vertical | Actor de referencia | País | Modelo de ingresos | Señal económica |
|---|---|---|---|---|
| Registral | Industria de seguro de título sobre *title plants* | EE. UU. | Prima de seguro | **USD 16 200 M en primas (2024)** |
| Urbanístico | [Sprift](https://sprift.com/home) | Reino Unido | Suscripción y API | 300+ puntos de dato sobre 30 M+ propiedades |
| Peligro físico | [Jupiter Intelligence](https://www.crunchbase.com/organization/jupiter-intelligence) | EE. UU. | Licencia empresarial | **USD 88 M levantados** |
| Peligro físico | [Cape Analytics](https://capeanalytics.com/real-estate-property-intelligence/) | EE. UU. | Licencia empresarial | Imagen satelital + aprendizaje automático |
| Peligro físico | First Street Foundation | EE. UU. | Licencia a portales | Integrada en Redfin, Realtor.com, Homes.com |
| Geometría parcelaria | Regrid | EE. UU. | Datos y API | Capa base nacional |
| Exposición delictiva | [SpotCrime](https://spotcrime.io/about) | EE. UU. | Publicidad y datos premium | **~USD 7 M anuales** |
| Livability agregada | NeighborhoodScout, CrimeGrade, AreaVibes | EE. UU. | Reportes y publicidad | 45 000+ ubicaciones (AreaVibes) |
| Accesibilidad a servicios | [Walk Score](https://www.walkscore.com/methodology.shtml) | EE. UU. | API a portales | Consumido por Zillow |

---

## 2. Lectura de las cifras

```
Seguro de título (registral)     ████████████████████████████████  USD 16 200 M / año
Jupiter Intelligence (peligro)   ▌                                  USD 88 M levantados
SpotCrime (delictiva)            ▏                                  USD 7 M / año
```

**Tres órdenes de magnitud separan el vertical registral del vertical delictivo.** Esta es la evidencia que fundamenta el reencuadre del problema original.

---

## 3. Arquetipos de modelo de negocio

### A. Agregador puro — **el modelo recomendado**

No produce dato primario. Ingesta, normaliza, estandariza y entrega.

- **Sprift**: 300+ puntos de dato sobre más de 30 millones de propiedades vía API REST o paquetes a medida. No levanta información de campo.
- **Regrid**: geometría parcelaria a escala nacional.

*Por qué encaja:* costo de construcción concentrado en la capa de dato, no en producción de información nueva. Viable con recursos limitados.

### B. Productor de dato propio mediante sensor o modelo

- **Cape Analytics**: imagen satelital y aérea más aprendizaje automático para evaluar condición del predio, densidad de vegetación, material del techo y riesgo de incendio, viento y granizo.
- **Jupiter Intelligence**: modelación física y de IA — ClimateScore, FloodScore, HeatScore.

*Por qué no encaja ahora:* exige capital y capacidad científica. Es una segunda fase, no un punto de partida.

### C. Transferencia de riesgo

- **Industria de seguro de título**: no informa el riesgo, lo asume a cambio de una prima.

*Por qué no encaja ahora:* requiere licencia y capital regulatorio. Es el techo del sector, no su entrada.

### D. Capa sobre portales — **descartado por conflicto de incentivos**

- **First Street en Zillow**: retirado de más de un millón de avisos en noviembre–diciembre de 2025 tras presión gremial. Las propiedades marcadas como de alto riesgo se vendían ~1 % por debajo de mercado.

*Por qué se descarta:* el pagador es el actor que pierde dinero si el producto funciona.

---

## 4. Latinoamérica

| Empresa | País | Foco | ¿Verifica riesgo de ubicación? |
|---|---|---|---|
| **[UbicaBien](ubicabien.md)** | **Perú — Arequipa** | **Geoverificación: valorización, zonificación, conectividad y desastres** | **Sí — competidor directo** |
| Houm | Chile | Arriendo residencial digital | No |
| Homie | México | Renta sin aval, garantías | No |
| La Haus | Colombia | Venta de vivienda nueva | No |
| Gojom | Perú | Transacción — Perú, Colombia, México, Ecuador | No |
| Valia | Perú | Conexión agente–cliente | No |
| Urbania / Adondevivir / Properati | Perú | Portales de avisos | No |

### Contexto de mercado

| Indicador | Valor |
|---|---|
| Mercado global proptech 2026 | USD 44 590 M, proyección USD 104 570 M a 2034 (TCAC 11,9 %) |
| Mercado inmobiliario latinoamericano 2026 | Podría superar USD 1,1 billones |
| Epicentros regionales | Santiago, Ciudad de México, Bogotá |
| Startups proptech mapeadas en el Perú | Más de 15, según Perú PropTech |

Según el **BID**, las proptech de la región atacan dos problemas: **falta de transparencia** e **ineficiencia de procesos**. Este proyecto se ubica en el primero.

---

## 5. Conclusión competitiva

> **CORREGIDO.** La versión inicial de este documento afirmaba que ningún actor latinoamericano ofrecía verificación integral de una ubicación residencial. **Esa afirmación era falsa.** [UbicaBien](ubicabien.md) opera en Arequipa desde 2026 con respaldo de ProInnóvate, StartUp Perú e Innicia (UCSM), y cubre cuatro capas: valorización, zonificación, conectividad y desastres.

El grueso del ecosistema regional sigue enfocado en la **transacción** —firmar más rápido, alquilar sin aval, pagar más fácil— y no en la **verificación previa a la decisión**. Pero en Arequipa el espacio **no está vacío**.

### Dos lecturas, ambas válidas

**Validación del problema.** Un equipo con financiamiento público apostó a este problema en esta misma ciudad. Eso es evidencia externa de que el problema es real y financiable — más fuerte que cualquier argumento propio. Levanta específicamente la advertencia previa de «si nadie lo construyó quizá no hay demanda».

**Amenaza competitiva.** Están lanzados, con planes de pago activos, un equipo cuya CEO viene de gestión de riesgos de desastres y planificación territorial, y respaldo institucional local. **Si ya digitalizaron la zonificación de Arequipa, la ventaja competitiva propuesta está tomada.**

---

## 6. Posicionamiento propuesto — revisado

El posicionamiento genérico de «cinco capas» ya no es diferenciable. La posición defendible es más angosta:

> **Verificación registral y de habilitación urbana orientada a la prevención de fraude, para el comprador de primera vivienda en el borde de expansión informal de Arequipa — con cobro por evento, no por suscripción.**

| Dimensión | Definición |
|---|---|
| Arquetipo | Agregador puro (A) |
| **Vertical de diferenciación** | **Registral (SUNARP) + habilitación urbana** — no visible en la oferta pública de UbicaBien |
| Vertical de captación | Exposición delictiva |
| Fuera de alcance deliberado | **Valorización** — es la capa central del competidor |
| Segmento | Comprador único del borde informal, no corredor ni inversionista recurrente |
| Cobro | Por evento, no suscripción mensual |
| Pregunta que responde | **«¿Me van a estafar?»**, no «¿es buena inversión?» |

Fundamento económico: el comparable internacional de la capa registral mueve **USD 16 200 millones anuales**; los cuatro mecanismos de fraude documentados en Arequipa se detectan con partida registral y habilitación urbana, no con valorización.

> **Verificación pendiente y bloqueante:** registrarse en el plan gratuito de UbicaBien y confirmar si incluyen capa registral. Hasta entonces, esta diferenciación es una inferencia a partir de su sitio público. Ver [`ubicabien.md`](ubicabien.md), sección 9.
