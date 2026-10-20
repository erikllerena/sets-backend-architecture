# Instalación — SETS | Backend Architecture & Design v1.5.1

## 1. Crea o abre el Proyecto

Nombre sugerido: **SETS | Backend Architecture & Design**. Si la opción está disponible, usa memoria solo del Proyecto para mantener aislado el progreso académico. No necesitas archivos ni sesiones de otras especializaciones.

## 2. Instrucciones activas

Pega **solo** el contenido de `CHATGPT_PROJECT_INSTRUCTIONS.md` en las instrucciones del Proyecto. Si ya existía, reemplaza las instrucciones anteriores para evitar directrices contradictorias.

## 3. Fuentes del framework común

Desde `sets-framework` v1.4.1, carga:

**Esenciales**
- `core/PROJECT_INSTRUCTIONS.md`
- `core/CONCEPTUAL_ENGINE.md` — nuevo motor conceptual, imprescindible en esta versión.
- `core/INTERACTION_ENGINE.md`
- `core/DECISION_ENGINE.md`
- `core/PRACTICE_ENGINE.md`
- `core/ASSESSMENT_ENGINE.md`
- `core/SESSION_HANDOFF.md`
- `templates/LAST_HANDOFF.template.md`

**Recomendadas**
- `templates/CONCEPT_MAP.template.md`
- `templates/ADR_TEMPLATE.md`
- `docs/REFERENCE_POLICY.md`
- `docs/LEARNING_SCIENCE.md`
- `docs/QUALITY_CHECKS.md`
- `docs/COMMAND_REFERENCE.md`

Si el Proyecto ya tenía fuentes del framework v1.3.2, reemplaza las versiones antiguas en vez de dejarlas compitiendo con las nuevas.

## 4. Fuentes de ESTE repositorio

Carga:
- `PROJECT_CONFIG.yaml`
- `PROJECT_RULES.md`
- `learning/CURRICULUM.md`
- `learning/CASEBOOK.md`
- `learning/REFERENCES.md`
- `learning/INTERVIEW_SPRINT.md` (modo opcional)
- `state/LEARNING_STATE.md`
- `state/EVIDENCE_LOG.md`
- `state/CONCEPT_MAP.md` (opcional)

`state/LAST_HANDOFF.md` no se adjunta antes del primer cierre real. Las instrucciones activas son las del archivo `CHATGPT_PROJECT_INSTRUCTIONS.md`, no un texto concatenado con otras fuentes.

## 5. Primer uso

- `/start`: diagnóstico breve de Backend; al finalizar, síntesis y enseñanza conceptual.
- `/learn <tema>`: empieza directamente una lección conceptual.
- `/deep <tema>`: profundiza en mecanismo, invariantes, límites y fallos.
- `/explain`: explicación directa, sin intento previo obligatorio.
- `/lab <tema>`: práctica implementable cuando la solicites.
- `/interview` o `/sprint`: activa preparación de entrevista; no se activa por defecto.
- `/close`: genera los tres artefactos obligatorios; revisa antes de guardar.

## 6. Verificación rápida

Pregunta: «Explícame por qué un timeout al cobrar no demuestra que el cobro falló, qué mecanismos ayudan a evitar efectos duplicados y qué límites tienen». La respuesta debe razonar sobre estado desconocido, idempotencia, conciliación, reintentos y límites del proveedor, sin exigir código ni declarar garantías absolutas.

## 7. Continuidad

Guarda resultados en GitHub de este repositorio y actualiza manualmente las fuentes del Proyecto. Para continuar en un chat nuevo, permanece en el mismo Proyecto y usa `/resume`. No afirmes que existe sincronización automática entre GitHub y ChatGPT.


## Currículo y casos abiertos (v1.5.1)

Las fuentes de esta versión declaran el currículo y el casebook como mapas no exhaustivos. Al actualizar el Proyecto de ChatGPT, reemplaza las instrucciones activas y las fuentes antiguas por las de este paquete y por SETS Framework v1.4.1. Las pruebas de `docs/ACCEPTANCE_CHECKS.md` son manuales y quedan pendientes hasta ejecutarlas.
