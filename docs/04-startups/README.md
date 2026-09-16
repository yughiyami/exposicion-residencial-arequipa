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

> **Ningún actor latinoamericano identificado ofrece verificación integral de la condición legal-urbanística, de servicios y de peligro de una ubicación residencial.**

El foco regional está en la **transacción** —firmar más rápido, alquilar sin aval, pagar más fácil— y no en la **verificación previa a la decisión**.

Esto arroja dos lecturas simultáneas, y ambas deben declararse con la misma honestidad:

**Lectura optimista.** El espacio está vacío en toda la región. La barrera de entrada —normalización del dato municipal— es local y defendible. No existe competidor directo.

**Lectura de advertencia.** Que nadie lo haya construido en un mercado de USD 1,1 billones puede indicar que la disposición a pagar es menor que la magnitud del daño. Es exactamente la razón por la cual el dossier de evidencia mantiene el veredicto `PENDIENTE` hasta ejecutar el experimento con umbral precomprometido.

---

## 6. Posicionamiento propuesto

> **Un *title plant* aplicado a la capa de zonificación y habilitación urbana de Arequipa.**

| Dimensión | Definición |
|---|---|
| Arquetipo | Agregador puro (A) |
| Vertical de ingresos | Registral y urbanístico |
| Vertical de captación | Exposición delictiva |
| Canal | Directo al comprador; institucional en segunda fase |
| Barrera de entrada | Capa de zonificación digitalizada y mantenida — local, costosa, no replicable a distancia |
