
# Week-5

# ADR – Arquitectura de Software

Cada Rol deberá aplicar **5 ADR (Architecture Decision Records)** dentro del proyecto.

Los ADR pueden estar relacionados con:

- Patrones de diseño
- Patrones estructurales
- Patrones comportamentales

## Proceso para los ADR

1. Identificación de patrones
2. Análisis del proyecto para determinar qué ADR pueden aplicarse
3. Identificación de antipatrones
4. Detección de segmentos de código con malas prácticas
5. Diseño e implementación del ADR
6. Análisis del impacto del ADR sobre el sistema

- Listar todos los ADR posibles del proyecto.
- De esa lista, cada Rol debera implementar **3 ADR**.
- Entregar un **informe de impacto**, explicando cómo cada ADR mejora el sistema.

## Listado de ADR

- [ADR-001-secretos-configuracion](docs/ADR/ADR-001-secretos-configuracion.md)
- [ADR-002-rutas-gateway](docs/ADR/ADR-002-rutas-gateway.md)
- [ADR-003-integracion-gateway-compose](docs/ADR/ADR-003-integracion-gateway-compose.md)
- [ADR-004-endurecimiento-seguridad](docs/ADR/ADR-004-endurecimiento-seguridad.md)
- [ADR-005-contratos-api](docs/ADR/ADR-005-contratos-api.md)
- [ADR-006-comunicacion-errores-microservicios](docs/ADR/ADR-006-comunicacion-errores-microservicios.md)
- [ADR-007-observabilidad-monitoreo](docs/ADR/ADR-007-observabilidad-monitoreo.md)
- [ADR-008-documentacion-versionado-api](docs/ADR/ADR-008-documentacion-versionado-api.md)
- [ADR-009-estrategia-pruebas-microservicios](docs/ADR/ADR-009-estrategia-pruebas-microservicios.md)
- [ADR-010-uso-obligatorio-gateway](docs/ADR/ADR-010-uso-obligatorio-gateway.md)
- [ADR-011-logging-basico](docs/ADR/ADR-011-logging-basico.md)
- [ADR-012-endpoint-status](docs/ADR/ADR-012-endpoint-status.md)
- [ADR-013-puerto-entorno](docs/ADR/ADR-013-puerto-entorno.md)
- [ADR-014-validacion-dto](docs/ADR/ADR-014-validacion-dto.md)
- [ADR-015-excepciones-simples](docs/ADR/ADR-015-excepciones-simples.md)

## Preguntas de seguimiento semanal

### ¿Qué se hizo?
- Se identificaron y documentaron los ADR relevantes para el proyecto.
- Se actualizaron los archivos ADR en la carpeta correspondiente.
- Se mejoró la estructura del README para incluir la lista de ADR y las preguntas de seguimiento.

### ¿Qué no se logró?
- No se ha realizado aún el informe de impacto de cada ADR implementado.
- No todos los roles han implementado sus 3 ADR asignados.

### ¿Qué se va a hacer?
- Completar la implementación de los ADR faltantes por cada rol.
- Elaborar y entregar el informe de impacto de los ADR.
- Revisar y mejorar la documentación según retroalimentación del equipo.

## ADR aplicados por cada rol

### Rol Backend
1. **ADR-001: Externalización de Secretos y Configuración Sensible**
	- Se implementó la gestión de secretos fuera del código fuente, usando variables de entorno y archivos de configuración seguros, para evitar la exposición de información sensible.
2. **ADR-002: Unificación de Rutas entre API Gateway y Microservicios**
	- Se definió una estructura de rutas centralizada en el API Gateway, asegurando consistencia y control de acceso en todos los servicios.
3. **ADR-003: Integración Completa del API Gateway en el Despliegue**
	- Se integró el API Gateway en el proceso de despliegue con Docker Compose, garantizando que todo el tráfico pase por el gateway y facilitando la orquestación.

### Rol Frontend
1. **ADR-006: Comunicación y Manejo de Errores entre Microservicios**
	- Se estandarizó la forma en que los microservicios reportan y gestionan errores, permitiendo una mejor experiencia de usuario y trazabilidad de fallos.
2. **ADR-007: Observabilidad y Monitoreo del Sistema**
	- Se implementaron mecanismos de monitoreo y logging para detectar problemas en tiempo real y facilitar el análisis de eventos.
3. **ADR-008: Estrategia de Documentación y Versionado de API**
	- Se estableció una estrategia para documentar y versionar las APIs, asegurando que los consumidores puedan adaptarse a cambios de manera controlada.

### Rol QA
1. **ADR-011: Configuración de Logging Básico**
	- Se definió una configuración mínima de logging para todos los servicios, permitiendo registrar eventos relevantes para auditoría y depuración.
2. **ADR-012: Endpoint de Estado Simple**
	- Se implementó un endpoint `/status` en los servicios para verificar su disponibilidad y estado de salud.


