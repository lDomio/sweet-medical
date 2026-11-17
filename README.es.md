# Sweet Medical — Plataforma de Turnos Médicos

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

[English](README.md) | [Español](README.es.md)

> Trabajo práctico grupal de **Desarrollo de Software**, UTN FRBA, 2026.
> Hecho con **5 compañeros**.

![Sweet Medical](packages/frontend/public/logo512.png)

## Descripción

Sweet Medical es una plataforma de obra social y turnos médicos. Los pacientes pueden buscar turnos, comparar coberturas, reservar y gestionar sus visitas; los médicos pueden administrar su disponibilidad, perfil y agenda.

## Features

- Roles de paciente y médico.
- Búsqueda de turnos por especialidad, fecha y ubicación.
- Niveles de cobertura: total, parcial y no cubierta.
- Reserva, cancelación e historial de turnos.
- Perfiles de médicos, ratings y reseñas.
- Notificaciones.
- UI responsive para mobile y desktop.
- Configuración de administración y despliegue.

## Arquitectura

```mermaid
flowchart LR
    WEB[Frontend React] --> API[API Express]
    API --> DB[(MongoDB)]
    API --> AUTH[JWT]
    API --> VALID[Validación Zod]
    API --> CRON[Jobs programados]
    WEB --> NETLIFY[Netlify]
    API --> RENDER[Render]
```

Monorepo con npm workspaces:

- `packages/frontend` — aplicación React.
- `packages/backend` — API Express con MongoDB, JWT, Zod, Swagger y schedulers.

## Mi rol

Trabajé en el frontend y en el despliegue:

- Vistas responsive de home y búsqueda de turnos.
- Renderizado condicional según rol (paciente/médico).
- Menú hamburguesa y layouts mobile.
- Snackbars de confirmación y UI de notificaciones.
- Dockerfiles y Docker Compose para todo el stack.
- Deploy con Render y Netlify.
- Colaboración en backend: validación Zod, modelos MongoDB e integración de API.

## Stack

`React` · `Express` · `MongoDB` · `Mongoose` · `JWT` · `Zod` · `Swagger` · `Docker` · `Render` · `Netlify` · `Jest` · `Cypress`

## Cómo levantarlo

```bash
npm install
cp packages/backend/.env.example packages/backend/.env
npm run start:dev
```

Variables principales en `packages/backend/.env`:

| Variable | Uso |
|---|---|
| `MONGODB_URI` | Conexión a MongoDB |
| `MONGODB_DB_NAME` | Nombre de la base |
| `JWT_SECRET` | Firma de tokens |
| `JWT_EXPIRATION` | Duración del token |
| `SERVER_PORT` | Puerto de la API |
| `ALLOWED_ORIGINS` | Orígenes CORS |

## Estructura

```text
├── packages/
│   ├── backend/     # API Express, dominio, repositorios y rutas
│   └── frontend/    # App React, features, componentes y clientes API
├── package.json
└── packages/docker-compose.yml
```

## Notas

- Código publicado con fines de portfolio.
- No hay credenciales en el repo; usar `.env.example`.
- Proyecto académico grupal.
