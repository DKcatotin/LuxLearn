# ADR-009: Integración con Sistemas Externos (Email, SMS, Pagos)

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
El sistema debe interoperar con servicios externos confiables.

## Decisión
Integrar SMTP, Twilio y Stripe mediante servicios dedicados en backend.

## Consecuencias
- Alta disponibilidad.
- Reducción de carga interna.
- Cumple estándares de seguridad.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Interna | Implementación propia | Control total | Lento y costoso | Descartada |
| Servicios no verificados | APIs genéricas | Bajo costo | Inseguras | Descartada |
| APIs confiables | SMTP, Twilio, Stripe | Confiables y escalables | Costo mensual | Aceptada |

## Referencias
Twilio API, SMTP RFC 5321, Stripe Developers.

---
