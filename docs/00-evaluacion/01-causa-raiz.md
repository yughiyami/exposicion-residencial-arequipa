# 01 — Hipótesis de Causa Raíz

> Método: `problem-root-cause`. Se aplicaron cuatro marcos de análisis sobre el síntoma declarado. La salida es una hipótesis falsable, no un hecho de mercado probado.

---

## Síntoma declarado (literal, sin reinterpretar)

> «Las personas que buscan comprar o alquilar una vivienda en Arequipa tienen dificultades para evaluar objetivamente la exposición delictiva de una ubicación específica, debido a que la información sobre hechos delictivos, aunque disponible mediante plataformas y bases de datos oficiales, requiere procesos de consulta, interpretación y comparación espacial que no están orientados directamente a la decisión residencial.»

## Reencuadre del síntoma

El planteamiento original es correcto en su mecánica —dato disponible pero no accionable— y **demasiado estrecho en su alcance**. La exposición delictiva es la capa más visible del problema, pero no la de mayor consecuencia económica.

| Dimensión | Exposición delictiva | Condición legal-urbanística |
|---|---|---|
| Magnitud de la pérdida | Incomodidad; efecto documentado cercano al 1 % del valor | Pérdida total del capital invertido |
| Reversibilidad | Alta — el afectado puede mudarse | Nula — no existe contraparte a quien reclamar |
| Ventana de decisión | Permanente | Únicamente antes de la firma |
| Gasto observable hoy | No documentado | Sí — búsqueda registral, honorarios legales, tasación |

**Conclusión del reencuadre:** el problema real es de **verificación integral previa a la transacción**, con cinco capas de información, de las cuales el delito es una.

---

## Quién

Comprador de primera vivienda o de lote en las zonas de expansión de Arequipa Metropolitana: Cerro Colorado, Yura, Characato, La Joya, y el eje Majes–Pedregal.

Perfil conductual: compra una sola vez en su vida, financia con ahorro familiar o crédito de caja municipal, no cuenta con asesoría profesional contratada, y opera bajo presión de escasez inducida por el vendedor.

**Segmento secundario (pagador institucional):** notarías, tasadores y analistas de crédito de entidades microfinancieras.

## Dolor

No puede verificar, **antes de transferir dinero**, si la ubicación es:

1. legalmente transferible,
2. urbanísticamente habilitable,
3. físicamente segura,
4. servible con agua y desagüe,
5. tolerable en términos de exposición delictiva.

El descubrimiento del defecto ocurre sistemáticamente **después** de la firma.

## Workaround actual

Conducta observada hoy:

- Solicitud de partida registral en SUNARP (canal en línea disponible).
- Consulta informal a un abogado conocido.
- Confianza depositada en el dirigente de la asociación de vivienda o en el propio vendedor.
- Consulta presencial no vinculante en la municipalidad distrital.

Resultado: cuatro a cinco consultas desacopladas, semanas de duración, respuestas parciales y **ningún veredicto único**.

---

## Causa raíz

> **El Estado organiza la información por institución. El ciudadano la necesita organizada por predio.**

SUNARP custodia la titularidad. La municipalidad distrital, la zonificación y la habilitación urbana. CENEPRED, el peligro físico. SEDAPAR y SEAL, la factibilidad de servicios. El MININTER, la incidencia delictiva.

Cada entidad es soberana sobre su dato, tiene su propio procedimiento administrativo y **ninguna tiene el mandato de responder la única pregunta que le importa al ciudadano**: ¿me conviene comprar en esta ubicación?

El problema no es de disponibilidad. Es de **integración orientada a la decisión**.

---

## Traza de marcos aplicados

### TRIZ — Análisis de contradicción

| Para lograr | El sistema debe ser | Pero eso impide |
|---|---|---|
| Validez jurídica y confiabilidad del dato | Custodiado por la institución soberana que lo produce | Consolidación en un punto único |
| Utilidad en la decisión de compra | Consolidado en un punto y en un instante | Soberanía institucional del dato |

La contradicción **no está resuelta por ningún actor**: se traslada íntegramente al ciudadano. Esa transferencia de carga constituye la causa raíz.

### Jobs-to-be-Done

El trabajo contratado no es «ver un mapa de delitos». Es **«no arruinarme»**. Nadie desea un mapa; se desea la tranquilidad posterior a la firma. El producto compite contra la incertidumbre, no contra otros mapas.

### Marketing Myopia — Levitt

Definir el negocio como «plataforma de mapas de seguridad» es miopía de categoría. La definición correcta desde el punto de vista del cliente es **due diligence residencial**: el equivalente predial de una central de riesgo crediticio.

En el Perú cualquier ciudadano comprende la consulta de historial crediticio de una persona. **No existe el equivalente para un predio.**

### Progress-Making Forces — Moesta

| Fuerza | Contenido | Intensidad |
|---|---|---|
| Push | Más de 1 000 denuncias por estafa en compraventa de terrenos en Arequipa al cierre de 2024; 33,5 % de victimización urbana | Alta |
| Pull | Veredicto consolidado en minutos frente a semanas de trámites | Alta |
| Anxiety | «¿Puedo confiar en este dato?» | Media — mitigable citando la fuente oficial y su fecha en cada línea |
| Habit | «Le pregunto a un conocido» | Media |

Push + Pull superan a Anxiety + Habit porque **el costo del error es catastrófico e irreversible**.

---

## Predicción falsable

> Si la causa raíz es la fragmentación institucional y no la ausencia de datos, entonces debe observarse que:
>
> **(a)** los compradores ya incurren en gasto y tiempo en consultas separadas antes de firmar;
> **(b)** las denuncias por estafa se concentran en el borde periurbano de expansión, donde el estado legal es ambiguo, y no en el cercado consolidado;
> **(c)** notarios, tasadores y analistas de crédito ejecutan hoy, de forma manual, un checklist de verificación multi-fuente.

**Qué la falsaría:** si en una muestra de compradores recientes la mayoría no realizó más de una consulta, no incurrió en gasto alguno y no percibe el asunto como relevante, la hipótesis queda refutada y debe regresarse a la etapa de exploración.

---

## Supuestos declarados y evidencia faltante

| # | Supuesto | Estado |
|---|---|---|
| 1 | Las municipalidades de Arequipa no publican zonificación en formato geoespacial estructurado | **Verificado** — ver `docs/03-region/02-arequipa.md` |
| 2 | Monto y frecuencia del gasto por comprador en verificación previa | **No verificado** — requiere entrevistas |
| 3 | SEDAPAR emite factibilidad consultable por ubicación y no solo por expediente | **Verificado como falso** — el trámite es presencial y por expediente |
| 4 | Concentración geográfica de las denuncias por estafa en el borde periurbano | **No verificado** — requiere acceso al registro de la Procuraduría regional |

---

## Condición de parada

Se detiene la descomposición en este nivel porque la hipótesis es **(a)** falsable —se ha declarado explícitamente qué evidencia la refutaría— y **(b)** está anclada en conducta y gasto observables hoy, no en un deseo hipotético futuro.

Continuar preguntando «¿por qué el Estado peruano está fragmentado?» conduciría a un problema de reforma institucional sobre el cual el equipo no tiene capacidad de intervención. Eso constituiría el error de capa del caso Segway: resolver correctamente en el nivel equivocado.
