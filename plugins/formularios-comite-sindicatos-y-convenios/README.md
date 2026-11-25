# Representantes de los trabajadores, sindicatos y convenios

> Plugin de Claude Code `formularios-comite-sindicatos-y-convenios` · **14 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para las relaciones colectivas: información y consulta a los representantes de los trabajadores, elecciones sindicales y su impugnación, garantías de los representantes, secciones sindicales, negociación de convenios y acuerdos de empresa, inaplicación del convenio y huelga.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 14 está al final):

- **Demandas, peticiones y solicitudes iniciales** (3). Por ejemplo: Demanda contra la denegación del registro de las actas de elección de delegados de personal; Solicitud de ejecución provisional para que la empresa respete la condición de representante; Solicitud de arbitraje para impugnar el proceso de elecciones sindicales.
- **Estatutos, actas, certificaciones y escrituras** (2). Por ejemplo: Acta de discrepancia de los representantes sobre las acciones formativas de la empresa; Acta de comparecencia de las partes en el arbitraje de elecciones sindicales.
- **Comunicaciones, requerimientos y cartas** (4). Por ejemplo: Comunicación de la plantilla sin representantes a la empresa de la opción elegida para designarlos; Comunicación de la empresa a los representantes del inicio de las acciones formativas; Comunicación mensual a los representantes de las horas extraordinarias realizadas en la empresa.
- **Escritos de trámite y otros** (5). Por ejemplo: Personal de libre disponibilidad y registro de jornada - acuerdo con la representación; Instalación de cámaras de videovigilancia - aviso a la representación de los trabajadores; Escrito del miembro del comité que invoca su prioridad de permanencia frente al traslado.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Comunicación mensual a los representantes de las horas extraordinarias»
   - «Solicitud de arbitraje para impugnar las elecciones sindicales»
   - «Información a los representantes de los contratos temporales celebrados»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-comite-sindicatos-y-convenios:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-comite-sindicatos-y-convenios:personal-libre-disponibilidad-registro-jornada-acuerdo-lab-0373`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 949 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-comite-sindicatos-y-convenios@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-comite-sindicatos-y-convenios@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-comite-sindicatos-y-convenios.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (14)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0373 | Personal de libre disponibilidad y registro de jornada - acuerdo con la representación | `personal-libre-disponibilidad-registro-jornada-acuerdo-lab-0373` |
| LAB-0374 | Instalación de cámaras de videovigilancia - aviso a la representación de los trabajadores | `instalacion-camaras-videovigilancia-aviso-lab-0374` |
| LAB-0375 | Comunicación de la plantilla sin representantes a la empresa de la opción elegida para designarlos | `comunicacion-plantilla-sin-representantes-empresa-lab-0375` |
| LAB-0376 | Demanda contra la denegación del registro de las actas de elección de delegados de personal | `demanda-contra-denegacion-registro-actas-eleccion-lab-0376` |
| LAB-0377 | Comunicación de la empresa a los representantes del inicio de las acciones formativas | `comunicacion-empresa-representantes-inicio-acciones-lab-0377` |
| LAB-0378 | Acta de discrepancia de los representantes sobre las acciones formativas de la empresa | `acta-discrepancia-representantes-sobre-acciones-lab-0378` |
| LAB-0379 | Solicitud de ejecución provisional para que la empresa respete la condición de representante | `solicitud-ejecucion-provisional-empresa-respete-lab-0379` |
| LAB-0380 | Escrito del miembro del comité que invoca su prioridad de permanencia frente al traslado | `escrito-miembro-comite-invoca-prioridad-permanencia-lab-0380` |
| LAB-0381 | Solicitud de arbitraje para impugnar el proceso de elecciones sindicales | `solicitud-arbitraje-impugnar-proceso-elecciones-lab-0381` |
| LAB-0382 | Información de la contratista a los representantes de los trabajadores antes de iniciar la actividad | `informacion-contratista-representantes-trabajadores-lab-0382` |
| LAB-0383 | Comunicación mensual a los representantes de las horas extraordinarias realizadas en la empresa | `comunicacion-mensual-representantes-horas-lab-0383` |
| LAB-0384 | Notificación a los representantes de los contratos de duración determinada celebrados | `notificacion-representantes-contratos-duracion-lab-0384` |
| LAB-0386 | Impugnación en vía arbitral de la designación de un delegado de personal | `impugnacion-via-arbitral-designacion-delegado-personal-lab-0386` |
| LAB-0387 | Acta de comparecencia de las partes en el arbitraje de elecciones sindicales | `acta-comparecencia-partes-arbitraje-elecciones-lab-0387` |

## Privacidad

Ver `PRIVACY.md`.
