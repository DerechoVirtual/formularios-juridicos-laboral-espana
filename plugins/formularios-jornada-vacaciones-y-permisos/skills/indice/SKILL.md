---
name: indice
description: "Índice de los 87 formularios de Jornada, vacaciones, permisos y conciliación. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Jornada, vacaciones, permisos y conciliación: índice de formularios

> Plugin `formularios-jornada-vacaciones-y-permisos` · 87 formularios · normativa revisada el 25-11-2026.

## Qué es

Para el tiempo de trabajo: jornada y horario, registro de jornada, horas extraordinarias y trabajo nocturno, vacaciones, permisos retribuidos y no retribuidos, reducción de jornada y adaptación por conciliación, excedencias y reingreso, suspensiones del contrato y trabajo a distancia.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Petición de reducción de jornada por cuidado de un hijo»
- «Solicitud de excedencia voluntaria»
- «Acuerdo de trabajo a distancia»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-jornada-vacaciones-y-permisos:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (6)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0244 | Demanda de adaptación de jornada por conciliación | `demanda-adaptacion-jornada-conciliacion-lab-0244` |
| LAB-0273 | Demanda para volver al puesto de trabajo tras una excedencia voluntaria | `demanda-volver-puesto-trabajo-tras-excedencia-lab-0273` |
| LAB-0274 | Demanda para volver al puesto tras la excedencia por cuidado de un menor ante la falta de vacante | `demanda-volver-puesto-tras-excedencia-cuidado-menor-lab-0274` |
| LAB-0275 | Demanda de la trabajadora víctima de violencia de género para reducir su jornada | `demanda-trabajadora-victima-violencia-genero-reducir-lab-0275` |
| LAB-0276 | Demanda de la trabajadora víctima de violencia de género para reordenar su tiempo de trabajo | `demanda-trabajadora-victima-violencia-genero-reordenar-lab-0276` |
| LAB-0287 | Demanda de reincorporación tras la excedencia voluntaria y de indemnización por el retraso | `demanda-reincorporacion-tras-excedencia-voluntaria-lab-0287` |

### Contratos, pactos y cláusulas (10)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0278 | Pacto con los representantes para acumular el medio día de descanso semanal en comercio y hostelería | `pacto-representantes-acumular-medio-dia-descanso-lab-0278` |
| LAB-0280 | Pacto sobre el control empresarial de la actividad del trabajador a distancia | `pacto-sobre-control-empresarial-actividad-trabajador-lab-0280` |
| LAB-0286 | Acuerdo de trabajo a distancia entre empresa y trabajador | `acuerdo-trabajo-distancia-entre-empresa-trabajador-lab-0286` |
| LAB-0288 | Acuerdo de bolsa de horas para ajustar la jornada a las necesidades productivas | `acuerdo-bolsa-horas-ajustar-jornada-necesidades-lab-0288` |
| LAB-0289 | Acuerdo de bolsa de horas para recuperar o compensar las horas no trabajadas | `acuerdo-bolsa-horas-recuperar-compensar-horas-no-lab-0289` |
| LAB-0307 | Acuerdo sobre la distribución diaria del tiempo de trabajo | `acuerdo-sobre-distribucion-diaria-tiempo-trabajo-lab-0307` |
| LAB-0308 | Acuerdo sobre el descanso durante la jornada continuada | `acuerdo-sobre-descanso-durante-jornada-continuada-lab-0308` |
| LAB-0311 | Pacto con el trabajador para la realización de horas extraordinarias | `pacto-trabajador-realizacion-horas-extraordinarias-lab-0311` |
| LAB-0313 | Acuerdo que fija las fechas de disfrute de las vacaciones | `acuerdo-fija-fechas-disfrute-vacaciones-lab-0313` |
| LAB-0314 | Pacto sobre el pago o la compensación con descanso de las horas extraordinarias | `pacto-sobre-pago-compensacion-descanso-horas-lab-0314` |

