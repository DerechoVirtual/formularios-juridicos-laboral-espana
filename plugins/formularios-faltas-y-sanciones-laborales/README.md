# Faltas y sanciones laborales

> Plugin de Claude Code `formularios-faltas-y-sanciones-laborales` · **42 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el poder disciplinario de la empresa: cartas de amonestación y sanción por faltas leves, graves y muy graves, expediente contradictorio, pliego de cargos y descargos, audiencia a representantes y delegados sindicales, y cancelación de antecedentes.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 42 está al final):

- **Contestaciones, oposiciones y alegaciones** (2). Por ejemplo: Descargos del trabajador - pliego; Alegaciones del trabajador en el expediente contradictorio.
- **Recursos** (1). Por ejemplo: Recurso del socio trabajador contra su expulsión disciplinaria de la cooperativa.
- **Estatutos, actas, certificaciones y escrituras** (3). Por ejemplo: Acta del consejo rector que impone una sanción disciplinaria definitiva al socio trabajador; Informe final del instructor en el expediente contradictorio a un representante de los trabajadores; Informe de los representantes de los trabajadores en un expediente disciplinario contradictorio.
- **Comunicaciones, requerimientos y cartas** (7). Por ejemplo: Comunicación a los representantes de los trabajadores de los despidos disciplinarios impuestos; Comunicación al socio trabajador de la apertura de expediente disciplinario de expulsión; Notificación al socio trabajador de su expulsión disciplinaria de la cooperativa.
- **Escritos de trámite y otros** (29). Por ejemplo: Cancelar antecedentes por sanción - comunicación del trabajador; Ficha de antecedentes por sanción; Pedir la cancelación de antecedentes por sanción.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Carta de sanción por falta grave»
   - «Pliego de cargos en un expediente contradictorio»
   - «Petición de cancelación de antecedentes por sanción»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-faltas-y-sanciones-laborales:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-faltas-y-sanciones-laborales:cancelar-antecedentes-sancion-comunicacion-trabajador-lab-0388`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 2.387 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-faltas-y-sanciones-laborales@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-faltas-y-sanciones-laborales@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-faltas-y-sanciones-laborales.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (42)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0388 | Cancelar antecedentes por sanción - comunicación del trabajador | `cancelar-antecedentes-sancion-comunicacion-trabajador-lab-0388` |
| LAB-0389 | Ficha de antecedentes por sanción | `ficha-antecedentes-sancion-lab-0389` |
| LAB-0390 | Pedir la cancelación de antecedentes por sanción | `pedir-cancelacion-antecedentes-sancion-lab-0390` |
| LAB-0391 | Sanción por faltas de asistencia o puntualidad - carta | `sancion-faltas-asistencia-puntualidad-carta-lab-0391` |
| LAB-0392 | Sanción por transgresión de la buena fe y abuso de confianza - carta | `sancion-transgresion-buena-fe-abuso-confianza-carta-lab-0392` |
| LAB-0393 | Sanción por ofensas verbales o físicas - carta | `sancion-ofensas-verbales-fisicas-carta-lab-0393` |
| LAB-0394 | Sanción por indisciplina o desobediencia - carta | `sancion-indisciplina-desobediencia-carta-lab-0394` |
| LAB-0395 | Sanción por otras infracciones del convenio - carta | `sancion-otras-infracciones-convenio-carta-lab-0395` |
| LAB-0396 | Sanción por reincidencia o reiteración de faltas - carta | `sancion-reincidencia-reiteracion-faltas-carta-lab-0396` |
| LAB-0397 | Sanción por bajo rendimiento - carta | `sancion-bajo-rendimiento-carta-lab-0397` |
| LAB-0398 | Sanción por embriaguez habitual o toxicomanía - carta | `sancion-embriaguez-habitual-toxicomania-carta-lab-0398` |
| LAB-0399 | Sobreseimiento del expediente sancionador - propuesta | `sobreseimiento-expediente-sancionador-propuesta-lab-0399` |
| LAB-0400 | Sanción impuesta - aviso a la representación de los trabajadores en el expediente sancionador | `sancion-impuesta-aviso-representacion-trabajadores-lab-0400` |
| LAB-0401 | Sanción propuesta en el expediente disciplinario | `sancion-propuesta-expediente-disciplinario-lab-0401` |
| LAB-0402 | Cargos por reincidencia o reiteración de faltas - pliego | `cargos-reincidencia-reiteracion-faltas-pliego-lab-0402` |
| LAB-0403 | Cargos por otras infracciones del convenio - pliego | `cargos-otras-infracciones-convenio-pliego-lab-0403` |
| LAB-0404 | Descargos del trabajador - pliego | `descargos-trabajador-pliego-lab-0404` |
| LAB-0405 | Cargos por embriaguez habitual o toxicomanía - pliego | `cargos-embriaguez-habitual-toxicomania-pliego-lab-0405` |
| LAB-0406 | Actuaciones no disciplinarias - propuesta | `actuaciones-no-disciplinarias-propuesta-lab-0406` |
| LAB-0407 | Cargos por transgresión de la buena fe y abuso de confianza - pliego | `cargos-transgresion-buena-fe-abuso-confianza-pliego-lab-0407` |
| LAB-0408 | Cargos por bajo rendimiento - pliego | `cargos-bajo-rendimiento-pliego-lab-0408` |
| LAB-0409 | Cargos por ofensas verbales o físicas - pliego | `cargos-ofensas-verbales-fisicas-pliego-lab-0409` |
| LAB-0410 | Cargos por indisciplina o desobediencia - pliego | `cargos-indisciplina-desobediencia-pliego-lab-0410` |
| LAB-0411 | Cargos por faltas de asistencia o puntualidad - pliego | `cargos-faltas-asistencia-puntualidad-pliego-lab-0411` |
| LAB-0412 | Diligencias en el expediente sancionador | `diligencias-expediente-sancionador-lab-0412` |
| LAB-0413 | Aceptación del cargo en el expediente sancionador | `aceptacion-cargo-expediente-sancionador-lab-0413` |
| LAB-0414 | Nombramiento en el expediente sancionador | `nombramiento-expediente-sancionador-lab-0414` |
| LAB-0415 | Apercibimiento sin sanción - carta | `apercibimiento-sin-sancion-carta-lab-0415` |
| LAB-0416 | Comunicación a los representantes de los trabajadores de los despidos disciplinarios impuestos | `comunicacion-representantes-trabajadores-despidos-lab-0416` |
| LAB-0417 | Acta del consejo rector que impone una sanción disciplinaria definitiva al socio trabajador | `acta-consejo-rector-impone-sancion-disciplinaria-lab-0417` |
| LAB-0418 | Comunicación al socio trabajador de la apertura de expediente disciplinario de expulsión | `comunicacion-socio-trabajador-apertura-expediente-lab-0418` |
| LAB-0419 | Pliego de descargo del socio trabajador frente a la propuesta de expulsión | `pliego-descargo-socio-trabajador-frente-propuesta-lab-0419` |
| LAB-0420 | Notificación al socio trabajador de su expulsión disciplinaria de la cooperativa | `notificacion-socio-trabajador-expulsion-disciplinaria-lab-0420` |
| LAB-0421 | Recurso del socio trabajador contra su expulsión disciplinaria de la cooperativa | `recurso-socio-trabajador-contra-expulsion-lab-0421` |
| LAB-0422 | Informe final del instructor en el expediente contradictorio a un representante de los trabajadores | `informe-final-instructor-expediente-contradictorio-lab-0422` |
| LAB-0423 | Informe de los representantes de los trabajadores en un expediente disciplinario contradictorio | `informe-representantes-trabajadores-expediente-lab-0423` |
| LAB-0424 | Comunicación a los representantes de una falta muy grave y de la sanción distinta del despido | `comunicacion-representantes-falta-muy-grave-sancion-lab-0424` |
| LAB-0425 | Aviso al trabajador del cierre del expediente contradictorio y de la sanción distinta del despido | `aviso-trabajador-cierre-expediente-contradictorio-lab-0425` |
| LAB-0426 | Carta de sanción al trabajador que abandonó su puesto de trabajo | `carta-sancion-trabajador-abandono-puesto-trabajo-lab-0426` |
| LAB-0427 | Aviso al trabajador de la fecha en que empieza a cumplir la suspensión de empleo y sueldo | `aviso-trabajador-fecha-empieza-cumplir-suspension-lab-0427` |
| LAB-0428 | Alegaciones del trabajador en el expediente contradictorio | `alegaciones-trabajador-expediente-contradictorio-lab-0428` |
| LAB-0429 | Propuesta del instructor de despido del representante en el expediente contradictorio | `propuesta-instructor-despido-representante-expediente-lab-0429` |

## Privacidad

Ver `PRIVACY.md`.
