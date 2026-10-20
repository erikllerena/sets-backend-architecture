# CASEBOOK — Backend Architecture & Design (v1.5.1)

Los casos de este archivo son ejemplos iniciales, no un conjunto cerrado. OrderCore es un caso conductor opcional para construir continuidad, no una parada obligatoria de cada sesión. Selecciona o crea casos nuevos si explican mejor el concepto o prueban transferencia; etiqueta supuestos ficticios y distingue los hechos reales que requieran verificación. El currículo y este casebook pueden evolucionar, pero no añadas módulos por cada curiosidad ni cambies IDs sin una revisión deliberada.

## Caso conductor: OrderCore — Backend (escenario ficticio)

OrderCore procesa pedidos, reserva inventario, cobra a través de un proveedor externo y publica cambios de estado. Es un caso evolutivo para estudiar mecanismos; **no presupone microservicios, Kafka, Kubernetes ni una nube concreta**.

| Iteración | Situación | Pregunta causal y evidencia posible |
|---|---|---|
| B-0 | MVP de pedidos con equipo pequeño y base de datos relacional | ¿Qué límites de módulo son necesarios hoy? Comparación de monolito modular y servicios separados con costes de operación. |
| B-1 | Dos solicitudes intentan reservar la última unidad | ¿Qué invariante se rompe y dónde se hace cumplir? Traza de concurrencia, aislamiento/locking/actualización condicional y prueba reproducible. |
| B-2 | El proveedor de pago devuelve timeout después de haber cobrado | ¿Qué sabe el backend y qué no sabe? Idempotencia, conciliación, reintentos limitados y auditoría. |
| B-3 | La misma petición de creación se reintenta desde un cliente | ¿Qué significa idempotencia a nivel de efecto de negocio? Clave idempotente, almacenamiento de resultado y límites de retención/duplicación. |
| B-4 | Lecturas de catálogo aumentan 30×; escrituras, 2× | ¿Cuál es el cuello de botella real? Hipótesis, medición, índices/caché/réplicas y evaluación de invalidación. |
| B-5 | Un proveedor externo cae durante 30 minutos | ¿Qué falla en cascada? Timeouts, circuit breaker, cola, backpressure, recuperación y límites de retry. |
| B-6 | Una confirmación de pedido se publica dos veces o llega tarde | ¿Qué garantía ofrece el broker y qué debe proteger el consumidor? Outbox, deduplicación, orden y estado idempotente. |
| B-7 | El negocio requiere separar equipos y ciclos de despliegue | ¿Qué ownership justifica una frontera? Bounded contexts, contratos, datos propios, coste de red y migración incremental. |
| B-8 | Una API debe proteger datos personales y acciones administrativas | ¿Qué identidad se autentica, qué autorización se aplica y dónde se audita? Threat model proporcional y controles verificables. |
| B-9 | El servicio se degrada bajo carga aunque CPU no está al 100 % | ¿Qué recurso está saturado? Colas, pools, bloqueos, conexiones, latencia p95/p99 y medición antes de optimizar. |
| B-10 | Se requiere migrar una columna y desplegar una nueva versión sin parada | ¿Cómo convivirán ambas versiones? Expand/contract, compatibilidad, backfill, observación y rollback. |

## Transferencias

- Reservas médicas con recursos limitados.
- Notificaciones masivas con duplicados y límites de proveedor.
- Ledger financiero donde importa la invariante contable.
- Carga de archivos con estados parciales y expiración.
- Catálogo multi-región con réplicas y caché.
- Procesamiento de eventos de sensores con orden parcial y consumidores lentos.

## Protocolo de enseñanza del caso

Antes de pedir una decisión, enseñar los fundamentos que falten: problema, mecanismo, invariantes, supuestos, alternativas y señales observables. La primera interacción puede ser una explicación completa con diagrama conceptual, sin implementación. No revelar la solución antes del intento cuando se haya activado explícitamente un reto o entrevista; para una pregunta de explicación directa, responder directamente.

Separar **hipótesis** de **pruebas realizadas**. No elegir broker, microservicios, caché o Kubernetes por moda: justificarlo por requisitos y fallos que se quieren manejar. Registrar el nivel de ayuda solo cuando exista una evaluación real. El laboratorio es optativo salvo solicitud explícita.
