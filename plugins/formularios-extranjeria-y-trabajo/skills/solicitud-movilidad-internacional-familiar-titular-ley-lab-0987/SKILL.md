---
name: solicitud-movilidad-internacional-familiar-titular-ley-lab-0987
description: "Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013

> Formulario **LAB-0987** del plugin **Extranjería y movilidad internacional de trabajadores** (`formularios-extranjeria-y-trabajo`) · Laboral › Extranjería y movilidad internacional de trabajadores · normativa revisada el 25-11-2026.

## Qué es

Ficha práctica y modelo de solicitud de la autorización de residencia (y, en su caso, del visado) para los familiares de un extranjero que reside en España o va a hacerlo al amparo del régimen de movilidad internacional de la Ley 14/2013, de apoyo a los emprendedores (inversores, emprendedores, profesionales altamente cualificados, investigadores, traslados intraempresariales, teletrabajadores de carácter internacional). Se usa para tramitar la residencia del cónyuge o pareja, hijos y ascendientes a cargo ante la Unidad de Grandes Empresas y Colectivos Estratégicos.

Es un modelo de tipo **comunicaciones, requerimientos y cartas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013” para mi caso». También puedes invocarla directamente con `/formularios-extranjeria-y-trabajo:solicitud-movilidad-internacional-familiar-titular-ley-lab-0987`.
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
- [ ] LOCALIDAD (3 veces)
- [ ] DOMICILIO (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DOCUMENTO DE REPRESENTACIÓN
- [ ] DÍA
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIE
- [ ] NIE / Nº DE PASAPORTE
- [ ] NOMBRE Y APELLIDOS DEL FAMILIAR
- [ ] NOMBRE Y APELLIDOS DEL TITULAR PRINCIPAL
- [ ] Nº DE EXPEDIENTE
- [ ] Nº DE PASAPORTE
- [ ] PAÍS
- [ ] PROVINCIA
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] TELÉFONO

## Normas que cita el formulario

- art. 62.3 Ley 14/2013
- art. 62.4 Ley 14/2013

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

- Al principio del formulario: el original no traía el texto del formulario (solo remitía a un impreso oficial en PDF); se redacta de nuevo una ficha práctica y una solicitud conforme a la normativa vigente. Descargar y utilizar siempre el impreso oficial vigente de familiares de la Unidad de Grandes Empresas y Colectivos Estratégicos.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

FICHA PRÁCTICA

1. Qué es

Es la solicitud de autorización de residencia en el marco de la movilidad internacional para los familiares del titular principal (inversor, emprendedor, profesional altamente cualificado, investigador, trabajador en traslado intraempresarial o teletrabajador de carácter internacional). Los familiares pueden solicitar la autorización, y en su caso el visado, de forma conjunta y simultánea con el titular o de forma sucesiva (art. 62.4 de la Ley 14/2013). Si las solicitudes se presentan a la vez que la del titular, se resuelven también de forma simultánea.

2. Quiénes pueden solicitarla

El cónyuge o la persona con análoga relación de afectividad.

Los hijos menores de edad.

Los hijos mayores de edad que dependan económicamente del titular y no hayan constituido por sí mismos una unidad familiar.

Los ascendientes a cargo.

3. Ante quién y cómo se presenta

Si el familiar se encuentra en España en situación regular: solicitud de autorización de residencia ante la Unidad de Grandes Empresas y Colectivos Estratégicos (UGE-CE), por medios telemáticos, a través de la sede electrónica habilitada al efecto. La concesión corresponde a la Dirección General de Migraciones (art. 76.1 de la Ley 14/2013).

Si el familiar se encuentra fuera de España: solicitud de visado de residencia en la misión diplomática u oficina consular española de su demarcación, que comprobará los requisitos.

Plazo de resolución de la autorización: veinte días desde la presentación electrónica de la solicitud en el órgano competente; transcurrido sin resolución, la autorización se entiende estimada por silencio administrativo. Las resoluciones son recurribles en alzada (arts. 121 y 122 de la Ley 39/2015) (art. 76.1 de la Ley 14/2013).

La presentación de la solicitud prorroga la situación de residencia o estancia de la que fuera titular el solicitante hasta la resolución del procedimiento (art. 76.1 de la Ley 14/2013).

Concedida la autorización por un periodo superior a seis meses, debe solicitarse personalmente la Tarjeta de Identidad de Extranjero (TIE) en el plazo de un mes (art. 76.2 de la Ley 14/2013 y art. 4.2 de la LO 4/2000).

Renovación: por periodos de dos años, mientras se mantengan las condiciones que generaron el derecho, también por medios electrónicos (art. 76.3 de la Ley 14/2013).

4. Requisitos (art. 62.3 de la Ley 14/2013)

No encontrarse irregularmente en territorio español.

Carecer de antecedentes penales en España y en los países donde se haya residido durante los dos últimos años, por delitos previstos en el ordenamiento jurídico español, y presentar declaración responsable de inexistencia de antecedentes penales de los últimos cinco años (exigible a los mayores de edad).

No figurar como rechazable en el espacio territorial de países con los que España tenga firmado un convenio en tal sentido.

Contar con un seguro público o un seguro privado de enfermedad concertado con una entidad aseguradora autorizada para operar en España.

Contar con recursos económicos suficientes para sí y para los miembros de la familia durante el periodo de residencia en España.

Abonar la tasa por tramitación de la autorización o del visado.

5. Documentación habitual

Impreso oficial de solicitud para familiares, debidamente cumplimentado y firmado.

Copia completa del pasaporte en vigor del familiar.

Documento que acredite el vínculo familiar (certificado de matrimonio o de inscripción de la pareja, certificado de nacimiento), legalizado o apostillado y, en su caso, traducido al castellano o a la lengua cooficial.

Para hijos mayores de edad y ascendientes: documentación acreditativa de la dependencia económica o de estar a cargo del titular.

Certificado de antecedentes penales de los países de residencia de los dos últimos años y declaración responsable relativa a los últimos cinco años (mayores de edad).

Seguro de enfermedad.

Acreditación de medios económicos suficientes.

Justificante del pago de la tasa.

Copia de la autorización o de la solicitud del titular principal.

Si se actúa por medio de representante: documento acreditativo de la representación.

6. Normativa aplicable

Ley 14/2013, de 27 de septiembre, de apoyo a los emprendedores y su internacionalización (sección sobre movilidad internacional, en particular arts. 61, 62 y 76).

Ley Orgánica 4/2000, de 11 de enero, sobre derechos y libertades de los extranjeros en España y su integración social, y su Reglamento, aprobado por Real Decreto 1155/2024, de 19 de noviembre, con carácter supletorio.

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
