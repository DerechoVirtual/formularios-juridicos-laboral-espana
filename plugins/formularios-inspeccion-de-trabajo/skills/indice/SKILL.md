---
name: indice
description: "Índice de los 62 formularios de Inspección de Trabajo y sanciones administrativas. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Inspección de Trabajo y sanciones administrativas: índice de formularios

> Plugin `formularios-inspeccion-de-trabajo` · 62 formularios · normativa revisada el 25-11-2026.

## Qué es

Para tratar con la Inspección de Trabajo y la autoridad laboral: alegaciones a actas de infracción y de liquidación, recursos de alzada contra sanciones en el orden social, pago voluntario con reducción, denuncias ante la Inspección y comunicaciones a la autoridad laboral.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Alegaciones a un acta de infracción de la Inspección de Trabajo»
- «Recurso de alzada contra una sanción en el orden social»
- «Denuncia ante la Inspección de Trabajo»

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

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-inspeccion-de-trabajo:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (1)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0696 | Recurso contencioso-administrativo contra la resolución firme de actas de liquidación o infracción | `recurso-contencioso-administrativo-contra-resolucion-lab-0696` |

### Contestaciones, oposiciones y alegaciones (22)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0659 | Alegaciones al acta de infracción de movimientos migratorios | `alegaciones-acta-infraccion-movimientos-migratorios-lab-0659` |
| LAB-0660 | Alegaciones al acta de infracción de empresas colaboradoras en la gestión de la Seguridad Social | `alegaciones-acta-infraccion-empresas-colaboradoras-lab-0660` |
| LAB-0661 | Alegaciones al acta de infracción muy grave por autorización de trabajo de extranjeros | `alegaciones-acta-infraccion-muy-grave-autorizacion-lab-0661` |
| LAB-0662 | Alegaciones al acta de infracción en materia de cooperativas | `alegaciones-acta-infraccion-materia-cooperativas-lab-0662` |
| LAB-0663 | Alegaciones al acta de infracción por obstrucción a la labor inspectora | `alegaciones-acta-infraccion-obstruccion-labor-lab-0663` |
| LAB-0666 | Alegaciones al acta de infracción de Seguridad Social (trabajadores, beneficiarios y solicitantes) | `alegaciones-acta-infraccion-seguridad-social-lab-0666` |
| LAB-0667 | Alegaciones al acta de infracción de las Mutuas de AT y EP | `alegaciones-acta-infraccion-mutuas-at-ep-lab-0667` |
| LAB-0669 | Alegaciones al acta de infracción de empresas de inserción | `alegaciones-acta-infraccion-empresas-insercion-lab-0669` |
| LAB-0673 | Alegaciones al acta de infracción de empresas usuarias | `alegaciones-acta-infraccion-empresas-usuarias-lab-0673` |
| LAB-0674 | Alegaciones al acta de infracción de trabajadores | `alegaciones-acta-infraccion-trabajadores-lab-0674` |
| LAB-0675 | Alegaciones al acta de infracción de empresas de trabajo temporal | `alegaciones-acta-infraccion-empresas-trabajo-temporal-lab-0675` |
| LAB-0677 | Alegaciones al acta de infracción en materia de empleo y fomento del empleo | `alegaciones-acta-infraccion-materia-empleo-fomento-lab-0677` |
| LAB-0679 | Alegaciones al acta de infracción de prevención de riesgos laborales | `alegaciones-acta-infraccion-prevencion-riesgos-lab-0679` |
| LAB-0681 | Alegaciones al acta de infracción por actividad transnacional de empresas de trabajo temporal | `alegaciones-acta-infraccion-actividad-transnacional-lab-0681` |
| LAB-0684 | Alegaciones al acta de infracción por desplazamiento de trabajadores a España | `alegaciones-acta-infraccion-desplazamiento-lab-0684` |
| LAB-0685 | Alegaciones al acta de infracción por información y consulta en sociedades europeas | `alegaciones-acta-infraccion-informacion-consulta-lab-0685` |
| LAB-0687 | Alegaciones al acta de infracción por información y consulta en grupos de dimensión comunitaria | `alegaciones-acta-infraccion-informacion-consulta-lab-0687` |
| LAB-0689 | Alegaciones al acta de infracción de relaciones laborales individuales y colectivas | `alegaciones-acta-infraccion-relaciones-laborales-lab-0689` |
| LAB-0695 | Alegaciones negando la relación laboral y pidiendo comunicación de oficio (art. 151 LJS) | `alegaciones-negando-relacion-laboral-pidiendo-lab-0695` |
| LAB-0700 | Alegaciones de la empresa al acta de liquidación de cuotas de la Inspección de Trabajo | `alegaciones-empresa-acta-liquidacion-cuotas-inspeccion-lab-0700` |
| LAB-0701 | Alegaciones de la empresa a las actas de infracción y liquidación por los mismos hechos | `alegaciones-empresa-actas-infraccion-liquidacion-lab-0701` |
| LAB-0706 | Alegaciones de una ETT contra un acta de infracción en prevención de riesgos laborales | `alegaciones-ett-contra-acta-infraccion-prevencion-lab-0706` |

