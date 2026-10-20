# Changelog — SETS Backend Architecture & Design

## 1.5.2 — 2026-10-20 (fuentes individuales de ChatGPT)

- Renombradas las guías `state/README.md`, `labs/README.md` y `decisions/README.md` para que su finalidad sea inequívoca fuera de GitHub.
- Auditadas las fuentes de `SETUP_CHATGPT.md` y su correspondencia con SETS Framework v1.4.1; motores INTERACTION/DECISION/PRACTICE ya estaban presentes.
- `CONCEPT_MAP.md` recomendado al inicio pero no obligatorio; `INTERVIEW_SPRINT.md` solo cuando se active entrevista.
- Guías de laboratorios y ADRs técnicos, pruebas de aceptación y notas de actualización como documentos bajo demanda. No se agregó una carpeta de práctica ficticia.
- Diferenciada la guía de decisiones técnicas (ADRs) del `DECISION_ENGINE.md` pedagógico.
- Mantenidos currículo, casebook y registros de estado/evidencias sin modificar; pruebas del tutor documentadas, no ejecutadas.



## 1.5.1 — 2026-10-19 (aprendizaje abierto sin deriva de alcance)

- Alineado con SETS Framework v1.4.1.
- Formalizado que las tecnologías familiares son contexto opcional, no whitelist ni cuota de uso; no se fuerza novedad.
- Declarados currículo y casebook como mapas no exhaustivos; se pueden enseñar temas pertinentes y utilizar casos nuevos sin añadir módulos por cada curiosidad.
- Añadida una distinción adaptativa entre fundamento, profundización y especialización, sin fases obligatorias.
- Reforzado el límite disciplinar para evitar que la apertura diluya la misión de Backend Architecture & Design.
- Añadidos cinco checks manuales de aceptación para verificar neutralidad, apertura, profundidad y foco; pendientes de ejecución real.

## 1.5.0 — 2026-10-19 (Conceptual Mastery)

- Alineado con SETS Framework v1.4.0.
- Integrado `CONCEPTUAL_ENGINE.md` y las cinco lentes adaptativas, sin crear una escala nueva.
- Reforzado el razonamiento causal sobre invariantes, concurrencia, idempotencia, fallos parciales y límites de garantías.
- Neutralizado el stack por defecto: las tecnologías conocidas son ejemplos opcionales.
- Ampliado el currículo y el caso OrderCore con preguntas conceptuales y evidencia no necesariamente basada en código.
- Actualizado setup y checks; añadido `docs/UPGRADE_1.5.0.md` y `state/CONCEPT_MAP.md` opcional.
- Estado inicial limpio, sin evidencia ficticia.

## 1.4.1 — 2026-10-19 (autonomía del programa y profundidad conceptual)

- Programa autosuficiente con memoria, currículo, evidencia y continuidad propios.
- Enseñanza conceptual primero, preguntas dosificadas, práctica optativa y selección flexible de tecnologías.
- Reinicio de las plantillas de progreso por decisión del estudiante.

## 1.4.0 — Separación por dominio

- Especialización Backend con namespace `Bxx` y estado inicial vacío.
- Currículo y casos delimitados al diseño y operación de servicios backend.
