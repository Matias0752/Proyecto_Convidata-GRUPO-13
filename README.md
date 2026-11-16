# ConviData

Sistema web para el registro, seguimiento y análisis de casos de convivencia escolar. Permite administrar usuarios y alumnos, registrar y gestionar casos, visualizar estadísticas, generar alertas y notificaciones, y mantener la trazabilidad de los incidentes dentro del establecimiento educacional.

---

## Descripción del Proyecto

ConviData es un proyecto desarrollado en la asignatura de Ingeniería de Software para el Colegio Particular San Sebastián de Melipilla. Su objetivo es reemplazar el registro manual y descentralizado de incidencias por una plataforma web que centralice la información de convivencia escolar y apoye la toma de decisiones del equipo directivo.

El sistema trabaja con cuatro roles de usuario, cada uno con permisos específicos:

- Administrador
- Inspector
- Convivencia
- Profesor

---

## Objetivo General

Desarrollar una plataforma web que optimice la gestión, el seguimiento y el análisis de los casos de convivencia escolar, centralizando la información y facilitando el acceso según los privilegios definidos para cada rol de usuario.

---

## Alcance del Proyecto

| Elemento | Cantidad | Estado |
|---|---|---|
| Requerimientos funcionales | 77 | 100 % implementados |
| Requerimientos de usuario | 77 | 100 % implementados |
| Requerimientos no funcionales | 11 | Definidos |
| Casos de uso | 81 | 100 % implementados |

---

## Funcionalidades Implementadas

**Acceso y autenticación**
- Inicio de sesión con correo institucional
- Recuperación de contraseña mediante contraseña temporal enviada por correo
- Cambio obligatorio de contraseña en el primer ingreso
- Bloqueo de cuenta tras 5 intentos fallidos

**Inicio y navegación**
- Gráfico de casos por zona del colegio y panel de resumen de los últimos 30 días
- Listado de casos paginado y ordenado del más reciente al más antiguo
- Barra de tareas con acceso a los módulos según el rol

**Gestión de casos**
- Registro de casos con adjuntos y múltiples estudiantes involucrados
- Historial de casos con búsqueda, filtros y contador
- Edición dentro de 48 horas (sin límite para el Administrador)
- Eliminación de casos con confirmación
- Descarga de casos en PDF o XLSX
- Solicitudes de casos del Profesor con aprobación o rechazo

**Estadísticas**
- Gráficos de barras, líneas y torta
- Filtros por gravedad, curso, zona y rango de fechas
- Panel de resumen con variación respecto al año anterior
- Descarga de gráficos y datos

**Notificaciones y alertas**
- Aviso al creador cuando su caso es editado o eliminado
- Alerta automática cuando un curso supera los 10 casos semanales

**Administración**
- Gestión de usuarios: creación, edición, búsqueda, filtros y acciones masivas
- Historial de acciones de los usuarios
- Gestión de alumnos: registro, importación XLSX, edición y activación o desactivación
- Carga y visualización de documentos institucionales (Reglamento Interno y protocolos)

**Perfil**
- Visualización de datos públicos, configuración de la cuenta y cierre de sesión

---

## Desarrollo por Incrementos

| Incremento | Módulos | RF | % del proyecto | % acumulado |
|---|---|---|---|---|
| Incremento 1 | Acceso, inicio, barra de tareas, perfil, registro, descarga y detalle de casos | 25 | 32,47 % | 32,47 % |
| Incremento 2 | Historial, búsqueda, edición y eliminación de casos, gestión de usuarios y documentos institucionales | 30 | 38,96 % | 71,43 % |
| Incremento 3 | Notificaciones, alertas, estadísticas y gestión de alumnos | 20 | 25,97 % | 97,40 % |
| Incremento 4 | Solicitudes de casos del Profesor | 2 | 2,60 % | 100 % |

---

## Arquitectura del Sistema

El sistema se estructura en capas que separan la interfaz de usuario, la lógica de aplicación y la persistencia de datos, siguiendo el patrón MVC (Modelo Vista Controlador).

Componentes principales:

- Frontend web
- API REST
- Autenticación mediante JWT
- ORM para acceso a datos
- Base de datos relacional PostgreSQL
- Servicio de correos para notificaciones y contraseñas temporales

Documentación de arquitectura:

- Modelo de vistas 4+1
- Diagrama de componentes
- Diagrama de despliegue
- Modelo de datos (MER y MERE)
- Árbol de navegación

---

## Tecnologías

Backend:

- Python
- Django
- PostgreSQL
- JWT Authentication

Frontend:

- HTML
- CSS
- JavaScript

Infraestructura y servicios:

- Cloudflare Pages (alojamiento del frontend)
- Resend (envío de correos)

Herramientas:

- Draw.io
- Bizagi
- Git y GitHub
- Excel (Scrum++, backlog, carta Gantt y matriz de requerimientos)

---

## Estado del Proyecto

**Proyecto finalizado: 4 de 4 incrementos completados (100 % del alcance funcional).**

Entregables:

- Documento 0: diagnóstico de la organización, requerimientos y casos de uso
- Informes y presentaciones de los Incrementos 1 al 4
- Casos de uso y diagramas de casos de uso
- Diagramas de secuencia
- Diagramas de base de datos, componentes y despliegue
- Árbol de navegación
- Pruebas funcionales del sistema con evidencias
- Documentación Scrum++ (backlog, burnup y burndown)

---

## Estructura del Repositorio

```text
Proyecto_Convidata-GRUPO-13/
│
├── Documento 0/
│   ├── Carta gantt/
│   ├── Casos de uso/
│   ├── Confirmacion de los requerimientos/
│   ├── Diagrama de secuencia/
│   ├── Diagramas de casos de uso/
│   ├── Estimación Costo y Beneficio/
│   ├── Levantamiento de proceso/
│   ├── Matriz de Requerimientos/
│   └── Scrum++/
│
├── Incremento 1/
├── Incremento 2/
├── Incremento 3/
├── Incremento 4/
│   (cada incremento incluye informe, ppt, diagramas y Scrum++)
│
└── README.md
```

---

## Equipo de Desarrollo

- Max Fernández
- Matías Urria
- Isaías Ortiz
- Osvaldo Caraccioli
- Maximiliano Soto
- Benjamín Orellana

Profesor: Paulo Quinsacara

---

## Metodología de Trabajo

El proyecto se desarrolló bajo la metodología Scrum++, considerando:

- Product Backlog
- Sprint Planning
- Daily Scrum
- Sprint Review
- Sprint Retrospective
- Seguimiento mediante gráficos Burnup y Burndown

---

## Versionamiento

El control de versiones se gestiona mediante Git y GitHub, manteniendo la trazabilidad del trabajo realizado por cada integrante a través del historial de commits.

---

## Estado Académico

Proyecto desarrollado para la asignatura Ingeniería de Software – Año 2026.
