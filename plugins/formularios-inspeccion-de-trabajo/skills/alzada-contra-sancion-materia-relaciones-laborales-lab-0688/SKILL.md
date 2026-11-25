---
name: alzada-contra-sancion-materia-relaciones-laborales-lab-0688
description: "Alzada contra sanción en materia de relaciones laborales individuales y colectivas. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Alzada contra sanción en materia de relaciones laborales individuales y colectivas

> Formulario **LAB-0688** del plugin **Inspección de Trabajo y sanciones administrativas** (`formularios-inspeccion-de-trabajo`) · Laboral › Inspección de Trabajo y sanciones administrativas · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **escritos de trámite y otros**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Alzada contra sanción en materia de relaciones laborales individuales y colectivas» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Alzada contra sanción en materia de relaciones laborales individuales y colectivas” para mi caso». También puedes invocarla directamente con `/formularios-inspeccion-de-trabajo:alzada-contra-sancion-materia-relaciones-laborales-lab-0688`.
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
- [ ] FECHA (4 veces)
- [ ] IMPORTE (2 veces)
- [ ] NOMBRE Y APELLIDOS (2 veces)
- [ ] DNI/NIE
- [ ] DOMICILIO A EFECTOS DE NOTIFICACIONES
- [ ] Nº DE EXPEDIENTE
- [ ] ÓRGANO AL QUE SE DIRIGE
- [ ] ÓRGANO O PERSONA

## Normas que cita el formulario

- art. 23 Real Decreto 928/1998
- art. 6 LIS
- art. 7 LIS
- art. 8 LIS
- art. 54 Real Decreto Legislativo 5/2000
- art. 25.2 Ley 40/2015
- art. 25.1 Ley 40/2015
- art. 53.1.b Real Decreto Legislativo 5/2000
- art. 53.2 Real Decreto Legislativo 5/2000
- art. 14.1 Real Decreto 928/1998
- art. 21.1 Ley 23/2015
- art. 39 Real Decreto Legislativo 5/2000

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

- Al principio del formulario: Alzada: un mes ante el órgano superior (art. 23.1 RD 928/1998, red. RD 688/2021; arts. 121-122 LPAC); no cabe si se pagó con la reducción del 40 % (art. 23.1, párr. 2.º); silencio desestimatorio a los tres meses (art. 23.2).
- Junto a «…% (art. 23.1, párr. 2.º); silencio desestimatorio a los tres meses (art. 23.2).]»: Cuantías vigentes (art. 40.1 LISOS, red. RDL 32/2021): leves 70-750 €; graves 751-7.500 €; muy graves 7.501-225.018 €. Arts. 7.2 y 7.14: una infracción por cada persona trabajadora afectada o contratada, con multa de 1.000-10.000 € cada una (art. 40.1.c bis).

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Modelo de recurso de alzada, ante el órgano superior jerárquico del que dictó la resolución, contra resolución sancionadora por infracción leve, conforme establecen los artículos 54 del Real Decreto Legislativo 5/2000, de 4 de agosto, por el que se aprueba el texto refundido de la Ley sobre Infracciones y Sanciones en el Orden Social, 23 del Real Decreto 928/1998, de 14 de mayo, por el que se aprueba el Reglamento General sobre Procedimientos para la Imposición de las Sanciones por Infracciones de Orden Social y para los Expedientes Liquidatorios de Cuotas de la Seguridad Social, y 121 y 122 de la Ley 39/2015, de 1 de octubre, del Procedimiento Administrativo Común de las Administraciones Públicas, por las siguientes causas establecidas en los artículos 6, 7 y 8 de la LISOS:

- No exponer en lugar visible del centro de trabajo el calendario laboral vigente
- No entregar al trabajador puntualmente el recibo de salarios
- No utilizar el modelo de recibo de salarios aplicable, oficial o pactado
- No informar por escrito al trabajador sobre los elementos esenciales del contrato y las principales condiciones de la prestación laboral
- No entregar al trabajador documento justificativo sobre su nueva condición de trabajador fijo de la empresa
- No informar a los trabajadores a tiempo parcial, a distancia y con contratos de duración determinada o temporales, incluidos los contratos formativos, y a los contratos fijos discontinuos, sobre las vacantes existentes en la empresa
- Incumplir obligaciones meramente formales o documentales
- No formalizar por escrito el contrato de trabajo cuando así sea exigible o lo haya solicitado el trabajador
- Transgredir la normativa sobre modalidades contractuales
- No consignar en el recibo de salarios las cantidades realmente abonadas al trabajador
- Incumplir las obligaciones en materia de tramitación de recibos del finiquito
- Transgredir las normas y los límites legales o pactados en materia de tiempo de trabajo
- Imponer unilateralmente la modificación de condiciones sustanciales de trabajo
- Transgredir los derechos de información, audiencia y consulta de los representantes de los trabajadores y de los delegados sindicales
- Transgredir los derechos de los representantes de los trabajadores y de las secciones sindicales en materia de crédito horario, locales y tablones de anuncio
- Vulnerar los derechos de las secciones sindicales en orden a la recaudación de cuotas distribución y recepción de información sindical
- Establecer condiciones de trabajo inferiores o vulneración de los derechos legales de los trabajadores
- Incumplir el deber de información a los trabajadores en los supuestos de contratas o subcontratas y sucesión de empresas
- No disponer la empresa principal del libro registro de las empresas contratistas o subcontratistas
- No cumplir las obligaciones que en materia de planes de igualdad
- La formalización de nuevas contrataciones laborales incumpliendo la prohibición establecida para las situaciones de ERTE
- Impago y retrasos reiterados en el pago del salario
- Cesión ilegal de trabajadores
- Despido colectivo o suspensión de contratos o reducción de jornada por causas económicas, técnicas, organizativas o de producción, fuerza mayor, o mecanismo RED, sin acudir a los procedimientos establecidos
- Transgresión de normas sobre trabajo de menores
- Impedir el derecho de reunión de trabajadores, sus representantes y secciones sindicales
- Vulneración del derecho de asistencia y acceso a los centros de trabajo de cargos electivos en organizaciones sindicales
- Transgresión de deberes de colaboración en procesos electorales a representantes de los trabajadores
- Transgresión de cláusulas normativas sobre materia sindical en convenios colectivos
- No reabrir el centro de trabajo en caso de cierre patronal
- Actos lesivos del derecho de huelga
- Actos del empresario contrarios a la intimidad y dignidad de los trabajadores
- Discriminación o trato desfavorable de los trabajadores
- Acoso sexual
- El acoso por razón de origen racial o étnico, religión o convicciones, discapacidad, edad y orientación e identidad sexual, expresión de género o características sexuales y el acoso por razón de sexo
- Incumplir las medidas sociales de acompañamiento en caso de despido colectivo
- No instrumentar los compromisos por pensiones con el personal
- Incumplir la proporción mínima de trabajadores contratados con carácter indefinido en el sector de la construcción
- No elaborar o no aplicar el plan de igualdad, o incumplirla manifiestamente
- No presentar, las empresas con beneficios que realicen despidos colectivos que afecten a mayores de 50 años, la certificación a que se refiere el apartado 7 de la Disposición Adicional Decimosexta de la Ley 27/2011, de 1 de agosto, sobre actualización, adecuación y modernización del sistema de Seguridad Social, o presentar información falsa o inexacta
- Incumplir las obligaciones establecidas en el artículo 57.3 de la Ley Orgánica de Protección Integral de la Infancia y la Adolescencia frente a la Violencia
- Establecer nuevas externalizaciones de actividad incumpliendo la prohibición establecida para las situaciones de ERTE


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
