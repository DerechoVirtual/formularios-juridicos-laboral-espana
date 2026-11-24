# Laboral: préstamo al trabajador, despido en concurso y suplicación

> Plugin de Claude Code `formularios-laboral` · **3 formularios** · Laboral · normativa revisada el 24-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Tres formularios laborales que aparecían en estas colecciones: contrato de préstamo de la empresa a un trabajador, papeleta de conciliación contra el despido objetivo por causas económicas en una empresa en concurso y recurso de suplicación contra el auto que deniega autorizar el despido colectivo.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 3 está al final):

- **Demandas, peticiones y solicitudes iniciales** (1). Por ejemplo: Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso.
- **Contratos, pactos y cláusulas** (1). Por ejemplo: Contrato de préstamo de la empresa a un trabajador.
- **Escritos de trámite y otros** (1). Por ejemplo: Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Contrato de préstamo de la empresa a un trabajador»
   - «Papeleta de conciliación por despido objetivo en empresa en concurso»
   - «Recurso de suplicación contra el auto del despido colectivo en el concurso»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-laboral:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-laboral:contrato-prestamo-empresa-trabajador-lab-0001`. Los nombres están en la lista de formularios de abajo.

## Qué hace Claude cuando usas un formulario

1. Comprueba que Jurisprudenciator está conectado. Si no lo está, se para y te dice cómo conectarlo: no redacta nada sin él. Todos los datos jurídicos del documento (artículos vigentes, sentencias con su ECLI, datos registrales) salen de Jurisprudenciator; nunca de memoria.
2. Te pide en una sola tanda los datos del caso (partes, órgano, fechas, importes…). Lo que no sepas queda como hueco visible.
3. Resuelve contigo las opciones que el formulario deja abiertas y decide qué párrafos opcionales entran según los hechos.
4. Aplica las notas de actualización de la revisión del 24-11-2026 (reformas legales, órganos judiciales de la LO 1/2025, plazos).
5. Comprueba en el BOE, con Jurisprudenciator, cada norma que cita el documento; si alguna ha cambiado, usa la redacción vigente y te lo dice.
6. Te entrega el documento en Word **tal cual es el formulario**: empieza por su primera línea, sin títulos, notas ni explicaciones añadidas, en Times New Roman 12, interlineado 1,15 y texto justificado. En el chat te dice lo que queda pendiente y, si es un escrito, el plazo y ante quién se presenta.

El resultado es un borrador para que lo revise un profesional antes de usarlo.

## Antes de empezar

- **Dónde funciona:** en Claude Code y en Claude (web, escritorio y Cowork). Se instala desde este repositorio de GitHub o subiendo el ZIP del plugin.
- **Jurisprudenciator es imprescindible:** el plugin trae el conector y cada skill trabaja siempre con él. Sin una cuenta de Jurisprudenciator conectada, las skills se paran y no redactan nada. La primera vez hay que iniciar sesión (en Claude Code, con `/mcp`; o con tu URL personal: https://jurisprudenciator.lexiaipro.org/instalacion). Si ya tienes Jurisprudenciator conectado en Claude, las skills usan ese.
- **Espacio que ocupa:** unos 240 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-laboral@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-laboral@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-laboral.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0001 | Contrato de préstamo de la empresa a un trabajador | `contrato-prestamo-empresa-trabajador-lab-0001` |
| LAB-0002 | Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso | `papeleta-conciliacion-contra-despido-objetivo-causas-lab-0002` |
| LAB-0003 | Escrito de recurso de suplicación contra el auto que deniega autorizar el despido colectivo | `escrito-recurso-suplicacion-contra-auto-deniega-lab-0003` |

## Privacidad

Ver `PRIVACY.md`.
