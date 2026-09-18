# BRIEFING DEL PROYECTO

**Proyecto:** EtiquetaClara
**Grupo consultor:** ____________________ 
**Integrantes:** _Andrea valentina ochoa Andres felipe velez_
**Grupo cliente:** ______________________ 
**Entrevistado:** ____________________
**Fecha:** ______________
**Duración de la entrevista:** 15 minutos

---

## 1. EL PROBLEMA

**1.1 Descrito en una frase:**

> Una persona que compra snacks en el supermercado necesita entender qué trae un producto en pocos segundos porque tiene que decidir ahí mismo, de pie y con afán, pero actualmente la etiqueta trae letra diminuta, términos técnicos y una tabla que casi nadie sabe leer.

**1.2 Cómo se resuelve hoy, sin el producto:**

Agarra el paquete, lo voltea y trata de leer la lista de ingredientes como pueda. Si no entiende algo, se guía por lo que ya conoce, mira solo las calorías o busca el nombre en Google desde el celular, que se demora más. Cuando compra para alguien que tiene alergias, revisa el empaque completo dos veces y, si le queda una duda, no lo lleva.

**1.3 Costo del problema (tiempo, dinero, frustración):**

- **Tiempo:** entre dos y tres minutos por producto cuando de verdad quiere leer, y en una compra son varios productos.
- **Frustración:** termina eligiendo por costumbre y no por lo que dice la etiqueta.
- **Dinero:** a veces compra algo y en la casa descubre un ingrediente que quería evitar. Un snack abierto ya no se devuelve.

**1.4 Frases textuales del cliente (mínimo dos, entre comillas):**

1. “Yo agarro el paquete, le doy la vuelta y no entiendo nada. Al final me llevo el de siempre.”
2. “No necesito que me digan si es sano o no, necesito ver qué trae y decidir yo.”
3. “Con la fila detrás de mí no me pongo a leer con lupa.”

---

## 2. EL USUARIO

| Campo | Usuario principal | Usuario secundario |
| --- | --- | --- |
| Nombre y edad | Laura Gómez, 27 años | Marta Rincón, 52 años |
| Ocupación o rol | Analista administrativa | Ama de casa, hace el mercado para su familia |
| Contexto de uso | En el pasillo del supermercado, de pie, con afán, después del trabajo | En la tienda o en la casa armando la lista de compras, con las gafas de lectura a la mano |
| Dispositivo | Celular Android, con una mano | Celular, y a veces tableta o computador en casa |
| Nivel tecnológico | Medio: usa apps todos los días, pero no le interesa lo técnico | Bajo a medio: usa WhatsApp y apps sencillas |
| Objetivo principal | Decidir en menos de 30 segundos si se lleva un snack o no | Confirmar qué alérgenos declara un producto antes de comprarlo para su hijo |
| Principal frustración | La letra diminuta de la etiqueta y los términos que no entiende | Frases como “puede contener trazas de…”, que no sabe cómo interpretar |

---

## 3. LA TAREA PRINCIPAL

**3.1 Si solo pudiera hacer una cosa, sería:**

Ver de forma clara qué trae un producto (ingredientes, nutrientes y alérgenos declarados) para decidir si lo compra.

**3.2 Pasos que sigue para lograrla:**

1. Abre la app y ve una lista de snacks con foto, nombre y marca.
2. Busca el producto por nombre o marca, o lo va reconociendo por la imagen.
3. Entra al detalle y lee ingredientes, nutrientes y alérgenos declarados.
4. Decide: si le interesa lo guarda en favoritos, si no, vuelve a la lista y sigue con otro.

**3.3 Información que necesita para decidir:**

Nombre, marca, imagen para reconocer el paquete, lista de ingredientes, valores nutricionales y alérgenos que declara el fabricante.

**3.4 Información que sobra:**

Datos internos de la base de datos (quién editó el producto, códigos, fechas de modificación), nombres de categorías en inglés, enlaces técnicos, y cualquier nota, puntaje o calificación sobre si el producto es “bueno” o “malo” para la salud. La app solo muestra lo que declara la etiqueta.

---

## 4. CONTENIDO Y DATOS

**4.1 Datos que debe mostrar cada elemento del listado**

| Dato | ¿Imprescindible o adicional? | ¿Lo entrega la API? |
| --- | --- | --- |
| Nombre del producto | Imprescindible | Sí (a veces viene vacío) |
| Marca | Imprescindible | Sí (a veces viene vacío) |
| Imagen del empaque | Imprescindible | Sí, pero no todos los productos tienen |
| Ingredientes | Imprescindible | Sí, aunque en varios productos viene incompleto |
| Nutrientes (energía, grasas, azúcares, sal, proteínas) | Imprescindible | Sí, con datos parciales según el producto |
| Alérgenos declarados | Imprescindible | Sí, a veces vacío |
| Cantidad o porción | Adicional | A veces |
| Marcar como favorito | Adicional | No, lo guarda la propia app |

*Los nombres exactos de los campos se confirman revisando la respuesta real de la API de Open Food Facts.*

**4.2 Criterios de búsqueda y filtrado acordados:**

