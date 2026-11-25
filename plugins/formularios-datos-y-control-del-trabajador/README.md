# Protección de datos y control empresarial

> Plugin de Claude Code `formularios-datos-y-control-del-trabajador` · **11 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para el control de la actividad y los datos de la plantilla: información sobre protección de datos a los empleados, videovigilancia y geolocalización, uso de medios informáticos y teléfono de empresa, desconexión digital, códigos de conducta y de vestimenta, y cláusulas de confidencialidad.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 11 está al final):

- **Comunicaciones, requerimientos y cartas** (4). Por ejemplo: Aviso emergente sobre el uso laboral de los medios de la empresa; Aviso al trabajador de videovigilancia, control de jornada o geolocalización; Comunicación al trabajador de las normas y controles sobre el uso de los equipos informáticos.
- **Escritos de trámite y otros** (7). Por ejemplo: Confidencialidad, control de medios y desconexión digital - cláusula; Información sobre protección de datos a los empleados; Código de conducta en la relación empresa-trabajador.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Información sobre protección de datos a los empleados»
   - «Normas sobre el uso de los equipos informáticos de la empresa»
   - «Cláusula de confidencialidad y desconexión digital»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-datos-y-control-del-trabajador:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-datos-y-control-del-trabajador:confidencialidad-control-medios-desconexion-digital-lab-0355`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 698 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-datos-y-control-del-trabajador@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-datos-y-control-del-trabajador@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-datos-y-control-del-trabajador.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (11)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0355 | Confidencialidad, control de medios y desconexión digital - cláusula | `confidencialidad-control-medios-desconexion-digital-lab-0355` |
| LAB-0356 | Información sobre protección de datos a los empleados | `informacion-sobre-proteccion-datos-empleados-lab-0356` |
| LAB-0357 | Aviso emergente sobre el uso laboral de los medios de la empresa | `aviso-emergente-sobre-uso-laboral-medios-empresa-lab-0357` |
| LAB-0358 | Código de conducta en la relación empresa-trabajador | `codigo-conducta-relacion-empresa-trabajador-lab-0358` |
| LAB-0359 | Vestimenta en la empresa - código | `vestimenta-empresa-codigo-lab-0359` |
| LAB-0360 | Normas de uso del sistema informático y las comunicaciones electrónicas | `normas-uso-sistema-informatico-comunicaciones-lab-0360` |
| LAB-0361 | Protección de datos en contratos con empresa subcontratista - cláusula | `proteccion-datos-contratos-empresa-subcontratista-lab-0361` |
| LAB-0362 | Información sobre protección de datos en la geolocalización - cláusula | `informacion-sobre-proteccion-datos-geolocalizacion-lab-0362` |
| LAB-0363 | Aviso al trabajador de videovigilancia, control de jornada o geolocalización | `aviso-trabajador-videovigilancia-control-jornada-lab-0363` |
| LAB-0364 | Comunicación al trabajador de las normas y controles sobre el uso de los equipos informáticos | `comunicacion-trabajador-normas-controles-sobre-uso-lab-0364` |
| LAB-0365 | Comunicación al trabajador de las normas y controles sobre el uso del teléfono de empresa | `comunicacion-trabajador-normas-controles-sobre-uso-lab-0365` |

## Privacidad

Ver `PRIVACY.md`.
