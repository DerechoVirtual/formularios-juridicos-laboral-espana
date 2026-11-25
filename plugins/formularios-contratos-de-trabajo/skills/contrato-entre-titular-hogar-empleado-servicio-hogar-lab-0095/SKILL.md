---
name: contrato-entre-titular-hogar-empleado-servicio-hogar-lab-0095
description: "Contrato entre el titular del hogar y el empleado para el servicio del hogar familiar. Lo redacta con los datos del caso y comprueba las normas en el BOE. Requiere Jurisprudenciator."
---

# Contrato entre el titular del hogar y el empleado para el servicio del hogar familiar

> Formulario **LAB-0095** del plugin **Contratos de trabajo y contratación laboral** (`formularios-contratos-de-trabajo`) · Laboral › Contratación laboral · normativa revisada el 25-11-2026.

## Qué es

Es un modelo de tipo **contratos, pactos y cláusulas**, en su versión revisada y actualizada a la normativa vigente.

## Para qué sirve

Para obtener, en pocos minutos, un borrador completo de «Contrato entre el titular del hogar y el empleado para el servicio del hogar familiar» adaptado a tu caso y a la normativa vigente, en Word y listo para revisar. Claude no se limita a copiar el modelo: te pide los datos, decide contigo las opciones, redacta las partes que dependen de los hechos y comprueba en el BOE cada norma que cita.

## Cómo se usa

1. **Pídelo con tus palabras**, por ejemplo: «Prepárame el documento “Contrato entre el titular del hogar y el empleado para el servicio del hogar familiar” para mi caso». También puedes invocarla directamente con `/formularios-contratos-de-trabajo:contrato-entre-titular-hogar-empleado-servicio-hogar-lab-0095`.
2. **Dale los datos del caso** cuando te los pida (abajo tienes la lista para tenerlos a mano). Lo que no sepas queda como hueco visible.
3. **Resuelve las opciones** que te plantee (las marcadas [ELEGIR] y [OPCIONAL] en el modelo).
4. **Recibe el documento en Word, tal cual es el formulario**: empieza por su primera línea (por ejemplo «En [LOCALIDAD], a [FECHA]» o «A LA SECCIÓN…»), sin títulos ni notas añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. Lo pendiente, las normas comprobadas y el plazo te los dice en el chat.

Si no estás seguro de que este sea el formulario que necesitas, usa el índice del plugin: `/formularios-contratos-de-trabajo:indice`.

## Qué contiene esta skill

- `SKILL.md` (este fichero): qué es el formulario, para qué sirve, cómo se usa, los datos que pide, las normas que cita, los avisos de actualización y las instrucciones para Claude.
- `assets/formulario.md`: el formulario seco, tal cual, desde su primera línea hasta la firma, con sus campos [EN MAYÚSCULAS] y sus opciones [ELEGIR…] / [OPCIONAL…]. Es el texto que se rellena; no lleva explicaciones.
- `../indice/marco.md` (en la skill `indice` del plugin): la guía del tema (Contratos de trabajo y contratación laboral) con las normas, órganos y plazos vigentes que Claude lee antes de redactar.

## Datos que conviene tener a mano

- [ ] COMPLETAR (7 veces)
- [ ] NOMBRE Y APELLIDOS (4 veces)
- [ ] DNI/NIE (2 veces)
- [ ] LOCALIDAD (2 veces)
- [ ] AÑO
- [ ] CALLE
- [ ] DESCRIBIR
- [ ] DÍA
- [ ] LUGAR
- [ ] MES
- [ ] PLAZO

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

### Avisos de actualización (0) — se aplican en el texto, nunca se copian en el documento

- Ninguno.

### Notas de uso del formulario — orientan la redacción, nunca se copian en el documento

Notas al pie del formulario original:
(1) Determinar el tipo de tareas domésticas a realizar, pudiendo extenderse al cuidado de los miembros de la familia, guardería, jardinería, conducción de vehículos y otros análogos (artículo 1.º 4 del Real Decreto 1620/2011, de 14 de noviembre).

(2) Podrá optarse por alguna de las modalidades y duraciones del Estatuto de los Trabajadores, o bien por su duración indefinida. En defecto de pacto se entiende celebrado a jornada completa y por tiempo indefinido (artículos 5 y 6 del Real Decreto 1620/2011, de 14 de noviembre).

(3) El período de prueba no podrá tener una duración superior a dos meses, salvo pacto contrario en convenio colectivo aplicable.

(4) Táchese lo que no proceda.

(5) El período de presencia no podrá superar las veinte horas semanales de promedio, dentro de un período de cómputo mensual, salvo descanso compensatorio, debiendo en todo caso respetarse los períodos de descanso semanal e interjornadas (artículo 9.2 del Real Decreto 1620/2011, de 14 de noviembre).

(6) Su compensación será en metálico, sin que su importe pueda ser inferior al valor de la hora ordinaria, o en tiempos equivalentes de descanso (artículo 9.2 del Real Decreto 1620/2011, de 14 de noviembre).

(7) Ha de garantizarse en dinero el salario mínimo interprofesional si se realiza jornada completa, o la parte proporcional establecida en la normativa anual pertinente de trabajarse por horas (artículo 8 del Real Decreto 1620/2011, de 14 de noviembre y la normativa anual se salarios mínimos).

Se tiene derecho a dos pagas extraordinarias al año, cuyo período de devengo será el semestre en función del tiempo trabajado en el mismo, y cuyo importe no podrá ser inferior al salario mínimo interprofesional, que en el caso de ser un empleado de hogar por horas, se incluirá dentro del valor de la hora ordinaria a fijar anualmente por el Gobierno al establecer el salario mínimo interprofesional (artículo 8 del Real Decreto 1620/2011, de 14 de noviembre).

(8) En defecto de pacto será aplicable el incremento salarial medio pactado en los convenios colectivo recogido en resolución de del ministerio del área competente (artículo 8.3 del Real Decreto 1620/2011, de 14 de noviembre).

(9) Táchese lo que no proceda.

(10) Fíjense las retribuciones en especie y su valoración, teniendo en cuenta que no pueden superar el 30% del salario total y que, en todo caso, el empleado ha de percibir como retribución en dinero, el importe equivalente al salario mínimo interprofesional a prorrata de la jornada realizada.

(11) Preferentemente el domingo (artículo 9.5 del Real Decreto 1620/2011, de 14 de noviembre).

(12) Se podrá determinar del día de disfrute del resto del descanso, que como regla general será la tarde del sábado o la mañana de lunes (artículo 9.5 del Real Decreto 1620/2011, de 14 de noviembre).

(13) Será de treinta días naturales al año, que podrá fraccionarse en dos o más períodos, siempre que uno de ellos sea como mínimo de quince días naturales consecutivos (artículo 9.7 del Real Decreto 1620/2011, de 14 de noviembre).


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
