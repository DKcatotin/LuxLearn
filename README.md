# 🎓 LuxLearn - Plataforma Educativa Digital Integral

[![Node.js](https://img.shields.io/badge/Node.js-v18.x-green.svg)](https://nodejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-blue.svg)](https://www.mysql.com/)
[![Docker](https://img.shields.io/badge/Docker-24.x-blue.svg)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**LuxLearn** es una plataforma educativa digital integral diseñada para centralizar, automatizar y optimizar los procesos académicos, administrativos y comunicacionales de instituciones educativas privadas.

---

## 📑 Tabla de Contenidos

- [Características Principales](#-características-principales)
- [Arquitectura del Sistema](#-arquitectura-del-sistema)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Requisitos Previos](#-requisitos-previos)
- [Instalación y Configuración](#-instalación-y-configuración)
- [Ejecución Local](#-ejecución-local)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [API Endpoints](#-api-endpoints)
- [Testing](#-testing)
- [Despliegue](#-despliegue)
- [Documentación Técnica](#-documentación-técnica)
- [Contribución](#-contribución)
- [Equipo de Desarrollo](#-equipo-de-desarrollo)
- [Licencia](#-licencia)

---

## ✨ Características Principales

### Gestión Académica
- ✅ Registro y consulta de calificaciones
- ✅ Control de asistencia en tiempo real
- ✅ Gestión de actividades y tareas
- ✅ Historial académico completo del estudiante

### Gestión Administrativa
- ✅ Proceso de matrículas automatizado
- ✅ Asignación de cursos y docentes
- ✅ Gestión de usuarios y roles (RBAC)
- ✅ Control de estructuras académicas

### Sistema de Pagos
- ✅ Generación de órdenes de pago
- ✅ Integración con pasarela de pagos
- ✅ Registro de transacciones
- ✅ Alertas de pagos pendientes

### Comunicación Institucional
- ✅ Mensajería interna
- ✅ Notificaciones automáticas (Email/SMS)
- ✅ Alertas académicas y administrativas
- ✅ Comunicados generales

### Analítica y Reportes
- ✅ Dashboards interactivos
- ✅ Reportes académicos personalizados
- ✅ Reportes financieros
- ✅ KPIs educativos

### Gestión de Archivos
- ✅ Almacenamiento en la nube
- ✅ Certificados digitales
- ✅ Boletines de calificaciones
- ✅ Documentación académica

---

## 🏗️ Arquitectura del Sistema

LuxLearn está construido siguiendo principios de **Domain-Driven Design (DDD)** y el **Modelo C4**, con una arquitectura **Cloud-Native Híbrida** que combina:

- **Contenedores (CaaS)**: Para la API principal y servicios core
- **Funciones Serverless (FaaS)**: Para tareas event-driven (notificaciones, webhooks)
- **Base de Datos Relacional**: MySQL 8.0 para garantizar integridad ACID

### Bounded Contexts (DDD)
```
┌─────────────────────────────────────────────────────────────┐
│                        LuxLearn                              │
├─────────────────────────────────────────────────────────────┤
│  📚 Gestión Académica    │  🏢 Gestión Administrativa        │
│  💰 Pagos                │  📢 Comunicación Institucional    │
│  📊 Analítica & Reportes │  📁 Gestión de Archivos           │
│  🔌 Integraciones Externas                                   │
└─────────────────────────────────────────────────────────────┘
```

Para más detalles, consulta el [Documento de Diseño de Arquitectura (DDA)](docs/DDA_LuxLearn.pdf).

---

## 🛠️ Tecnologías Utilizadas

### Backend
- **Runtime**: Node.js 18.x
- **Framework**: Express.js 4.x
- **Base de Datos**: MySQL 8.0
- **ORM**: Sequelize / TypeORM
- **Autenticación**: JWT (JSON Web Tokens)
- **Validación**: Joi / Express-validator

### Frontend
- **Framework**: React 18.x / Next.js 14.x
- **Estado Global**: Redux Toolkit / Zustand
- **UI Components**: Tailwind CSS + shadcn/ui
- **HTTP Client**: Axios

### DevOps & Cloud
- **Contenedores**: Docker + Docker Compose
- **Orquestación**: Kubernetes (producción)
- **CI/CD**: GitHub Actions / GitLab CI
- **IaC**: Terraform
- **Cloud Provider**: AWS / Google Cloud Platform
- **Almacenamiento**: AWS S3 / Google Cloud Storage

### Monitoreo y Observabilidad
- **Logs**: Winston / Pino
- **Métricas**: Prometheus + Grafana
- **Tracing**: OpenTelemetry (opcional)

---

## 📋 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- **Node.js** v18.x o superior ([Descargar](https://nodejs.org/))
- **npm** v9.x o **yarn** v1.22.x
- **Docker** v24.x y Docker Compose v2.x ([Descargar](https://www.docker.com/))
- **MySQL** 8.0 (o usar Docker)
- **Git** ([Descargar](https://git-scm.com/))

### Verificar instalación:
```bash
node --version  # v18.x o superior
npm --version   # v9.x o superior
docker --version # v24.x o superior
docker-compose --version # v2.x o superior
```

---

## 🚀 Instalación y Configuración

### 1. Clonar el repositorio
```bash
git clone https://github.com/tu-organizacion/luxlearn.git
cd luxlearn
```

### 2. Instalar dependencias

#### Backend
```bash
cd backend
npm install
```

#### Frontend
```bash
cd ../frontend
npm install
```

### 3. Configurar variables de entorno

Crea un archivo `.env` en la carpeta `backend/` basado en `.env.example`:
```bash
cd backend
cp .env.example .env
```

Edita el archivo `.env` con tus configuraciones:
```env
# Configuración de la aplicación
NODE_ENV=development
PORT=3000
API_VERSION=v1

# Base de datos MySQL
DB_HOST=localhost
DB_PORT=3306
DB_NAME=luxlearn_db
DB_USER=root
DB_PASSWORD=tu_password_seguro

# JWT
JWT_SECRET=tu_secret_key_muy_segura_aqui
JWT_EXPIRES_IN=24h
JWT_REFRESH_SECRET=tu_refresh_secret_key
JWT_REFRESH_EXPIRES_IN=7d

# CORS
ALLOWED_ORIGINS=http://localhost:3001,http://localhost:3000

# Email (SMTP)
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=tu_email@gmail.com
SMTP_PASSWORD=tu_password_aplicacion

# Almacenamiento en la nube (AWS S3)
AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=tu_access_key
AWS_SECRET_ACCESS_KEY=tu_secret_key
AWS_S3_BUCKET=luxlearn-files

# Pasarela de pagos (Ejemplo: Stripe)
STRIPE_SECRET_KEY=sk_test_xxxxxxxxxxxxx
STRIPE_WEBHOOK_SECRET=whsec_xxxxxxxxxxxxx

# Logs
LOG_LEVEL=debug
```

### 4. Configurar Base de Datos

#### Opción A: Usando Docker (Recomendado)
```bash
cd backend
docker-compose up -d mysql
```

#### Opción B: MySQL Local

1. Crear base de datos:
```sql
CREATE DATABASE luxlearn_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

2. Ejecutar migraciones:
```bash
npm run migrate
```

3. Poblar datos de prueba (opcional):
```bash
npm run seed
```

---

## 🎮 Ejecución Local

### Opción 1: Ejecución con Docker Compose (Recomendado)

Ejecuta toda la aplicación (backend + frontend + MySQL) con un solo comando:
```bash
docker-compose up
```

Accede a:
- **Backend API**: http://localhost:3000
- **Frontend**: http://localhost:3001
- **Documentación API**: http://localhost:3000/api-docs

### Opción 2: Ejecución Manual

#### 1. Iniciar Backend
```bash
cd backend
npm run dev
```

La API estará disponible en: `http://localhost:3000`

#### 2. Iniciar Frontend (en otra terminal)
```bash
cd frontend
npm run dev
```

La aplicación web estará disponible en: `http://localhost:3001`

### Usuarios de Prueba

Una vez iniciada la aplicación, puedes usar estas credenciales:

| Rol           | Email                    | Password    |
|---------------|--------------------------|-------------|
| Administrador | admin@luxlearn.edu.ec    | Admin123!   |
| Docente       | docente@luxlearn.edu.ec  | Docente123! |
| Estudiante    | estudiante@luxlearn.edu.ec | Est123!   |
| Padre         | padre@luxlearn.edu.ec    | Padre123!   |

---

## 📁 Estructura del Proyecto
```
luxlearn/
├── backend/                    # API REST - Node.js + Express
│   ├── src/
│   │   ├── config/            # Configuraciones (DB, JWT, etc.)
│   │   ├── modules/           # Bounded Contexts (DDD)
│   │   │   ├── academico/     # Gestión Académica
│   │   │   ├── administrativo/ # Gestión Administrativa
│   │   │   ├── pagos/         # Sistema de Pagos
│   │   │   ├── comunicacion/  # Comunicación Institucional
│   │   │   ├── analytics/     # Analítica y Reportes
│   │   │   ├── archivos/      # Gestión de Archivos
│   │   │   └── auth/          # Autenticación y Autorización
│   │   ├── shared/            # Código compartido
│   │   │   ├── middleware/    # Middlewares (auth, validation, etc.)
│   │   │   ├── utils/         # Utilidades
│   │   │   └── errors/        # Manejo de errores
│   │   ├── database/          # Modelos y migraciones
│   │   │   ├── models/        # Modelos Sequelize/TypeORM
│   │   │   ├── migrations/    # Migraciones de BD
│   │   │   └── seeders/       # Datos de prueba
│   │   └── app.js             # Configuración Express
│   ├── tests/                 # Tests unitarios y de integración
│   ├── docker-compose.yml     # Orquestación de servicios
│   ├── Dockerfile             # Imagen Docker del backend
│   ├── package.json
│   └── .env.example
│
├── frontend/                  # Aplicación Web - React/Next.js
│   ├── src/
│   │   ├── components/        # Componentes reutilizables
│   │   ├── pages/             # Páginas de la aplicación
│   │   ├── layouts/           # Layouts
│   │   ├── services/          # Servicios API (Axios)
│   │   ├── store/             # Estado global (Redux/Zustand)
│   │   ├── hooks/             # Custom hooks
│   │   ├── utils/             # Utilidades
│   │   └── styles/            # Estilos globales
│   ├── public/                # Recursos estáticos
│   ├── Dockerfile
│   ├── package.json
│   └── .env.example
│
├── docs/                      # Documentación técnica
│   ├── DDA_LuxLearn.pdf       # Documento de Diseño de Arquitectura
│   ├── API_Documentation.md   # Documentación de APIs
│   ├── C4_Diagrams/           # Diagramas arquitectónicos
│   └── ADRs/                  # Registros de Decisiones (ADRs)
│
├── infrastructure/            # IaC - Terraform
│   ├── terraform/
│   │   ├── modules/
│   │   └── environments/
│   └── kubernetes/            # Manifiestos K8s
│
├── .github/                   # GitHub Actions CI/CD
│   └── workflows/
│       ├── backend-ci.yml
│       └── frontend-ci.yml
│
├── docker-compose.yml         # Orquestación completa
├── README.md                  # Este archivo
└── LICENSE
```

---

## 🔌 API Endpoints

### Autenticación
```http
POST   /api/v1/auth/login            # Iniciar sesión
POST   /api/v1/auth/register          # Registrar usuario
POST   /api/v1/auth/refresh-token     # Refrescar token
POST   /api/v1/auth/logout            # Cerrar sesión
```

### Gestión Académica
```http
GET    /api/v1/academico/notas                    # Listar calificaciones
POST   /api/v1/academico/notas                    # Registrar calificación
GET    /api/v1/academico/notas/{id}               # Obtener calificación
PUT    /api/v1/academico/notas/{id}               # Actualizar calificación
DELETE /api/v1/academico/notas/{id}               # Eliminar calificación
GET    /api/v1/academico/historial/{estudiante_id} # Historial académico
POST   /api/v1/academico/asistencias              # Registrar asistencia
```

### Gestión Administrativa
```http
GET    /api/v1/admin/cursos                # Listar cursos
POST   /api/v1/admin/cursos                # Crear curso
GET    /api/v1/admin/matriculas            # Listar matrículas
POST   /api/v1/admin/matriculas            # Crear matrícula
PATCH  /api/v1/admin/matriculas/{id}       # Actualizar matrícula
DELETE /api/v1/admin/matriculas/{id}       # Eliminar matrícula
```

### Pagos
```http
POST   /api/v1/pagos/orden                 # Generar orden de pago
POST   /api/v1/pagos/procesar               # Procesar pago
GET    /api/v1/pagos/transacciones         # Listar transacciones
POST   /api/v1/pagos/webhook                # Webhook pasarela
```

### Comunicación
```http
GET    /api/v1/comunicacion/mensajes       # Listar mensajes
POST   /api/v1/comunicacion/mensajes       # Enviar mensaje
POST   /api/v1/comunicacion/notificar      # Enviar notificación
GET    /api/v1/comunicacion/alertas        # Listar alertas
```

### Analítica
```http
GET    /api/v1/analytics/academico         # Reporte académico
GET    /api/v1/analytics/pagos             # Reporte financiero
GET    /api/v1/analytics/asistencia        # Reporte de asistencia
GET    /api/v1/analytics/dashboard         # Dashboard general
```

### Archivos
```http
POST   /api/v1/archivos/subir              # Subir archivo
GET    /api/v1/archivos/{id}               # Descargar archivo
DELETE /api/v1/archivos/{id}               # Eliminar archivo
```

📖 **Documentación completa de la API**: [Swagger/OpenAPI](docs/API_Documentation.md) o accede a `/api-docs` cuando el servidor esté corriendo.

---

## 🧪 Testing

### Ejecutar todos los tests
```bash
cd backend
npm test
```

### Tests por módulo
```bash
npm test -- --grep "Gestión Académica"
npm test -- --grep "Autenticación"
```

### Coverage
```bash
npm run test:coverage
```

Los reportes de coverage se generan en `backend/coverage/`.

### Tests E2E (End-to-End)
```bash
npm run test:e2e
```

---

## 🚢 Despliegue

### Despliegue con Docker

#### 1. Construir imágenes
```bash
docker-compose build
```

#### 2. Ejecutar en producción
```bash
docker-compose -f docker-compose.prod.yml up -d
```

### Despliegue en la Nube (AWS/GCP)

Consulta la guía completa en: [docs/deployment-guide.md](docs/deployment-guide.md)

#### Requisitos:
1. Cuenta en AWS/GCP
2. Terraform instalado
3. Configurar credenciales cloud

#### Pasos:
```bash
cd infrastructure/terraform
terraform init
terraform plan
terraform apply
```

### CI/CD

El proyecto incluye pipelines de CI/CD configurados en GitHub Actions:

- **Backend CI**: Tests automáticos, linting, build
- **Frontend CI**: Tests, build, deployment
- **Deploy**: Despliegue automático a staging/producción

---

## 📚 Documentación Técnica

- 📄 [Documento de Diseño de Arquitectura (DDA)](docs/DDA_LuxLearn.pdf)
- 🔌 [Documentación de APIs (OpenAPI)](docs/API_Documentation.md)
- 🏗️ [Diagramas C4](docs/C4_Diagrams/)
- 📝 [ADRs - Decisiones de Arquitectura](docs/ADRs/)
- 🗄️ [Modelo de Base de Datos](docs/database-schema.md)
- 🔐 [Guía de Seguridad](docs/security-guide.md)

---

## 🤝 Contribución

¡Las contribuciones son bienvenidas! Por favor, sigue estos pasos:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add: Amazing Feature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Convenciones de commits

Seguimos [Conventional Commits](https://www.conventionalcommits.org/):
```
feat: Nueva funcionalidad
fix: Corrección de bug
docs: Cambios en documentación
style: Formateo de código
refactor: Refactorización
test: Agregar tests
chore: Tareas de mantenimiento
```

---

## 👥 Equipo de Desarrollo

### Instituto Superior Tecnológico de Turismo y Patrimonio Yavirac
**Carrera**: Desarrollo de Software

**Integrantes**:
- **Edison Flores** - Backend Developer & DevOps
- **Jeremy Catota** - Frontend Developer & UX/UI
- **Alejandro Maldonado** - Full Stack Developer & Database Architect

**Docente**:
- **Ing. Diego Alexander Yánez Flores** - Advisor

**Contacto**: [luxlearn@yavirac.edu.ec](mailto:luxlearn@yavirac.edu.ec)

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo [LICENSE](LICENSE) para más detalles.

---

## 🙏 Agradecimientos

- Instituto Yavirac por el apoyo académico
- Comunidad de código abierto
- Instituciones educativas que colaboraron en la validación

---

## 📞 Soporte

Si tienes preguntas o encuentras algún problema:

1. 🐛 [Reporta un bug](https://github.com/tu-organizacion/luxlearn/issues)
2. 💡 [Solicita una funcionalidad](https://github.com/tu-organizacion/luxlearn/issues/new?template=feature_request.md)
3. 📧 Contacto: dad.maldonado@yavirac.edu.ec
                 ela.flores@yavirac.edu.ec
                jda.catota@yavirac.edu.ec

---

