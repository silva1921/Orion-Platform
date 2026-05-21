# ADR 001 - Selección Stack Tecnológico

## Estado

Aceptado

---

# Contexto

Se requiere construir una plataforma moderna orientada a:

- aprendizaje DevOps real,
- despliegues modernos,
- observabilidad,
- automatización,
- seguridad,
- CI/CD.

---

# Decisión

Se utilizará el siguiente stack:

## Frontend

- Next.js
- TypeScript
- TailwindCSS

## Backend

- Python
- FastAPI

## Base de Datos

- PostgreSQL

## Cache

- Redis

## Infraestructura

- Docker
- Docker Compose
- NGINX
- Ubuntu Server

## Observabilidad

- Grafana
- Prometheus
- Loki

---

# Razones

## FastAPI

- Alto rendimiento
- Soporte async
- Excelente documentación
- Ideal para APIs modernas

## Next.js

- SSR moderno
- Excelente ecosistema
- Arquitectura escalable

## PostgreSQL

- Robusto
- Confiable
- Estándar industria

## Docker

- Reproducibilidad
- Portabilidad
- Facilita CI/CD

---

# Consecuencias

## Positivas

- Arquitectura moderna
- Escalable
- Fácil despliegue
- Lista para Kubernetes

## Negativas

- Mayor complejidad inicial
- Curva aprendizaje operacional
