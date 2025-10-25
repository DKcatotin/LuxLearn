# ADR-019: Escalabilidad y Balanceo de Carga

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Preparar LuxLearn para soportar alto tráfico concurrente.

## Decisión
Usar NGINX, Load Balancer y scaling horizontal (Swarm/K8s).

## Consecuencias
- Disponibilidad alta.
- Reducción de latencia.
- Escalabilidad controlada.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Servidor único | Un nodo principal | Simple | Poco tolerante a fallos | Descartada |
| Replicación manual | Múltiples instancias | Distribuible | Difícil de mantener | Descartada |
| Balanceo automático | NGINX + Swarm/K8s | Escalable y seguro | Mayor complejidad | Aceptada |

## Referencias
NGINX Docs, Docker Swarm Guide.

---