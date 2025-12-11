# Sistema de Gestión Universitaria

Sistema web para la gestión de estudiantes, profesores y asignaturas de la Fundación Universitaria Los Libertadores.

## 🚀 Características

- **Gestión de Estudiantes**: Registro, consulta, actualización y eliminación de estudiantes
- **Gestión de Profesores**: Administración completa de la información de profesores
- **Gestión de Asignaturas**: Control de materias y créditos académicos
- **Inscripciones**: Registro de estudiantes en asignaturas con seguimiento de notas (N1, N2, N3)
- **Horarios**: Asignación de horarios para profesores y materias (tabla Imparte)

## 🛠️ Tecnologías

### Backend
- **Node.js** con Express
- **TypeScript**
- **PostgreSQL** como base de datos
- **Joi** para validación de datos
- Arquitectura en capas (Controllers, Services, Repositories)

### Frontend
- HTML5, CSS3, JavaScript
- Diseño responsive

## 📋 Requisitos Previos

- Node.js (v14 o superior)
- PostgreSQL (v12 o superior)
- npm o yarn

## ⚙️ Instalación

### 1. Clonar el repositorio
```bash
git clone <url-del-repositorio>
cd proyecto-universidad
```

### 2. Configurar Backend
```bash
cd Back-end
npm install
```

### 3. Configurar Base de Datos
Crear una base de datos PostgreSQL llamada `universidad` y actualizar el archivo `.env`:

```env
PORT=3000
DB_USER=postgres
DB_PASSWORD=tu_contraseña
DB_HOST=localhost
DB_NAME=universidad
DB_PORT=5432
```

### 4. Compilar y ejecutar
```bash
npm run build
npm start
```

Para desarrollo:
```bash
npm run dev
```

## 📁 Estructura del Proyecto

```
Back-end/
├── src/
│   ├── controllers/      # Lógica de controladores
│   ├── services/         # Lógica de negocio
│   ├── repositories/     # Acceso a datos
│   ├── interfaces/       # Definiciones TypeScript
│   ├── middleware/       # Validaciones y utilidades
│   └── routers/          # Rutas de la API
├── index.ts              # Punto de entrada
└── .env                  # Variables de entorno

Front-end/
├── HTML/                 # Páginas HTML
├── Scripts/              # JavaScript
├── Styles/               # CSS
└── img/                  # Imágenes
```

## 🔌 API Endpoints

### Estudiantes
- `GET /api/estudiante` - Listar todos
- `GET /api/estudiante/:id` - Obtener por ID
- `POST /api/estudiante` - Crear nuevo
- `PUT /api/estudiante/:id` - Actualizar
- `DELETE /api/estudiante/:id` - Eliminar

### Profesores
- `GET /api/profesor` - Listar todos
- `GET /api/profesor/:id` - Obtener por ID
- `POST /api/profesor` - Crear nuevo
- `PUT /api/profesor/:id` - Actualizar
- `DELETE /api/profesor/:id` - Eliminar

### Asignaturas
- `GET /api/asignatura` - Listar todas
- `GET /api/asignatura/:id` - Obtener por ID
- `POST /api/asignatura` - Crear nueva
- `PUT /api/asignatura/:id` - Actualizar
- `DELETE /api/asignatura/:id` - Eliminar

### Inscripciones
- `GET /api/estudiante/inscribe` - Listar inscripciones
- `GET /api/estudiante/inscribe/:id` - Obtener por estudiante
- `POST /api/estudiante/inscribe` - Crear inscripción
- `PUT /api/estudiante/inscribe/:id` - Actualizar notas

### Horarios (Imparte)
- `GET /api/profesor/imparte` - Listar horarios
- `GET /api/profesor/imparte/:id` - Obtener por profesor
- `POST /api/profesor/imparte` - Crear horario
- `PUT /api/profesor/imparte/:id` - Actualizar
- `DELETE /api/profesor/imparte/:id` - Eliminar

## 📊 Modelo de Datos

### Estudiantes
- `cod_e`: Código (PK, generado automáticamente)
- `nom_e`: Nombre
- `dir_e`: Dirección
- `tel_e`: Teléfono
- `fech_nac`: Fecha de nacimiento

### Profesores
- `cod_p`: Código (PK, generado automáticamente)
- `nom_p`: Nombre
- `dir_p`: Dirección
- `tel_p`: Teléfono
- `profecion`: Profesión
- `fech_nac`: Fecha de nacimiento

### Asignaturas
- `cod_a`: Código (PK, auto-incremental)
- `nom_a`: Nombre
- `int_h`: Intensidad horaria
- `creditos`: Créditos académicos

## 🔒 Validaciones

El sistema implementa validaciones con Joi para:
- Formato de fechas (ISO)
- Formato de horas (HH:mm:ss)
- Campos requeridos
- Tipos de datos correctos

## 👥 Autores

Fundación Universitaria Los Libertadores

## 📄 Licencia

ISC
