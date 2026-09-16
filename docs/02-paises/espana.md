# España — Modelo 3: Bien público digital con criterio de privacidad explícito

Relevante para este proyecto por una razón específica: **resolvió por norma qué dato predial es público y cuál no**. Ese criterio es directamente adoptable.

---

## Instrumento: Sede Electrónica del Catastro

Portal: [sedecatastro.gob.es](https://www.sedecatastro.gob.es/)

Ofrece visor temático catastral, descarga de información cartográfica y alfanumérica, servicios web, formatos **INSPIRE** y datos estadísticos.

---

## La separación público / protegido

Este es el aporte central del caso español.

| Categoría | Contenido | Acceso |
|---|---|---|
| **Datos no protegidos** | Toda la información catastral incluida la **cartografía**: geometría, superficie, uso, antigüedad, croquis, certificaciones catastrales descriptivas y gráficas | **Libre y gratuito, sin identificación** |
| **Datos protegidos** | Nombre, apellidos, razón social, código de identificación y domicilio del titular o sujeto pasivo del IBI; **valor catastral** | Restringido |

> Se pueden consultar libremente los datos catastrales no protegidos —incluida la cartografía catastral— incorporados a la Base de Datos Nacional del Catastro; es decir, los que no hacen referencia al titular ni al valor catastral.

**Fuente:** [Servicios de acceso libre — Catastro](https://www.catastro.hacienda.gob.es/ayuda/ayuda_cl.htm)

---

## Separación entre catastro y registro

España mantiene dos sistemas distintos y complementarios:

| Sistema | Qué acredita | Canal |
|---|---|---|
| **Catastro** | Descripción física, geometría, superficie, uso | Sede Electrónica del Catastro — gratuito |
| **Registro de la Propiedad** | Titularidad y cargas | Nota simple electrónica, sede de los registradores — de pago |

La **referencia catastral** actúa como clave de vinculación entre ambos. Es el equivalente funcional del identificador único neerlandés.

---

## Lecciones transferibles al caso Arequipa

### 1. El criterio de privacidad, adoptable tal cual

> **Geometría y atributos del predio: públicos. Identidad del titular y valor: protegidos.**

Este criterio resuelve de antemano la principal objeción ética y legal al producto propuesto, y proporciona un fundamento normativo comparado —no una opinión del equipo— para el capítulo de protección de datos.

### 2. La clave de vinculación es indispensable

La referencia catastral española y el identificador único neerlandés cumplen la misma función: permitir que dos registros soberanos hablen del mismo predio sin fusionarse.

**En el Perú esa clave no existe de forma universal.** La integración entre SUNARP, municipalidad y prestadores de servicio debe resolverse por coincidencia geográfica, lo cual introduce error. Es una limitación que el proyecto debe declarar explícitamente, no ocultar.

### 3. Formatos INSPIRE como referencia de interoperabilidad

La adopción de estándares europeos de información geoespacial demuestra que la interoperabilidad se logra por **estándar de formato**, no por centralización institucional. Es la vía realista para el Perú: no unificar las 1 800 municipalidades, sino estandarizar cómo publican.

---

## Contraste con el Perú

| Dimensión | España | Perú |
|---|---|---|
| Cartografía catastral pública y gratuita | Sí | Parcial — Visor BGR SUNARP |
| Criterio normativo público/protegido | Explícito | No estandarizado |
| Clave de vinculación entre registros | Referencia catastral | Inexistente a nivel universal |
| Estándar de interoperabilidad | INSPIRE | No adoptado en el nivel municipal |
