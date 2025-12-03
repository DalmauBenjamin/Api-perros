# 🐕 API Perritos

Una aplicación web simple que permite gestionar una lista de perros con operaciones CRUD (Crear, Leer, Actualizar, Eliminar).

## 📋 Descripción

Este proyecto consta de:
- **Backend**: API REST construida con Node.js y Express que gestiona perros
- **Frontend**: Interfaz web interactiva para interactuar con la API

La aplicación permite:
- ✅ Ver todos los perros registrados
- ✅ Agregar nuevos perros
- ✅ Editar información de perros existentes
- ✅ Eliminar perros

## 🛠️ Requisitos Previos

Asegúrate de tener instalado:
- [Node.js](https://nodejs.org/) (versión 14 o superior)
- npm (viene con Node.js)

## 📦 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/DalmauBenjamin/Api-perros.git
cd Api-perros
```

### 2. Instalar dependencias

```bash
npm install
```

Esto instalará:
- **express**: Framework web para Node.js
- **cors**: Middleware para habilitar CORS (Cross-Origin Resource Sharing)

## 🚀 Ejecución

### Iniciar el servidor

```bash
node index.js
```

Deberías ver en la consola:
```
API funcionando en http://localhost:3000
```

### Acceder a la aplicación

1. Abre tu navegador
2. Ve a `http://localhost:3000`
3. Carga el archivo `index.html` localmente o sirve la carpeta con un servidor web simple

### Opción alternativa: Usar Live Server

Si tienes Live Server instalado en VS Code:
1. Click derecho en `index.html`
2. Selecciona "Open with Live Server"

## 📚 Endpoints de la API

### GET /perros
Obtiene la lista de todos los perros.

**Respuesta:**
```json
[
  {
    "id": 1,
    "nombre": "Firulais",
    "raza": "Labrador",
    "edad": 4
  }
]
```

### GET /perros/:id
Obtiene un perro específico por ID.

### POST /perros
Crea un nuevo perro.

**Body requerido:**
```json
{
  "nombre": "Rocco",
  "raza": "Pitbull",
  "edad": 2
}
```

### PUT /perros/:id
Actualiza completamente un perro existente.

**Body requerido:**
```json
{
  "nombre": "Nuevo Nombre",
  "raza": "Nueva Raza",
  "edad": 5
}
```

### PATCH /perros/:id
Actualiza parcialmente un perro (solo los campos proporcionados).

### DELETE /perros/:id
Elimina un perro por ID.

## 📁 Estructura del Proyecto

```
api-perros/
├── index.js          # API Backend con Express
├── index.html        # Interfaz Frontend
├── package.json      # Dependencias del proyecto
└── README.md         # Este archivo
```

## 🔧 Datos Iniciales

Por defecto, la API inicia con dos perros:
- Firulais (Labrador, 4 años)
- Rocco (Pitbull, 2 años)

Estos datos se almacenan en memoria, por lo que se perderán cuando reinicies el servidor.

## 💡 Funcionalidades de la Interfaz

### Agregar Perro
1. Completa los campos: Nombre, Raza y Edad
2. Haz click en "Agregar"

### Editar Perro
1. Haz click en "✏️ Editar" en la fila del perro
2. Modifica los datos en el formulario
3. Haz click en "Guardar Cambios"

### Eliminar Perro
1. Haz click en "🗑️ Eliminar"
2. Confirma la acción en el diálogo

## 🔐 Características de Seguridad

- CORS habilitado para permitir solicitudes desde el frontend
- Validación de campos en el frontend

## 🚧 Notas Importantes

- Los datos se almacenan en memoria (no persisten después de reiniciar)
- Para una aplicación de producción, considera usar una base de datos real

## 📝 Licencia

ISC

## 👤 Autor

Benjamin Dalmau

---

¿Necesitas ayuda? Abre un issue en el repositorio.
