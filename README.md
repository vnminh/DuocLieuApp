# Duoc Lieu - Docker Quick Start

## Prerequisites

- Docker
- Docker Compose

## 1) Clone

Clone this repo with submodules:

```bash
git clone --recurse-submodules <YOUR_REPO_URL>
cd DuocLieu
```

If you already cloned without submodules:

```bash
git submodule update --init --recursive
```

## 2) Run Docker

From the repository root (`DuocLieu`):

```bash
docker compose up --build -d
```

## URLs

- Frontend: `http://localhost:8080`
- Backend: `http://localhost:3001`
- Database: `localhost:5432`

## Stop

```bash
docker compose down
```

Remove DB volume too:

```bash
docker compose down -v
```

## Bash Command Summary

```bash
# Clone project with submodules
git clone --recurse-submodules <YOUR_REPO_URL>
cd DuocLieu

# If cloned without submodules
git submodule update --init --recursive

# Start all services
docker compose up --build -d

# Check running services
docker compose ps

# Stop services
docker compose down

# Stop and remove DB volume
docker compose down -v
```
