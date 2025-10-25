# ADR-010: Sistema de Notificaciones Multicanal

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Los usuarios deben recibir alertas por diferentes medios.

## Decisión
Diseñar servicio interno con canales (email, SMS, push, in-app).

## Consecuencias
- Comunicación inmediata.
- Mayor engagement de usuarios.
- Personalización por canal.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Solo email | Correo electrónico | Amplio alcance | Poca inmediatez | Descartada |
| Solo push | Notificación navegador | Instantánea | Dependiente del cliente | Descartada |
| Multicanal | Combinación flexible | Integral y escalable | Mayor implementación inicial | Aceptada |

## Referencias
Firebase Cloud Messaging, Twilio Docs.

---
