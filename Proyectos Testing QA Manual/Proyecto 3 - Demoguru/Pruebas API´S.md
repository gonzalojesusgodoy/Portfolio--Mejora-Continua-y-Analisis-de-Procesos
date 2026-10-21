### 🔌 Pruebas API

Las **pruebas API** fueron realizadas en una página web distinta a la que veníamos trabajando, pero se probaron dentro del mismo proyecto. Se ejecutaron un total de **10 casos de prueba: 5 casos positivos y 5 casos negativos**.

Todos los casos fueron documentados de manera detallada, adjuntando la información requerida, como los **endpoints utilizados, los parámetros enviados, las respuestas obtenidas y las expectativas de los resultados**.

Para llevar a cabo estas pruebas se utilizó la herramienta **Postman**, asegurando la correcta validación y verificación de las funcionalidades de la API.

---

### ✅ Casos positivos

#### 001 — Obtener información de un Pokémon existente

- **Método:** `GET`
- **Descripción:** Verificar si la API devuelve correctamente los datos del Pokémon existente.
- **URL:** https://pokeapi.co/api/v2/pokemon/pikachu/
- **Esperado:** Código de estado `200`.
- **Obtenido:** Código de estado `200`.

#### 002 — Obtener una lista de Pokémon

- **Método:** `GET`
- **Descripción:** Verificar si la API devuelve de forma correcta una lista de 10 Pokémon.
- **URL:** https://pokeapi.co/api/v2/pokemon/?limit=10
- **Esperado:** Código de estado `200` y una lista con 10 Pokémon.
- **Obtenido:** Código de estado `200` y links del listado de Pokémon.

#### 003 — Obtener información de un tipo de Pokémon

- **Método:** `GET`
- **Descripción:** Comprobar que la API devuelva correctamente la información del tipo de Pokémon solicitado.
- **URL:** https://pokeapi.co/api/v2/type/3/
- **Esperado:** Código de estado `200` y detalles sobre el tipo `Flying`.
- **Obtenido:** Código de estado `200`.

#### 004 — Obtener información de una habilidad de un Pokémon

- **Método:** `GET`
- **Descripción:** Verificar si la API devuelve de forma correcta la habilidad del Pokémon.
- **URL:** https://pokeapi.co/api/v2/ability/4/
- **Esperado:** Código de estado `200`.
- **Obtenido:** Código de estado `200`.

#### 005 — Obtener información sobre un movimiento específico

- **Método:** `GET`
- **Descripción:** Verificar que la API proporcione información sobre un movimiento específico.
- **URL:** https://pokeapi.co/api/v2/move/15/
- **Esperado:** Código de estado `200` y detalles sobre el movimiento `Cut`.
- **Obtenido:** Código de estado `200`.

---

### ❌ Casos negativos

#### 006 — Obtener un Pokémon inexistente

- **Método:** `GET`
- **Descripción:** Verificar si la API actúa de forma correcta al solicitar un Pokémon inexistente.
- **URL:** https://pokeapi.co/api/v2/pokemon/nonexistentpokemon/
- **Esperado:** Código de estado `404` y mensaje `Not Found`.
- **Razón del error:** La API intenta buscar un Pokémon con el nombre `nonexistentpokemon`, que no existe en su base de datos. Por ello, la API no encuentra lo solicitado y devuelve el código `404`.

#### 007 — Usar un método incorrecto en un endpoint

- **Método:** `POST`
- **Descripción:** Verificar que la API no permita utilizar un método HTTP incorrecto para el endpoint.
- **URL:** https://pokeapi.co/api/v2/pokemon/pikachu/
- **Esperado:** Código de estado `404`.
- **Razón del error:** Se utilizó el método `POST` en lugar del método `GET`, que es el utilizado para obtener información.

#### 008 — Endpoint mal escrito

- **Método:** `GET`
- **Descripción:** Verificar que la API devuelva un error cuando se solicita un endpoint mal escrito.
- **URL:** https://pokeapi.co/api/v2/pokemons/
- **Esperado:** Código de estado `404`.
- **Razón del error:** El endpoint está mal escrito. La API no tiene un endpoint llamado `pokemons`.

#### 009 — Obtener información con un ID incorrecto

- **Método:** `GET`
- **Descripción:** Verificar que la API maneje correctamente las solicitudes con un identificador incorrecto.
- **URL:** https://pokeapi.co/api/v2/pokemon/abc/
- **Esperado:** Código de estado `404` o `400`.
- **Razón del error:** La API espera un ID numérico del Pokémon y no un identificador compuesto por letras.

#### 010 — Falta de parámetros necesarios en una solicitud

- **Método:** `GET`
- **Descripción:** Verificar que la API devuelva un error cuando se solicita una subruta que no existe.
- **URL:** https://pokeapi.co/api/v2/pokemon/
- **Esperado:** Código de estado `400`.
- **Razón del error:** Se solicitó un recurso que no está definido en la API.
