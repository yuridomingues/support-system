# Support System

Full-stack support ticket management system built with FastAPI, React and PostgreSQL.

This repository consolidates the original backend and frontend projects into a single monorepo while preserving their Git history.

## What it does

- JWT authentication and protected routes
- client management
- support ticket CRUD linked to clients
- PostgreSQL persistence with SQLAlchemy and Alembic
- React interface with routing and error handling
- automated backend tests
- Docker-based local development

## Architecture

```text
React / Vite
     ↓
   Axios
     ↓
FastAPI
     ↓
SQLAlchemy / Alembic
     ↓
PostgreSQL
```

## Repository structure

```text
backend/    FastAPI API, tests and database configuration
frontend/   React / Vite interface
```

## Run locally

Backend:

```bash
cd backend
uv sync
make up
```

Frontend:

```bash
cd frontend
npm install
npm run dev
```

The frontend runs on `http://localhost:5173` and the API on `http://localhost:8000` in the default local setup.

## Engineering notes

The backend uses JWT authentication, migrations and isolated tests. Secrets must be supplied through environment configuration and should never be committed.

This repository replaces the former `support-system-api` and `support-system-interface` repositories as the canonical project.
