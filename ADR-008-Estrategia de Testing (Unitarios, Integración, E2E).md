# ADR-008: Estrategia de Testing (Unitarios, Integración, E2E)

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Garantizar calidad en los módulos del sistema educativo.

## Decisión
Implementar pruebas con Jest, Supertest y Cypress.

## Consecuencias
- Asegura estabilidad.
- Detecta fallos antes del despliegue.
- Mejora la confianza en releases.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Manual | Pruebas no automatizadas | Rápido inicio | Propenso a error humano | Descartada |
| Unitario solo | Cobertura básica | Menor tiempo | Cobertura limitada | Descartada |
| Multinivel | Unitario, integración, E2E | Completa y escalable | Más configuración inicial | Aceptada |

## Referencias
Jest Docs, Cypress Docs.

---