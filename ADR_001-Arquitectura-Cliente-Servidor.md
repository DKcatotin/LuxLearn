# ADR-001: Arquitectura Cliente-Servidor con Capas Múltiples

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
El sistema LuxLearn requiere una arquitectura escalable y segura que permita manejar módulos académicos, administrativos y de comunicación sin comprometer la mantenibilidad.

## Decisión
Adoptar un estilo cliente-servidor con arquitectura en capas (presentación, lógica de negocio, datos e integración). Cada capa podrá evolucionar de manera independiente, garantizando extensibilidad y seguridad.

## Consecuencias
- Bajo acoplamiento entre componentes.
- Facilidad para actualizar o reemplazar servicios sin impacto global.
- Base sólida para migrar hacia microservicios en el futuro.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Monolítica | Todo en un único bloque de código | Simplicidad inicial | Escalabilidad baja y mantenimiento complejo | Descartada |
| Microservicios | Separación total por dominios | Alta escalabilidad y resiliencia | Complejidad y sobrecosto de infraestructura | Descartada |
| Cliente-Servidor en Capas | Separación clara por responsabilidades | Mantenible, segura y escalable progresivamente | Requiere definir contratos de capa | Aceptada |

## Referencias
Modelo C4 – Simon Brown; OWASP Architecture Cheat Sheet.

---
