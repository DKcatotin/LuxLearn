# ADR-012: CI/CD – Despliegue Automatizado

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
El sistema necesita despliegues rápidos y controlados.

## Decisión
Usar GitHub Actions con integración a Docker.

## Consecuencias
- Automatiza entregas.
- Evita errores manuales.
- Mejora consistencia de entornos.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Manual | Despliegues a mano | Sin dependencias externas | Propenso a fallos | Descartada |
| Jenkins | Pipeline clásico | Flexible | Difícil mantenimiento | Descartada |
| GitHub Actions | Flujos YAML nativos | Integrado y ágil | Depende de GitHub | Aceptada |

## Referencias
GitHub Actions Docs, Docker Compose Docs.

---
