# Mapa de competencias — Backend Architecture & Design

**Programa v1.5.1 · SETS Framework v1.4.1 · Namespace `B00–B14`**

El foco está en servicios, datos e infraestructura que ejecuta el backend. No es un curso de un framework concreto ni una lista de tecnologías para instalar. La meta es explicar mecanismos, reconocer garantías reales, anticipar fallos y defender decisiones transferibles.

Este mapa define competencias prioritarias, no agota todos los temas que pueden estudiarse. SETS puede enseñar una pregunta pertinente fuera de `B00–B14` y relacionarla con una competencia existente cuando ayude; solo se propone un módulo nuevo si el tema es recurrente o estratégicamente central. Fundamento, profundización y especialización son alcances adaptativos, no fases obligatorias. La apertura no cambia el foco backend.

## Competencias observables

| ID | Módulo | Capacidad observable | Pregunta conceptual central | Evidencia posible |
|---|---|---|---|---|
| B00 | Diagnóstico de backend | Reconocer contexto, invariantes, restricciones, incertidumbres y fallos relevantes | ¿Qué necesitamos saber antes de elegir una solución backend? | Diagnóstico razonado con supuestos y brechas observadas |
| B01 | Runtime y fundamentos del servidor | Razonar sobre ejecución, concurrencia, IO, memoria, threads, event loops, pools, colas y latencia | ¿Cómo convierte el runtime trabajo concurrente en recursos limitados y dónde aparece la saturación? | Traza causal y una hipótesis verificable de cuello de botella |
| B02 | Modularidad y arquitectura de aplicación | Comparar capas, puertos/adaptadores, monolito modular y servicios separados | ¿Qué acoplamiento queremos reducir y qué coste crea cada frontera? | Mapa de dependencias y alternativa defendible |
| B03 | Modelado de dominio y DDD | Definir invariantes, entidades, value objects, aggregates, bounded contexts y ownership | ¿Qué reglas deben mantenerse ciertas incluso bajo concurrencia o fallos? | Modelo de dominio y pruebas de invariantes |
| B04 | APIs y contratos | Diseñar contratos HTTP/REST/RPC/eventos, errores, compatibilidad, versionado e idempotencia | ¿Qué garantiza el contrato y qué ocurre si el cliente repite o abandona una operación? | Contrato con casos límite, compatibilidad y efectos secundarios |
| B05 | Datos, transacciones y consistencia | Razonar sobre SQL/NoSQL, atomicidad, aislamiento, locking, índices, migraciones y replicación | ¿Qué propiedad protege una transacción y qué queda fuera de ella? | Análisis de carrera y plan de prueba reproducible |
| B06 | Sistemas distribuidos | Analizar fallos parciales, particiones, orden, relojes, consistencia y disponibilidad | ¿Qué deja de ser cierto cuando dos procesos no comparten memoria ni fallan juntos? | Flujo bajo fallo y límites explícitos de la garantía |
| B07 | Mensajería e integración | Diseñar colas, pub/sub, eventos, outbox, sagas, reintentos, deduplicación y evolución de esquemas | ¿Qué sucede si un mensaje se pierde, se duplica, llega tarde o fuera de orden? | Tabla de estados y contrato de eventos |
| B08 | Resiliencia y recuperación | Diseñar timeouts, retries, backoff, jitter, circuit breakers, bulkheads y backpressure | ¿Cómo evitamos que una falla local se propague y cómo recuperamos el trabajo? | Política de recuperación con límites, riesgos y pruebas |
| B09 | Seguridad backend | Razonar sobre identidad, autenticación, autorización, OAuth2/OIDC, secretos, aislamiento y auditoría | ¿Quién puede hacer qué sobre qué recurso, bajo qué evidencia y límites de confianza? | Modelo de amenazas y controles verificables |
| B10 | Rendimiento y capacidad | Medir throughput, latencia p95/p99, saturación, profiling, GC, pools, cachés y escalado | ¿Qué recurso limita el sistema y cómo distinguir causa de síntoma? | Plan de medición reproducible y predicción de capacidad |
| B11 | Cloud-native y despliegue | Evaluar contenedores, configuración, redes, orquestación, CI/CD, rollout y rollback | ¿Qué cambia al pasar del proceso local a un entorno operado y distribuido? | Diagrama de despliegue y runbook con rollback |
| B12 | Observabilidad y confiabilidad | Relacionar logs, métricas, trazas, SLI/SLO, alertas, incidentes y recuperación | ¿Qué señal permite distinguir una falla y comprobar la recuperación? | Plan de instrumentación y diagnóstico basado en señales |
| B13 | Evolución de backend | Planificar migraciones, compatibilidad, strangler, cambios de datos y reversibilidad | ¿Cómo cambiamos sin exigir una migración atómica de todo el sistema? | Ruta incremental, riesgos, criterios de salida y reversión |
| B14 | Capstone backend | Integrar dominio, APIs, datos, integración, seguridad, rendimiento y operación | ¿Qué diseño preserva los invariantes bajo las cargas y fallos plausibles? | Diseño backend defendible, validaciones y revisión adversarial |

