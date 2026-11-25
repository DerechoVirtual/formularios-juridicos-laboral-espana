---
name: indice
description: "Índice de los 43 formularios de Extranjería y movilidad internacional de trabajadores. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Extranjería y movilidad internacional de trabajadores: índice de formularios

> Plugin `formularios-extranjeria-y-trabajo` · 43 formularios · normativa revisada el 25-11-2026.

## Qué es

Para la extranjería laboral: autorizaciones de residencia y trabajo, arraigo, residencia de larga duración, visados y movilidad internacional (Ley 14/2013), desplazamiento de trabajadores, TIE, recursos y contencioso en materia de extranjería, expulsión y medidas cautelares.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Solicitud de autorización de residencia y trabajo por arraigo»
- «Recurso de reposición por silencio positivo en la residencia de larga duración»
- «Solicitud de suspensión cautelar de una expulsión»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-extranjeria-y-trabajo:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (5)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0988 | Recurso contencioso-administrativo contra la denegación del visado de reagrupación familiar | `recurso-contencioso-administrativo-contra-denegacion-lab-0988` |
| LAB-0993 | Solicitud de ejecución forzosa de sentencia firme en un procedimiento abreviado de extranjería | `solicitud-ejecucion-forzosa-sentencia-firme-lab-0993` |
| LAB-0994 | Solicitud de ejecución forzosa de la sentencia que reconoce la renovación de residencia y trabajo | `solicitud-ejecucion-forzosa-sentencia-reconoce-lab-0994` |
| LAB-0999 | Recurso contencioso contra la denegación consular del visado de residencia | `recurso-contencioso-contra-denegacion-consular-visado-lab-0999` |
| LAB-1000 | Demanda contencioso-administrativa por la denegación de un visado exento de autorización de trabajo | `demanda-contencioso-administrativa-denegacion-visado-lab-1000` |

### Contestaciones, oposiciones y alegaciones (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-1027 | Alegaciones contra el acta de infracción a un extranjero por trabajar por cuenta propia en España | `alegaciones-contra-acta-infraccion-extranjero-trabajar-lab-1027` |

### Recursos (2)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0997 | Recurso de reposición para que se reconozca por silencio positivo la residencia de larga duración | `recurso-reposicion-reconozca-silencio-positivo-lab-0997` |
| LAB-1026 | Recurso de reposición contra la sanción a un extranjero por trabajar por cuenta propia en España | `recurso-reposicion-contra-sancion-extranjero-trabajar-lab-1026` |

### Contratos, pactos y cláusulas (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0989 | Acuerdo entre la empresa y un alto directivo para su desplazamiento al extranjero | `acuerdo-entre-empresa-alto-directivo-desplazamiento-lab-0989` |

### Estatutos, actas, certificaciones y escrituras (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-1003 | Acta notarial de manifestaciones de los cónyuges para el visado de reagrupación familiar | `acta-notarial-manifestaciones-conyuges-visado-lab-1003` |

### Comunicaciones, requerimientos y cartas (12)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0987 | Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013 | `solicitud-movilidad-internacional-familiar-titular-ley-lab-0987` |
| LAB-0992 | Solicitud de medida cautelar en el recurso contencioso sobre reagrupación familiar | `solicitud-medida-cautelar-recurso-contencioso-sobre-lab-0992` |
| LAB-0995 | Carta poder para gestiones consulares de reagrupación familiar y autorización de salida del menor | `carta-poder-gestiones-consulares-reagrupacion-familiar-lab-0995` |
| LAB-0996 | Solicitud de residencia y trabajo por arraigo con limitación sectorial y geográfica | `solicitud-residencia-trabajo-arraigo-limitacion-lab-0996` |
| LAB-0998 | Solicitud para que se certifique la concesión por silencio de la residencia de larga duración | `solicitud-certifique-concesion-silencio-residencia-lab-0998` |
| LAB-1001 | Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional | `solicitud-autorizacion-trabajo-extranjeros-penados-lab-1001` |
| LAB-1005 | Comunicación individual de denuncia ante el Comité de Derechos Humanos de la ONU | `comunicacion-individual-denuncia-ante-comite-derechos-lab-1005` |
| LAB-1008 | Solicitud de residencia por razones humanitarias en el expediente de asilo | `solicitud-residencia-razones-humanitarias-expediente-lab-1008` |
| LAB-1009 | Solicitud de revocación de la orden de expulsión por arraigo | `solicitud-revocacion-orden-expulsion-arraigo-lab-1009` |
| LAB-1012 | Solicitud de suspensión cautelar de la expulsión de un extranjero en centro de internamiento | `solicitud-suspension-cautelar-expulsion-extranjero-lab-1012` |
| LAB-1013 | Solicitud urgente al juzgado de guardia de medida cautelar contra la denegación de entrada | `solicitud-urgente-juzgado-guardia-medida-cautelar-lab-1013` |
| LAB-1019 | Solicitud de reexamen de la inadmisión a trámite de la protección internacional en frontera | `solicitud-reexamen-inadmision-tramite-proteccion-lab-1019` |

