# ADR-018: Versionamiento y Estilo de Código

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Mantener consistencia en desarrollo y control de cambios.

## Decisión
Usar SemVer, ESLint, Prettier y Husky en CI.

## Consecuencias
- Código limpio.
- Control de versiones predecible.
- Previene errores comunes.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Manual | Sin reglas definidas | Flexible | Caos total | Descartada |
| Convención parcial | Solo linting | Ayuda básica | Inconsistente | Descartada |
| SemVer + ESLint | Versionado y linting automáticos | Orden y calidad | Requiere configuración | Aceptada |

## Referencias
semver.org, ESLint Docs.

---