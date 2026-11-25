---
name: impreso-ex11-pedir-residencia-larga-duracion-larga-lab-1022
description: "Impreso EX11 para pedir la residencia de larga duración o de larga duración UE. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Impreso EX11 para pedir la residencia de larga duración o de larga duración UE

> Formulario **LAB-1022** del plugin **Extranjería y movilidad internacional de trabajadores** (`formularios-extranjeria-y-trabajo`) · Laboral › Extranjería y movilidad internacional de trabajadores · normativa revisada el 25-11-2026.

## Qué es

Ficha práctica sobre el impreso oficial EX-11, con el que una persona extranjera no comunitaria solicita la autorización de residencia de larga duración o de larga duración-UE, que le permite residir y trabajar en España indefinidamente en las mismas condiciones que los españoles (art. 32 de la LO 4/2000), con un modelo de escrito de presentación.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Impreso EX11 para pedir la residencia de larga duración o de larga duración UE» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Impreso EX11 para pedir la residencia de larga duración o de larga duración UE” para mi caso». También puedes invocarla directamente con `/formularios-extranjeria-y-trabajo:impreso-ex11-pedir-residencia-larga-duracion-larga-lab-1022`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-extranjeria-y-trabajo:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Extranjería y movilidad internacional de trabajadores) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] PROVINCIA (2 veces)
- [ ] AÑO
- [ ] CORREO ELECTRÓNICO
- [ ] DOMICILIO
- [ ] DÍA
- [ ] MES
- [ ] NACIONALIDAD
- [ ] NIE
- [ ] Nº DE PASAPORTE
- [ ] RELACIÓN DE DOCUMENTOS
- [ ] SUPUESTO DEL ART. 32 LO 4/2000
- [ ] TELÉFONO
- [ ] TIPO DE AUTORIZACIÓN DE RESIDENCIA DE LA QUE ES TITULAR

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

- Al principio del formulario: Códigos de tasa del modelo 790 (052 y 012) y numeración de los impresos EX: sin comprobar con Jurisprudenciator; verificarlos en el portal de la Secretaría de Estado de Migraciones.
- Junto a «…denciator; verificarlos en el portal de la Secretaría de Estado de Migraciones.]»: el original no traía el texto del formulario (solo remitía al impreso oficial EX-11 en PDF); se redacta de nuevo una ficha práctica conforme a la normativa vigente. Utilizar siempre la versión vigente del impreso EX-11 publicada por la Secretaría de Estado de Migraciones.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

FICHA PRÁCTICA

1. Qué es

El EX-11 es el impreso oficial de solicitud de la autorización de residencia de larga duración (nacional) y de la autorización de residencia de larga duración-UE. Ambas autorizan a residir y trabajar en España indefinidamente en las mismas condiciones que los españoles. La de larga duración-UE se ajusta además al estatuto de residente de larga duración de la Directiva 2003/109/CE y facilita la movilidad a otros Estados miembros.

2. Supuestos principales (art. 32 LO 4/2000)

Haber tenido residencia temporal en España durante cinco años de forma continuada, reuniendo las condiciones reglamentarias. Computan los periodos de residencia previa y continuada en otros Estados miembros como titular de la tarjeta azul-UE. La residencia se considera continuada aunque se haya abandonado temporalmente el territorio por vacaciones u otras razones previstas reglamentariamente.

Ser residente de larga duración en otro Estado miembro de la Unión Europea y venir a desarrollar en España una actividad por cuenta propia o ajena, o por otros fines.

Tener reconocida protección internacional por España u otro Estado miembro y encontrarse en España.

Otros supuestos individuales de especial vinculación con España previstos en el art. 183.3 del Reglamento (entre otros, beneficiarios de pensión de jubilación o de incapacidad permanente absoluta o gran invalidez contributivas; nacidos en España que al llegar a la mayoría de edad acrediten tres años consecutivos de residencia legal y continuada; antiguos españoles de origen; quienes al llegar a la mayoría de edad hayan estado tutelados por una entidad pública española durante los cinco años anteriores; y apátridas, refugiados o beneficiarios de protección subsidiaria).

