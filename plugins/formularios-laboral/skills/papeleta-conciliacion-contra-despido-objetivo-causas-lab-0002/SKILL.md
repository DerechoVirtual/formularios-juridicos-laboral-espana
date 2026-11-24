---
name: papeleta-conciliacion-contra-despido-objetivo-causas-lab-0002
description: "Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso

> Formulario **LAB-0002** del plugin **Laboral: préstamo al trabajador, despido en concurso y suplicación** (`formularios-laboral`) · Laboral › Relación laboral · normativa revisada el 24-11-2026.

## Qué es

Papeleta de conciliación previa a la demanda por despido objetivo por causas económicas (artículo 52.c del Estatuto de los Trabajadores) cuando la empresa empleadora se encuentra en concurso de acreedores, dirigida al servicio administrativo de mediación, arbitraje y conciliación. Se presenta por los trabajadores despedidos para intentar la conciliación, trámite previo obligatorio a la demanda, que suspende el plazo de caducidad de la acción de despido.

Es un modelo de tipo **demandas, peticiones y solicitudes iniciales**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso” para mi caso». También puedes invocarla directamente con `/formularios-laboral:papeleta-conciliacion-contra-despido-objetivo-causas-lab-0002`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-laboral:indice`.

## Qué contiene esta skill

- `formulario.md`: el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `marco.md`: la guía del tema (Laboral: préstamo al trabajador, despido en concurso y suplicación) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA A (7 veces)
- [ ] DOMICILIO (6 veces)
- [ ] AÑO (5 veces)
- [ ] NOMBRE Y APELLIDOS (5 veces)
- [ ] Nº (5 veces)
- [ ] MES (3 veces)
- [ ] TELÉFONO (3 veces)
- [ ] DÍA (2 veces)
- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NIF (2 veces)
- [ ] CONCRETA ACTIVIDAD DESARROLLADA POR LA EMPRESA
- [ ] DENOMINACIÓN SOCIAL DE LA EMPRESA B
- [ ] EDADES
- [ ] FIRMA DE CADA UNO DE LOS TRABAJADORES
- [ ] IMPORTE
- [ ] Nº DE PROCEDIMIENTO
- [ ] SEDE
- [ ] SINDICATO

## Normas que cita el formulario

- No cita artículos concretos; Claude localizará las normas aplicables con Jurisprudenciator si el documento las necesita.

---

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

- Junto a «…n la papeleta de conciliación o en la solicitud de mediación (artículo 66 LRJS).»: el original citaba el Real Decreto 2756/1979 para el contenido de la papeleta; comprobar su vigencia y la normativa autonómica aplicable al servicio de conciliación competente. Los trabajadores afectados por un despido colectivo o con empresa concursada deben comprobar, además, si procede el cauce del texto refundido de la Ley Concursal.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

NOTAS EXPLICATIVAS

Contenido mínimo de la papeleta de conciliación (artículo 6 del Real Decreto 2756/1979): datos personales y profesionales del promotor e interesados, y hechos sobre los que versa la pretensión; se presentará un número de copias igual al número de interesados y dos más.

Órgano al que se dirige: el órgano administrativo (o, en su caso, convencional) con funciones conciliadoras que tenga su sede en el lugar de trabajo del solicitante o domicilio de los interesados y futuros demandados, pudiendo presentarse el escrito ante el propio registro del servicio de mediación, arbitraje y conciliación u órganos administrativos correspondientes de las comunidades autónomas que tengan atribuidas dichas funciones. Pueden constituirse por los acuerdos interprofesionales o los convenios colectivos a los que se refiere el artículo 83 del texto refundido de la Ley del Estatuto de los Trabajadores, así como mediante los acuerdos de interés profesional a los que se refieren el artículo 13 y el apartado 1 del artículo 18 de la Ley del Estatuto del trabajo autónomo (artículo 63 de la Ley 36/2011, reguladora de la jurisdicción social, LRJS).

Partes interesadas: son los futuros demandados y se deben identificar con claridad, sobre todo en pretensiones sometidas al corto plazo de caducidad, como es la de despido, en que la subsanación de la demanda respecto de la identificación del empresario sólo será posible por error no imputable al trabajador (artículo 103.2 LRJS).

Hechos: deben especificarse los hechos concretos sobre los que versa la pretensión, que en procedimientos de despido serán como mínimo los que exige el artículo 104 LRJS, por la necesidad de congruencia que ha de existir entre este escrito y la demanda.

Pretensión: se debe concretar cuál es la pretensión deducida, que en vía preprocesal siempre será que la otra parte «se avenga» a asumir la nulidad o la improcedencia del despido con las consecuencias inherentes a estas declaraciones (nulidad: readmisión y abono de los salarios de tramitación; improcedencia: opción a favor del empresario, o del trabajador si es representante legal o sindical, entre la readmisión o el abono de la pertinente indemnización, con abono, cualquiera que sea el sentido de la opción, de los salarios de tramitación). En caso de que se pretenda la nulidad del despido, es conveniente solicitar subsidiariamente la improcedencia.

El pedimento o solicitud de la papeleta de conciliación va dirigido no a la parte contraria, sino al órgano administrativo de conciliación y, teniendo en cuenta que su intervención no es dirimente sino sólo de exhortación al acuerdo, la petición se constreñirá a que se inicie el oportuno expediente administrativo.

La presentación de la solicitud de conciliación o de mediación suspenderá los plazos de caducidad e interrumpirá los de prescripción. El cómputo de la caducidad se reanudará al día siguiente de intentada la conciliación o mediación o transcurridos quince días hábiles, excluyendo del cómputo los sábados, desde su presentación sin que se haya celebrado (artículo 65.1 LRJS).

La asistencia al acto de conciliación o de mediación es obligatoria para los litigantes. Cuando, estando debidamente citadas las partes para el acto de conciliación o de mediación, no compareciese el solicitante ni alegase justa causa, se tendrá por no presentada la papeleta de conciliación o la solicitud de mediación, archivándose todo lo actuado. Si no compareciera la otra parte, debidamente citada, se hará constar expresamente en la certificación del acta de conciliación o de mediación y se tendrá la conciliación o la mediación por intentada sin efecto, y el juez o tribunal impondrá las costas del proceso a la parte que no hubiere comparecido sin causa justificada, incluidos honorarios, hasta el límite de seiscientos euros, del letrado o graduado social colegiado de la parte contraria que hubieren intervenido, si la sentencia que en su día dicte coincidiera esencialmente con la pretensión contenida en la papeleta de conciliación o en la solicitud de mediación (artículo 66 LRJS).


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee `formulario.md` entero y la parte de `marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea de `formulario.md` y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.