### Recursos (6)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0697 | Recurso de alzada contra la resolución que confirma el acta de liquidación de cuotas de la ITSS | `recurso-alzada-contra-resolucion-confirma-acta-lab-0697` |
| LAB-0698 | Recurso de alzada contra lo resuelto sobre actas de infracción y liquidación por los mismos hechos | `recurso-alzada-contra-lo-resuelto-sobre-actas-lab-0698` |
| LAB-0699 | Recurso de alzada contra la sanción impuesta por la autoridad laboral | `recurso-alzada-contra-sancion-impuesta-autoridad-lab-0699` |
| LAB-0702 | Recurso de alzada por motivos de fondo contra una sanción por infracción en el orden social | `recurso-alzada-motivos-fondo-contra-sancion-infraccion-lab-0702` |
| LAB-0703 | Recurso de alzada por defectos de procedimiento contra una sanción por infracción en el orden social | `recurso-alzada-defectos-procedimiento-contra-sancion-lab-0703` |
| LAB-0705 | Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción | `recurso-alzada-ett-contra-resolucion-confirma-acta-lab-0705` |

### Comunicaciones, requerimientos y cartas (2)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0693 | Requerimiento normalizado de la ITSS | `requerimiento-normalizado-itss-lab-0693` |
| LAB-0704 | Denuncia ante la Inspección de Trabajo y Seguridad Social | `denuncia-ante-inspeccion-trabajo-seguridad-social-lab-0704` |