Para la de larga duración-UE se exige, además, acreditar recursos fijos y regulares suficientes para la propia manutención y la de la familia y un seguro de enfermedad, en los términos reglamentarios (art. 176 del Reglamento). En ambos casos, la continuidad de la residencia no se ve afectada por ausencias de hasta seis meses continuados que no superen en total diez meses en los cinco años (dieciocho meses si se deben a motivos laborales) (arts. 176.a) y 183.2 del Reglamento).

3. Ante quién y por dónde se presenta

Ante la Oficina de Extranjería de la provincia en la que resida la persona solicitante, personalmente o por medio de representante, o por medios electrónicos a través de la sede electrónica de las Administraciones Públicas (procedimientos de extranjería). Pueden utilizarse también los registros previstos en el art. 16 de la Ley 39/2015.

Plazo: la solicitud debe presentarse en los dos meses anteriores a la expiración de la autorización de residencia de la que se es titular, lo que prorroga su validez hasta la resolución; también se prorroga si se presenta en los tres meses posteriores a la expiración, sin perjuicio del procedimiento sancionador. Esta regla no se aplica a quien, con una autorización de residencia en vigor, ya cumple los requisitos. La resolución debe notificarse en el plazo máximo de tres meses; transcurrido sin resolución expresa, la solicitud se entiende estimada (arts. 177.2 y 6 y 184.2 y 6 del Reglamento).

4. Documentación habitual

Impreso EX-11 cumplimentado y firmado, marcando el tipo de autorización solicitada (larga duración o larga duración-UE) y el supuesto.

Copia completa del pasaporte en vigor o documento de viaje.

Justificante del abono de la tasa correspondiente (modelo 790, código 052).

Según el supuesto: documentación que acredite los periodos de residencia previa (en particular, los de otros Estados miembros como titular de tarjeta azul-UE), la condición de residente de larga duración en otro Estado miembro o la protección internacional reconocida.

Para la larga duración-UE: acreditación de recursos suficientes y de seguro de enfermedad, público o privado.

Para la larga duración nacional basada en periodos de residencia previos: informe que acredite la escolarización de los menores a cargo en edad de escolarización obligatoria (art. 184.3.c) del Reglamento).

En su caso, certificado de antecedentes penales del país o países en que se haya residido durante los cinco años anteriores a la solicitud (arts. 177.3.f) y 184.3.e) del Reglamento).

Si se actúa por medio de representante: documento acreditativo de la representación.

5. Tras la concesión

La persona titular debe solicitar personalmente la Tarjeta de Identidad de Extranjero (TIE) en el plazo de un mes desde la notificación de la resolución de concesión (art. 4.2 LO 4/2000 y arts. 177.7 y 184.7 del Reglamento), mediante el impreso EX-17 y el abono de la tasa (modelo 790, código 012).

6. Extinción y recuperación (art. 32.5 y 6 LO 4/2000)

La autorización se extingue, entre otros casos, por obtenerse de manera fraudulenta, por orden de expulsión, por ausencia del territorio de la Unión Europea durante doce meses consecutivos (con las excepciones reglamentarias) o por adquirirse la residencia de larga duración en otro Estado miembro. Quien la haya perdido puede recuperarla mediante un procedimiento simplificado.

7. Normativa aplicable

Ley Orgánica 4/2000, de 11 de enero, sobre derechos y libertades de los extranjeros en España y su integración social, art. 32.

Reglamento de la Ley Orgánica 4/2000, aprobado por Real Decreto 1155/2024, de 19 de noviembre, en particular arts. 175 a 177 (larga duración-UE) y 183 y 184 (larga duración nacional).

Directiva 2003/109/CE del Consejo, de 25 de noviembre de 2003, relativa al estatuto de los nacionales de terceros países residentes de larga duración.

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
