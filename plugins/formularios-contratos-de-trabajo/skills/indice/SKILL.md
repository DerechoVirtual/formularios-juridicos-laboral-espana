---
name: indice
description: "Índice de los 136 formularios de Contratos de trabajo y contratación laboral. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Contratos de trabajo y contratación laboral: índice de formularios

> Plugin `formularios-contratos-de-trabajo` · 136 formularios · normativa revisada el 25-11-2026.

## Qué es

Para contratar: contratos indefinidos, temporales y formativos tras la reforma de 2021, fijos discontinuos, relaciones laborales especiales (alta dirección, deportistas, artistas, representantes de comercio, hogar), periodo de prueba, pactos y cláusulas del contrato, ETT y cesión de trabajadores, y su información y comunicación.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Contrato de trabajo indefinido a tiempo completo»
- «Contrato de trabajo de deportista profesional»
- «Pacto de no competencia postcontractual»

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

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-contratos-de-trabajo:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Recursos (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0106 | Recurso del aspirante contra la denegación de su admisión como socio trabajador de cooperativa | `recurso-aspirante-contra-denegacion-admision-como-lab-0106` |

### Contratos, pactos y cláusulas (82)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0021 | Contrato indefinido del Plan de Recuperación (en valenciano) | `contrato-indefinido-plan-recuperacion-valenciano-lab-0021` |
| LAB-0022 | Contrato de trabajo de pescadores (en inglés) | `contrato-trabajo-pescadores-ingles-lab-0022` |
| LAB-0023 | Contrato de trabajo de pescadores (en euskera) | `contrato-trabajo-pescadores-euskera-lab-0023` |
| LAB-0024 | Contrato de trabajo de pescadores (en catalán) | `contrato-trabajo-pescadores-catalan-lab-0024` |
| LAB-0025 | Contrato de trabajo de pescadores (en gallego) | `contrato-trabajo-pescadores-gallego-lab-0025` |
| LAB-0026 | Contrato de trabajo de pescadores (en valenciano) | `contrato-trabajo-pescadores-valenciano-lab-0026` |
| LAB-0027 | Contrato indefinido del Plan de Recuperación (en catalán) | `contrato-indefinido-plan-recuperacion-catalan-lab-0027` |
| LAB-0028 | Contrato indefinido del Plan de Recuperación (en euskera) | `contrato-indefinido-plan-recuperacion-euskera-lab-0028` |
| LAB-0029 | Contrato indefinido del Plan de Recuperación (en gallego) | `contrato-indefinido-plan-recuperacion-gallego-lab-0029` |
| LAB-0030 | Contrato indefinido del Plan de Recuperación | `contrato-indefinido-plan-recuperacion-lab-0030` |
| LAB-0031 | Contrato de formación en alternancia del Plan de Recuperación (en valenciano) | `contrato-formacion-alternancia-plan-recuperacion-lab-0031` |
| LAB-0032 | Contrato formativo de práctica profesional del Plan de Recuperación (en valenciano) | `contrato-formativo-practica-profesional-plan-lab-0032` |
| LAB-0033 | Contrato formativo de práctica profesional del Plan de Recuperación (en catalán) | `contrato-formativo-practica-profesional-plan-lab-0033` |
| LAB-0034 | Contrato de formación en alternancia del Plan de Recuperación (en euskera) | `contrato-formacion-alternancia-plan-recuperacion-lab-0034` |
| LAB-0035 | Contrato de formación en alternancia del Plan de Recuperación (en catalán) | `contrato-formacion-alternancia-plan-recuperacion-lab-0035` |
| LAB-0036 | Contrato de formación en alternancia del Plan de Recuperación (en gallego) | `contrato-formacion-alternancia-plan-recuperacion-lab-0036` |
| LAB-0037 | Contrato formativo de práctica profesional del Plan de Recuperación (en euskera) | `contrato-formativo-practica-profesional-plan-lab-0037` |
| LAB-0038 | Contrato formativo de práctica profesional del Plan de Recuperación (en gallego) | `contrato-formativo-practica-profesional-plan-lab-0038` |
| LAB-0039 | Contrato formativo de práctica profesional del Plan de Recuperación | `contrato-formativo-practica-profesional-plan-lab-0039` |
| LAB-0040 | Contrato de formación en alternancia del Plan de Recuperación | `contrato-formacion-alternancia-plan-recuperacion-lab-0040` |
| LAB-0041 | Contrato temporal del Plan de Recuperación (en valenciano) | `contrato-temporal-plan-recuperacion-valenciano-lab-0041` |
| LAB-0042 | Contrato temporal del Plan de Recuperación (en gallego) | `contrato-temporal-plan-recuperacion-gallego-lab-0042` |
| LAB-0043 | Contrato temporal del Plan de Recuperación (en euskera) | `contrato-temporal-plan-recuperacion-euskera-lab-0043` |
| LAB-0044 | Contrato temporal del Plan de Recuperación (en catalán) | `contrato-temporal-plan-recuperacion-catalan-lab-0044` |
| LAB-0045 | Contrato temporal del Plan de Recuperación | `contrato-temporal-plan-recuperacion-lab-0045` |
| LAB-0046 | Contrato formativo para la práctica profesional (en valenciano) | `contrato-formativo-practica-profesional-valenciano-lab-0046` |
| LAB-0047 | Contrato formativo para la práctica profesional (en catalán) | `contrato-formativo-practica-profesional-catalan-lab-0047` |
| LAB-0048 | Contrato formativo para la práctica profesional (en gallego) | `contrato-formativo-practica-profesional-gallego-lab-0048` |
| LAB-0049 | Contrato formativo para la práctica profesional (en euskera) | `contrato-formativo-practica-profesional-euskera-lab-0049` |
| LAB-0050 | Contrato formativo en alternancia (en catalán) | `contrato-formativo-alternancia-catalan-lab-0050` |
| LAB-0051 | Contrato formativo en alternancia (en gallego) | `contrato-formativo-alternancia-gallego-lab-0051` |
| LAB-0052 | Contrato formativo en alternancia (en euskera) | `contrato-formativo-alternancia-euskera-lab-0052` |
| LAB-0053 | Contrato formativo en alternancia (en valenciano) | `contrato-formativo-alternancia-valenciano-lab-0053` |
| LAB-0054 | Contrato laboral temporal (en valenciano) | `contrato-laboral-temporal-valenciano-lab-0054` |
| LAB-0055 | Contrato laboral temporal (en gallego) | `contrato-laboral-temporal-gallego-lab-0055` |
| LAB-0056 | Contrato laboral temporal (en euskera) | `contrato-laboral-temporal-euskera-lab-0056` |
| LAB-0057 | Contrato laboral temporal (en catalán) | `contrato-laboral-temporal-catalan-lab-0057` |
| LAB-0058 | Contrato laboral indefinido (en gallego) | `contrato-laboral-indefinido-gallego-lab-0058` |
| LAB-0059 | Contrato laboral indefinido (en euskera) | `contrato-laboral-indefinido-euskera-lab-0059` |
| LAB-0060 | Contrato laboral indefinido (en valenciano) | `contrato-laboral-indefinido-valenciano-lab-0060` |
| LAB-0061 | Contrato laboral indefinido (en catalán) | `contrato-laboral-indefinido-catalan-lab-0061` |
| LAB-0062 | Contrato de actuación de toreros, novilleros y rejoneadores | `contrato-actuacion-toreros-novilleros-rejoneadores-lab-0062` |
| LAB-0063 | Contrato laboral de colaboración para formar una cuadrilla | `contrato-laboral-colaboracion-formar-cuadrilla-lab-0063` |
| LAB-0065 | Contrato de artistas de duración determinada (relación laboral especial) | `contrato-artistas-duracion-determinada-relacion-lab-0065` |
| LAB-0066 | Contrato de personal técnico y auxiliar artístico de duración determinada | `contrato-personal-tecnico-auxiliar-artistico-duracion-lab-0066` |
| LAB-0067 | Contrato de servicios profesionales | `contrato-servicios-profesionales-lab-0067` |
| LAB-0068 | Contrato de trabajo de pescadores | `contrato-trabajo-pescadores-lab-0068` |
| LAB-0072 | Cláusulas adicionales del contrato de grupo | `clausulas-adicionales-contrato-grupo-lab-0072` |
| LAB-0074 | Contrato del autónomo económicamente dependiente (TRADE) | `contrato-autonomo-economicamente-dependiente-trade-lab-0074` |
| LAB-0076 | Cláusulas adicionales del contrato de trabajo | `clausulas-adicionales-contrato-trabajo-lab-0076` |
| LAB-0078 | Contrato de patrón de embarcaciones de recreo | `contrato-patron-embarcaciones-recreo-lab-0078` |
| LAB-0081 | Acuerdo con voluntarios | `acuerdo-voluntarios-lab-0081` |
| LAB-0082 | Contrato de interinidad de profesor de religión | `contrato-interinidad-profesor-religion-lab-0082` |
| LAB-0083 | Contrato indefinido de profesor de religión | `contrato-indefinido-profesor-religion-lab-0083` |
| LAB-0084 | Contrato de personal civil de establecimientos militares | `contrato-personal-civil-establecimientos-militares-lab-0084` |
| LAB-0085 | Contrato laboral por tiempo indefinido | `contrato-laboral-tiempo-indefinido-lab-0085` |
| LAB-0086 | Contrato formativo en alternancia de trabajo y formación | `contrato-formativo-alternancia-trabajo-formacion-lab-0086` |
| LAB-0087 | Contrato laboral de duración determinada | `contrato-laboral-duracion-determinada-lab-0087` |
| LAB-0088 | Contrato formativo para obtener la práctica profesional adecuada a los estudios | `contrato-formativo-obtener-practica-profesional-lab-0088` |
| LAB-0091 | Acuerdo tripartito de cesión de un trabajador de la empresa cedente a la cesionaria | `acuerdo-tripartito-cesion-trabajador-empresa-cedente-lab-0091` |
| LAB-0092 | Contrato de formación como integrante de una cuadrilla taurina | `contrato-formacion-como-integrante-cuadrilla-taurina-lab-0092` |
| LAB-0094 | Contrato de trabajo de empleado de hogar adaptado a la regulación de 2011 | `contrato-trabajo-empleado-hogar-adaptado-regulacion-lab-0094` |
| LAB-0095 | Contrato entre el titular del hogar y el empleado para el servicio del hogar familiar | `contrato-entre-titular-hogar-empleado-servicio-hogar-lab-0095` |
| LAB-0096 | Contrato de la relación laboral especial de abogado en despacho | `contrato-relacion-laboral-especial-abogado-despacho-lab-0096` |
| LAB-0097 | Cláusula adicional del contrato que asigna al trabajador su grupo profesional | `clausula-adicional-contrato-asigna-trabajador-grupo-lab-0097` |
| LAB-0102 | Acuerdo entre entidades deportivas para la cesión temporal de un deportista profesional | `acuerdo-entre-entidades-deportivas-cesion-temporal-lab-0102` |
| LAB-0107 | Acuerdo del consejo rector que deniega la admisión de un socio trabajador en la cooperativa | `acuerdo-consejo-rector-deniega-admision-socio-lab-0107` |
| LAB-0108 | Acuerdo del consejo rector que admite a un socio trabajador en la cooperativa | `acuerdo-consejo-rector-admite-socio-trabajador-lab-0108` |
| LAB-0113 | Contrato de contrata de obras o servicios entre empresa principal y contratista | `contrato-contrata-obras-servicios-entre-empresa-lab-0113` |
| LAB-0114 | Contrato de alta dirección para un trabajador promocionado internamente | `contrato-alta-direccion-trabajador-promocionado-lab-0114` |
| LAB-0115 | Contrato de trabajo de facultativo residente en formación sanitaria especializada | `contrato-trabajo-facultativo-residente-formacion-lab-0115` |
| LAB-0119 | Contrato de opción sobre acciones (stock options) ligado a un contrato de alta dirección | `contrato-opcion-sobre-acciones-stock-options-ligado-lab-0119` |
| LAB-0122 | Contrato indefinido de artista en espectáculos públicos (relación laboral especial) | `contrato-indefinido-artista-espectaculos-publicos-lab-0122` |
| LAB-0123 | Contrato de trabajo de alta dirección (relación laboral especial) | `contrato-trabajo-alta-direccion-relacion-laboral-lab-0123` |
| LAB-0124 | Contrato de trabajo de deportista profesional (relación laboral especial) | `contrato-trabajo-deportista-profesional-relacion-lab-0124` |
| LAB-0125 | Contrato de trabajo de representante de comercio (relación laboral especial) | `contrato-trabajo-representante-comercio-relacion-lab-0125` |
| LAB-0126 | Contrato de trabajo de un jugador de fútbol profesional con su club | `contrato-trabajo-jugador-futbol-profesional-club-lab-0126` |
| LAB-0129 | Contrato tipo del convenio colectivo para jugadores profesionales de baloncesto de la Liga ACB | `contrato-tipo-convenio-colectivo-jugadores-lab-0129` |
| LAB-0130 | Contrato tipo del convenio colectivo para jugadores profesionales de balonmano de la Liga ASOBAL | `contrato-tipo-convenio-colectivo-jugadores-lab-0130` |
| LAB-0131 | Contrato tipo del convenio colectivo para corredores ciclistas profesionales | `contrato-tipo-convenio-colectivo-corredores-ciclistas-lab-0131` |
| LAB-0132 | Contrato tipo del convenio colectivo para futbolistas profesionales | `contrato-tipo-convenio-colectivo-futbolistas-lab-0132` |
| LAB-0140 | Contrato de trabajo de grupo entre la empresa y el jefe del grupo | `contrato-trabajo-grupo-entre-empresa-jefe-grupo-lab-0140` |

### Estatutos, actas, certificaciones y escrituras (5)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0100 | Anuncio a los trabajadores temporales de las vacantes existentes en la empresa | `anuncio-trabajadores-temporales-vacantes-existentes-lab-0100` |
| LAB-0103 | Certificado de la entidad que acredita las tareas de voluntariado realizadas | `certificado-entidad-acredita-tareas-voluntariado-lab-0103` |
| LAB-0134 | Certificado de la empresa, sin efectos académicos, de las prácticas realizadas por el trabajador | `certificado-empresa-sin-efectos-academicos-practicas-lab-0134` |
| LAB-0137 | Certificado de la empresa al terminar el contrato para la formación y el aprendizaje | `certificado-empresa-terminar-contrato-formacion-lab-0137` |
| LAB-0138 | Certificado de la empresa al terminar el contrato para la obtención de práctica profesional | `certificado-empresa-terminar-contrato-obtencion-lab-0138` |

### Comunicaciones, requerimientos y cartas (9)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0089 | Carta de la empresa al trabajador fijo discontinuo que le comunica la interrupción de la actividad | `carta-empresa-trabajador-fijo-discontinuo-le-comunica-lab-0089` |
| LAB-0104 | Carta de recomendación de la empresa sobre un trabajador | `carta-recomendacion-empresa-sobre-trabajador-lab-0104` |
| LAB-0105 | Aviso de fijeza por superar la duración máxima del contrato por circunstancias de la producción | `aviso-fijeza-superar-duracion-maxima-contrato-lab-0105` |
| LAB-0112 | Comunicación de la contratista a cada trabajador de la empresa principal donde prestará servicios | `comunicacion-contratista-cada-trabajador-empresa-lab-0112` |
| LAB-0116 | Aviso a la persona trabajadora de la prórroga de su contrato acogido a un Real Decreto | `aviso-persona-trabajadora-prorroga-contrato-acogido-lab-0116` |
| LAB-0120 | Solicitud a la autoridad laboral para emplear a menores en trabajos prohibidos | `solicitud-autoridad-laboral-emplear-menores-trabajos-lab-0120` |
| LAB-0127 | Requerimiento al representante de comercio para que entregue sus partes diarios de trabajo | `requerimiento-representante-comercio-entregue-partes-lab-0127` |
| LAB-0141 | Comunicación de la ETT a la empresa usuaria con la documentación de los trabajadores cedidos | `comunicacion-ett-empresa-usuaria-documentacion-lab-0141` |
| LAB-0142 | Comunicación de la empresa usuaria a la ETT de los incumplimientos del trabajador cedido | `comunicacion-empresa-usuaria-ett-incumplimientos-lab-0142` |

### Escritos de trámite y otros (39)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0004 | Información al trabajador sobre los elementos esenciales del contrato | `informacion-trabajador-sobre-elementos-esenciales-lab-0004` |
| LAB-0005 | Información al trabajador sobre los elementos esenciales del contrato (en valenciano) | `informacion-trabajador-sobre-elementos-esenciales-lab-0005` |
| LAB-0006 | Información al trabajador sobre los elementos esenciales del contrato (en euskera) | `informacion-trabajador-sobre-elementos-esenciales-lab-0006` |
| LAB-0007 | Información al trabajador sobre los elementos esenciales del contrato (en gallego) | `informacion-trabajador-sobre-elementos-esenciales-lab-0007` |
| LAB-0008 | Información al trabajador sobre los elementos esenciales del contrato (en catalán) | `informacion-trabajador-sobre-elementos-esenciales-lab-0008` |
| LAB-0009 | Información al trabajador sobre los elementos esenciales del contrato - carta | `informacion-trabajador-sobre-elementos-esenciales-lab-0009` |
| LAB-0010 | Pedir información sobre los elementos esenciales de la relación laboral | `pedir-informacion-sobre-elementos-esenciales-relacion-lab-0010` |
| LAB-0011 | Llamamiento a la actividad del fijo discontinuo - comunicación de la empresa | `llamamiento-actividad-fijo-discontinuo-comunicacion-lab-0011` |
| LAB-0012 | Prórroga del contrato de trabajo acogida al Real Decreto - comunicación (en valenciano) | `prorroga-contrato-trabajo-acogida-real-decreto-lab-0012` |
| LAB-0013 | Prórroga del contrato de trabajo acogida al Real Decreto - comunicación (en euskera) | `prorroga-contrato-trabajo-acogida-real-decreto-lab-0013` |
| LAB-0014 | Prórroga del contrato de trabajo acogida al Real Decreto - comunicación (en gallego) | `prorroga-contrato-trabajo-acogida-real-decreto-lab-0014` |
| LAB-0015 | Prórroga del contrato de trabajo acogida al Real Decreto - comunicación (en catalán) | `prorroga-contrato-trabajo-acogida-real-decreto-lab-0015` |
| LAB-0016 | Llamamiento a la actividad de fijos discontinuos - comunicación (en catalán) | `llamamiento-actividad-fijos-discontinuos-comunicacion-lab-0016` |
| LAB-0017 | Llamamiento a la actividad de fijos discontinuos - comunicación (en gallego) | `llamamiento-actividad-fijos-discontinuos-comunicacion-lab-0017` |
| LAB-0018 | Llamamiento a la actividad de fijos discontinuos - comunicación (en euskera) | `llamamiento-actividad-fijos-discontinuos-comunicacion-lab-0018` |
| LAB-0019 | Llamamiento a la actividad de fijos discontinuos - comunicación (en valenciano) | `llamamiento-actividad-fijos-discontinuos-comunicacion-lab-0019` |
| LAB-0020 | Novación de fijo discontinuo a indefinido ordinario - acuerdo | `novacion-fijo-discontinuo-indefinido-ordinario-acuerdo-lab-0020` |
| LAB-0064 | Plan individual de formación | `plan-individual-formacion-lab-0064` |
| LAB-0069 | Pedir trabajar a distancia | `pedir-trabajar-distancia-lab-0069` |
| LAB-0070 | Plan formativo | `plan-formativo-lab-0070` |
| LAB-0071 | Currículum anónimo | `curriculum-anonimo-lab-0071` |
| LAB-0073 | Pedir que el contrato de trabajo conste por escrito | `pedir-contrato-trabajo-conste-escrito-lab-0073` |
| LAB-0075 | Memoria sobre la organización de una empresa de trabajo temporal | `memoria-sobre-organizacion-empresa-trabajo-temporal-lab-0075` |
| LAB-0077 | Interrupción de actividad del TRADE - comunicación | `interrupcion-actividad-trade-comunicacion-lab-0077` |
| LAB-0079 | Puesta a disposición - contrato | `puesta-disposicion-contrato-lab-0079` |
| LAB-0080 | Registro de contratos de puesta a disposición (CPD) | `registro-contratos-puesta-disposicion-cpd-lab-0080` |
| LAB-0090 | Petición del trabajador para pasar de jornada completa a contrato a tiempo parcial | `peticion-trabajador-pasar-jornada-completa-contrato-lab-0090` |
| LAB-0101 | Respuesta de la empresa que rechaza convertir el contrato a tiempo parcial o a tiempo completo | `respuesta-empresa-rechaza-convertir-contrato-tiempo-lab-0101` |
| LAB-0109 | Petición para ingresar como socio trabajador en una cooperativa | `peticion-ingresar-como-socio-trabajador-cooperativa-lab-0109` |
| LAB-0110 | Cuestionario de calidad de las acciones formativas organizadas por las empresas | `cuestionario-calidad-acciones-formativas-organizadas-lab-0110` |
| LAB-0111 | Cuestionario de calidad de las acciones de formación profesional para el empleo | `cuestionario-calidad-acciones-formacion-profesional-lab-0111` |
| LAB-0117 | Llamamiento a las personas trabajadoras fijas discontinuas para reincorporarse a la actividad | `llamamiento-personas-trabajadoras-fijas-discontinuas-lab-0117` |
| LAB-0118 | Encabezamiento del contrato de trabajo de un menor de edad o de un adulto con capacidad limitada | `encabezamiento-contrato-trabajo-menor-edad-adulto-lab-0118` |
| LAB-0121 | Autorización del representante legal para que trabaje un menor o un adulto con capacidad limitada | `autorizacion-representante-legal-trabaje-menor-adulto-lab-0121` |
| LAB-0128 | Precontrato de trabajo entre la empresa y el candidato | `precontrato-trabajo-entre-empresa-candidato-lab-0128` |
| LAB-0133 | Oferta de contrato tipo del convenio colectivo para jugadores de baloncesto de la Liga ACB | `oferta-contrato-tipo-convenio-colectivo-jugadores-lab-0133` |
| LAB-0135 | Escrito del trabajador cedido ilegalmente que opta por ser fijo en la empresa cesionaria | `escrito-trabajador-cedido-ilegalmente-opta-ser-fijo-lab-0135` |
| LAB-0136 | Copia básica del contrato de trabajo para la representación legal | `copia-basica-contrato-trabajo-representacion-legal-lab-0136` |
| LAB-0139 | Petición al Servicio Público de Empleo de certificado del tiempo trabajado con contratos formativos | `peticion-servicio-publico-empleo-certificado-tiempo-lab-0139` |
