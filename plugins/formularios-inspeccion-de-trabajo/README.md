# Inspección de Trabajo y sanciones administrativas

> Plugin de Claude Code `formularios-inspeccion-de-trabajo` · **62 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para tratar con la Inspección de Trabajo y la autoridad laboral: alegaciones a actas de infracción y de liquidación, recursos de alzada contra sanciones en el orden social, pago voluntario con reducción, denuncias ante la Inspección y comunicaciones a la autoridad laboral.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 62 está al final):

- **Demandas, peticiones y solicitudes iniciales** (1). Por ejemplo: Recurso contencioso-administrativo contra la resolución firme de actas de liquidación o infracción.
- **Contestaciones, oposiciones y alegaciones** (22). Por ejemplo: Alegaciones al acta de infracción de movimientos migratorios; Alegaciones al acta de infracción de empresas colaboradoras en la gestión de la Seguridad Social; Alegaciones al acta de infracción muy grave por autorización de trabajo de extranjeros.
- **Recursos** (6). Por ejemplo: Recurso de alzada contra la resolución que confirma el acta de liquidación de cuotas de la ITSS; Recurso de alzada contra lo resuelto sobre actas de infracción y liquidación por los mismos hechos; Recurso de alzada contra la sanción impuesta por la autoridad laboral.
- **Comunicaciones, requerimientos y cartas** (2). Por ejemplo: Requerimiento normalizado de la ITSS; Denuncia ante la Inspección de Trabajo y Seguridad Social.
- **Escritos de trámite y otros** (31). Por ejemplo: Pedir ampliación del plazo del requerimiento de la Inspección de Trabajo; Reconocer la responsabilidad y pagar voluntariamente la sanción de la Inspección; Autorización para representar ante la Inspección de Trabajo.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Alegaciones a un acta de infracción de la Inspección de Trabajo»
   - «Recurso de alzada contra una sanción en el orden social»
   - «Denuncia ante la Inspección de Trabajo»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-inspeccion-de-trabajo:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-inspeccion-de-trabajo:pedir-ampliacion-plazo-requerimiento-inspeccion-trabajo-lab-0645`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 25-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 11, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 3.651 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-inspeccion-de-trabajo@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-inspeccion-de-trabajo@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-inspeccion-de-trabajo.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (62)

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
| LAB-0659 | Alegaciones al acta de infracción de movimientos migratorios | `alegaciones-acta-infraccion-movimientos-migratorios-lab-0659` |
| LAB-0660 | Alegaciones al acta de infracción de empresas colaboradoras en la gestión de la Seguridad Social | `alegaciones-acta-infraccion-empresas-colaboradoras-lab-0660` |
| LAB-0661 | Alegaciones al acta de infracción muy grave por autorización de trabajo de extranjeros | `alegaciones-acta-infraccion-muy-grave-autorizacion-lab-0661` |
| LAB-0662 | Alegaciones al acta de infracción en materia de cooperativas | `alegaciones-acta-infraccion-materia-cooperativas-lab-0662` |
| LAB-0663 | Alegaciones al acta de infracción por obstrucción a la labor inspectora | `alegaciones-acta-infraccion-obstruccion-labor-lab-0663` |
| LAB-0664 | Alzada contra sanción de Seguridad Social a trabajadores y beneficiarios de prestaciones | `alzada-contra-sancion-seguridad-social-trabajadores-lab-0664` |
| LAB-0665 | Alzada contra sanción a las Mutuas de AT y EP | `alzada-contra-sancion-mutuas-at-ep-lab-0665` |
| LAB-0666 | Alegaciones al acta de infracción de Seguridad Social (trabajadores, beneficiarios y solicitantes) | `alegaciones-acta-infraccion-seguridad-social-lab-0666` |
| LAB-0667 | Alegaciones al acta de infracción de las Mutuas de AT y EP | `alegaciones-acta-infraccion-mutuas-at-ep-lab-0667` |
| LAB-0668 | Alzada contra sanción a empresas de inserción | `alzada-contra-sancion-empresas-insercion-lab-0668` |
| LAB-0669 | Alegaciones al acta de infracción de empresas de inserción | `alegaciones-acta-infraccion-empresas-insercion-lab-0669` |
| LAB-0670 | Alzada contra sanción a empresas de trabajo temporal | `alzada-contra-sancion-empresas-trabajo-temporal-lab-0670` |
| LAB-0671 | Alzada contra sanción a empresas usuarias | `alzada-contra-sancion-empresas-usuarias-lab-0671` |
| LAB-0672 | Alzada contra sanción a trabajadores | `alzada-contra-sancion-trabajadores-lab-0672` |
| LAB-0673 | Alegaciones al acta de infracción de empresas usuarias | `alegaciones-acta-infraccion-empresas-usuarias-lab-0673` |
| LAB-0674 | Alegaciones al acta de infracción de trabajadores | `alegaciones-acta-infraccion-trabajadores-lab-0674` |
| LAB-0675 | Alegaciones al acta de infracción de empresas de trabajo temporal | `alegaciones-acta-infraccion-empresas-trabajo-temporal-lab-0675` |
| LAB-0676 | Alzada contra sanción en materia de empleo y fomento del empleo | `alzada-contra-sancion-materia-empleo-fomento-empleo-lab-0676` |
| LAB-0677 | Alegaciones al acta de infracción en materia de empleo y fomento del empleo | `alegaciones-acta-infraccion-materia-empleo-fomento-lab-0677` |
| LAB-0678 | Alzada contra sanción de la Inspección por prevención de riesgos | `alzada-contra-sancion-inspeccion-prevencion-riesgos-lab-0678` |
| LAB-0679 | Alegaciones al acta de infracción de prevención de riesgos laborales | `alegaciones-acta-infraccion-prevencion-riesgos-lab-0679` |
| LAB-0680 | Alzada contra sanción por actividad transnacional de empresas de trabajo temporal | `alzada-contra-sancion-actividad-transnacional-empresas-lab-0680` |
| LAB-0681 | Alegaciones al acta de infracción por actividad transnacional de empresas de trabajo temporal | `alegaciones-acta-infraccion-actividad-transnacional-lab-0681` |
| LAB-0682 | Alzada contra sanción por incumplir las normas sobre desplazamiento de trabajadores a España | `alzada-contra-sancion-incumplir-normas-sobre-lab-0682` |
| LAB-0683 | Alzada contra sanción por información y consulta en sociedades anónimas y cooperativas europeas | `alzada-contra-sancion-informacion-consulta-sociedades-lab-0683` |
| LAB-0684 | Alegaciones al acta de infracción por desplazamiento de trabajadores a España | `alegaciones-acta-infraccion-desplazamiento-lab-0684` |
| LAB-0685 | Alegaciones al acta de infracción por información y consulta en sociedades europeas | `alegaciones-acta-infraccion-informacion-consulta-lab-0685` |
| LAB-0686 | Alzada contra sanción por información y consulta en empresas y grupos de dimensión comunitaria | `alzada-contra-sancion-informacion-consulta-empresas-lab-0686` |
| LAB-0687 | Alegaciones al acta de infracción por información y consulta en grupos de dimensión comunitaria | `alegaciones-acta-infraccion-informacion-consulta-lab-0687` |
| LAB-0688 | Alzada contra sanción en materia de relaciones laborales individuales y colectivas | `alzada-contra-sancion-materia-relaciones-laborales-lab-0688` |
| LAB-0689 | Alegaciones al acta de infracción de relaciones laborales individuales y colectivas | `alegaciones-acta-infraccion-relaciones-laborales-lab-0689` |
| LAB-0690 | Impugnar la sanción de Seguridad Social a un empresario - demanda | `impugnar-sancion-seguridad-social-empresario-demanda-lab-0690` |
| LAB-0691 | Citación oficial del Inspector de Trabajo y Seguridad Social | `citacion-oficial-inspector-trabajo-seguridad-social-lab-0691` |
| LAB-0692 | Citación oficial del Subinspector Laboral de Empleo y Seguridad Social | `citacion-oficial-subinspector-laboral-empleo-seguridad-lab-0692` |
| LAB-0693 | Requerimiento normalizado de la ITSS | `requerimiento-normalizado-itss-lab-0693` |
| LAB-0694 | Caducidad de las actuaciones previas de la ITSS - declaración | `caducidad-actuaciones-previas-itss-declaracion-lab-0694` |
| LAB-0695 | Alegaciones negando la relación laboral y pidiendo comunicación de oficio (art. 151 LJS) | `alegaciones-negando-relacion-laboral-pidiendo-lab-0695` |
| LAB-0696 | Recurso contencioso-administrativo contra la resolución firme de actas de liquidación o infracción | `recurso-contencioso-administrativo-contra-resolucion-lab-0696` |
| LAB-0697 | Recurso de alzada contra la resolución que confirma el acta de liquidación de cuotas de la ITSS | `recurso-alzada-contra-resolucion-confirma-acta-lab-0697` |
| LAB-0698 | Recurso de alzada contra lo resuelto sobre actas de infracción y liquidación por los mismos hechos | `recurso-alzada-contra-lo-resuelto-sobre-actas-lab-0698` |
| LAB-0699 | Recurso de alzada contra la sanción impuesta por la autoridad laboral | `recurso-alzada-contra-sancion-impuesta-autoridad-lab-0699` |
| LAB-0700 | Alegaciones de la empresa al acta de liquidación de cuotas de la Inspección de Trabajo | `alegaciones-empresa-acta-liquidacion-cuotas-inspeccion-lab-0700` |
| LAB-0701 | Alegaciones de la empresa a las actas de infracción y liquidación por los mismos hechos | `alegaciones-empresa-actas-infraccion-liquidacion-lab-0701` |
| LAB-0702 | Recurso de alzada por motivos de fondo contra una sanción por infracción en el orden social | `recurso-alzada-motivos-fondo-contra-sancion-infraccion-lab-0702` |
| LAB-0703 | Recurso de alzada por defectos de procedimiento contra una sanción por infracción en el orden social | `recurso-alzada-defectos-procedimiento-contra-sancion-lab-0703` |
| LAB-0704 | Denuncia ante la Inspección de Trabajo y Seguridad Social | `denuncia-ante-inspeccion-trabajo-seguridad-social-lab-0704` |
| LAB-0705 | Recurso de alzada de una ETT contra la resolución que confirma un acta de infracción | `recurso-alzada-ett-contra-resolucion-confirma-acta-lab-0705` |
| LAB-0706 | Alegaciones de una ETT contra un acta de infracción en prevención de riesgos laborales | `alegaciones-ett-contra-acta-infraccion-prevencion-lab-0706` |

## Privacidad

Ver `PRIVACY.md`.
