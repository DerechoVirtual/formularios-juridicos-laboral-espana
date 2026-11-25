---
name: indice
description: "Índice de los 11 formularios de Protección de datos y control empresarial. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Protección de datos y control empresarial: índice de formularios

> Plugin `formularios-datos-y-control-del-trabajador` · 11 formularios · normativa revisada el 25-11-2026.

## Qué es

Para el control de la actividad y los datos de la plantilla: información sobre protección de datos a los empleados, videovigilancia y geolocalización, uso de medios informáticos y teléfono de empresa, desconexión digital, códigos de conducta y de vestimenta, y cláusulas de confidencialidad.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Información sobre protección de datos a los empleados»
- «Normas sobre el uso de los equipos informáticos de la empresa»
- «Cláusula de confidencialidad y desconexión digital»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-datos-y-control-del-trabajador:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Comunicaciones, requerimientos y cartas (4)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0357 | Aviso emergente sobre el uso laboral de los medios de la empresa | `aviso-emergente-sobre-uso-laboral-medios-empresa-lab-0357` |
| LAB-0363 | Aviso al trabajador de videovigilancia, control de jornada o geolocalización | `aviso-trabajador-videovigilancia-control-jornada-lab-0363` |
| LAB-0364 | Comunicación al trabajador de las normas y controles sobre el uso de los equipos informáticos | `comunicacion-trabajador-normas-controles-sobre-uso-lab-0364` |
| LAB-0365 | Comunicación al trabajador de las normas y controles sobre el uso del teléfono de empresa | `comunicacion-trabajador-normas-controles-sobre-uso-lab-0365` |

### Escritos de trámite y otros (7)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0355 | Confidencialidad, control de medios y desconexión digital - cláusula | `confidencialidad-control-medios-desconexion-digital-lab-0355` |
| LAB-0356 | Información sobre protección de datos a los empleados | `informacion-sobre-proteccion-datos-empleados-lab-0356` |
| LAB-0358 | Código de conducta en la relación empresa-trabajador | `codigo-conducta-relacion-empresa-trabajador-lab-0358` |
| LAB-0359 | Vestimenta en la empresa - código | `vestimenta-empresa-codigo-lab-0359` |
| LAB-0360 | Normas de uso del sistema informático y las comunicaciones electrónicas | `normas-uso-sistema-informatico-comunicaciones-lab-0360` |
| LAB-0361 | Protección de datos en contratos con empresa subcontratista - cláusula | `proteccion-datos-contratos-empresa-subcontratista-lab-0361` |
| LAB-0362 | Información sobre protección de datos en la geolocalización - cláusula | `informacion-sobre-proteccion-datos-geolocalizacion-lab-0362` |
