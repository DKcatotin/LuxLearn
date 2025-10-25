# ADR-015: Seguridad y Privacidad de Datos

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Proteger la información sensible de los usuarios.

## Decisión
Aplicar cifrado, control de acceso y políticas GDPR/LOPD locales.

## Consecuencias
- Cumplimiento legal.
- Mayor confianza del usuario.
- Reducción de riesgos.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Seguridad básica | Protección mínima | Fácil implementación | Riesgo alto | Descartada |
| Anonimización total | Eliminación de trazabilidad | Privacidad completa | Sin trazabilidad | Descartada |
| Seguridad avanzada | Cifrado AES, JWT, roles | Confiable y normativo | Más mantenimiento | Aceptada |

## Referencias
GDPR 2016/679, OWASP ASVS.

---