### Escritos de trámite y otros (31)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0645 | Pedir ampliación del plazo del requerimiento de la Inspección de Trabajo | `pedir-ampliacion-plazo-requerimiento-inspeccion-trabajo-lab-0645` |
| LAB-0646 | Reconocer la responsabilidad y pagar voluntariamente la sanción de la Inspección | `reconocer-responsabilidad-pagar-voluntariamente-lab-0646` |
| LAB-0647 | Autorización para representar ante la Inspección de Trabajo | `autorizacion-representar-ante-inspeccion-trabajo-lab-0647` |
| LAB-0648 | Caducidad de las actuaciones de comprobación de la Inspección - alegaciones | `caducidad-actuaciones-comprobacion-inspeccion-lab-0648` |
| LAB-0649 | Prescripción de infracciones - alegaciones | `prescripcion-infracciones-alegaciones-lab-0649` |
| LAB-0650 | Alzada por caducidad de las actuaciones de comprobación de la Inspección | `alzada-caducidad-actuaciones-comprobacion-inspeccion-lab-0650` |
| LAB-0651 | Alzada por prescripción de infracciones | `alzada-prescripcion-infracciones-lab-0651` |
| LAB-0652 | Alzada por concurrencia de sanciones | `alzada-concurrencia-sanciones-lab-0652` |
| LAB-0653 | Concurrencia de sanciones - alegaciones | `concurrencia-sanciones-alegaciones-lab-0653` |
| LAB-0654 | Alzada contra sanción por obstrucción a la labor inspectora | `alzada-contra-sancion-obstruccion-labor-inspectora-lab-0654` |
| LAB-0655 | Alzada contra sanción a empresas colaboradoras en la gestión de la Seguridad Social | `alzada-contra-sancion-empresas-colaboradoras-gestion-lab-0655` |
| LAB-0656 | Alzada contra sanción en materia de movimientos migratorios | `alzada-contra-sancion-materia-movimientos-migratorios-lab-0656` |
| LAB-0657 | Alzada contra sanción en materia de cooperativas | `alzada-contra-sancion-materia-cooperativas-lab-0657` |
| LAB-0658 | Alzada contra sanción muy grave por autorización de trabajo de extranjeros | `alzada-contra-sancion-muy-grave-autorizacion-trabajo-lab-0658` |
| LAB-0664 | Alzada contra sanción de Seguridad Social a trabajadores y beneficiarios de prestaciones | `alzada-contra-sancion-seguridad-social-trabajadores-lab-0664` |
| LAB-0665 | Alzada contra sanción a las Mutuas de AT y EP | `alzada-contra-sancion-mutuas-at-ep-lab-0665` |
| LAB-0668 | Alzada contra sanción a empresas de inserción | `alzada-contra-sancion-empresas-insercion-lab-0668` |
| LAB-0670 | Alzada contra sanción a empresas de trabajo temporal | `alzada-contra-sancion-empresas-trabajo-temporal-lab-0670` |
| LAB-0671 | Alzada contra sanción a empresas usuarias | `alzada-contra-sancion-empresas-usuarias-lab-0671` |
| LAB-0672 | Alzada contra sanción a trabajadores | `alzada-contra-sancion-trabajadores-lab-0672` |
| LAB-0676 | Alzada contra sanción en materia de empleo y fomento del empleo | `alzada-contra-sancion-materia-empleo-fomento-empleo-lab-0676` |
| LAB-0678 | Alzada contra sanción de la Inspección por prevención de riesgos | `alzada-contra-sancion-inspeccion-prevencion-riesgos-lab-0678` |
| LAB-0680 | Alzada contra sanción por actividad transnacional de empresas de trabajo temporal | `alzada-contra-sancion-actividad-transnacional-empresas-lab-0680` |
| LAB-0682 | Alzada contra sanción por incumplir las normas sobre desplazamiento de trabajadores a España | `alzada-contra-sancion-incumplir-normas-sobre-lab-0682` |
| LAB-0683 | Alzada contra sanción por información y consulta en sociedades anónimas y cooperativas europeas | `alzada-contra-sancion-informacion-consulta-sociedades-lab-0683` |
| LAB-0686 | Alzada contra sanción por información y consulta en empresas y grupos de dimensión comunitaria | `alzada-contra-sancion-informacion-consulta-empresas-lab-0686` |
| LAB-0688 | Alzada contra sanción en materia de relaciones laborales individuales y colectivas | `alzada-contra-sancion-materia-relaciones-laborales-lab-0688` |
| LAB-0690 | Impugnar la sanción de Seguridad Social a un empresario - demanda | `impugnar-sancion-seguridad-social-empresario-demanda-lab-0690` |
| LAB-0691 | Citación oficial del Inspector de Trabajo y Seguridad Social | `citacion-oficial-inspector-trabajo-seguridad-social-lab-0691` |
| LAB-0692 | Citación oficial del Subinspector Laboral de Empleo y Seguridad Social | `citacion-oficial-subinspector-laboral-empleo-seguridad-lab-0692` |
| LAB-0694 | Caducidad de las actuaciones previas de la ITSS - declaración | `caducidad-actuaciones-previas-itss-declaracion-lab-0694` |
