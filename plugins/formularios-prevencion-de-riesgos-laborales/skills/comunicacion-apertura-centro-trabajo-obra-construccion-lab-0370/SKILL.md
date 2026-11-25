---
name: comunicacion-apertura-centro-trabajo-obra-construccion-lab-0370
description: "Comunicación de apertura del centro de trabajo en una obra de construcción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Comunicación de apertura del centro de trabajo en una obra de construcción

> Formulario **LAB-0370** del plugin **Prevención de riesgos laborales** (`formularios-prevencion-de-riesgos-laborales`) · Laboral › Prevención de riesgos laborales · normativa revisada el 25-11-2026.

## Qué es

Ficha práctica y modelo de la comunicación de apertura del centro de trabajo que, en las obras de construcción, debe presentar la empresa contratista ante la autoridad laboral competente antes del comienzo de los trabajos, acompañada del plan de seguridad y salud (art. 19 del Real Decreto 1627/1997).

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Comunicación de apertura del centro de trabajo en una obra de construcción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Comunicación de apertura del centro de trabajo en una obra de construcción” para mi caso». También puedes invocarla directamente con `/formularios-prevencion-de-riesgos-laborales:comunicacion-apertura-centro-trabajo-obra-construccion-lab-0370`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-prevencion-de-riesgos-laborales:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Prevención de riesgos laborales) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] DENOMINACIÓN (2 veces)
- [ ] DOMICILIO (2 veces)
- [ ] FECHA (2 veces)
- [ ] NIF (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] ACTIVIDAD
- [ ] AÑO
- [ ] CARGO
- [ ] COMUNIDAD AUTÓNOMA
- [ ] CÓDIGO DE CUENTA DE COTIZACIÓN
- [ ] DENOMINACIÓN DEL ÓRGANO COMPETENTE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DESCRIPCIÓN
- [ ] DIRECCIÓN DE LA OBRA
- [ ] DNI/NIE
- [ ] DURACIÓN
- [ ] DÍA
- [ ] MES
- [ ] NOMBRE O DENOMINACIÓN SOCIAL
- [ ] Nº DE INSCRIPCIÓN REA

## Normas que cita el formulario

- art. 19 Real Decreto 1627/1997

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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: La Orden TIN/1071/2010, de 27 de abril, no figura en la base consolidada consultada: su vigencia y el anexo de datos no se han podido comprobar (sin comprobar). Se mantiene la nota que remite al impreso de la comunidad autónoma.
- Junto a «…comprobar). Se mantiene la nota que remite al impreso de la comunidad autónoma.]»: el original no traía el texto del formulario (solo remitía al impreso oficial en PDF); se redacta de nuevo una ficha práctica y un modelo conforme a la normativa vigente. La comunicación se presenta en el impreso o formulario electrónico que tenga aprobado la comunidad autónoma donde radique la obra, ajustado a los datos exigidos por la Orden TIN/1071/2010, de 27 de abril; comprobar el formulario vigente en la sede electrónica de la autoridad laboral autonómica.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

FICHA PRÁCTICA

1. Qué es

La comunicación de apertura del centro de trabajo es la declaración por la que se pone en conocimiento de la autoridad laboral la apertura de un centro de trabajo o la reanudación de la actividad. En las obras de construcción tiene un régimen específico: debe ser previa al comienzo de los trabajos, la presentan únicamente los empresarios que tengan la consideración de contratistas y debe incluir el plan de seguridad y salud (art. 19.1 del RD 1627/1997).

2. Quién la presenta

Cada empresa contratista de la obra (no el promotor ni los subcontratistas ni los trabajadores autónomos), respecto de la obra en la que interviene.

3. Cuándo

Con carácter previo al comienzo de los trabajos. Deben comunicarse también las modificaciones relevantes de los datos declarados y, en su caso, la reanudación de la actividad.

4. Ante quién y por dónde

Ante la autoridad laboral de la comunidad autónoma en cuyo territorio se ubique la obra (en Ceuta y Melilla, la Administración General del Estado), normalmente por medios electrónicos a través de su sede electrónica, o en los registros del art. 16 de la Ley 39/2015. Las personas jurídicas están obligadas a relacionarse electrónicamente con la Administración (art. 14.2 de la Ley 39/2015).

5. Datos y documentos que se piden

Datos de la empresa contratista: denominación o razón social, NIF, domicilio social, código de cuenta de cotización, actividad económica, mutua colaboradora con la Seguridad Social o entidad gestora que cubre las contingencias profesionales, modalidad de organización preventiva y número de inscripción en el Registro de Empresas Acreditadas del sector de la construcción.

Datos de la obra: dirección o emplazamiento, tipo de obra, fecha prevista de inicio y duración, número máximo estimado de trabajadores, y número previsto de subcontratistas y trabajadores autónomos.

Datos del promotor, del proyectista o autor del proyecto, de la dirección facultativa y del coordinador o coordinadores en materia de seguridad y salud durante la elaboración del proyecto y durante la ejecución de la obra, en su caso.

Plan de seguridad y salud en el trabajo, aprobado conforme al art. 7 del RD 1627/1997 (por el coordinador en materia de seguridad y salud durante la ejecución de la obra o, cuando no sea necesaria su designación, por la dirección facultativa).

Identificación y firma de la persona que realiza la comunicación en nombre de la empresa contratista.

6. Obligaciones relacionadas

El plan de seguridad y salud debe estar a disposición permanente de la Inspección de Trabajo y Seguridad Social y de los técnicos de los órganos especializados en seguridad y salud de las Administraciones públicas (art. 19.2 del RD 1627/1997).

Las empresas contratistas y subcontratistas deben estar inscritas en el Registro de Empresas Acreditadas y el contratista debe disponer del Libro de Subcontratación (Ley 32/2006, de 18 de octubre, reguladora de la subcontratación en el sector de la construcción, y Real Decreto 1109/2007, de 24 de agosto).

7. Normativa aplicable

Real Decreto 1627/1997, de 24 de octubre, por el que se establecen disposiciones mínimas de seguridad y de salud en las obras de construcción, arts. 7 y 19.

Orden TIN/1071/2010, de 27 de abril, sobre los requisitos y datos que deben reunir las comunicaciones de apertura o de reanudación de actividades en los centros de trabajo.

Ley 31/1995, de 8 de noviembre, de Prevención de Riesgos Laborales.

Ley 32/2006, de 18 de octubre, y Real Decreto 1109/2007, de 24 de agosto.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero `assets/formulario.md` (el formulario que vas a rellenar, en la carpeta de esta skill) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `assets/formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 11 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
