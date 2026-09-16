# Estonia — Modelo 3: Interoperabilidad por diseño

El caso extremo del Modelo 3. Relevante no por el registro en sí, sino por **cómo los registros se hablan entre ellos**.

---

## Instrumento: e-Land Register

Portal operado por el *Registrite ja Infosüsteemide Keskus* (Centro de Registros y Sistemas de Información).

El e-Land Register contiene datos de **todos los inmuebles registrados en Estonia**. En el entorno electrónico, cualquier persona puede verificar rápidamente:

- Datos generales del inmueble registrado
- Superficie
- Propietarios
- **Restricciones**
- **Hipotecas que gravan el inmueble**

Contenido completo del registro: número de referencia del predio, ubicación, superficie, nombre del propietario registrado, dirección postal del propietario, tipo de tenencia, **uso permitido del suelo**, gravámenes, restricciones e hipotecas.

**Fuentes:** [e-Land Register — RIK](https://www.rik.ee/en/e-land-register/e-land-register-portal) · [e-Estonia](https://e-estonia.com/solutions/e-governance/e-services-registries/)

Obsérvese que el **uso permitido del suelo** —el equivalente estonio de la zonificación— está incorporado al mismo registro que la titularidad. En el Perú son dos instituciones distintas.

---

## El principio arquitectónico que importa

> Una característica clave de la gobernanza estonia es el **entrecruzamiento de las bases de datos del sector público**: los registros estonios se referencian entre sí, evitando la doble recolección del mismo dato, y **se utilizan los mismos identificadores únicos en todos los registros** para toda clase de objetos, incluidas las unidades geoespaciales y las parcelas.

Tres reglas derivadas:

1. **Un dato, un dueño.** Cada registro es responsable de su dato y nadie lo duplica.
2. **Identificador único compartido.** La misma parcela tiene la misma clave en todos los sistemas.
3. **Referencia, no copia.** Los sistemas consultan al registro fuente en lugar de mantener réplicas.

---

## Por qué esto es relevante para el proyecto

El producto propuesto para Arequipa es, técnicamente, **un intento privado de lograr lo que Estonia logró por diseño institucional**.

| Estonia | Producto propuesto para Arequipa |
|---|---|
| Identificador único compartido por norma | Vinculación por coincidencia geográfica, con margen de error |
| Referencia al registro fuente | Consumo asistido y, en la capa municipal, réplica normalizada |
| Dato de uso del suelo dentro del registro predial | Dato de zonificación en PDF de una institución distinta |
| Costo de integración: cero, resuelto en origen | Costo de integración: el núcleo del modelo de negocio |

**La conclusión estratégica.** El valor económico del producto es directamente proporcional al desorden institucional. En Estonia el producto no tendría razón de existir. En el Perú la tiene, y la tendrá mientras la capa municipal no se estandarice.

---

## Lección para la propuesta de política pública

Si el proyecto se presenta también como recomendación institucional, el aporte estonio es concreto y de bajo costo:

> **Antes de construir un sistema integrador, adoptar un identificador único de predio compartido entre SUNARP, las municipalidades y los prestadores de servicios.**

Sin esa clave, cualquier integración —pública o privada— es aproximada. Con ella, el problema deja de requerir un producto.
