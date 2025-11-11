# 🎬 Nuestro Netflix - Aplicación de Gestión de Películas

Una aplicación web completa para gestionar una base de datos de películas, desarrollada con HTML, CSS y JavaScript siguiendo el patrón de diseño MVC (Modelo-Vista-Controlador).

## 📋 Descripción

Esta aplicación permite a los usuarios:
- ✅ **Listar** todas las películas almacenadas
- 👁️ **Ver** información detallada de cada película
- ➕ **Añadir** nuevas películas
- ✏️ **Editar** películas existentes
- 🗑️ **Eliminar** películas (con confirmación)
- 🔄 **Resetear** la base de datos al estado inicial

Los datos se almacenan en el navegador usando `localStorage`, por lo que persisten entre sesiones.

## 🚀 Cómo Usar

1. Abre el archivo `index.html` en tu navegador web (Chrome, Firefox, Edge, etc.)
2. La aplicación se cargará automáticamente con un conjunto de películas predeterminadas
3. Usa los botones para interactuar con las películas

## 🏗️ Arquitectura - Patrón MVC

### Modelo (Model)
El modelo gestiona los datos de las películas:
- Array de películas almacenado en `localStorage`
- Cada película tiene: `titulo`, `director`, `miniatura`
- Funciones CRUD: crear, leer, actualizar, eliminar

### Vista (View)
Generan el HTML dinámico para la interfaz:
- **indexView**: Vista principal con la lista de películas
- **showView**: Vista de detalle de una película
- **editView**: Formulario para editar una película
- **newView**: Formulario para crear una nueva película

### Controlador (Controller)
Gestionan la lógica de la aplicación:
- **indexContr**: Muestra la lista de películas
- **showContr**: Muestra detalles de una película
- **editContr**: Prepara la edición de una película
- **updateContr**: Guarda los cambios de una película
- **newContr**: Muestra el formulario de nueva película
- **createContr**: Crea una nueva película
- **deleteContr**: Elimina una película
- **resetContr**: Restaura la base de datos

### Router
- Asocia eventos de clic con controladores
- Implementado mediante delegación de eventos

## 🎨 Características

- **Interfaz moderna y atractiva** con gradientes y animaciones
- **Responsive** - se adapta a diferentes tamaños de pantalla
- **Grid layout** para visualización de películas
- **Formularios intuitivos** para crear y editar
- **Confirmaciones** antes de acciones destructivas
- **Persistencia de datos** con localStorage
- **Emojis** para mejor experiencia visual

## 📂 Estructura del Proyecto

```
Nuestro_Netflix/
├── index.html          # Archivo principal con HTML, CSS y JavaScript
├── files/              # Directorio para imágenes locales
│   └── README.md       # Información sobre uso de imágenes
└── README.md           # Este archivo
```

## 💾 Almacenamiento de Datos

Los datos se almacenan en `localStorage` bajo la clave `mis_peliculas`. La estructura de cada película es:

```javascript
{
  titulo: "Título de la película",
  director: "Nombre del director",
  miniatura: "URL de la imagen"
}
```

## 🔧 Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos con Flexbox y Grid
- **JavaScript ES6**: Lógica de la aplicación
- **localStorage**: Persistencia de datos en el navegador

## 📖 Funcionalidades Implementadas

### 1. Show (Ver)
- Botón "👁️ Ver" en cada película
- Muestra título, director e imagen
- Botón "Volver" para regresar a la lista

### 2. New (Nueva)
- Botón "➕ Añadir Película" en la vista principal
- Formulario con campos: título, director, URL miniatura
- Validación de campos requeridos

### 3. Create (Crear)
- Botón "Crear" en el formulario de nueva película
- Añade la película al array y localStorage
- Regresa automáticamente a la vista principal

### 4. Delete (Eliminar)
- Botón "🗑️ Borrar" en cada película
- Solicita confirmación antes de eliminar
- Actualiza la vista automáticamente

### 5. Reset (Resetear)
- Botón "🔄 Reset" en la vista principal
- Restaura las películas iniciales
- Solicita confirmación antes de proceder

### 6. Edit (Editar) - Previamente Implementado
- Botón "✏️ Editar" en cada película
- Formulario pre-llenado con datos actuales
- Botón "Actualizar" para guardar cambios

### 7. List (Listar) - Previamente Implementado
- Vista principal con todas las películas
- Grid responsive con miniaturas
- Botones de acción para cada película

## 🎓 Propósito Educativo

Esta aplicación fue desarrollada como práctica educativa para:
- Aprender el patrón MVC en aplicaciones web
- Comprender la manipulación del DOM con JavaScript
- Practicar el almacenamiento en localStorage
- Desarrollar interfaces de usuario interactivas
- Gestionar eventos y flujo de datos

## 🌐 Uso de Imágenes

La aplicación utiliza URLs de imágenes de ejemplo de Unsplash. Puedes:
- Usar las URLs proporcionadas
- Reemplazarlas con URLs propias
- Colocar imágenes en la carpeta `files/` y usar rutas relativas

## 📝 Notas

- La aplicación funciona completamente del lado del cliente
- No requiere servidor ni base de datos externa
- Los datos persisten solo en el navegador donde se ejecuta
- Limpiar el localStorage del navegador eliminará todos los datos

## 👨‍💻 Autor

Proyecto desarrollado como parte de una práctica de desarrollo web con tecnologías front-end.

## 📄 Licencia

Este proyecto es de código abierto y está disponible para uso educativo.