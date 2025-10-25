# ADR-020: Analítica Educativa (Learning Analytics)

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Proveer métricas sobre rendimiento y desempeño docente.

## Decisión
Incorporar módulo analítico con Chart.js y FastAPI.

## Consecuencias
- Toma de decisiones basada en datos.
- Seguimiento académico avanzado.
- Predicción de resultados.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Estadísticas básicas | Promedios simples | Fácil de implementar | Poca profundidad | Descartada |
| Servicios externos | Google Analytics u otros | Potentes | Pérdida de control de datos | Descartada |
| Analítica interna | Integración Chart.js + API Python | Flexible y privada | Requiere desarrollo | Aceptada |

## Referencias
Chart.js Docs, FastAPI Docs.

---