- Buscar por nombre del producto o por marca, con el campo siempre visible.
- Filtrar por alérgeno declarado, para ver qué productos lo mencionan.
- No habrá filtros del tipo “libre de…” ni “sin…”, porque los datos pueden venir incompletos y la app podría dar una falsa tranquilidad.

**4.3 Orden por defecto del listado:**

Alfabético por nombre del producto, de la A a la Z.

**4.4 Qué hacer cuando un dato viene vacío:**

No se inventa ni se rellena nada. Si falta una sección se muestra un mensaje neutro: “El fabricante no declaró esta información”. Si no hay imagen se usa un espacio gris con un ícono. En alérgenos, un dato vacío nunca se muestra como “sin alérgenos”, sino como “sin información declarada”, porque no es lo mismo que no tener alérgenos.

---

## 5. ALCANCE

**5.1 Funcionalidades acordadas, en orden de prioridad**

| # | Funcionalidad | Prioridad (alta, media, baja) | ¿Entra en la versión 1? |
| --- | --- | --- | --- |
| 1 | Catálogo de snacks en tarjetas (imagen, nombre y marca) | Alta | Sí |
| 2 | Detalle del producto con ingredientes, nutrientes y alérgenos declarados | Alta | Sí |
| 3 | Buscador por nombre o marca | Alta | Sí |
| 4 | Favoritos (guardar y quitar productos) | Media | Sí |
| 5 | Filtro por alérgeno declarado | Media | Sí |
| 6 | Páginas de Inicio, Contacto y Acerca de | Baja | Sí |

**5.2 Fuera de alcance, acordado explícitamente:**

- Cuentas de usuario e inicio de sesión.
- Escaneo del código de barras con la cámara.
- Puntajes, semáforos o cualquier diagnóstico de salud (“saludable”, “no recomendado”).
- Comparar dos productos lado a lado.
- Funcionamiento sin conexión.

---

## 6. RESTRICCIONES Y REFERENCIAS

**6.1 Referencias que le gustan al cliente y por qué:**

- Las tarjetas de producto de las apps de supermercado: foto grande, nombre y marca a la vista sin tener que entrar.
- Yuka: le gusta que el producto aparece rápido. No le gusta que le ponga una nota.
- La tabla nutricional de los empaques, pero con una letra que se pueda leer.

**6.2 Lo que quiere evitar:**

Calificaciones o colores que le digan qué debe comprar, pantallas recargadas, textos técnicos sin explicar, letra pequeña y ventanas emergentes que tapen la información.

**6.3 Restricciones de conexión, dispositivo o accesibilidad:**

- Se usa sobre todo desde el celular y de pie, así que la versión móvil manda.
- La señal dentro de un supermercado suele ser mala. La app no puede quedarse en blanco mientras carga.
- Hay usuarios con vista cansada o baja visión leve. Se necesita buen contraste, texto de mínimo 16 px y que la información no dependa solo del color.

**6.4 Tono y estilo visual esperado** *(marcar los que apliquen)*

```
[x] Sobrio        [x] Cercano       [ ] Juvenil       [ ] Institucional
[x] Minimalista   [ ] Colorido      [ ] Editorial     [ ] Técnico
```

---

## 7. CRITERIOS DE ÉXITO

**7.1 Cómo sabremos que funcionó:**

Cuando una persona en el pasillo pueda abrir un producto y entender qué trae sin tener que voltear el paquete ni buscar en otro lado.

**7.2 Indicador medible:**

Encontrar un producto y leer sus ingredientes y alérgenos en menos de 30 segundos y máximo 3 toques desde que se abre la app.

**7.3 Qué sería un fracaso:**

- Que la persona siga leyendo el empaque porque la pantalla no le aclaró nada.
- Que la app muestre “sin alérgenos” cuando en realidad el dato no existía.
- Que consultar el producto en la app tarde más que leer la etiqueta.

---

## 8. CONSECUENCIAS PARA EL DISEÑO

| Lo que dijo el cliente | Decisión de diseño que tomo | Pantalla o componente |
| --- | --- | --- |
| “Le doy la vuelta y no entiendo nada” | Texto de mínimo 16 px, bloques separados para ingredientes, nutrientes y alérgenos, con un texto de apoyo bajo los términos técnicos | Detalle |
| “Con la fila detrás no me pongo a leer con lupa” | La tarjeta muestra solo imagen, nombre y marca, y el detalle queda a un toque | Catálogo y detalle |
| “No necesito que me digan si es sano o no” | Nada de puntajes ni semáforos. Solo datos declarados y una nota que aclara que la información viene de la etiqueta | Detalle y Acerca de |
| Datos incompletos, sobre todo en alérgenos | Renderizado condicional: si falta el dato se muestra “sin información declarada”, distinto de “no declara alérgenos” | Detalle |
| Se usa casi siempre desde el celular y de pie | Diseño móvil primero, con el buscador visible arriba y no escondido en un ícono | Catálogo |
| Mala señal dentro del supermercado | Imágenes livianas con espacio reservado y un estado de carga para que la pantalla no salte | Catálogo |
| A veces no hay resultados o no hay favoritos | Estado vacío con un mensaje claro y una acción sugerida | Catálogo y Favoritos |
