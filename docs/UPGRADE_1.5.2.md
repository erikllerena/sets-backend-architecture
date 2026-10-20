# Actualización Backend Architecture & Design: v1.5.1 → v1.5.2

Versión del **programa**, no del framework. Se mantiene **SETS Framework v1.4.1**, sin cambios.

## Archivos renombrados (GitHub)

- `state/README.md` → `state/STATE_ARTIFACTS_GUIDE.md`
- `labs/README.md` → `labs/LAB_GUIDE.md`
- `decisions/README.md` → `decisions/ARCHITECTURE_DECISIONS_GUIDE.md`

**Atención:** las decisiones de este programa son ADRs técnicos, a diferencia de `DECISION_ENGINE.md`, que es un motor pedagógico común. No se cambian los conceptos de fondo de las guías.

## Configuración ChatGPT

1. Sustituir el texto anterior en Instrucciones por `CHATGPT_PROJECT_INSTRUCTIONS.md` v1.5.2 de este programa.
2. Seguir `SETUP_CHATGPT.md` v1.5.2, que enumera archivos **individuales** y separa esenciales, recomendados y bajo demanda.
3. Si subiste los `README.md` de `state/`, `labs/` o `decisions/`, elimina esas fuentes y sustituye con su nombre nuevo **solo cuando corresponda**. El `README.md` raíz no hace falta como fuente.
4. Mantener los motores `INTERACTION_ENGINE.md`, `DECISION_ENGINE.md` y `PRACTICE_ENGINE.md` del framework; ya estaban en v1.5.1.
5. `CONCEPT_MAP.md` pasa a **recomendado, no obligatorio**, sin computarse como evidencia. `INTERVIEW_SPRINT.md` es bajo demanda.
6. Preservar `LEARNING_STATE.md`, `EVIDENCE_LOG.md`, `CONCEPT_MAP.md` y `LAST_HANDOFF.md` reales: **no sustituir progreso** por archivos vacíos de los ZIP.
7. GitHub y las fuentes de ChatGPT se actualizan por separado.

**No cambiado:** ámbitos y competencias B, currículo, casebook, evidencia preexistente, motores del framework y régimen de práctica optativa. Las pruebas `SRC-01`–`SRC-04` requieren validación manual.
