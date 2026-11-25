---
name: alegaciones-acta-infraccion-informacion-consulta-lab-0685
description: "Alegaciones al acta de infracción por información y consulta en sociedades europeas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alegaciones al acta de infracción por información y consulta en sociedades europeas

> Formulario **LAB-0685** del plugin **Inspección de Trabajo y sanciones administrativas** (`formularios-inspeccion-de-trabajo`) · Laboral › Inspección de Trabajo y sanciones administrativas · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **contestaciones, oposiciones y alegaciones**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alegaciones al acta de infracción por información y consulta en sociedades europeas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alegaciones al acta de infracción por información y consulta en sociedades europeas” para mi caso». También puedes invocarla directamente con `/formularios-inspeccion-de-trabajo:alegaciones-acta-infraccion-informacion-consulta-lab-0685`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-inspeccion-de-trabajo:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Inspección de Trabajo y sanciones administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (6 veces)
- [ ] FECHA (3 veces)
- [ ] NOMBRE Y APELLIDOS (3 veces)
- [ ] IMPORTE (2 veces)
- [ ] DESCRIBIR
- [ ] DNI/NIE
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] Nº
- [ ] NÚMERO
- [ ] ÓRGANO AL QUE SE DIRIGE

## Normas que cita el formulario

- art. 52.1.b Real Decreto Legislativo 5/2000
- art. 17.1 Real Decreto 928/1998

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

- Al principio del formulario: Alegaciones: 15 días hábiles ante el órgano instructor (art. 17.1 RD 928/1998; art. 52.1.b LISOS). Si la sanción es solo pecuniaria, en el mismo plazo cabe pagar con reducción del 40 % renunciando a recursos (arts. 14.6 y 17.1). El expediente caduca a los 6 meses desde la fecha del acta hasta la notificación de la resolución (art. 20.3).
- Junto a «…ses desde la fecha del acta hasta la notificación de la resolución (art. 20.3).]»: Cuantías vigentes (art. 40.1 LISOS, red. RDL 32/2021): leves 70-750 €; graves 751-7.500 €; muy graves 7.501-225.018 €. Art. 10 bis LISOS en redacción de la Ley 4/2023 (vigente desde 2-3-2023).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de escrito de alegaciones, ante el órgano competente para dictar resolución, en el caso de acta de infracción grave o muy grave, por las siguientes causas establecidas en el artículo 10 bis de la LISOS, con solicitud de sobreseimiento del expediente sancionador o, subsidiariamente, reducción de la sanción:

- No facilitar a los representantes de los trabajadores las informaciones necesarias para la adecuada constitución de la comisión negociadora

- Trasgresión de los derechos de reunión de la comisión negociadora, del órgano de representación de los trabajadores o de los representantes de los trabajadores

- Trasgresión de los derechos de la comisión negociadora, del órgano de representación y de los representantes de los trabajadores, en materia de recursos financieros y materiales

- No convocar la comisión negociadora y las reuniones del órgano de representación de los trabajadores con el órgano competente

- Trasgresión de los derechos y garantías de los miembros de la comisión negociadora, de los miembros del órgano de representación y de los representantes de los trabajadores

- Acciones u omisiones que impidan el inicio y desarrollo de la negociación sobre la implicación de los trabajadores

- Acciones u omisiones que impidan el funcionamiento de la comisión negociadora, del órgano de representación de los trabajadores, o del procedimiento de información y consulta acordado

- Acciones u omisiones que impidan el ejercicio efectivo de los derechos de información, consulta y participación de los trabajadores

- Decisiones que supongan cualquier tipo de discriminación por razón de edad o discapacidad o favorables o adversas por razón de sexo, nacionalidad, origen, incluido el racial o étnico, estado civil, religión o convicciones, ideas políticas, orientación e identidad sexual, expresión de género, características sexuales, adhesión o no a un sindicato, a sus acuerdos o al ejercicio, en general, de las actividades sindicales, o lengua

- Constituir una sociedad europea o una sociedad cooperativa europea a fin de privar a los trabajadores de sus derechos

Actualizado conforme a la modificación del art. 10 bis LISOS introducida por la Ley 4/2023, de 28 de febrero, para la igualdad real y efectiva de las personas trans y para la garantía de los derechos de las personas LGTBI


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
