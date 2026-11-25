---
name: conciliacion-laboral-personal-familiar-demanda-lab-0247
description: "Conciliación laboral, personal y familiar - demanda genérica de derechos. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Conciliación laboral, personal y familiar - demanda genérica de derechos

> Formulario **LAB-0247** del plugin **Jornada, vacaciones, permisos y conciliación** (`formularios-jornada-vacaciones-y-permisos`) · Laboral › Jornada, vacaciones, permisos y conciliación · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Conciliación laboral, personal y familiar - demanda genérica de derechos» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Conciliación laboral, personal y familiar - demanda genérica de derechos” para mi caso». También puedes invocarla directamente con `/formularios-jornada-vacaciones-y-permisos:conciliacion-laboral-personal-familiar-demanda-lab-0247`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-jornada-vacaciones-y-permisos:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Jornada, vacaciones, permisos y conciliación) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (14 veces)
- [ ] FECHA (5 veces)
- [ ] IMPORTE (3 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] CORREO ELECTRÓNICO
- [ ] LUGAR
- [ ] NIF
- [ ] Nº DE ARTÍCULO
- [ ] PARTE DEMANDADA
- [ ] SECTOR O EMPRESA
- [ ] SEDE
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 139 Ley 36/2011
- art. 2 LRJS
- art. 17.1 LRJS
- art. 139 LRJS
- art. 91.2 LRJS
- art. 64.1 LRJS

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

- Al principio del formulario: El art. 37.6 ET (reducción por cuidado de menor con cáncer o enfermedad grave) fue modificado por el RDL 31/2026 (BOE-A-2026-21872, vigente desde el 23-10-2026): extensión más allá de los 23 y 26 años con discapacidad del 65 % o grado III de dependencia, tratamiento continuado sin hospitalización y disfrute por ambos progenitores de forma alternativa o simultánea.
- Junto a «…talización y disfrute por ambos progenitores de forma alternativa o simultánea.]»: Adaptación del art. 34.8 ET: hasta que los hijos cumplan doce años, negociación de 15 días con presunción de concesión si no hay oposición motivada, y nulidad objetiva del despido o extinción por solicitarla o disfrutarla (arts. 53.4.b y 55.5.b, redacción LO 1/2025).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Las demandas en materia de derechos de conciliación de la vida familiar y laboral deben tramitarse por la modalidad procesal especial regulada en el artículo 139 de la LRJS. Este procedimiento es de carácter urgente y preferente, y está específicamente diseñado para resolver discrepancias entre la persona trabajadora y la empresa en relación con el ejercicio de los derechos de conciliación reconocidos legal o convencionalmente, incluyendo la adaptación de jornada, la concreción horaria y otras medidas análogas.

Esta modalidad procesal se utiliza en supuestos en que se reclaman asuntos sobre reducción de jornada por lactancia, reducción de jornada por cuidado de hijo o familiar dependiente, suspensión del contrato por nacimiento, adopción, guarda con fines de adopción o acogimiento familiar, excedencia por cuidado de hijo o familiar, distribución de horario o cambio de turno, etc. Pero no corresponde a todas las cuestiones que puedan plantearse, sino únicamente respecto a la concreción horaria y la determinación del período de disfrute; otras cuestiones de contenido diverso sobre la materia (retribución, reparto del derecho, alternancia de su ejercicio, el derecho en sí mismo, etc.), deberán tramitarse mediante el proceso ordinario.

Este procedimiento es igualmente aplicable al ejercicio de los derechos de la trabajadora víctima de violencia de género establecidos en la ley, a la reducción de la jornada de trabajo con disminución proporcional del salario y a la reordenación del tiempo de trabajo, a través de la adaptación del horario, de la aplicación del horario flexible o de otras formas de ordenación del tiempo de trabajo que se utilicen en la empresa.

La demanda debe contener la identificación clara del derecho de conciliación que se reclama (por ejemplo, concreción horaria, adaptación de jornada, teletrabajo, cambio de centro de trabajo, etc.), los hechos en los que se fundamenta la pretensión, la referencia a la negativa o disconformidad empresarial y, en su caso, la cuantificación de los daños y perjuicios reclamados. Es relevante que la persona trabajadora y la empresa lleven al acto de conciliación y al juicio sus respectivas propuestas y alternativas de concreción, pudiendo acompañar informes de los órganos paritarios o de seguimiento de los planes de igualdad de la empresa.

En la demanda sobre derechos de conciliación puede acumularse la acción de daños y perjuicios causados al trabajador, exclusivamente por los derivados de la negativa del derecho o de la demora en la efectividad de la medida, de los que el empresario podrá exonerarse si hubiere dado cumplimiento, al menos provisional, a la medida propuesta por el trabajador.


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
