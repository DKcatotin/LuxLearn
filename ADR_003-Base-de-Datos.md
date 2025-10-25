# ADR-003: Base de Datos Relacional – MySQL 8.0

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Se necesita una base de datos transaccional confiable para manejar estudiantes, calificaciones, pagos y asistencia.

## Decisión
Adoptar MySQL 8.0 por su estabilidad y soporte ACID.

## Consecuencias
- Gestión segura de datos educativos.
- Transacciones confiables.
- Compatibilidad con ORMs.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| MongoDB | NoSQL orientada a documentos | Flexible | No relacional | Descartada |
| PostgreSQL | Motor avanzado relacional | Robusto | Más complejo | Descartada |
| MySQL | Motor estándar relacional | Ligero y estable | Menos extensible | Aceptada |

## Referencias
MySQL 8.0 Documentation.

---
