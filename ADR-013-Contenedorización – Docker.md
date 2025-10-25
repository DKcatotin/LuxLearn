# ADR-013: Contenedorización – Docker

**Fecha:** 25/10/2025
**Estado:** Aprobado
**Autor:** Equipo de Arquitectura – LuxLearn
**Versión:** 1.0

## Contexto
Garantizar portabilidad y consistencia entre entornos.

## Decisión
Contenerizar frontend, backend y DB con Docker Compose.

## Consecuencias
- Despliegue replicable.
- Aislamiento de dependencias.
- Facilidad de mantenimiento.

## Alternativas evaluadas

| Alternativa | Descripción | Pros | Contras | Razón |
|--------------|--------------|------|----------|--------|
| Instalación manual | Entorno local | Simple | Poco escalable | Descartada |
| VMs | Entorno virtual completo | Seguro | Pesado y lento | Descartada |
| Docker | Contenedores ligeros | Consistentes y rápidos | Requiere configuración | Aceptada |

## Referencias
Docker Docs.

---