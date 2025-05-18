
# ☕ API REST de Cafés

Este proyecto es una **API REST** construida con **Node.js** y **Express**, que permite gestionar una lista de cafés. Incluye rutas para realizar operaciones **CRUD** (Crear, Leer, Actualizar, Eliminar) y está acompañada de pruebas automatizadas con **Jest** y **Supertest**.

---

## 📁 Estructura del Proyecto

```
.
├── index.js            # Archivo principal con la API Express
├── cafes.json          # Base de datos simulada con cafés
├── server.spec.js      # Archivo de pruebas con Supertest
├── package.json
└── README.md
```

---

## 🚀 Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/framirez-lab/cafeteria-monaco.git
cd nombre-del-repo
```

2. Instala las dependencias:

```bash
npm install
```

---

## 🧪 Ejecutar la API

```bash
node index.js
```

Servidor corriendo en: `http://localhost:3000`

---

## 🧪 Ejecutar pruebas con Supertest

```bash
npm test
```

Las pruebas cubren:

- ✅ GET `/cafes` devuelve lista de cafés
- ❌ DELETE `/cafes/:id` responde 404 si no existe el café
- ✅ POST `/cafes` agrega un nuevo café correctamente
- ❌ PUT `/cafes/:id` responde 400 si el `id` no coincide

---

## 🔄 Endpoints

### `GET /cafes`
Retorna la lista completa de cafés.

### `GET /cafes/:id`
Retorna un café específico por ID.

### `POST /cafes`
Agrega un nuevo café. Requiere un objeto con `id` y `nombre`.

### `PUT /cafes/:id`
Actualiza un café existente. El `id` del payload debe coincidir con el parámetro.

### `DELETE /cafes/:id`
Elimina un café. Requiere cabecera `Authorization` con un token (simulado).

---

## 📦 Dependencias

- [Express](https://expressjs.com/)
- [Supertest](https://www.npmjs.com/package/supertest)
- [Jest](https://jestjs.io/)

---

## 📌 Notas

- La API no utiliza una base de datos real, sino un archivo JSON (`cafes.json`) como fuente de datos.
- Para el endpoint DELETE, se simula un token JWT mediante la cabecera `Authorization`.

---

## 📝 Licencia

MIT - Proyecto educativo para practicar Node.js, Express y testing.