### Comunicaciones, requerimientos y cartas (14)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0237 | Declaración del hogar familiar sobre reducción de servicios por la DANA | `declaracion-hogar-familiar-sobre-reduccion-servicios-lab-0237` |
| LAB-0246 | Aviso de ausencia por fuerza mayor ante enfermedad o accidente de un familiar - carta | `aviso-ausencia-fuerza-mayor-ante-enfermedad-accidente-lab-0246` |
| LAB-0258 | Declaración responsable de trabajadores fuera del permiso retribuido recuperable del RDL 10 - 2020 | `declaracion-responsable-trabajadores-fuera-permiso-lab-0258` |
| LAB-0279 | Carta a los representantes para abrir la negociación de una distribución irregular de la jornada | `carta-representantes-abrir-negociacion-distribucion-lab-0279` |
| LAB-0282 | Aviso del trabajador a la empresa del inicio de su excedencia para cuidar de un hijo biológico | `aviso-trabajador-empresa-inicio-excedencia-cuidar-hijo-lab-0282` |
| LAB-0291 | Aviso del trabajador a la empresa de que acumulará el permiso por cuidado del lactante | `aviso-trabajador-empresa-acumulara-permiso-cuidado-lab-0291` |
| LAB-0292 | Carta de la empresa que concede la excedencia solicitada | `carta-empresa-concede-excedencia-solicitada-lab-0292` |
| LAB-0295 | Comunicación al trabajador de las fechas de sus vacaciones | `comunicacion-trabajador-fechas-vacaciones-lab-0295` |
| LAB-0297 | Carta de la empresa que deniega la excedencia solicitada | `carta-empresa-deniega-excedencia-solicitada-lab-0297` |
| LAB-0298 | Aviso del fin de la reducción de jornada por cuidado de hijo menor de doce años o con discapacidad | `aviso-fin-reduccion-jornada-cuidado-hijo-menor-doce-lab-0298` |
| LAB-0303 | Carta de la empresa que accede a suspender el contrato a petición del trabajador | `carta-empresa-accede-suspender-contrato-peticion-lab-0303` |
| LAB-0304 | Carta de la empresa que rechaza suspender el contrato a petición del trabajador | `carta-empresa-rechaza-suspender-contrato-peticion-lab-0304` |
| LAB-0317 | Notificación al trabajador de la suspensión del contrato por una causa prevista en él | `notificacion-trabajador-suspension-contrato-causa-lab-0317` |
| LAB-0318 | Aviso del trabajador a la empresa de la suspensión de su contrato por privación de libertad | `aviso-trabajador-empresa-suspension-contrato-privacion-lab-0318` |

