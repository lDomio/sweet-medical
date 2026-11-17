# Sweet Medical — Medical Appointment Platform

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

> Group project for **Desarrollo de Software**, UTN FRBA, 2026.
> The repository is private. This case study documents the product, architecture and my contribution.

## Overview

Sweet Medical is a health insurance and appointment platform. Patients can search for appointments, compare coverage, book and manage their visits; doctors can manage their availability and profile.

## Features

- Patient and doctor roles.
- Appointment search with specialty, date and location filters.
- Coverage levels: total, partial and not covered.
- Appointment booking and cancellation.
- Doctor profiles, ratings and reviews.
- Notifications.
- Responsive layouts for mobile and desktop.
- Admin and deployment configuration.

## Architecture

```mermaid
flowchart LR
    WEB[React frontend] --> API[Express API]
    API --> DB[(MongoDB)]
    API --> AUTH[JWT auth]
    API --> VALID[Zod validation]
    API --> CRON[Scheduled jobs]
    WEB --> NETLIFY[Netlify]
    API --> RENDER[Render]
```

The project is a monorepo managed with npm workspaces:

- `packages/frontend` — React application.
- `packages/backend` — Express API with MongoDB, JWT, Zod, Swagger and schedulers.

## My role

I worked across the frontend and the deployment:

- Responsive home and appointment-search views.
- Role-based rendering for patients and doctors.
- Hamburger navigation and mobile layouts.
- Confirmation snackbars and notification UI.
- Dockerfiles and Docker Compose for the full stack.
- Deployment with Render and Netlify.
- Backend collaboration: Zod validation, MongoDB models and API integration.

## Stack

`React` · `Express` · `MongoDB` · `Mongoose` · `JWT` · `Zod` · `Swagger` · `Docker` · `Render` · `Netlify`

## Links

- [LinkedIn](https://www.linkedin.com/in/luca-domio-dev)
- [Portfolio](https://github.com/lDomio)
- Code available on request.
