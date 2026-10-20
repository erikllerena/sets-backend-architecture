# SETS | Backend Architecture & Design

**Programa v1.5.1 · SETS Framework v1.4.1**

## Misión

Desarrollar comprensión conceptual profunda, razonamiento causal y criterio profesional para diseñar, construir, evaluar y evolucionar sistemas backend, con capacidad de transferir lo aprendido entre lenguajes, runtimes, bases de datos y plataformas.

El currículo y el casebook son mapas abiertos, no límites exhaustivos. Las tecnologías familiares son contexto opcional; el tutor puede abordar temas y casos nuevos cuando ayuden, manteniendo el foco de esta disciplina.

## Ámbito propio

Diseño y operación de servicios backend: modelos de ejecución, modularidad, dominio, APIs, persistencia, transacciones, consistencia, integración, sistemas distribuidos, mensajería, seguridad del servidor, rendimiento, resiliencia, observabilidad y despliegue. El programa es **académicamente autosuficiente**: explica aquí los fundamentos necesarios y no requiere progreso de otras especializaciones.

## Filosofía de aprendizaje

- **Concepto antes que herramienta.** Comprender el problema, el mecanismo causal, los invariantes y las consecuencias antes de memorizar una receta.
- **Neutralidad tecnológica real.** No hay lenguaje ni stack obligatorio. Java/Spring Boot, SQL, Kafka, contenedores o una nube son opciones ilustrativas, no requisitos.
- **El tutor elige con criterio.** Si el stack cambia materialmente la actividad, ofrece 2–3 opciones; si no, elige la representación más clara y explica brevemente por qué.
- **Razonar sobre fallos reales.** Distinguir garantía, supuesto, comportamiento documentado, hipótesis y resultado medido.
- **Práctica optativa por defecto.** Una explicación, predicción, traza, contrato, tabla de estados o diagrama puede ser suficiente para el objetivo; los laboratorios se proponen cuando aportan valor.
- **Evidencia honesta.** Recibir una explicación no demuestra dominio. El progreso se basa en respuestas y artefactos observables.

## Archivos principales

- `CHATGPT_PROJECT_INSTRUCTIONS.md`: instrucciones activas para el Proyecto de ChatGPT.
- `PROJECT_RULES.md`: contrato pedagógico específico de Backend.
- `PROJECT_CONFIG.yaml`: configuración del programa, no evidencia de dominio.
- `learning/CURRICULUM.md`: competencias `B00–B14`.
- `learning/CASEBOOK.md`: caso conductor OrderCore y transferencias.
- `learning/INTERVIEW_SPRINT.md`: preparación de entrevistas opcional.
- `learning/REFERENCES.md`: fuentes de referencia, no un curso obligatorio.
- `state/LEARNING_STATE.md`, `state/EVIDENCE_LOG.md`: progreso y evidencias reales de este programa.
- `state/CONCEPT_MAP.md`: mapa conceptual opcional y local a Backend.
- `state/LAST_HANDOFF.md`: se crea después del primer cierre real; no se incluye vacío.
- `SETUP_CHATGPT.md`: instalación y fuentes necesarias.

## Inicio rápido

1. Usa los motores genéricos de `sets-framework` v1.4.1.
2. Sigue `SETUP_CHATGPT.md`: pega solo `CHATGPT_PROJECT_INSTRUCTIONS.md` en las instrucciones del Proyecto y carga las fuentes indicadas.
3. Usa `/start` para diagnóstico breve y posterior enseñanza conceptual, o `/learn <tema>` para comenzar directamente.
4. Usa `/lab <tema>` cuando quieras una práctica implementable; no se inicia automáticamente.
5. Al cerrar una sesión, usa `/close`, revisa los artefactos y guarda manualmente los cambios en este repositorio y en las fuentes del Proyecto.

El estado inicial parte de cero por decisión del estudiante. No hay sincronización automática GitHub ↔ ChatGPT. No subas secretos, datos sensibles ni código propietario.
