---
name: despido-colectivo-acuerdo-demanda-sindicatos-no-lo-lab-0559
description: "Despido colectivo con acuerdo - demanda de sindicatos que no lo firmaron. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Despido colectivo con acuerdo - demanda de sindicatos que no lo firmaron

> Formulario **LAB-0559** del plugin **Despido colectivo y ERTE** (`formularios-ere-y-erte`) · Laboral › Despido colectivo y ERTE · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Despido colectivo con acuerdo - demanda de sindicatos que no lo firmaron» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Despido colectivo con acuerdo - demanda de sindicatos que no lo firmaron” para mi caso». También puedes invocarla directamente con `/formularios-ere-y-erte:despido-colectivo-acuerdo-demanda-sindicatos-no-lo-lab-0559`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-ere-y-erte:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Despido colectivo y ERTE) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (16 veces)
- [ ] NOMBRE Y APELLIDOS (12 veces)
- [ ] CALLE (10 veces)
- [ ] NÚMERO (10 veces)
- [ ] DNI/NIE (4 veces)
- [ ] AÑO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DÍA
- [ ] FECHA
- [ ] LUGAR
- [ ] MES

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

- Al principio del formulario: Despido colectivo: art. 51 ET (consultas de hasta 30 días, 15 si menos de 50 trabajadores; comisión constituida en 7 días o 15 sin representantes; plan de recolocación externa de al menos seis meses si afecta a más de 50) y RD 1483/2012.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Si el despido extiende sus efectos al ámbito territorial de una Comunidad Autónoma, es competente para conocer de la demanda la Sala de lo Social del Tribunal Superior de Justicia de dicha Comunidad. Si extiende sus efectos a un ámbito territorial superior al de una Comunidad Autónoma, es competente la Sala de lo Social de la Audiencia Nacional.

(2) La demanda puede ser presentada por todos los representantes de los trabajadores de la empresa o sólo por parte de ellos, siempre que el acuerdo de presentar la demanda se adopte por la mayoría de miembros del comité de empresa ya que, al tratarse de un órgano colegiado, sus decisiones han de ser adoptadas por acuerdo mayoritario de sus miembros.

Asimismo puede presentarse por los representantes sindicales de un solo sindicato o de varios, siempre que tengan implantación suficiente en el ámbito del despido colectivo. Si no tienen implantación suficiente no están legitimados para presentar la demanda –STS de 21 de octubre de 2014, recurso 11/2014.

(3) En el caso de que el período de consultas hubiera finalizado con acuerdo, los representantes de los trabajadores, que formulan la demanda y no firmaron dicho acuerdo, deberán demandar a los firmantes del mismo (artículo 124.4).

(4) La demanda deberá presentarse en el plazo de caducidad de veinte días desde la fecha del acuerdo alcanzado en el período de consultas o de la notificación a los representantes de los trabajadores de la decisión empresarial de despido colectivo.

(5) A tenor del artículo 51.1 ET, se entiende que concurren causas organizativas cuando se produzcan cambios, entre otros, en el ámbito de los sistemas y métodos de trabajo del personal o en el modo de organizar la producción y causas productivas cuando se produzcan cambios, entre otros, en la demanda de los productos o servicios que la empresa pretende colocar en el mercado.

(6) La demanda podrá fundarse en los siguientes motivos:

a) Que no concurre la causa legal indicada en la comunicación escrita.

b) Que no se ha realizado el período de consultas o entregado la documentación prevista en el artículo 51.2 ET.

c) Que la decisión extintiva se ha adoptado con fraude, dolo, coacción o abuso de derecho.

d) Que la decisión extintiva se ha efectuado vulnerando derechos fundamentales y libertades públicas.

(7) El artículo 51.1 ET dispone que se entenderá por despido colectivo la extinción de contratos de trabajo fundada en causas económicas, técnicas, organizativas o de producción cuando, en un período de noventa días la extinción afecta al menos a;

1-Diez trabajadores, en las empresas que ocupen menos de cien trabajadores.

2-El 10% del número de trabajadores de la empresa en aquellas que ocupen entre cien y trescientos trabajadores

3-Treinta trabajadores en las empresas que ocupen más de trescientos trabajadores.

4-La totalidad de la plantilla de la empresa, siempre que el número de trabajadores afectados sea superior a cinco, cuando aquel se produzca como consecuencia de la cesación total de su actividad empresarial.

La sentencia declarará nula la decisión extintiva cuando el empresario no haya realizado el período de consultas o entregado la documentación prevista en el artículo 51.2 ET o cuando la medida empresarial se haya efectuado con vulneración de derechos fundamentales y libertades públicas. La sentencia declarará no ajustada a derecho la decisión extintiva cuando el empresario no haya acreditado la concurrencia de la causa legal indicada en la comunicación extintiva (artículo 124.11 LRJS).

(8) El número de trabajadores de la empresa es importante para saber si ha de seguirse el cauce del despido colectivo (artículo 51.1 ET).

(9) Así lo establece el artículo 64.1 LRJS.

(10) Así está previsto en el artículo 124.11 párrafo 3º LRJS.

(11) Si el demandante va a acudir a juicio asistido de letrado o representado por graduado social o procurador, lo hará constar en la demanda por medio de OTROSÍ (véase demanda de despido tipo).

Si el demandante quiere solicitar la práctica de pruebas, lo hará asimismo por medio de OTROSÍ (véase demanda de despido tipo).

════════════════════════════════════════════════════════════════════════


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
