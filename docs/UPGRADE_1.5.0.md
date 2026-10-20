# Actualización — sets-backend-architecture 1.4.1 → 1.5.0

## Objetivo

Alinear el programa con **SETS Framework v1.4.0 / Conceptual Mastery**, manteniendo el ámbito Backend, el namespace `B00–B14` y el aislamiento del progreso de este Proyecto.

## Cambios principales

- Actualizadas las referencias del framework a v1.4.0 y del programa a v1.5.0.
- Integrado explícitamente `core/CONCEPTUAL_ENGINE.md` en las instrucciones y en la guía de instalación.
- Incorporadas cinco lentes adaptativas: origen, mecanismo, límites, criterio y transferencia; no son pasos obligatorios ni escala de dominio.
- Reforzado el razonamiento causal sobre invariantes, concurrencia, transacciones, idempotencia, entrega de mensajes y fallos parciales.
- Neutralizado el stack predeterminado: Java/Spring Boot y demás tecnologías familiares son puentes opcionales.
- Ampliado el currículo con preguntas conceptuales centrales y formas de evidencia que no requieren código.
- Enriquecido el caso OrderCore para estudiar timeouts ambiguos, idempotencia, duplicados, compatibilidad y migraciones.
- Reiniciado el estado inicial sin evidencia ficticia y añadido `state/CONCEPT_MAP.md` opcional.
- Actualizadas las comprobaciones manuales, el setup y este documento.

## Contratos preservados

- Namespace `B00–B14`.
- Evaluación 0–4 y ayudas H0–H4; las lentes conceptuales no crean una escala nueva.
- `/close` produce los tres artefactos obligatorios: `LAST_HANDOFF.md`, `LEARNING_STATE.md` completo y delta append-only de `EVIDENCE_LOG.md`.
- El mapa conceptual es opcional y no prueba dominio por sí solo.
- El progreso de este programa no se importa de otras especializaciones.
- Sincronización GitHub ↔ ChatGPT sigue siendo manual.

## Actualización recomendada

1. Conserva el historial Git y copia los archivos del paquete respetando sus rutas.
2. Reemplaza las instrucciones activas del Proyecto por `CHATGPT_PROJECT_INSTRUCTIONS.md`.
3. Sustituye las fuentes de framework v1.3.2 por las de `sets-framework` v1.4.0 e incluye `core/CONCEPTUAL_ENGINE.md`.
4. Reemplaza las fuentes académicas de Backend por las de esta versión.
5. Ejecuta los checks manuales de `docs/ACCEPTANCE_CHECKS.md`.

Actualizar GitHub no actualiza automáticamente las instrucciones ni las fuentes activas del Proyecto de ChatGPT.
