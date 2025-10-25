# ADR-017: Backups y Recuperación ante Desastres

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Garantizar resiliencia ante fallos o pérdida de datos.

## Decisión
Configurar backups diarios automáticos y redundancia en servidores secundarios.

## Consecuencias
- Evita pérdida de información.
- Rápida recuperación.
- Cumple políticas institucionales.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Manual | Respaldos esporádicos | Sin costo | Riesgo alto | Descartada |
| Mensual | Snapshots ocasionales | Menor espacio | Pérdida potencial alta | Descartada |
| Automático diario | Con rsync o S3 | Seguro y estable | Requiere almacenamiento adicional | Aceptada |

## Referencias
MySQL Dump Docs, AWS Backup Best Practices.

---