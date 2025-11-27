# ADR-002: Base de Datos Relacional (MySQL)

**Estado:** Aceptado  
**Fecha:** 2025-01-xx

## 1. Decisión
Adoptar **MySQL** como motor de base de datos principal, siguiendo un **modelo relacional normalizado**, orientado a garantizar consistencia y transacciones ACID.

## 2. Beneficio
- Consistencia fuerte para notas, pagos, historial y matrículas.  
- Integridad referencial clara.  
- Transacciones ACID.  
- Soporte maduro y estable.  
- Facilita auditoría y trazabilidad.

## 3. Trade-offs
- Menos flexible que NoSQL para datos semiestructurados.  
- Cambios de esquema requieren migraciones.  
- Escalamiento horizontal más complejo.

## 4. Alternativas Consideradas
- **MongoDB / DynamoDB (NoSQL):** descartados por no garantizar consistencia fuerte.  
- **PostgreSQL:** viable, pero MySQL resultó más simple para la infraestructura prevista.
