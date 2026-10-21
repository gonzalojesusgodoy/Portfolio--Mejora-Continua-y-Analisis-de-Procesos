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
- <img width="1366" height="768" alt="unnamed (14)" src="https://github.com/user-attachments/assets/23d1737c-3bdf-4a18-a2a0-091868f12289" />


#### 002 — Obtener una lista de Pokémon

- **Método:** `GET`
- **Descripción:** Verificar si la API devuelve de forma correcta una lista de 10 Pokémon.
- **URL:** https://pokeapi.co/api/v2/pokemon/?limit=10
- **Esperado:** Código de estado `200` y una lista con 10 Pokémon.
- **Obtenido:** Código de estado `200` y links del listado de Pokémon.
<img width="1366" height="768" alt="unnamed (15)" src="https://github.com/user-attachments/assets/468af709-ad76-4127-b360-330c38e1e0cd" />

#### 003 — Obtener información de un tipo de Pokémon

- **Método:** `GET`
- **Descripción:** Comprobar que la API devuelva correctamente la información del tipo de Pokémon solicitado.
- **URL:** https://pokeapi.co/api/v2/type/3/
- **Esperado:** Código de estado `200` y detalles sobre el tipo `Flying`.
- **Obtenido:** Código de estado `200`.
<img width="1366" height="768" alt="unnamed (16)" src="https://github.com/user-attachments/assets/0a9acfca-0b86-4413-acb8-91575cc070ea" />

#### 004 — Obtener información de una habilidad de un Pokémon

- **Método:** `GET`
- **Descripción:** Verificar si la API devuelve de forma correcta la habilidad del Pokémon.
- **URL:** https://pokeapi.co/api/v2/ability/4/
- **Esperado:** Código de estado `200`.
- **Obtenido:** Código de estado `200`.
<img width="1366" height="768" alt="unnamed (17)" src="https://github.com/user-attachments/assets/6d544746-e5dd-4747-b5f2-b3e717b2150b" />

#### 005 — Obtener información sobre un movimiento específico

- **Método:** `GET`
- **Descripción:** Verificar que la API proporcione información sobre un movimiento específico.
- **URL:** https://pokeapi.co/api/v2/move/15/
- **Esperado:** Código de estado `200` y detalles sobre el movimiento `Cut`.
- **Obtenido:** Código de estado `200`.
<img width="1366" height="768" alt="unnamed (18)" src="https://github.com/user-attachments/assets/a91c6567-933b-4f58-8a48-a4d7c129ead9" />

---

### ❌ Casos negativos

#### 006 — Obtener un Pokémon inexistente

- **Método:** `GET`
- **Descripción:** Verificar si la API actúa de forma correcta al solicitar un Pokémon inexistente.
- **URL:** https://pokeapi.co/api/v2/pokemon/nonexistentpokemon/
- **Esperado:** Código de estado `404` y mensaje `Not Found`.
- **Razón del error:** La API intenta buscar un Pokémon con el nombre `nonexistentpokemon`, que no existe en su base de datos. Por ello, la API no encuentra lo solicitado y devuelve el código `404`.
<img width="1366" height="768" alt="unnamed (19)" src="https://github.com/user-attachments/assets/d3134091-e266-4c46-9862-65b1c5037019" />

#### 007 — Usar un método incorrecto en un endpoint

- **Método:** `POST`
- **Descripción:** Verificar que la API no permita utilizar un método HTTP incorrecto para el endpoint.
- **URL:** https://pokeapi.co/api/v2/pokemon/pikachu/
- **Esperado:** Código de estado `404`.
- **Razón del error:** Se utilizó el método `POST` en lugar del método `GET`, que es el utilizado para obtener información.
<img width="1366" height="768" alt="unnamed (19)" src="https://github.com/user-attachments/assets/a647ae1a-2b10-4714-be5c-9a21a6c27279" />

#### 008 — Endpoint mal escrito

- **Método:** `GET`
- **Descripción:** Verificar que la API devuelva un error cuando se solicita un endpoint mal escrito.
- **URL:** https://pokeapi.co/api/v2/pokemons/
- **Esperado:** Código de estado `404`.
- **Razón del error:** El endpoint está mal escrito. La API no tiene un endpoint llamado `pokemons`.
<img width="1366" height="768" alt="unnamed (20)" src="https://github.com/user-attachments/assets/177efdb3-db8e-433d-b6df-9541c1ad0a2e" />

#### 009 — Obtener información con un ID incorrecto

- **Método:** `GET`
- **Descripción:** Verificar que la API maneje correctamente las solicitudes con un identificador incorrecto.
- **URL:** https://pokeapi.co/api/v2/pokemon/abc/
- **Esperado:** Código de estado `404` o `400`.
- **Razón del error:** La API espera un ID numérico del Pokémon y no un identificador compuesto por letras.
<img width="1366" height="768" alt="unnamed (21)" src="https://github.com/user-attachments/assets/f38df44f-cabd-4efa-b703-a3fda88b9300" />

#### 010 — Falta de parámetros necesarios en una solicitud

- **Método:** `GET`
- **Descripción:** Verificar que la API devuelva un error cuando se solicita una subruta que no existe.
- **URL:** https://pokeapi.co/api/v2/pokemon/
- **Esperado:** Código de estado `400`.
- **Razón del error:** Se solicitó un recurso que no está definido en la API.
<img width="1366" height="768" alt="unnamed (21)" src="https://github.com/user-attachments/assets/dfd00c86-1aa0-4b7c-90c8-6c202e8898b3" />
