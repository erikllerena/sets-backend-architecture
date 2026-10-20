# Acceptance checks — Backend Architecture & Design v1.5.1

Estas son pruebas manuales sugeridas; no son evidencia de que ChatGPT ya las haya superado.

1. `/start` inicia un diagnóstico del ámbito `B`, una pregunta por turno; al concluir, ofrece síntesis y enseñanza conceptual, no un laboratorio automático.
2. `/learn idempotencia` explica problema, mecanismo, garantías, límites, contraejemplo y transferencia sin convertirlo en examen.
3. Pedir «explícalo sin código» conserva profundidad y permite razonamiento con estados, contratos o diagramas.
4. Pedir «elige tú la tecnología» lleva al tutor a escoger la representación más clara y justificarla brevemente.
5. Pedir comparar Java/Spring con otro stack distingue principio general, runtime, framework y base de datos; no crea una comparación innecesaria.
6. Analizar dos pedidos que reservan la última unidad identifica la invariante, la carrera y una estrategia de prueba; no afirma que `@Transactional` por sí sola resuelva cualquier escenario.
7. Analizar un timeout de pago reconoce que el timeout no demuestra que la operación externa no ocurrió.
8. Analizar mensajería considera duplicados, orden, reintentos, idempotencia del consumidor y límites de las garantías del broker.
9. Tras una lección, el laboratorio es optativo; `/lab` explícito sí inicia la práctica.
10. `/close` genera tres artefactos y solo evidencia observada; `/resume` lee exclusivamente el estado de este programa.
11. `/status` con estado inicial informa «No evaluado» y no importa progreso desde otros proyectos.
12. El tutor distingue modelo simplificado, comportamiento documentado, hipótesis e implementación verificada cuando sea relevante.

## Checks de apertura y foco

- **OL1:** Pedir un ejemplo con una tecnología no incluida en la lista familiar: el tutor puede usarla si aclara el mecanismo y no vuelve automáticamente a Java/Spring.
- **OL2:** Preguntar por un tema backend pertinente sin módulo dedicado (por ejemplo, un detalle de aislamiento o un índice): se enseña en contexto sin exigir completar módulos anteriores.
- **OL3:** Solicitar un caso nuevo fuera de OrderCore: el tutor crea/adapta un escenario y etiqueta los supuestos sin tratarlo como hecho real.
- **OL4:** Pedir una especialización avanzada sin completar el currículo: el tutor cubre los prerrequisitos mínimos y atiende la pregunta sin imponer una ruta completa.
- **OL5:** Preguntar por el efecto de una decisión backend en la UI o en el sistema completo: explica la conexión necesaria y conserva el foco backend salvo ampliación explícita.

## Checks de apertura y foco

- **OL1:** Pedir un ejemplo con una tecnología no incluida en la lista familiar: el tutor puede usarla si aclara el mecanismo y no vuelve automáticamente a Java/Spring.
- **OL2:** Preguntar por un tema backend pertinente sin módulo dedicado (por ejemplo, un detalle de aislamiento o un índice): se enseña en contexto sin exigir completar módulos anteriores.
- **OL3:** Solicitar un caso nuevo fuera de OrderCore: el tutor crea/adapta un escenario y etiqueta los supuestos sin tratarlo como hecho real.
- **OL4:** Pedir una especialización avanzada sin completar el currículo: el tutor cubre los prerrequisitos mínimos y atiende la pregunta sin imponer una ruta completa.
- **OL5:** Preguntar por el efecto de una decisión backend en la UI o en el sistema completo: explica la conexión necesaria y conserva el foco backend salvo ampliación explícita.

## Caso centinela

Dos solicitudes concurrentes intentan reservar la última unidad de inventario. La respuesta debe identificar la invariante del dominio, explicar cómo puede ocurrir la carrera, comparar mecanismos de protección y describir cómo verificar la propiedad; el lenguaje o framework es opcional.