### Escritos de trámite y otros (21)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0981 | Memoria de actividad de la empresa y perfil del puesto para desplazar y contratar extranjeros | `memoria-actividad-empresa-perfil-puesto-desplazar-lab-0981` |
| LAB-0982 | Silencio positivo en la modificación de autorización - certificado | `silencio-positivo-modificacion-autorizacion-certificado-lab-0982` |
| LAB-0983 | Silencio positivo en la residencia de larga duración - certificado | `silencio-positivo-residencia-larga-duracion-certificado-lab-0983` |
| LAB-0985 | Revocar la resolución de expulsión - solicitud | `revocar-resolucion-expulsion-solicitud-lab-0985` |
| LAB-0986 | Designar representante para tramitar visados | `designar-representante-tramitar-visados-lab-0986` |
| LAB-0991 | Escrito de alegaciones del extranjero frente a la propuesta de expulsión por estancia irregular | `escrito-alegaciones-extranjero-frente-propuesta-lab-0991` |
| LAB-1002 | Escrito de desistimiento de la solicitud de residencia y trabajo por cuenta ajena | `escrito-desistimiento-solicitud-residencia-trabajo-lab-1002` |
| LAB-1004 | Cuestionario de denuncia ante el Relator Especial de la ONU sobre derechos de los migrantes | `cuestionario-denuncia-ante-relator-especial-onu-sobre-lab-1004` |
| LAB-1006 | Escrito a la Comisaría que revoca el poder otorgado en un expediente de extranjería | `escrito-comisaria-revoca-poder-otorgado-expediente-lab-1006` |
| LAB-1010 | Memoria de la empresa para la residencia y trabajo en el marco de prestaciones transnacionales | `memoria-empresa-residencia-trabajo-marco-prestaciones-lab-1010` |
| LAB-1011 | Memoria del puesto que ocupará el trabajador extranjero | `memoria-puesto-ocupara-trabajador-extranjero-lab-1011` |
| LAB-1014 | Autorización del titular de la vivienda para la reagrupación familiar | `autorizacion-titular-vivienda-reagrupacion-familiar-lab-1014` |
| LAB-1015 | Escrito que amplía las alegaciones en el expediente de expulsión | `escrito-amplia-alegaciones-expediente-expulsion-lab-1015` |
| LAB-1016 | Escrito del extranjero que apodera a su letrado para recurrir en vía administrativa | `escrito-extranjero-apodera-letrado-recurrir-via-lab-1016` |
| LAB-1017 | Escrito que reclama la asistencia sanitaria gratuita de un menor extranjero | `escrito-reclama-asistencia-sanitaria-gratuita-menor-lab-1017` |
| LAB-1018 | Escrito que reclama la asistencia sanitaria gratuita de una extranjera en el embarazo y el parto | `escrito-reclama-asistencia-sanitaria-gratuita-lab-1018` |
| LAB-1020 | Petición de un documento que acredite que la autorización de trabajo sigue vigente | `peticion-documento-acredite-autorizacion-trabajo-sigue-lab-1020` |
| LAB-1022 | Impreso EX11 para pedir la residencia de larga duración o de larga duración UE | `impreso-ex11-pedir-residencia-larga-duracion-larga-lab-1022` |
| LAB-1023 | Impresos oficiales para iniciar procedimientos de documentación de extranjeros en España | `impresos-oficiales-iniciar-procedimientos-lab-1023` |
| LAB-1024 | Impreso EX13 para pedir la autorización de regreso a España | `impreso-ex13-pedir-autorizacion-regreso-espana-lab-1024` |
| LAB-1025 | Impreso EX17 para pedir la Tarjeta de Identidad de Extranjero | `impreso-ex17-pedir-tarjeta-identidad-extranjero-lab-1025` |
