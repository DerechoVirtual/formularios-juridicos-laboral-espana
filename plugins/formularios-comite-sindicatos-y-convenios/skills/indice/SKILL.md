---
name: indice
description: "Índice de los 14 formularios de Representantes de los trabajadores, sindicatos y convenios. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Representantes de los trabajadores, sindicatos y convenios: índice de formularios

> Plugin `formularios-comite-sindicatos-y-convenios` · 14 formularios · normativa revisada el 25-11-2026.

## Qué es

Para las relaciones colectivas: información y consulta a los representantes de los trabajadores, elecciones sindicales y su impugnación, garantías de los representantes, secciones sindicales, negociación de convenios y acuerdos de empresa, inaplicación del convenio y huelga.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Comunicación mensual a los representantes de las horas extraordinarias»
- «Solicitud de arbitraje para impugnar las elecciones sindicales»
- «Información a los representantes de los contratos temporales celebrados»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-comite-sindicatos-y-convenios:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0376 | Demanda contra la denegación del registro de las actas de elección de delegados de personal | `demanda-contra-denegacion-registro-actas-eleccion-lab-0376` |
| LAB-0379 | Solicitud de ejecución provisional para que la empresa respete la condición de representante | `solicitud-ejecucion-provisional-empresa-respete-lab-0379` |
| LAB-0381 | Solicitud de arbitraje para impugnar el proceso de elecciones sindicales | `solicitud-arbitraje-impugnar-proceso-elecciones-lab-0381` |

### Estatutos, actas, certificaciones y escrituras (2)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0378 | Acta de discrepancia de los representantes sobre las acciones formativas de la empresa | `acta-discrepancia-representantes-sobre-acciones-lab-0378` |
| LAB-0387 | Acta de comparecencia de las partes en el arbitraje de elecciones sindicales | `acta-comparecencia-partes-arbitraje-elecciones-lab-0387` |

### Comunicaciones, requerimientos y cartas (4)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0375 | Comunicación de la plantilla sin representantes a la empresa de la opción elegida para designarlos | `comunicacion-plantilla-sin-representantes-empresa-lab-0375` |
| LAB-0377 | Comunicación de la empresa a los representantes del inicio de las acciones formativas | `comunicacion-empresa-representantes-inicio-acciones-lab-0377` |
| LAB-0383 | Comunicación mensual a los representantes de las horas extraordinarias realizadas en la empresa | `comunicacion-mensual-representantes-horas-lab-0383` |
| LAB-0384 | Notificación a los representantes de los contratos de duración determinada celebrados | `notificacion-representantes-contratos-duracion-lab-0384` |

### Escritos de trámite y otros (5)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0373 | Personal de libre disponibilidad y registro de jornada - acuerdo con la representación | `personal-libre-disponibilidad-registro-jornada-acuerdo-lab-0373` |
| LAB-0374 | Instalación de cámaras de videovigilancia - aviso a la representación de los trabajadores | `instalacion-camaras-videovigilancia-aviso-lab-0374` |
| LAB-0380 | Escrito del miembro del comité que invoca su prioridad de permanencia frente al traslado | `escrito-miembro-comite-invoca-prioridad-permanencia-lab-0380` |
| LAB-0382 | Información de la contratista a los representantes de los trabajadores antes de iniciar la actividad | `informacion-contratista-representantes-trabajadores-lab-0382` |
| LAB-0386 | Impugnación en vía arbitral de la designación de un delegado de personal | `impugnacion-via-arbitral-designacion-delegado-personal-lab-0386` |
