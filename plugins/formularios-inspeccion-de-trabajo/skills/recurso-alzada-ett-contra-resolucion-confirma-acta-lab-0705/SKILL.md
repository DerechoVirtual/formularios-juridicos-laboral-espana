---
name: recurso-alzada-ett-contra-resolucion-confirma-acta-lab-0705
description: "Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción

> Formulario **LAB-0705** del plugin **Inspección de Trabajo y sanciones administrativas** (`formularios-inspeccion-de-trabajo`) · Laboral › Inspección de Trabajo y sanciones administrativas · normativa revisada el 25-11-2026.

## Qué es

Recurso de alzada de una empresa de trabajo temporal contra la resolución que confirma un acta de infracción en materia de prevención de riesgos laborales levantada tras el accidente de trabajo de una persona trabajadora cedida. Se interpone en el plazo de un mes ante el órgano superior competente (art. 23 del RD 928/1998 y arts. 121 y 122 de la Ley 39/2015).

Es un modelo de tipo **recursos**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción” para mi caso». También puedes invocarla directamente con `/formularios-inspeccion-de-trabajo:recurso-alzada-ett-contra-resolucion-confirma-acta-lab-0705`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-inspeccion-de-trabajo:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Inspección de Trabajo y sanciones administrativas) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE DEL TRABAJADOR ACCIDENTADO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] Nº (2 veces)
- [ ] Nº DE ACTA (2 veces)
- [ ] Nº DE RESOLUCIÓN (2 veces)
- [ ] SEDE (2 veces)
- [ ] CARGO, P. EJ. DIRECTOR/A-GERENTE
- [ ] DENOMINACIÓN SOCIAL
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA USUARIA
- [ ] DESCRIPCIÓN DEL INCUMPLIMIENTO IMPUTADO EN EL ACTA
- [ ] DNI/NIE
- [ ] DOMICILIO
- [ ] IMPORTE
- [ ] IMPORTE EN CIFRA
- [ ] IMPORTE EN LETRA
- [ ] NIF
- [ ] Nº DE EXPEDIENTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] RIESGO PREVISIBLE, P. EJ. EL DESLIZAMIENTO DE LAS CHAPAS INFERIORES
- [ ] ÓRGANO COMPETENTE PARA RESOLVER
- [ ] ÓRGANO QUE DICTÓ LA RESOLUCIÓN
- [ ] ÓRGANO SUPERIOR COMPETENTE PARA RESOLVER EL RECURSO DE ALZADA

## Normas que cita el formulario

- art. 121 Ley 39/2015
- art. 4 Real Decreto 216/1999

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

### Avisos de actualización (4) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: La STSJ Cataluña de 18-10-2001 resolvió una reclamación de responsabilidad por daños derivados de accidente, no una sanción administrativa: se invoca por analogía.
- Junto a «… derivados de accidente, no una sanción administrativa: se invoca por analogía.]»: Se mantiene la nota de revisión sobre la obligación formativa de la ETT (art. 12.3 Ley 14/1994 y art. 3.3 RD 216/1999), que debe adaptarse a los hechos.
- Junto a «…guridad y salud en el trabajo en el ámbito de las empresas de trabajo temporal).»: el artículo 12.3 de la Ley 14/1994 y el artículo 3.3 del RD 216/1999 obligan a la ETT a asegurarse, antes de la puesta a disposición, de que el trabajador posee la formación teórica y práctica en prevención necesaria para el puesto y, en caso contrario, a facilitársela; adaptar este motivo a los hechos (por ejemplo, acreditando la formación impartida o comprobada por la ETT).
- Junto a «…ADO]. Es justicia que pido en [LOCALIDAD], a [FECHA]. Fdo.: [NOMBRE Y APELLIDOS]»: no cabe recurso de alzada si la empresa ha abonado la sanción con carácter previo a la resolución en los términos del artículo 14.6 del RD 928/1998. Transcurridos tres meses desde la interposición sin resolución, el recurso puede entenderse desestimado y queda expedita la vía jurisdiccional (art. 23.2 del RD 928/1998), que para las sanciones en materia laboral es la del orden social (art. 2 de la Ley 36/2011, reguladora de la jurisdicción social).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

- Ninguna.

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
