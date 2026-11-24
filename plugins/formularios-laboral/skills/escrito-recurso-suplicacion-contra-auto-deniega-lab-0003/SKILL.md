---
name: escrito-recurso-suplicacion-contra-auto-deniega-lab-0003
description: "Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo

> Formulario **LAB-0003** del plugin **Laboral: préstamo al trabajador, despido en concurso y suplicación** (`formularios-laboral`) · Laboral › Relación laboral · normativa revisada el 24-11-2026.

## Qué es

Escrito de interposición de recurso de suplicación contra el auto denegando autorizar la extinción colectiva de contratos de trabajo.

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo” para mi caso». También puedes invocarla directamente con `/formularios-laboral:escrito-recurso-suplicacion-contra-auto-deniega-lab-0003`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-laboral:indice`.

## Qué contiene esta skill

- Este fichero: al final, en «Texto del formulario», está el formulario tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…].
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Laboral: préstamo al trabajador, despido en concurso y suplicación) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] FECHA (7 veces)
- [ ] LOCALIDAD (3 veces)
- [ ] Nº (3 veces)
- [ ] NÚMERO (2 veces)
- [ ] SEDE (2 veces)
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] LUGAR
- [ ] MES Y AÑO
- [ ] NOMBRE DE LA PARTE
- [ ] NOMBRE Y APELLIDOS
- [ ] Nº DE PROCEDIMIENTO

## Normas que cita el formulario

- art. 195.1 Ley 36/2011
- art. 51 ET
- art. 51.1 ET

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Escrito de interposición de recurso de suplicación contra el auto denegando autorizar la extinción colectiva de contratos de trabajo.


### Flujo

1. **Paso 0**: comprueba Jurisprudenciator (arriba).
2. Lee entero el «Texto del formulario» (al final de este fichero) y la parte de `../indice/marco.md` que afecte al caso. Limítate a la materia de este formulario: no añadas contenido ajeno a él.
3. Pide los datos de la lista en una sola tanda. Si un dato aparece varias veces, aclara a qué persona o acto corresponde cada vez. Lo que el usuario no sepa se queda como hueco visible con su etiqueta (p. ej. [FECHA]).
4. Resuelve cada [ELEGIR …] y cada [OPCIONAL …] según los hechos, y sustituye cualquier indicación entre paréntesis del formulario («(se describirá…)», «(indicar…)») por el contenido que corresponda. Redacta las partes que dependen del caso (hechos, motivos, descripción de bienes).
5. Aplica los avisos de actualización en el lugar que indican. Comprueba con `buscar_articulo` cada norma citada; si alguna ha cambiado, usa la redacción vigente. Si citas jurisprudencia, localízala con `buscar_sentencias` o `buscar_por_cita` y léela con `leer_sentencias`.
6. Antes de entregarlo, pasa `verificar_escrito` con las frases que citan normas o sentencias y corrige lo que señale.
7. **Documento final = el formulario tal cual, rellenado y limpio.**
   - Empieza exactamente por la primera línea del «Texto del formulario» y sigue su estructura y su orden hasta la firma.
   - No pongas en el documento título, nombre del formulario o de la skill, código, encabezados, «Para qué sirve», leyendas, avisos, notas de uso, comentarios ni explicaciones. Tampoco marcas [ELEGIR…] u [OPCIONAL…]: ya están resueltas.
   - Formato Word (.docx, con la skill de Word disponible): **Times New Roman 12 pt** en todo el documento, **interlineado 1,15**, **texto justificado**, márgenes de 2,5 cm. Los rótulos del formulario (REUNIDOS, CLÁUSULAS, HECHOS, SUPLICO…) en su propia línea y en negrita, sin cambiar su texto.
8. En el chat (nunca dentro del documento): datos pendientes, partes redactadas por ti, normas y sentencias comprobadas con Jurisprudenciator (y, si algún dato sale de internet, cuál y su enlace) y, si es un escrito judicial o administrativo, el plazo y el órgano ante el que se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Texto del formulario

Lo que sigue, hasta el final de este fichero, es el formulario tal cual: desde su primera línea hasta la firma.

AL TRIBUNAL DE LO MERCANTIL
A LA SECCIÓN DE LO MERCANTIL DEL TRIBUNAL DE INSTANCIA
 NÚMERO [NÚMERO], PARA ANTE LA SALA DE LO SOCIAL DEL TSJ DE [LOCALIDAD]

D./Dña. [NOMBRE Y APELLIDOS], [ELEGIR: Letrado/a perteneciente al Ilustre Colegio de Abogados de / graduado social perteneciente al Iltre. Colegio de], en nombre y representación del concursado [NOMBRE DE LA PARTE], comparezco ante [ELEGIR: el Tribunal de Instancia (Sección de lo Mercantil) / la Sala de lo Mercantil del Tribunal de Instancia] núm. [Nº] de [SEDE], y como mejor en derecho proceda, DIGO:

Que mediante el presente escrito, de conformidad con lo dispuesto en el artículo 64.8 de la Ley Concursal, y dentro del plazo legalmente conferido por el art. 195.1 de la Ley 36/2011, de 10 de octubre, reguladora de la jurisdicción social (LJS), se INTERPONE RECURSO DE SUPLICACIÓN, anunciado en su día, contra el auto denegatorio de la autorización de extinción colectiva de fecha [FECHA] dictado en proceso concursal número [NÚMERO].

El recurso se basa en los siguientes hechos:

1) Que con fecha [FECHA] de [MES Y AÑO], recayó auto denegando la solicitud formulada por mi representado, que me fue notificada el día [FECHA] del mismo mes y año.

2) Con fecha [FECHA] se me notifica resolución dictada con fecha [FECHA], por la que se acuerda tener por anunciado, definitivamente, el recurso de suplicación y se ponen los autos a mi disposición, otorgándoseme un plazo de diez días sucesivos al de una audiencia a fin de que formalice el RECURSO DE SUPLICACIÓN anunciado en su día contra el auto de fecha [ELEGIR: del Tribunal de Instancia (Sección de lo Mercantil) / de la Sala de lo Mercantil del Tribunal de Instancia] núm. [Nº] de [SEDE] en los autos de proceso concursal [Nº DE PROCEDIMIENTO], por lo que por medio del presente escrito, lo interpongo y formalizo con devolución de los autos basándome en los siguientes:

I. FUNDAMENTOS Y REQUISITOS PROCESALES

1. RECURRIBILIDAD: Conforme con el artículo 64.8 de la Ley Concursal es recurrible en suplicación el auto dictado por [ELEGIR: el Tribunal de Instancia (Sección de lo Mercantil) / la Sala de lo Mercantil del Tribunal de Instancia].

2. PLAZOS: De acuerdo con lo dispuesto en el artículo 195.1 LJS, este recurso se interpone en el plazo de los diez días siguientes al de finalización de una audiencia concedida para retirar los autos.

3. FORMA: Tal y como previene el artículo 196.2 LJS, el escrito de interposición del recurso de suplicación, expresa, con suficiente claridad y precisión los motivos en que se ampara, con identificación suficiente de las normas del ordenamiento jurídico o la jurisprudencia que se consideran infringidas, y, de la misma forma y manera, con la identificación de los documentos o pericias en que se basa la revisión de hechos probados, y razonamiento de la pertinencia y fundamento de los motivos.

4. COPIAS: Conforme a lo dispuesto en el artículo 191.1 LJS se presenta el recurso con tantas copias como partes sean las recurridas.

5. PRESENTACIÓN: El recurso se presenta ante el Tribunal que dictó la sentencia impugnada para, su elevación ante la Sala que haya de resolverlo, tal y como previene el artículo 194.1 LJS.

6. LETRADO/a: El recurso se presenta con firma de [ELEGIR: letrado/a / graduado/a social] que lo autoriza, tal y como lo estipulan los artículos 21 y 231 LJS.

II. MOTIVOS DEL RECURSO

PRIMERO.-Al amparo del apartado c) del artículo 193 de la LJS por infracción de lo dispuesto en el artículo 51 del Estatuto de los Trabajadores, en relación con el artículo 64 de la Ley Concursal, por cuanto que concurren causas económicas justificativas de la extinción colectiva solicitada, siendo ésta necesaria para garantizar la viabilidad futura de la empresa.

El auto recurrido no entra a valorar el cumplimiento de los requisitos que se establecen en el artículo 51 del ET para que una empresa pueda extinguir un contrato de trabajo amparándose en causas económicas, desestimando la solicitud por motivos totalmente ajenos a los contemplados en el precepto, al indicar en el fundamento segundo que «la empresa no necesariamente entrará en beneficios con las medidas propuestas y la situación económica negativa no es irreversible», verdadera razón esencial por la que se deniega la solicitud. En este punto, el art. 51.1 del ET, en la redacción vigente, establece que debe entenderse que concurren causas económicas cuando de los resultados de la empresa se desprenda una situación económica negativa, en casos tales como la existencia de pérdidas actuales o previstas, o la disminución persistente de su nivel de ingresos ordinarios o ventas. En todo caso, se entenderá que la disminución es persistente si durante tres trimestres consecutivos el nivel de ingresos ordinarios o ventas de cada trimestre es inferior al registrado en el mismo trimestre del año anterior. Por tanto, es suficiente la situación de pérdidas o disminución persistente de ingresos, lo cual en este caso ha quedado totalmente acreditado por la documentación aportada.

Se infringe el artículo 51 ET y la doctrina que lo interpreta, puesto que aun entendiéndose probada en la resolución que ha existido una reducción paulatina de los beneficios de la empresa, hasta incurrir en pérdidas, se deniega con motivo de no ser situación irreversible, infringiendo con ello la doctrina establecida, según la cual, debe tenerse presente, que la negativa situación económica de la empresa no precisa ser «irreversible» para poder utilizar este supuesto de extinción de los contratos de trabajo, recogiendo literalmente lo siguiente:

«Para llevar a cabo la extinción de contratos de trabajo que permite este precepto legal no es necesario, de ningún modo, que la situación económica negativa de la empresa sea irreversible; antes al contrario, lo más propio y característico de estos supuestos es que se trate de situaciones no definitivas, es decir recuperables, y que precisamente con la adopción de esas medidas extintivas se busca y pretende superar esa situación deficitaria de la entidad y conseguir un adecuado funcionamiento económico de la misma. Así en el artículo 51.1 se habla de medidas que contribuyan "a superar una situación económica negativa", y en la Exposición de Motivos de la Ley 11/1994, de 19 de mayo, se manifiesta que las decisiones rescisorias se han de llevar a cabo "con la finalidad precisamente de mantener en el futuro la pervivencia de la empresa".

En esta misma línea profundiza la reforma operada por la Ley 3/2012, de 6 de julio, que expresa con claridad que el control judicial de estos despidos debe ceñirse a una valoración sobre la concurrencia de unos hechos: las causa, de manera que la decisión extintiva debe considerarse procedente, y por ende ser aprobada, siempre que se acredite la concurrencia de la causa en que se fundamentó la decisión extintiva.

Se ha de concluir, por consiguiente, que en el presente supuesto existe, con toda claridad y evidencia, la causa económica precisa para que pueda entrar en acción el artículo 52.c) mencionado».

Abundando aún más en la cuestión, el Juzgador infringe doblemente la doctrina jurisprudencial del TSJ de Cataluña que invoca en apoyo de su decisión, ya que entra a hacer una valoración de los motivos que condujeron a la empresa a solicitar el concurso, valoración que le resulta vetada si atendemos a la reseñada sentencia. Así, la citada sentencia dice textualmente que «Finalmente hemos dicho (Sentencia de TSJ Cataluña de 6 de octubre de 1995) que no es necesario justificar las razones de la situación económica negativa, es decir que no es preciso acreditar que se ha desarrollado una buena gestión empresarial pues no puede convertirse a los Tribunales en analistas económicos que juzguen si la actividad empresarial se ha desarrollado bien o mal, naturalmente dejando a salvo una actuación fraudulenta alegada y probada».

Finalmente, el auto recurrido prescinde de la definición legal, vinculante, del artículo 51.1 del ET, tras la reforma operada por Ley 3/2012, de 6 de julio, donde se incluye en las causas económicas, no sólo los supuestos de situación económica negativa, en casos tales como la existencia de pérdidas actuales o previstas, sino también la disminución persistente de su nivel de ingresos ordinarios o ventas, entendiéndose que concurre ésta si durante tres trimestres consecutivos el nivel de ingresos ordinarios o ventas de cada trimestre es inferior al registrado en el mismo trimestre del año anterior, lo cual se produce indudablemente en el caso contemplado.

Procedamos ahora a analizar si en el supuesto enjuiciado concurre el segundo de los requisitos que establece el artículo 51 del ET. Esto es, que la medida propuesta, contribuya a la superación de situaciones económicas negativas.

De nuevo se hace preciso, por tanto, acudir a la doctrina jurisprudencial que interpreta dichos preceptos para observar el error en que incurre el Juzgador (que ni tan siquiera entra a analizar el segundo de los requisitos), puesto que la medida extintiva no tiene que solucionar «per se», las dificultades económicas de la empresa, sino que dicha medida debe contribuir a superarlas, y contribuir, significa, «ayudar, auxiliar, asistir, favorecer, apoyar, socorrer, concurrir, cooperar, colaborar, coadyuvar, etc.», en definitiva que la medida extintiva, razonablemente, proporcione, junto con otras medidas, una expectativa de superación de la crisis.

Con ello, lo que se quiere indicar es que la relación de instrumentalidad o conexión entre despido y superación de los problemas económicos, no exige la demostración de que mediante el despido se superará la crisis. El despido en su caso, contribuirá a la superación de la situación económica negativa, lo que denota que no es preciso, como se ha dicho, que genere «per se» el resurgimiento económico. Por ello, resulta lógico considerar que la extinción de puestos de trabajo (especialmente de sus costes económicos) en una empresa que atraviesa una mala situación, debe contribuir a superarla. La Jurisprudencia ha creado así, una presunción probatoria enormemente importante, que despliega efectos desde el momento que se aportan datos evidenciadores de la desfavorable coyuntura. En definitiva, el artículo 51 ET debe ser examinado dentro de una concepción preventiva de la viabilidad de la empresa, y no dentro de una concepción final de la misma.

Por tanto, entendemos que se cumple, sobradamente, la exigencia de una contribución racional de las medidas extintivas de los contratos de trabajo de los actores, a la superación de la situación económica negativa, puesto que en el presente caso, las distintas actuaciones ejecutadas por la demandada van mucho más allá de la mera extinción de dos contratos de trabajo, lo que conduce a concluir que nos encontramos ante un conjunto de medidas que razonablemente deben contribuir a mejorar su situación económica y en cuyo contexto la extinción de los dos contratos de trabajo de los actores es adecuada, eficiente y proporcionada.

Por todo ello,

SUPLICO AL TRIBUNAL Que por presentado este escrito con sus copias, se sirva admitirlo, tenga por devueltos los autos, por interpuesto en tiempo y forma recurso de suplicación contra el auto recaído en los presentes autos de fecha [FECHA], dar traslado del mismo a las otras partes, para su impugnación si así conviene a su derecho y, transcurrido el plazo, háyase impugnado el recurso o no, eleve los autos a la Sala de lo Social del Tribunal Superior de Justicia de [LOCALIDAD].

Y, al propio tiempo, SUPLICO A LA SALA DEL TRIBUNAL SUPERIOR DE JUSTICIA de [LOCALIDAD]: Que, por interpuesto recurso de suplicación contra el auto de fecha [ELEGIR: del Tribunal de Instancia (Sección de lo Mercantil) / de la Sala de lo Mercantil del Tribunal de Instancia] núm. [Nº], dicte en su día sentencia por la que, con expresa estimación de los motivos aducido, se estime el presente recurso, y se revoque el auto de instancia, autorizando las extinciones contractuales solicitadas por mi representado, con todos los pronunciamientos inherentes a tal declaración.

OTROSÍ DIGO De conformidad con el artículo 198 de la Ley de la Jurisdicción Social designo como domicilio a efectos de notificaciones [DOMICILIO A EFECTOS DE NOTIFICACIONES].

Por lo expuesto,

SUPLICO A LA SALA: Tenga por realizada la anterior manifestación a los efectos procedentes en Derecho.

Es justicia que respetuosamente solicito en [LUGAR], a [FECHA].

Fdo.:
letrado/a
graduado/a social colegiado/a
