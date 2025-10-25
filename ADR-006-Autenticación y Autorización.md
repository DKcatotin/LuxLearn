# ADR-006: Autenticación y Autorización – JWT

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
El sistema necesita controlar accesos según roles.

## Decisión
Usar JWT para autenticación basada en tokens con middleware de control de roles.

## Consecuencias
- Autenticación segura y sin estado.
- Escalable en frontend/backend.
- Facilita integración móvil.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Session-based | Sesiones en servidor | Compatibilidad clásica | No escalable | Descartada |
| OAuth2 | Protocolo de terceros | Estándar seguro | Más complejo | Postergada |
| JWT | JSON Web Tokens | Ligero y portable | Requiere expiración controlada | Aceptada |

## Referencias
RFC 7519 JSON Web Token Specification.

---