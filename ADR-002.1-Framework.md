# ADR-002: Framework Backend – Node.js + Express

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Se requiere un entorno ligero y eficiente para la API REST del sistema educativo LuxLearn.

## Decisión
Seleccionar Node.js con Express por su rendimiento no bloqueante y amplio ecosistema.

## Consecuencias
- Desarrollo ágil de servicios REST.
- Fácil integración con librerías modernas.
- Mayor compatibilidad multiplataforma.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Spring Boot | Framework Java empresarial | Robusto | Pesado | Descartada |
| Django | Framework Python de alto nivel | Rápido | Menor eficiencia en concurrencia | Descartada |
| Node.js + Express | Entorno ligero y flexible | Eficiente y popular | Menor estructura inicial | Aceptada |

## Referencias
Node.js 20 LTS Docs, Express.js 5.x Docs.

---