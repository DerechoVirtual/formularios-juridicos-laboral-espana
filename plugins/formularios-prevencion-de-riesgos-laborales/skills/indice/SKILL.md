---
name: indice
description: "Índice de los 7 formularios de Prevención de riesgos laborales. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Prevención de riesgos laborales: índice de formularios

> Plugin `formularios-prevencion-de-riesgos-laborales` · 7 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la prevención de riesgos: comunicación de apertura de centro de trabajo, formación e información preventiva, documentación preventiva en ETT y contratas, delegados de prevención y comunicaciones con ellos, y requerimientos de la Inspección en materia preventiva.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Comunicación de apertura del centro de trabajo en una obra»
- «Hoja de firmas de asistencia a la formación preventiva»
- «Aviso a los delegados de prevención de un requerimiento de la Inspección»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-prevencion-de-riesgos-laborales:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Comunicaciones, requerimientos y cartas (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0368 | Comunicación a los delegados de prevención del requerimiento de los técnicos públicos habilitados | `comunicacion-delegados-prevencion-requerimiento-lab-0368` |
| LAB-0369 | Aviso a los delegados de prevención del requerimiento de subsanación de la Inspección de Trabajo | `aviso-delegados-prevencion-requerimiento-subsanacion-lab-0369` |
| LAB-0370 | Comunicación de apertura del centro de trabajo en una obra de construcción | `comunicacion-apertura-centro-trabajo-obra-construccion-lab-0370` |

### Escritos de trámite y otros (4)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0366 | Asistencia a formación - hoja de firmas | `asistencia-formacion-hoja-firmas-lab-0366` |
| LAB-0367 | Apertura de expediente sancionador - aviso a representantes, sindicato y delegado de prevención | `apertura-expediente-sancionador-aviso-representantes-lab-0367` |
| LAB-0371 | Anexo I del contrato de puesta a disposición sobre los riesgos laborales del puesto | `anexo-i-contrato-puesta-disposicion-sobre-riesgos-lab-0371` |
| LAB-0372 | Anexo III del contrato entre ETT y trabajador en misión sobre la formación preventiva recibida | `anexo-iii-contrato-entre-ett-trabajador-mision-sobre-lab-0372` |
