# ADR-001: Uso de Arquitectura Modular con Bounded Contexts (DDD)

**Estado:** Aceptado  
**Fecha:** 2025-01-xx

## 1. Decisión
Dividir el sistema LuxLearn en módulos independientes utilizando **Bounded Contexts** según Domain-Driven Design (DDD).

Los contextos definidos son:

- Gestión Administrativa  
- Gestión Académica  
- Pagos  
- Comunicación Institucional  
- Analítica & Reportes  
- Gestión de Archivos  

La interacción entre contextos utiliza:
- **OHS (Open Host Service)** para comunicación interna.  
- **ACL (Anti-Corruption Layer)** para integraciones externas.

## 2. Beneficio
- Alta mantenibilidad.  
- Equipos pueden trabajar en módulos separados.  
- Modelos del dominio aislados y consistentes.  
- Facilita la evolución independiente del sistema.

## 3. Trade-offs
- Mayor complejidad inicial en el diseño.  
- Necesidad de contratos API estrictos.  
- Requiere mayor esfuerzo de integración.

## 4. Alternativas Consideradas
- **Monolito clásico:** descartado por su baja flexibilidad futura.  
- **Microservicios completos:** descartado por su complejidad excesiva para el alcance actual.
