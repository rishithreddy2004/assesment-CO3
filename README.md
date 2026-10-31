# Intelligent Aviation Maintenance Management Platform
Educational full-stack demonstration. NOT a certified aircraft maintenance or airworthiness system.

## Requirements
Docker Desktop with Docker Compose, Git. No local Node or MySQL installation needed.

## Start
1. Copy `.env.example` to `.env` and change both passwords (must be set before first DB initialization).
2. Run `docker compose up --build -d` in the project folder.
3. Open http://localhost:8080
4. Verify `docker compose ps` and `docker compose logs --tail=50`.
5. Check API through browser at http://localhost:8080/api/health
6. Stop with `docker compose down` (preserves database); `docker compose down -v` deletes all saved data.

## Demo workflow
Add aircraft → create maintenance task → record inspection → view due/overdue alerts → change task status.

## API
GET /api/health, GET/POST /api/aircraft, GET/POST /api/tasks, PATCH /api/tasks/:id, GET/POST /api/inspections, GET /api/alerts.

## Security limitations
This is a local teaching prototype. It has no authentication, authorization, encryption-at-rest, regulatory signoff, immutable audit log, or validated predictive maintenance. Do not expose it to the internet or use it for real aviation operations. Use TLS, secrets management, RBAC, audit trails, validation and regulatory assessment before production use.
