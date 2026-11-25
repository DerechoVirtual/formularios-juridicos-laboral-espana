---
name: escrito-pide-poner-disposicion-cantidad-avalada-lab-0850
description: "Escrito que pide poner a disposición la cantidad avalada por un tercero como garantía para recurrir. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito que pide poner a disposición la cantidad avalada por un tercero como garantía para recurrir

> Formulario **LAB-0850** del plugin **Proceso laboral: conciliación, demandas y escritos** (`formularios-laboral`) · Laboral › Proceso laboral (conciliación, demandas, recursos y ejecución) · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito que pide poner a disposición la cantidad avalada por un tercero como garantía para recurrir» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito que pide poner a disposición la cantidad avalada por un tercero como garantía para recurrir” para mi caso». También puedes invocarla directamente con `/formularios-laboral:escrito-pide-poner-disposicion-cantidad-avalada-lab-0850`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-laboral:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Proceso laboral: conciliación, demandas y escritos) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR
- [ ] FECHA
- [ ] LOCALIDAD
- [ ] LUGAR
- [ ] Nº
- [ ] SEDE

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

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

### Avisos de actualización (1) — se aplican en el texto, nunca se copian en el documento

- Junto a «…ÓN DE LO SOCIAL DEL TRIBUNAL DE INSTANCIA DE [SEDE] – PLAZA N.º [Nº] [COMPLETAR]»: Desde el 31-12-2025 los Juzgados de lo Social son la Sección de lo Social del Tribunal de Instancia; el Tribunal no se numera, se numera la plaza. En la demanda inicial (antes del reparto) se omite la plaza. Fuente: arts. 84.2.i) y 94 LOPJ (red. LO 1/2025); LO 1/2025 DA 1.ª y DT 1.ª (la plaza conserva la numeración del Juzgado; Juzgados de lo Social transformados el 31-12-2025); LOPJ (LO 6/1985), BOE-A-1985-12666; LO 1/2025, BOE-A-2025-76.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

El art. 230.1 LRJS expresa que cuando la sentencia impugnada hubiere condenado al pago de cantidad, será indispensable que el recurrente que no gozare del derecho de asistencia jurídica gratuita acredite, al anunciar el recurso de suplicación o al preparar el recurso de casación, haber consignado en la oportuna entidad de crédito y en la cuenta de depósitos y consignaciones abierta a nombre del órgano jurisdiccional, la cantidad objeto de la condena, pudiendo sustituirse la consignación en metálico por el aseguramiento mediante aval solidario de duración indefinida y pagadero a primer requerimiento emitido por entidad de crédito. En este último caso, el documento de aseguramiento quedará registrado y depositado en la oficina judicial. El Letrado de la Administración de Justicia expedirá testimonio del mismo para su unión a autos, facilitando el oportuno recibo.

En el caso de condena solidaria, la obligación de consignación o aseguramiento alcanzará a todos los condenados con tal carácter, salvo que la consignación o el aseguramiento, aunque efectuado solamente por alguno de los condenados, tuviera expresamente carácter solidario respecto de todos ellos para responder íntegramente de la condena que pudiera finalmente recaer frente a cualquiera de los mismos.

Cuando la condena se haya efectuado por primera vez en la sentencia de suplicación, o se haya incrementado en la misma la cuantía previamente reconocida en la sentencia de instancia, la consignación o aseguramiento se efectuarán por primera vez, o se complementarán en la medida correspondiente, al preparar el recurso de casación.

Los requisitos de consignación y aseguramiento de la condena deben justificarse, junto con la constitución del depósito necesario para recurrir, en su caso, en el momento del anuncio del recurso de suplicación o de la preparación del recurso de casación. Si el anuncio o la preparación del recurso se hubiere efectuado por medio de mera manifestación en el momento de la notificación de la sentencia, el depósito y la consignación o aseguramiento podrá efectuarse hasta la expiración del plazo establecido para el anuncio o preparación del recurso, debiendo en este último caso acreditar dichos extremos dentro del mismo plazo ante la oficina judicial mediante los justificantes correspondientes (art. 230.3 LRJS).

Si el recurrente no hubiere efectuado la consignación o aseguramiento de la cantidad objeto de condena, el Tribunal tendrá por no anunciado o por no preparado el recurso de suplicación o de casación, según proceda, y declararán la firmeza de la resolución mediante auto contra el que podrá recurrirse en queja ante la Sala que hubiera debido conocer del recurso (art. 230.4 LRJS).

En caso de defectos en la consignación (insuficiencia, omisión de los justificantes, errores, problemas de acreditación, etc.), el Letrado de la Administración de Justicia concederá al recurrente, con carácter previo a que se resuelva sobre el anuncio o preparación, un plazo de cinco días para la subsanación de los defectos advertidos; de no efectuarse la subsanación en tiempo y forma, se dictará auto poniendo fin al trámite del recurso, quedando firme la resolución. Contra dicho auto podrá recurrirse en queja ante la Sala que hubiera debido conocer del recurso (art. 230, apartados 5 y 6 LRJS).


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