### Escritos de trámite y otros (57)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0232 | Pedir permiso retribuido por fallecimiento de familiar en incendios forestales | `pedir-permiso-retribuido-fallecimiento-familiar-lab-0232` |
| LAB-0233 | Pedir adaptación de jornada por cuidado de familiares tras la DANA | `pedir-adaptacion-jornada-cuidado-familiares-tras-dana-lab-0233` |
| LAB-0234 | Pedir permiso retribuido por la DANA | `pedir-permiso-retribuido-dana-lab-0234` |
| LAB-0235 | Respuesta de la empresa al permiso retribuido por la DANA | `respuesta-empresa-permiso-retribuido-dana-lab-0235` |
| LAB-0236 | Pedir trabajo a distancia por la DANA | `pedir-trabajo-distancia-dana-lab-0236` |
| LAB-0238 | Propuesta de turnos de guardia al trabajador | `propuesta-turnos-guardia-trabajador-lab-0238` |
| LAB-0239 | Anexo de horas complementarias (contrato a tiempo parcial) (en valenciano) | `anexo-horas-complementarias-contrato-tiempo-parcial-lab-0239` |
| LAB-0240 | Anexo de horas complementarias (contrato a tiempo parcial) (en euskera) | `anexo-horas-complementarias-contrato-tiempo-parcial-lab-0240` |
| LAB-0241 | Anexo de horas complementarias (contrato a tiempo parcial) (en catalán) | `anexo-horas-complementarias-contrato-tiempo-parcial-lab-0241` |
| LAB-0242 | Anexo de horas complementarias (contrato a tiempo parcial) (en gallego) | `anexo-horas-complementarias-contrato-tiempo-parcial-lab-0242` |
| LAB-0243 | Resumen mensual de horas de trabajo - comunicación | `resumen-mensual-horas-trabajo-comunicacion-lab-0243` |
| LAB-0245 | Pedir permiso por registro de pareja de hecho | `pedir-permiso-registro-pareja-hecho-lab-0245` |
| LAB-0247 | Conciliación laboral, personal y familiar - demanda genérica de derechos | `conciliacion-laboral-personal-familiar-demanda-lab-0247` |
| LAB-0248 | Desconexión digital - protocolo | `desconexion-digital-protocolo-lab-0248` |
| LAB-0249 | Suspensión del contrato por violencia de género o sexual - carta a la empresa | `suspension-contrato-violencia-genero-sexual-carta-lab-0249` |
| LAB-0250 | Suspensión del contrato por nacimiento, adopción o acogimiento - carta a la empresa | `suspension-contrato-nacimiento-adopcion-acogimiento-lab-0250` |
| LAB-0251 | Suplicación en procedimiento de acceso, reversión o modificación del trabajo a distancia - recurso | `suplicacion-procedimiento-acceso-reversion-lab-0251` |
| LAB-0252 | Trabajo a distancia - demanda por acceso, revisión o modificación | `trabajo-distancia-demanda-acceso-revision-modificacion-lab-0252` |
| LAB-0253 | Revertir el trabajo a distancia - comunicación de la decisión | `revertir-trabajo-distancia-comunicacion-decision-lab-0253` |
| LAB-0254 | Pedir trabajo a distancia como víctima de violencia de género | `pedir-trabajo-distancia-como-victima-violencia-genero-lab-0254` |
| LAB-0255 | Pedir trabajo a distancia por estudios | `pedir-trabajo-distancia-estudios-lab-0255` |
| LAB-0256 | Prórroga de excedencia voluntaria - demanda de reconocimiento | `prorroga-excedencia-voluntaria-demanda-reconocimiento-lab-0256` |
| LAB-0257 | Pedir adaptación de jornada por conciliación | `pedir-adaptacion-jornada-conciliacion-lab-0257` |
| LAB-0259 | Pedir adaptación de jornada por violencia de género, sexual o terrorismo | `pedir-adaptacion-jornada-violencia-genero-sexual-lab-0259` |
| LAB-0260 | Distribución irregular de la jornada - acuerdo con la representación | `distribucion-irregular-jornada-acuerdo-representacion-lab-0260` |
| LAB-0261 | Cambio de jornada completa a parcial o al revés - acuerdo | `cambio-jornada-completa-parcial-reves-acuerdo-lab-0261` |
| LAB-0262 | Compensar horas extra con descanso - petición del trabajador | `compensar-horas-extra-descanso-peticion-trabajador-lab-0262` |
| LAB-0263 | Reincorporación tras excedencia - comunicación del trabajador | `reincorporacion-tras-excedencia-comunicacion-trabajador-lab-0263` |
| LAB-0264 | Pedir días de vacaciones | `pedir-dias-vacaciones-lab-0264` |
| LAB-0265 | Pedir excedencia - carta | `pedir-excedencia-carta-lab-0265` |
| LAB-0266 | Registro de jornada diaria | `registro-jornada-diaria-lab-0266` |
| LAB-0267 | Disfrute de permiso retribuido - comunicación del trabajador | `disfrute-permiso-retribuido-comunicacion-trabajador-lab-0267` |
| LAB-0268 | Distribución irregular de la jornada - carta al trabajador | `distribucion-irregular-jornada-carta-trabajador-lab-0268` |
| LAB-0269 | Pedir permiso para informes psicológicos y sociales de adopción | `pedir-permiso-informes-psicologicos-sociales-adopcion-lab-0269` |
| LAB-0270 | Pedir permiso para sesiones informativas previas a la adopción | `pedir-permiso-sesiones-informativas-previas-adopcion-lab-0270` |
| LAB-0271 | Pedir justificante de ausencia al trabajador | `pedir-justificante-ausencia-trabajador-lab-0271` |
| LAB-0272 | Orden de la empresa al trabajador a tiempo parcial para hacer las horas complementarias pactadas | `orden-empresa-trabajador-tiempo-parcial-hacer-horas-lab-0272` |
| LAB-0277 | Petición del trabajador de permiso retribuido para un curso de formación vinculado al puesto | `peticion-trabajador-permiso-retribuido-curso-formacion-lab-0277` |
| LAB-0281 | Petición de excedencia para cuidar a un menor adoptado o acogido | `peticion-excedencia-cuidar-menor-adoptado-acogido-lab-0281` |
| LAB-0283 | Respuesta de la empresa a la petición de reducción o adaptación de jornada o de permiso | `respuesta-empresa-peticion-reduccion-adaptacion-lab-0283` |
| LAB-0284 | Respuesta de la empresa a la petición de reincorporación tras la excedencia | `respuesta-empresa-peticion-reincorporacion-tras-lab-0284` |
| LAB-0285 | Petición del trabajador de permiso de formación con reserva del puesto de trabajo | `peticion-trabajador-permiso-formacion-reserva-puesto-lab-0285` |
| LAB-0290 | Petición del trabajador de un permiso no retribuido | `peticion-trabajador-permiso-no-retribuido-lab-0290` |
| LAB-0293 | Anexo al contrato a tiempo parcial, temporal o indefinido, con el pacto de horas complementarias | `anexo-contrato-tiempo-parcial-temporal-indefinido-lab-0293` |
| LAB-0294 | Calendario laboral de la empresa para 2026 | `calendario-laboral-empresa-2026-lab-0294` |
| LAB-0296 | Parte diario de registro de horas extraordinarias | `parte-diario-registro-horas-extraordinarias-lab-0296` |
| LAB-0299 | Petición del trabajador para prorrogar su excedencia voluntaria | `peticion-trabajador-prorrogar-excedencia-voluntaria-lab-0299` |
| LAB-0300 | Respuesta de la empresa que concede la prórroga de la excedencia voluntaria | `respuesta-empresa-concede-prorroga-excedencia-lab-0300` |
| LAB-0301 | Petición de reingreso al terminar la excedencia voluntaria | `peticion-reingreso-terminar-excedencia-voluntaria-lab-0301` |
| LAB-0302 | Respuesta de la empresa que deniega el reingreso tras la excedencia voluntaria por falta de vacantes | `respuesta-empresa-deniega-reingreso-tras-excedencia-lab-0302` |
| LAB-0305 | Preaviso de la vuelta a la jornada ordinaria tras un permiso o una reducción de jornada | `preaviso-vuelta-jornada-ordinaria-tras-permiso-lab-0305` |
| LAB-0306 | Petición de adaptación de la jornada para cursar estudios | `peticion-adaptacion-jornada-cursar-estudios-lab-0306` |
| LAB-0309 | Información a la autoridad laboral del recurso habitual al trabajo nocturno | `informacion-autoridad-laboral-recurso-habitual-trabajo-lab-0309` |
| LAB-0310 | Hoja mensual resumen de horas extraordinarias | `hoja-mensual-resumen-horas-extraordinarias-lab-0310` |
| LAB-0312 | Petición del trabajador de adscribirse voluntariamente al turno de noche | `peticion-trabajador-adscribirse-voluntariamente-turno-lab-0312` |
| LAB-0315 | Petición de adaptación de la jornada para asistir a cursos de formación profesional | `peticion-adaptacion-jornada-asistir-cursos-formacion-lab-0315` |
| LAB-0316 | Petición de permiso para presentarse a exámenes | `peticion-permiso-presentarse-examenes-lab-0316` |
