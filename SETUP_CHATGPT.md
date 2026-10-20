# Instalación en ChatGPT — SETS | Backend Architecture & Design v1.5.2

Este programa utiliza **SETS Framework v1.4.1** sin modificaciones. Los archivos de GitHub se organizan en carpetas, pero **las Fuentes de un Proyecto de ChatGPT se cargan como archivos individuales**; una vez cargados, no dependas de que se conserve su ruta de origen. Por eso cada fuente propuesta tiene un nombre visible inequívoco.

**No es necesario subir todo el repositorio.** Separamos documentos esenciales, recomendados y bajo demanda para no saturar el Proyecto ni transformar la enseñanza en un ritual.

## 1. Proyecto e instrucciones activas

1. Crea o abre el Proyecto **SETS | Backend Architecture & Design**. Si la opción existe, usa memoria solo del Proyecto.
2. Pega **únicamente el contenido de `CHATGPT_PROJECT_INSTRUCTIONS.md` de este programa** en las Instrucciones del Proyecto. Reemplaza las versiones anteriores; no acumules textos ni motores como instrucciones activas.
3. Sube los archivos de las secciones siguientes **como Fuentes**, no como instrucciones. El archivo `CHATGPT_PROJECT_INSTRUCTIONS.md` no necesita cargarse de nuevo como fuente.

## 2. Fuentes esenciales — programa `sets-backend-architecture`

| Archivo visible en ChatGPT | Origen en GitHub | Propósito |
|---|---|---|
| `PROJECT_CONFIG.yaml` | `PROJECT_CONFIG.yaml` | Identidad, límites y preferencias. |
| `PROJECT_RULES.md` | `PROJECT_RULES.md` | Reglas especializadas, autonomía y frontera disciplinar. |
| `CURRICULUM.md` | `learning/CURRICULUM.md` | Mapa abierto de competencias, no temario cerrado. |
| `CASEBOOK.md` | `learning/CASEBOOK.md` | Casos ilustrativos, no obligatorios ni exclusivos. |
| `REFERENCES.md` | `learning/REFERENCES.md` | Referencias para contrastar y profundizar. |
| `LEARNING_STATE.md` | `state/LEARNING_STATE.md` | Estado real de aprendizaje (no importar progreso de otros SETS). |
| `EVIDENCE_LOG.md` | `state/EVIDENCE_LOG.md` | Evidencias verificables y acumulativas. |
| `STATE_ARTIFACTS_GUIDE.md` | `state/STATE_ARTIFACTS_GUIDE.md` | Convenciones de continuidad y de los archivos de estado. |

**Recomendada desde el inicio, no obligatoria:** `state/CONCEPT_MAP.md`, visible como **`CONCEPT_MAP.md`**, para identificar relaciones conceptuales justificadas. No reemplaza el currículo ni acredita dominio. El tutor puede continuar si no se carga; no debe fingir haberla leído.

## 3. Fuentes esenciales — SETS Framework v1.4.1

Carga los siguientes archivos desde **`sets-framework`**, no desde una copia independiente de otro programa:

| Archivo visible | Ruta de origen en el framework | Función |
|---|---|---|
| `PROJECT_INSTRUCTIONS.md` | `core/PROJECT_INSTRUCTIONS.md` | Contrato pedagógico común de referencia. |
| `CONCEPTUAL_ENGINE.md` | `core/CONCEPTUAL_ENGINE.md` | Comprensión, causalidad, mecanismos y límites. |
| `INTERACTION_ENGINE.md` | `core/INTERACTION_ENGINE.md` | Diálogo y adaptación. |
| `DECISION_ENGINE.md` | `core/DECISION_ENGINE.md` | Comparación razonada, criterios y trade-offs. |
| `PRACTICE_ENGINE.md` | `core/PRACTICE_ENGINE.md` | Práctica y transferencia incluso sin laboratorios preparados. |
| `ASSESSMENT_ENGINE.md` | `core/ASSESSMENT_ENGINE.md` | Evaluación apoyada en evidencia, sin progreso ficticio. |
| `SESSION_HANDOFF.md` | `core/SESSION_HANDOFF.md` | Cierre y continuidad. |
| `LAST_HANDOFF.template.md` | `templates/LAST_HANDOFF.template.md` | Formato para el handoff real. |

