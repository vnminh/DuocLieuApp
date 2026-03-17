# Duoc Lieu - Run With Docker

This repository includes:
- `duoc-lieu-be` (NestJS backend)
- `duoc-lieu-fe/duoc-lieu-fe` (Next.js frontend)
- PostgreSQL database

## Prerequisites

- Docker
- Docker Compose

## Run

From the repository root (`DuocLieu`), run:

```bash
docker compose up --build -d
```

This command will:
- start PostgreSQL
- build and run backend + frontend
- run backend migrations
- run seed scripts (including admin account seed)

## URLs

- Frontend: `http://localhost:8080`
- Backend: `http://localhost:3001`
- Database: `localhost:5432`

## Test Admin Account

On each backend start, the seed script ensures an admin account exists (idempotent upsert):

- Email: `admin@duoclieu.local`
- Password: `Admin@12345`

You can override these via `docker-compose.yml` environment variables:
- `ADMIN_EMAIL`
- `ADMIN_PASSWORD`
- `ADMIN_FULL_NAME`

## Stop

```bash
docker compose down
```

To stop and remove database data volume:

```bash
docker compose down -v
```
