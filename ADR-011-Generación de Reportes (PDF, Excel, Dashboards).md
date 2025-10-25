# ADR-011: Generación de Reportes (PDF, Excel, Dashboards)

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
El sistema debe generar reportes académicos y financieros.

## Decisión
Implementar con PDFKit, ExcelJS y Chart.js.

## Consecuencias
- Automatización de informes.
- Exportación múltiple.
- Visualización clara de métricas.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Manual | Hechos por usuario | Flexibles | Propensos a error | Descartada |
| Solo dashboards | Visuales online | Interactividad | Sin exportación | Descartada |
| Automatizada | PDF, Excel, Chart.js | Escalable y confiable | Mayor configuración | Aceptada |

## Referencias
PDFKit Docs, ExcelJS Docs.

---
