---
name: indice
description: "Índice de los 36 formularios de Igualdad, acoso y canal de denuncias en la empresa. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Igualdad, acoso y canal de denuncias en la empresa: índice de formularios

> Plugin `formularios-igualdad-y-acoso-laboral` · 36 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la igualdad en la empresa: plan de igualdad y su comisión negociadora, diagnóstico y cuestionarios, registro retributivo, protocolos frente al acoso sexual, por razón de sexo y laboral, medidas LGTBI, canal de denuncias y sanción del acoso.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Acta de constitución de la comisión negociadora del plan de igualdad»
- «Protocolo para prevenir y actuar frente al acoso sexual»
- «Carta de sanción por acoso»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-igualdad-y-acoso-laboral:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0353 | Demanda del trabajador acosado en el trabajo para tutelar sus derechos fundamentales | `demanda-trabajador-acosado-trabajo-tutelar-derechos-lab-0353` |

### Contratos, pactos y cláusulas (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0324 | Protocolo contra el acoso y la violencia hacia personas LGTBI | `protocolo-contra-acoso-violencia-hacia-personas-lgtbi-lab-0324` |
| LAB-0325 | Acuerdo con la representación de los trabajadores sobre medidas de igualdad LGTBI | `acuerdo-representacion-trabajadores-sobre-medidas-lab-0325` |
| LAB-0347 | Protocolo contra el acoso sexual y por razón de sexo en el trabajo | `protocolo-contra-acoso-sexual-razon-sexo-trabajo-lab-0347` |

### Estatutos, actas, certificaciones y escrituras (5)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0327 | Acta de reunión de la Comisión de seguimiento del Plan de Igualdad | `acta-reunion-comision-seguimiento-plan-igualdad-lab-0327` |
| LAB-0328 | Acta de constitución de la Comisión de seguimiento del plan de igualdad o plan LGTBI | `acta-constitucion-comision-seguimiento-plan-igualdad-lab-0328` |
| LAB-0329 | Acta de aprobación del protocolo contra el acoso sexual o por razón de sexo | `acta-aprobacion-protocolo-contra-acoso-sexual-razon-lab-0329` |
| LAB-0333 | Acta de aprobación del plan de igualdad o del plan LGTBI | `acta-aprobacion-plan-igualdad-plan-lgtbi-lab-0333` |
| LAB-0342 | Acta de constitución de la comisión negociadora del plan de igualdad o plan LGTBI | `acta-constitucion-comision-negociadora-plan-igualdad-lab-0342` |

### Comunicaciones, requerimientos y cartas (4)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0323 | Aviso a la plantilla de la implantación del canal de denuncias | `aviso-plantilla-implantacion-canal-denuncias-lab-0323` |
| LAB-0331 | Carta para constituir la comisión negociadora del plan de igualdad | `carta-constituir-comision-negociadora-plan-igualdad-lab-0331` |
| LAB-0344 | Aviso a la plantilla del inicio del Plan de Igualdad | `aviso-plantilla-inicio-plan-igualdad-lab-0344` |
| LAB-0348 | Denuncia de acoso sexual o por razón de sexo | `denuncia-acoso-sexual-razon-sexo-lab-0348` |

### Escritos de trámite y otros (23)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0319 | Evaluación para la comisión de seguimiento - cuestionario | `evaluacion-comision-seguimiento-cuestionario-lab-0319` |
| LAB-0320 | Cuestionario de evaluación del plan dirigido a la plantilla | `cuestionario-evaluacion-plan-dirigido-plantilla-lab-0320` |
| LAB-0321 | Cuestionario de evaluación dirigido a la dirección | `cuestionario-evaluacion-dirigido-direccion-lab-0321` |
| LAB-0322 | Impulso por la empresa de la negociación del plan de igualdad o del plan LGTBI | `impulso-empresa-negociacion-plan-igualdad-plan-lgtbi-lab-0322` |
| LAB-0326 | Reglamento de la Comisión de seguimiento y evaluación | `reglamento-comision-seguimiento-evaluacion-lab-0326` |
| LAB-0330 | Diagnóstico del Plan de Igualdad - acta de aprobación | `diagnostico-plan-igualdad-acta-aprobacion-lab-0330` |
| LAB-0332 | Acoso laboral (mobbing) - demanda por infracción de la normativa de prevención | `acoso-laboral-mobbing-demanda-infraccion-normativa-lab-0332` |
| LAB-0334 | Autorizar los trámites de inscripción del plan de igualdad o del protocolo de acoso | `autorizar-tramites-inscripcion-plan-igualdad-protocolo-lab-0334` |
| LAB-0335 | Plan de igualdad - hoja estadística | `plan-igualdad-hoja-estadistica-lab-0335` |
| LAB-0336 | Impulso por la representación de los trabajadores de la negociación del plan de igualdad | `impulso-representacion-trabajadores-negociacion-plan-lab-0336` |
| LAB-0337 | Cuestionario de igualdad para la plantilla | `cuestionario-igualdad-plantilla-lab-0337` |
| LAB-0338 | Cuestionario de igualdad para la dirección | `cuestionario-igualdad-direccion-lab-0338` |
| LAB-0339 | Criterios de selección de la empresa usuaria - comunicación a la empresa externa | `criterios-seleccion-empresa-usuaria-comunicacion-lab-0339` |
| LAB-0340 | Compromisos de la organización en selección y promoción | `compromisos-organizacion-seleccion-promocion-lab-0340` |
| LAB-0341 | Comisión negociadora del plan de igualdad - acta de reunión | `comision-negociadora-plan-igualdad-acta-reunion-lab-0341` |
| LAB-0343 | Reunión con perspectiva de igualdad - convocatoria | `reunion-perspectiva-igualdad-convocatoria-lab-0343` |
| LAB-0345 | Compromiso de la empresa con la igualdad - carta | `compromiso-empresa-igualdad-carta-lab-0345` |
| LAB-0346 | Compromiso de la organización contra el acoso sexual y por razón de sexo | `compromiso-organizacion-contra-acoso-sexual-razon-sexo-lab-0346` |
| LAB-0349 | Compromiso con el plan de igualdad en el convenio colectivo - cláusula | `compromiso-plan-igualdad-convenio-colectivo-clausula-lab-0349` |
| LAB-0350 | Confidencialidad en la tramitación de denuncias de acoso - compromiso | `confidencialidad-tramitacion-denuncias-acoso-compromiso-lab-0350` |
| LAB-0351 | Sanción por acoso - carta | `sancion-acoso-carta-lab-0351` |
| LAB-0352 | Cargos por acoso sexual - pliego | `cargos-acoso-sexual-pliego-lab-0352` |
| LAB-0354 | Autorización del trabajador a la sección sindical para denunciar un posible acoso | `autorizacion-trabajador-seccion-sindical-denunciar-lab-0354` |
