---
name: indice
description: "Índice de los 42 formularios de Faltas y sanciones laborales. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Faltas y sanciones laborales: índice de formularios

> Plugin `formularios-faltas-y-sanciones-laborales` · 42 formularios · normativa revisada el 25-11-2026.

## Qué es

Para el poder disciplinario de la empresa: cartas de amonestación y sanción por faltas leves, graves y muy graves, expediente contradictorio, pliego de cargos y descargos, audiencia a representantes y delegados sindicales, y cancelación de antecedentes.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Carta de sanción por falta grave»
- «Pliego de cargos en un expediente contradictorio»
- «Petición de cancelación de antecedentes por sanción»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-faltas-y-sanciones-laborales:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Contestaciones, oposiciones y alegaciones (2)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0404 | Descargos del trabajador - pliego | `descargos-trabajador-pliego-lab-0404` |
| LAB-0428 | Alegaciones del trabajador en el expediente contradictorio | `alegaciones-trabajador-expediente-contradictorio-lab-0428` |

### Recursos (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0421 | Recurso del socio trabajador contra su expulsión disciplinaria de la cooperativa | `recurso-socio-trabajador-contra-expulsion-lab-0421` |

### Estatutos, actas, certificaciones y escrituras (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0417 | Acta del consejo rector que impone una sanción disciplinaria definitiva al socio trabajador | `acta-consejo-rector-impone-sancion-disciplinaria-lab-0417` |
| LAB-0422 | Informe final del instructor en el expediente contradictorio a un representante de los trabajadores | `informe-final-instructor-expediente-contradictorio-lab-0422` |
| LAB-0423 | Informe de los representantes de los trabajadores en un expediente disciplinario contradictorio | `informe-representantes-trabajadores-expediente-lab-0423` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0416 | Comunicación a los representantes de los trabajadores de los despidos disciplinarios impuestos | `comunicacion-representantes-trabajadores-despidos-lab-0416` |
| LAB-0418 | Comunicación al socio trabajador de la apertura de expediente disciplinario de expulsión | `comunicacion-socio-trabajador-apertura-expediente-lab-0418` |
| LAB-0420 | Notificación al socio trabajador de su expulsión disciplinaria de la cooperativa | `notificacion-socio-trabajador-expulsion-disciplinaria-lab-0420` |
| LAB-0424 | Comunicación a los representantes de una falta muy grave y de la sanción distinta del despido | `comunicacion-representantes-falta-muy-grave-sancion-lab-0424` |
| LAB-0425 | Aviso al trabajador del cierre del expediente contradictorio y de la sanción distinta del despido | `aviso-trabajador-cierre-expediente-contradictorio-lab-0425` |
| LAB-0426 | Carta de sanción al trabajador que abandonó su puesto de trabajo | `carta-sancion-trabajador-abandono-puesto-trabajo-lab-0426` |
| LAB-0427 | Aviso al trabajador de la fecha en que empieza a cumplir la suspensión de empleo y sueldo | `aviso-trabajador-fecha-empieza-cumplir-suspension-lab-0427` |

### Escritos de trámite y otros (29)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0388 | Cancelar antecedentes por sanción - comunicación del trabajador | `cancelar-antecedentes-sancion-comunicacion-trabajador-lab-0388` |
| LAB-0389 | Ficha de antecedentes por sanción | `ficha-antecedentes-sancion-lab-0389` |
| LAB-0390 | Pedir la cancelación de antecedentes por sanción | `pedir-cancelacion-antecedentes-sancion-lab-0390` |
| LAB-0391 | Sanción por faltas de asistencia o puntualidad - carta | `sancion-faltas-asistencia-puntualidad-carta-lab-0391` |
| LAB-0392 | Sanción por transgresión de la buena fe y abuso de confianza - carta | `sancion-transgresion-buena-fe-abuso-confianza-carta-lab-0392` |
| LAB-0393 | Sanción por ofensas verbales o físicas - carta | `sancion-ofensas-verbales-fisicas-carta-lab-0393` |
| LAB-0394 | Sanción por indisciplina o desobediencia - carta | `sancion-indisciplina-desobediencia-carta-lab-0394` |
| LAB-0395 | Sanción por otras infracciones del convenio - carta | `sancion-otras-infracciones-convenio-carta-lab-0395` |
| LAB-0396 | Sanción por reincidencia o reiteración de faltas - carta | `sancion-reincidencia-reiteracion-faltas-carta-lab-0396` |
| LAB-0397 | Sanción por bajo rendimiento - carta | `sancion-bajo-rendimiento-carta-lab-0397` |
| LAB-0398 | Sanción por embriaguez habitual o toxicomanía - carta | `sancion-embriaguez-habitual-toxicomania-carta-lab-0398` |
| LAB-0399 | Sobreseimiento del expediente sancionador - propuesta | `sobreseimiento-expediente-sancionador-propuesta-lab-0399` |
| LAB-0400 | Sanción impuesta - aviso a la representación de los trabajadores en el expediente sancionador | `sancion-impuesta-aviso-representacion-trabajadores-lab-0400` |
| LAB-0401 | Sanción propuesta en el expediente disciplinario | `sancion-propuesta-expediente-disciplinario-lab-0401` |
| LAB-0402 | Cargos por reincidencia o reiteración de faltas - pliego | `cargos-reincidencia-reiteracion-faltas-pliego-lab-0402` |
| LAB-0403 | Cargos por otras infracciones del convenio - pliego | `cargos-otras-infracciones-convenio-pliego-lab-0403` |
| LAB-0405 | Cargos por embriaguez habitual o toxicomanía - pliego | `cargos-embriaguez-habitual-toxicomania-pliego-lab-0405` |
| LAB-0406 | Actuaciones no disciplinarias - propuesta | `actuaciones-no-disciplinarias-propuesta-lab-0406` |
| LAB-0407 | Cargos por transgresión de la buena fe y abuso de confianza - pliego | `cargos-transgresion-buena-fe-abuso-confianza-pliego-lab-0407` |
| LAB-0408 | Cargos por bajo rendimiento - pliego | `cargos-bajo-rendimiento-pliego-lab-0408` |
| LAB-0409 | Cargos por ofensas verbales o físicas - pliego | `cargos-ofensas-verbales-fisicas-pliego-lab-0409` |
| LAB-0410 | Cargos por indisciplina o desobediencia - pliego | `cargos-indisciplina-desobediencia-pliego-lab-0410` |
| LAB-0411 | Cargos por faltas de asistencia o puntualidad - pliego | `cargos-faltas-asistencia-puntualidad-pliego-lab-0411` |
| LAB-0412 | Diligencias en el expediente sancionador | `diligencias-expediente-sancionador-lab-0412` |
| LAB-0413 | Aceptación del cargo en el expediente sancionador | `aceptacion-cargo-expediente-sancionador-lab-0413` |
| LAB-0414 | Nombramiento en el expediente sancionador | `nombramiento-expediente-sancionador-lab-0414` |
| LAB-0415 | Apercibimiento sin sanción - carta | `apercibimiento-sin-sancion-carta-lab-0415` |
| LAB-0419 | Pliego de descargo del socio trabajador frente a la propuesta de expulsión | `pliego-descargo-socio-trabajador-frente-propuesta-lab-0419` |
| LAB-0429 | Propuesta del instructor de despido del representante en el expediente contradictorio | `propuesta-instructor-despido-representante-expediente-lab-0429` |
