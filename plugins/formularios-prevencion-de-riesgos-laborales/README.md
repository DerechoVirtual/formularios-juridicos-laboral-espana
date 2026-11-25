# Prevención de riesgos laborales

> Plugin de Claude Code `formularios-prevencion-de-riesgos-laborales` · **7 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la prevención de riesgos: comunicación de apertura de centro de trabajo, formación e información preventiva, documentación preventiva en ETT y contratas, delegados de prevención y comunicaciones con ellos, y requerimientos de la Inspección en materia preventiva.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 7 está al final):

- **Comunicaciones, requerimientos y cartas** (3). Por ejemplo: Comunicación a los delegados de prevención del requerimiento de los técnicos públicos habilitados; Aviso a los delegados de prevención del requerimiento de subsanación de la Inspección de Trabajo; Comunicación de apertura del centro de trabajo en una obra de construcción.
- **Escritos de trámite y otros** (4). Por ejemplo: Asistencia a formación - hoja de firmas; Apertura de expediente sancionador - aviso a representantes, sindicato y delegado de prevención; Anexo I del contrato de puesta a disposición sobre los riesgos laborales del puesto.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Comunicación de apertura del centro de trabajo en una obra»
   - «Hoja de firmas de asistencia a la formación preventiva»
   - «Aviso a los delegados de prevención de un requerimiento de la Inspección»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-prevencion-de-riesgos-laborales:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-prevencion-de-riesgos-laborales:asistencia-formacion-hoja-firmas-lab-0366`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 498 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-prevencion-de-riesgos-laborales@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-prevencion-de-riesgos-laborales@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-prevencion-de-riesgos-laborales.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (7)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0366 | Asistencia a formación - hoja de firmas | `asistencia-formacion-hoja-firmas-lab-0366` |
| LAB-0367 | Apertura de expediente sancionador - aviso a representantes, sindicato y delegado de prevención | `apertura-expediente-sancionador-aviso-representantes-lab-0367` |
| LAB-0368 | Comunicación a los delegados de prevención del requerimiento de los técnicos públicos habilitados | `comunicacion-delegados-prevencion-requerimiento-lab-0368` |
| LAB-0369 | Aviso a los delegados de prevención del requerimiento de subsanación de la Inspección de Trabajo | `aviso-delegados-prevencion-requerimiento-subsanacion-lab-0369` |
| LAB-0370 | Comunicación de apertura del centro de trabajo en una obra de construcción | `comunicacion-apertura-centro-trabajo-obra-construccion-lab-0370` |
| LAB-0371 | Anexo I del contrato de puesta a disposición sobre los riesgos laborales del puesto | `anexo-i-contrato-puesta-disposicion-sobre-riesgos-lab-0371` |
| LAB-0372 | Anexo III del contrato entre ETT y trabajador en misión sobre la formación preventiva recibida | `anexo-iii-contrato-entre-ett-trabajador-mision-sobre-lab-0372` |

## Privacidad

Ver `PRIVACY.md`.