## Cómo se aprende cada competencia

Las lentes de `CONCEPTUAL_ENGINE.md` se usan adaptativamente, no como formulario rígido:

1. **Origen:** problema y propósito del mecanismo.
2. **Mecanismo:** causalidad, estados, invariantes y garantías.
3. **Límites:** supuestos, condiciones de fallo, contraejemplos y casos límite.
4. **Criterio:** alternativas, trade-offs, costes y señales de validación.
5. **Transferencia:** qué permanece y qué cambia en un caso nuevo o stack diferente.

No son cinco niveles ni una escala numérica. Un problema como «dos solicitudes reservan la última unidad» puede requerir más de una interacción.

## Formas válidas de evidencia

Explicación propia, predicción de una carrera, traza causal, contrato, tabla de estados, diagrama, análisis de contraejemplo, comparación de alternativas, ADR, cálculo, experimento o implementación. **No se exige código para cada competencia.** Una solución escrita por el tutor, una hipótesis no probada o la lectura pasiva no cuentan como desempeño demostrado por el estudiante.

## Método pedagógico

- Diagnóstico breve, una pregunta por turno; al finalizar, síntesis e inicio de enseñanza conceptual.
- Explicar directamente cuando el estudiante lo pide; no bloquear la explicación con preguntas socráticas.
- No iniciar laboratorios automáticamente después del diagnóstico o de una lección.
- Elegir stack y representación por utilidad explicativa. Preguntar preferencias solo cuando la elección cambie materialmente el mecanismo o el objetivo.
- Distinguir invariante de dominio, garantía del protocolo, comportamiento de runtime/framework, garantía de base de datos, decisión arquitectónica y resultado medido.
- Para decisiones, comparar alternativas viables, supuestos, riesgos, trade-offs, métricas y reversibilidad.
- Evaluar mediante evidencia observable, ayudas H0–H4 y transferencia independiente; no inferir dominio por experiencia declarada o una única respuesta.
- Adaptar la ruta a brechas reales o a una entrevista/caso solicitado; no es obligatorio cursar todos los módulos en orden.

## Rutas orientativas

- **Fundamentos:** B01–B05 según diagnóstico y necesidad.
- **Integración distribuida:** B04–B08, especialmente semánticas de fallo y consistencia.
- **Producción y operación:** B08–B12, relacionando señales, saturación, seguridad y recuperación.
- **Entrevista:** solo cuando se active; priorizar la vacante y las brechas observadas, sin imponer un lenguaje.
- **Capstone:** B14 integra decisiones y validación; no obliga a implementar todos los componentes.

## Criterio de comprensión profunda

Se busca explicar el problema y el mecanismo, declarar supuestos, anticipar una consecuencia o modo de fallo, reconocer un límite y razonar sobre una alternativa. El dominio se decide con `ASSESSMENT_ENGINE.md`, no por contar cuántas lentes se mencionaron.
