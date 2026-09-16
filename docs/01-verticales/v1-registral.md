# Vertical 1 — Legal / Registral

**Pregunta que responde:** ¿este predio es legalmente transferible, y a quién pertenece realmente?

---

## Fuentes en el Perú

| Recurso | Qué entrega | Acceso |
|---|---|---|
| [Visor BGR — SUNARP](https://www.gob.pe/63173-acceder-al-visor-de-la-base-grafica-registral) | Ubicación gráfica georreferenciada del predio, polígonos sobre imagen satelital, más de 6 millones de imágenes | **Gratuito** |
| [SPRL — SUNARP](https://sprl.sunarp.gob.pe/sprl/ingreso) | Partida registral, índices, repositorio de títulos, publicidad simple y certificada con firma electrónica | Gratuito y de pago, 24/7 |
| [Manual del Visor BGR](https://www.sunarp.gob.pe/pdfs/visorbgr/MANUAL_DEL_USUARIO_VISOR_BGR.pdf) | Documentación oficial de uso | Público |

---

## Qué se puede detectar con este vertical

- Existencia o inexistencia de partida registral — un lote sin partida es la señal de alerta más grave
- Titularidad inscrita frente a quien se presenta como vendedor
- Cargas y gravámenes: hipotecas, embargos, medidas cautelares
- Superposición de polígonos: dos partidas reclamando el mismo terreno
- Predios de propiedad del Estado ofrecidos por seudodirigentes

> Tres de los cuatro mecanismos de fraude documentados en Arequipa se detectan con este solo vertical.

---

## Brecha

| Aspecto | Estado |
|---|---|
| Digitalización | Resuelta |
| Georreferenciación | Resuelta |
| Gratuidad de la consulta básica | Resuelta |
| **API pública documentada** | **No identificada** |

La consulta es humana, no programática. El producto debe diseñarse para **consumo asistido**: el sistema guía y estructura la consulta, el operador o el usuario la ejecuta, y el resultado se incorpora al reporte con su fecha y su trazabilidad de origen.

---

## Evidencia conductual

> El Visor BGR superó **3 millones de consultas de más de 360 mil ciudadanos**.

Es el indicio más fuerte disponible de demanda ciudadana de verificación predial en el Perú. Su límite como evidencia: el servicio es gratuito y por tanto no acredita disposición a pagar.

---

## Comparables internacionales

| País | Instrumento | Modelo |
|---|---|---|
| Estados Unidos | Seguro de título sobre *title plants* privados — **USD 16 200 M en primas (2024)** | Seguro |
| Reino Unido | LLC1, dentro de la Local Authority Search | Obligación legal |
| Estonia | e-Land Register: propietarios, restricciones e hipotecas en consulta pública | Bien público |
| España | Nota simple electrónica de los registradores | Bien público de pago |
| Chile | Certificado de Hipotecas, Gravámenes y Prohibiciones | Bien público de pago |

---

## Dificultad técnica: **media**

El dato existe, es georreferenciado y es público. La dificultad no es de obtención sino de **automatización del acceso** y de vinculación con las demás capas ante la ausencia de un identificador único de predio.

---

## Indicador de cuadro de mando asociado

- Porcentaje de consultas en las que se detecta ausencia de partida registral
- Porcentaje de consultas con cargas o gravámenes vigentes
- Tiempo medio de obtención de la capa registral por reporte