**Recomendadas según uso:** `docs/REFERENCE_POLICY.md`, `docs/LEARNING_SCIENCE.md`, `docs/COMMAND_REFERENCE.md`, `docs/QUALITY_CHECKS.md`, `templates/CONCEPT_MAP.template.md` y `templates/ADR_TEMPLATE.md`. No es preciso cargar todas permanentemente.

## 4. Archivos bajo demanda: entrevista, labs, decisions y docs

| Archivo visible | Ruta de origen | Cuándo cargarlo |
|---|---|---|
| `INTERVIEW_SPRINT.md` | `learning/INTERVIEW_SPRINT.md` | Solo cuando actives `/interview` o `/sprint`. No implica preparar entrevista por defecto. |
| `LAB_GUIDE.md` | `labs/LAB_GUIDE.md` | Si vas a archivar un laboratorio o necesitas sus convenciones. **No es obligatorio para `/lab`.** |
| `ARCHITECTURE_DECISIONS_GUIDE.md` | `decisions/ARCHITECTURE_DECISIONS_GUIDE.md` | Al producir ADRs **técnicos** sobre arquitectura del sistema. Distinto de `DECISION_ENGINE.md`. |
| `ACCEPTANCE_CHECKS.md` | `docs/ACCEPTANCE_CHECKS.md` | Al **validar el comportamiento del tutor**; no para evaluar al alumno en clases ordinarias. |
| `UPGRADE_1.5.2.md` | `docs/UPGRADE_1.5.2.md` | Solo durante la migración de versiones. |

Este programa **no contiene un banco `practice/` específico**; no inventes archivos ni dependencias: la práctica optativa se realiza mediante `PRACTICE_ENGINE.md`, el currículo y casos pertinentes o nuevos. El `README.md` raíz y el `CHANGELOG.md` son documentación del repositorio: no tienen que ser Fuentes del Proyecto.

## 5. Uso inicial y continuidad

- `/start`: diagnóstico breve, una pregunta por turno; después comienza la enseñanza conceptual.
- `/learn <tema>` y `/deep <tema>`: explica fundamentos, mecanismos, alternativas y límites con profundidad adaptativa; no impongas tecnología, rutas rígidas o práctica inmediata.
- `/lab <tema>`: propón una práctica pertinente si el usuario la pide; `LAB_GUIDE.md` es optativa. No inventes experimentos ejecutados.
- `/interview` o `/sprint`: activa el modo correspondiente a petición del usuario.
- `/close`: entrega `LAST_HANDOFF.md` completo, `LEARNING_STATE.md` actualizado e información nueva para añadir a `EVIDENCE_LOG.md`. No inventes evidencia y revisa antes de guardar.
- `/resume`: retoma únicamente desde el estado verificable de este Proyecto. `LAST_HANDOFF.md` no existe antes de un primer cierre real.

**Prueba rápida sugerida:** Pregúntale qué implica un timeout tras solicitar un cobro. Debe diferenciar estado desconocido, idempotencia, recuperación, verificación y límites de terceros. También confirma que el tutor no confunde las guías de ADR con `DECISION_ENGINE.md`, no necesita `LAB_GUIDE.md` para enseñar/practicar y no afirma haber leído una fuente ausente.

## 6. Comprobación de nombres y sincronización

1. Al subir Fuentes, verifica los **nombres individuales**: no uses tres archivos distintos llamados `README.md` esperando que ChatGPT deduzca sus carpetas. Las antiguas rutas `state/README.md`, `labs/README.md` y `decisions/README.md` fueron **renombradas**; elimina las fuentes antiguas si estaban cargadas.
2. No debe haber dos archivos con el mismo nombre visible. Los archivos de este programa se cargan en **su propio Proyecto**, no se mezclan con los de otras especialidades.
3. No añadas carpetas ni ZIP como sustitutos de esta selección. La ruta en la tabla es **para encontrar el archivo en GitHub o en tu computadora**, no una ruta garantizada dentro de ChatGPT.
4. Tras actualizar GitHub, **actualiza manualmente las fuentes del Proyecto**; no hay sincronización automática por defecto. Conserva respaldos si ya tienes progreso, evidencias o handoffs reales: no los sobrescribas con plantillas vacías.

**Framework común**: se reutiliza `sets-framework` v1.4.1. No se ha creado ni modificado un framework por especialidad.
