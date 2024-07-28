# 📚 TiendaLibrosApp

## 📖 Descripción
TiendaLibrosApp es una aplicación de escritorio desarrollada en Java utilizando Swing para la interfaz gráfica y Spring Boot para la lógica de negocio y acceso a datos. La aplicación permite gestionar un catálogo de libros, incluyendo agregar, listar, modificar y eliminar libros.

## 🌟 Características
- 📕 **Agregar Libro**: Añade un nuevo libro al catálogo proporcionando su nombre, autor, precio y existencias.
- 📑 **Listar Libros**: Muestra todos los libros en el catálogo.
- 📝 **Modificar Libro**: Permite modificar la información de un libro existente.
- 🗑️ **Eliminar Libro**: Elimina un libro del catálogo.
- 🚪 **Salir**: Opción para salir de la aplicación.

## 📝 Código Principal

### 📂 `lm.tienda_libros.modelo`

#### `Libro.java`
Define una clase `Libro` con los siguientes atributos y métodos:
- **Atributos**: `idLibro`, `nombreLibro`, `autor`, `precio`, `existencias`
- **Anotaciones**:
  - `@Entity`: Define la clase como una entidad JPA.
  - `@Id`, `@GeneratedValue`: Indican el identificador de la entidad y su estrategia de generación.
  - `@Data`, `@NoArgsConstructor`, `@AllArgsConstructor`, `@ToString`: Generan automáticamente los métodos getters, setters, constructores y el método `toString`.

### 📂 `lm.tienda_libros.repositorio`

#### `LibroRepositorio.java`
Define un repositorio JPA para la entidad `Libro`:
- **Métodos**:
  - Hereda los métodos CRUD de `JpaRepository<Libro, Integer>`.

### 📂 `lm.tienda_libros.servicio`

#### `ILibroServicio.java`
Define una interfaz para los servicios de gestión de libros:
- **Métodos**:
  - `listarLibros()`: Lista todos los libros.
  - `buscarLibroPorId(Integer idLibro)`: Busca un libro por su ID.
  - `guardarLibro(Libro libro)`: Guarda un libro.
  - `eliminarLibro(Libro libro)`: Elimina un libro.

#### `LibroServicio.java`
Implementa `ILibroServicio` para gestionar libros:
- **Atributos**:
  - `LibroRepositorio`: Inyección de dependencia para el repositorio de libros.
- **Métodos**:
  - Implementa los métodos definidos en `ILibroServicio`.

### 📂 `lm.tienda_libros.presentacion`

#### `LibroForm.java`
Define la interfaz gráfica utilizando Swing:
- **Componentes**:
  - `JPanel`, `JTable`, `JTextField`, `JButton`
- **Métodos**:
  - `agregarLibro()`: Agrega un nuevo libro.
  - `cargarLibroSeleccionado()`: Carga la información del libro seleccionado en la tabla.
  - `modificarLibro()`: Modifica la información de un libro.
  - `eliminarLibro()`: Elimina un libro.
  - `listarLibros()`: Lista todos los libros en la tabla.
  - `limpiarFormulario()`: Limpia el formulario.
  - `mostrarMensaje(String mensaje)`: Muestra un mensaje al usuario.

### 📂 `lm.tienda_libros`

#### `TiendaLibrosApplication.java`
Define la clase principal que inicia la aplicación Spring Boot y la interfaz gráfica:
- **Métodos**:
  - `main(String[] args)`: Inicia la aplicación Spring Boot y carga la interfaz gráfica.

## ⚙️ Requisitos
- Java 8 o superior
- Spring Boot 2.5 o superior
- IDE recomendado: IntelliJ IDEA o Eclipse

## 🚀 Ejecución
1. Clona el repositorio:
   ```bash
   git clone https://github.com/Martincho83/TiendaLibrosApp.git

2. Importa el proyecto en tu IDE preferido.
3. Ejecuta la clase `TiendaLibrosApplication` para iniciar la aplicación.
   
## 🤝 Contribuciones
Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y crea un pull request con tus cambios.

👨‍💻 Autor
Martín - Desarrollador Principal - [Martincho83](https://github.com/Martincho83)
