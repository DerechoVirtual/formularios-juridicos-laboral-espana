---
name: solicitud-autorizacion-trabajo-extranjeros-penados-lab-1001
description: "Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional

> Formulario **LAB-1001** del plugin **Extranjería y movilidad internacional de trabajadores** (`formularios-extranjeria-y-trabajo`) · Laboral › Extranjería y movilidad internacional de trabajadores · normativa revisada el 25-11-2026.

## Qué es

Ficha práctica sobre la autorización de trabajo de las personas extranjeras penadas que cumplen condena en régimen abierto (tercer grado) o en libertad condicional, supuesto en el que la resolución penitenciaria de clasificación o el auto judicial que la acuerda tiene validez de autorización de trabajo por cuenta ajena para desarrollar actividades laborales durante el cumplimiento, con un modelo de solicitud.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional” para mi caso». También puedes invocarla directamente con `/formularios-extranjeria-y-trabajo:solicitud-autorizacion-trabajo-extranjeros-penados-lab-1001`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-extranjeria-y-trabajo:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Extranjería y movilidad internacional de trabajadores) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AUTORIDAD PENITENCIARIA
- [ ] AÑO
- [ ] DENOMINACIÓN DEL CENTRO
- [ ] DENOMINACIÓN SOCIAL
- [ ] DOMICILIO O DIRECCIÓN ELECTRÓNICA A EFECTOS DE NOTIFICACIONES
- [ ] DURACIÓN
- [ ] DÍA
- [ ] IMPORTE
- [ ] JORNADA
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIE
- [ ] NIF
- [ ] Nº DE EXPEDIENTE
- [ ] Nº DE PASAPORTE
- [ ] PAÍS
- [ ] PROVINCIA
- [ ] PUESTO / OCUPACIÓN
- [ ] RELACIÓN DE DOCUMENTOS
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

### Avisos de actualización (2) — se aplican en el texto, nunca se copian en el documento

- Al principio del formulario: No se ha podido localizar con Jurisprudenciator el precepto del Reglamento aprobado por RD 1155/2024 que regula este supuesto; la base legal es el art. 36.1 LO 4/2000 (la autorización de trabajo no se concede conjuntamente con la de residencia en el caso de penados extranjeros que cumplen condena). Se mantiene la nota de revisión.
- Junto a «…o de penados extranjeros que cumplen condena). Se mantiene la nota de revisión.]»: el original no traía el texto del formulario (solo una frase y un enlace al procedimiento oficial); se redacta de nuevo una ficha práctica conforme a la normativa vigente. Comprobar en la hoja informativa oficial vigente de la Secretaría de Estado de Migraciones el precepto concreto del Reglamento de extranjería aprobado por Real Decreto 1155/2024, de 19 de noviembre, que regula este supuesto, así como el órgano ante el que se tramita y la documentación exigida.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

FICHA PRÁCTICA

1. Qué es

Se trata de que la resolución de la autoridad penitenciaria competente de clasificación en tercer grado, o el auto de la Sección de Vigilancia Penitenciaria del Tribunal de Instancia (antes, Juzgado de Vigilancia Penitenciaria) por el que se acuerda dicha clasificación o la libertad condicional, tenga validez de autorización de trabajo por cuenta ajena, bajo determinadas circunstancias, para el desarrollo de actividades laborales en régimen abierto o en libertad condicional. La finalidad es favorecer la reinserción social de la persona penada mediante el trabajo.

2. A quién se dirige

Personas extranjeras no comunitarias que cumplen condena en un centro penitenciario español y que han sido clasificadas en tercer grado o se encuentran en libertad condicional, y que cuentan con una oferta o contrato de trabajo.

3. Ante quién y por dónde se tramita

Ante la Oficina de Extranjería o el órgano competente en materia de autorizaciones de trabajo de la provincia, en coordinación con la Administración penitenciaria. La solicitud puede presentarse por medios electrónicos a través de la sede electrónica de las Administraciones Públicas (procedimientos de extranjería) o en los registros habilitados conforme al art. 16 de la Ley 39/2015.

4. Documentación habitual

Solicitud cumplimentada y firmada.

Pasaporte o documento de viaje de la persona penada, o, en su defecto, documentación que acredite su identidad.

Copia de la resolución de clasificación en tercer grado o del auto que acuerda dicha clasificación o la libertad condicional.

Contrato u oferta de trabajo firmada por la empresa, con indicación del puesto, jornada, duración y retribución.

Documentación de la empresa empleadora (NIF, inscripción en la Seguridad Social, alta en la actividad).

Informe o certificación del centro penitenciario sobre la situación penitenciaria y el programa de tratamiento, cuando se solicite.

Justificante del pago de las tasas que, en su caso, correspondan.

5. Efectos

La autorización habilita a la persona penada para trabajar por cuenta ajena mientras se mantenga en régimen abierto o en libertad condicional y en los términos de la resolución. La empresa debe dar de alta a la persona trabajadora en la Seguridad Social desde el inicio de la actividad.

6. Normativa aplicable

Ley Orgánica 4/2000, de 11 de enero, sobre derechos y libertades de los extranjeros en España y su integración social.

Reglamento de la Ley Orgánica 4/2000, aprobado por Real Decreto 1155/2024, de 19 de noviembre.

Ley Orgánica 1/1979, de 26 de septiembre, General Penitenciaria, y Reglamento Penitenciario aprobado por Real Decreto 190/1996, de 9 de febrero (clasificación en tercer grado y libertad condicional).

Código Penal (libertad condicional).

Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas.


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
