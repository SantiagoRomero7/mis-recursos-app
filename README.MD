# 📚 Mis Recursos App

Aplicación web para gestionar y llevar el control de progreso en series, películas y libros. Permite a los usuarios registrar, consultar, actualizar y eliminar recursos, además de realizar búsquedas y aplicar filtros por estado, formato y plataforma.

---

## 📋 Funcionalidades

### CRUD (Crear, Leer, Actualizar, Eliminar)
- **Crear**: Añadir un recurso con los campos:
  - Nombre del recurso.
  - Género.
  - Plataforma (Netflix, Amazon, HBO, Kindle, etc.).
  - Estado (En progreso, Terminado, Pendiente).
  - Formato (Serie, Película, Libro).
  - Fecha de terminación.
  - Valoración final (1 a 5 estrellas).
  - Reseña personal (comentarios).
  
- **Leer**: Visualización de todos los recursos almacenados.
- **Actualizar**: Modificación de datos de un recurso existente.
- **Eliminar**: Eliminación de recursos.

### Filtros y Búsqueda
- Filtros por Estado, Formato y Plataforma.
- Búsqueda por nombre del recurso.

---

## 🗄️ Diseño de Base de Datos (MongoDB)

### 📂 Colección Principal: `recursos`

#### Esquema del Documento:
```json
{
  "id": Number,
  "nombre": String,
  "genero": String,
  "plataforma": String,
  "estado": String,
  "formato": String,
  "fecha_terminacion": Date | null,
  "valoracion": Number | null,
  "reseña": String
}
```

## 🗃️ Comandos para Crear la Base de Datos
### 1. Crear la base de datos y colección en MongoDB:
- use mis_recursos_app;
db.createCollection("recursos");

### 2. Importar los registros de prueba desde el archivo JSON:
- mongoimport --db mis_recursos_app --collection recursos --file recursos.json --jsonArray

### 3. Verificar los datos cargados:
- use mis_recursos_app;
db.recursos.find().pretty();


## 📦 Archivos JSON Incluidos
- ### recursos.json: 
Contiene 50 registros de ejemplo con datos de series, películas y libros.
- ### ¿Qué colección alimenta este archivo?
El archivo recursos.json corresponde a la colección recursos en la base de datos mis_recursos_app.

## 📂 Estructura del Proyecto
```
mis-recursos-app/
│
├── README.md
└── recursos.json
```

## 📝 Instrucciones para Clonar y Probar
### Clonar este repositorio:


- git clone https://github.com/tu-usuario/mis-recursos-app.git
cd mis-recursos-app

### Abrir MongoDB e ingresar a la base de datos:


- use mis_recursos_app;

### Importar los datos de prueba desde el archivo JSON:

- mongoimport --db mis_recursos_app --collection recursos --file recursos.json --jsonArray

### Verificar los registros importados:

- db.recursos.find().pretty();

## 👨‍💻 Autores
Nombre: Santiago Romero
Nombre: Rircardo Palomino 

GitHub: https://github.com/tu-usuario
