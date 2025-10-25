# ADR-016: Logs y Monitoreo

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Registrar eventos y errores para auditoría y mantenimiento.

## Decisión
Implementar logging con Winston y monitoreo con PM2 + Grafana + Loki.

## Consecuencias
- Detección temprana de fallas.
- Auditoría centralizada.
- Optimización de rendimiento.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Logs locales | Por módulo | Sencillo | Difícil trazabilidad | Descartada |
| Servicios externos | New Relic o Datadog | Completo | Costo elevado | Postergada |
| Centralizado | Winston + PM2 + Grafana | Auditado y eficiente | Requiere configuración inicial | Aceptada |

## Referencias
Winston Docs, Grafana Docs.

---