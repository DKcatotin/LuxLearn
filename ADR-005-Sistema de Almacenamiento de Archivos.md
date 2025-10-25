# ADR-005: Sistema de Almacenamiento de Archivos

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Se requiere almacenamiento seguro para documentos, reportes y material educativo.

## Decisión
Implementar almacenamiento en servidor local con opción de escalar a nube (S3).

## Consecuencias
- Control local de archivos.
- Escalabilidad futura.
- Gestión eficiente de documentos.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Base de Datos | Guardar binarios en DB | Centralización | Bajo rendimiento | Descartada |
| Servicios externos | Uso de S3 u otros | Alta disponibilidad | Costo mensual | Postergada |
| Servidor local | Sistema de archivos interno | Seguro y controlado | Limitado en capacidad | Aceptada |

## Referencias
AWS S3 Docs, Node.js FileSystem API.

---