# Despido y extinción del contrato de trabajo

> Plugin de Claude Code `formularios-despidos` · **89 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la extinción del contrato: carta de despido disciplinario y objetivo, finiquito, dimisión y baja voluntaria, fin de contratos temporales, extinción a instancia del trabajador (art. 50 ET), acuerdos transaccionales y demandas por despido (nulo, improcedente, de representantes).

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 89 está al final):

- **Demandas, peticiones y solicitudes iniciales** (19). Por ejemplo: Demanda por despido de un eventual por circunstancias de la producción, previa a la reforma de 2021; Demanda de despido del trabajador jubilado parcialmente que tenía un contrato a tiempo parcial; Demanda de despido del representante de comercio con reclamación de la indemnización por clientela.
- **Contratos, pactos y cláusulas** (3). Por ejemplo: Acuerdo de empresa y trabajador para extinguir el contrato de mutuo acuerdo; Acuerdo que suspende cautelarmente los derechos del socio trabajador hasta que su baja sea ejecutiva; Acuerdo del consejo rector que califica como justificada la baja de un socio trabajador.
- **Comunicaciones, requerimientos y cartas** (25). Por ejemplo: Aviso de audiencia previa al despido disciplinario; Aviso al trabajador del fin de la excedencia; Carta del trabajador que denuncia su contrato temporal para extinguirlo a su vencimiento.
- **Escritos de trámite y otros** (42). Por ejemplo: Renuncia del fijo discontinuo al llamamiento; Despido nulo por negar la reincorporación tras excedencia por cuidado de pareja de hecho - demanda; Despido nulo por discriminación por enfermedad o estado de salud - demanda.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Carta de despido disciplinario»
   - «Carta de despido objetivo por causas económicas»
   - «Demanda por despido improcedente»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-despidos:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-despidos:aviso-audiencia-previa-despido-disciplinario-lab-0430`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 5.291 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-despidos@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-despidos@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-despidos.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (89)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0430 | Aviso de audiencia previa al despido disciplinario | `aviso-audiencia-previa-despido-disciplinario-lab-0430` |
| LAB-0431 | Renuncia del fijo discontinuo al llamamiento | `renuncia-fijo-discontinuo-llamamiento-lab-0431` |
| LAB-0432 | Despido nulo por negar la reincorporación tras excedencia por cuidado de pareja de hecho - demanda | `despido-nulo-negar-reincorporacion-tras-excedencia-lab-0432` |
| LAB-0434 | Despido nulo por discriminación por enfermedad o estado de salud - demanda | `despido-nulo-discriminacion-enfermedad-estado-salud-lab-0434` |
| LAB-0435 | Ejecución del auto de readmisión irregular - escrito | `ejecucion-auto-readmision-irregular-escrito-lab-0435` |
| LAB-0436 | Despido de empleada del hogar - demanda | `despido-empleada-hogar-demanda-lab-0436` |
| LAB-0437 | Respuesta del trabajador a la recolocación tras el fin de la obra de construcción | `respuesta-trabajador-recolocacion-tras-fin-obra-lab-0437` |
| LAB-0438 | Recolocación en contrato adscrito a obra de construcción - cláusula | `recolocacion-contrato-adscrito-obra-construccion-lab-0438` |
| LAB-0439 | Propuesta de recolocación al trabajador tras el fin de la obra de construcción | `propuesta-recolocacion-trabajador-tras-fin-obra-lab-0439` |
| LAB-0440 | Recolocación de obra de un indefinido adscrito a obra - propuesta de la empresa | `recolocacion-obra-indefinido-adscrito-obra-propuesta-lab-0440` |
| LAB-0441 | Baja voluntaria por jubilación - carta del trabajador | `baja-voluntaria-jubilacion-carta-trabajador-lab-0441` |
| LAB-0442 | Despido nulo por vulneración de derechos fundamentales - demanda | `despido-nulo-vulneracion-derechos-fundamentales-demanda-lab-0442` |
| LAB-0443 | Extinción del contrato por edad de jubilación - carta de la empresa | `extincion-contrato-edad-jubilacion-carta-empresa-lab-0443` |
| LAB-0444 | Respuesta a la baja voluntaria del trabajador - carta | `respuesta-baja-voluntaria-trabajador-carta-lab-0444` |
| LAB-0445 | Despido y reconocimiento de relación laboral - demanda | `despido-reconocimiento-relacion-laboral-demanda-lab-0445` |
| LAB-0446 | Extinción por impago o retrasos de salario - papeleta de conciliación del trabajador | `extincion-impago-retrasos-salario-papeleta-lab-0446` |
| LAB-0447 | Transacción sobre el despido - acuerdo | `transaccion-sobre-despido-acuerdo-lab-0447` |
| LAB-0448 | Aviso al trabajador del fin de la excedencia | `aviso-trabajador-fin-excedencia-lab-0448` |
| LAB-0449 | Indemnización por extinción por causas objetivas - demanda | `indemnizacion-extincion-causas-objetivas-demanda-lab-0449` |
| LAB-0450 | Despido verbal - demanda | `despido-verbal-demanda-lab-0450` |
| LAB-0451 | Dimisión o baja voluntaria del trabajador - carta | `dimision-baja-voluntaria-trabajador-carta-lab-0451` |
| LAB-0452 | Despido disciplinario - carta | `despido-disciplinario-carta-lab-0452` |
| LAB-0453 | Despido por causas objetivas - carta | `despido-causas-objetivas-carta-lab-0453` |
| LAB-0454 | Desistimiento del alto directivo - comunicación a la empresa | `desistimiento-alto-directivo-comunicacion-empresa-lab-0454` |
| LAB-0455 | Extinción del contrato de empleada del hogar - comunicación del empleador | `extincion-contrato-empleada-hogar-comunicacion-lab-0455` |
| LAB-0456 | Desistimiento de la empresa frente al alto directivo - comunicación | `desistimiento-empresa-frente-alto-directivo-lab-0456` |
| LAB-0457 | Fútbol sala - inicio del procedimiento abreviado de resolución contractual anticipada | `futbol-sala-inicio-procedimiento-abreviado-resolucion-lab-0457` |
| LAB-0458 | Resolución del contrato de TRADE - comunicación | `resolucion-contrato-trade-comunicacion-lab-0458` |
| LAB-0459 | Despido nulo por vulnerar derechos de conciliación - demanda | `despido-nulo-vulnerar-derechos-conciliacion-demanda-lab-0459` |
| LAB-0460 | Despido improcedente - demanda | `despido-improcedente-demanda-lab-0460` |
| LAB-0461 | Opción tras despido improcedente - escrito de la parte actora o representación | `opcion-tras-despido-improcedente-escrito-parte-actora-lab-0461` |
| LAB-0462 | Extinción por incumplimientos graves del empresario - demanda del trabajador | `extincion-incumplimientos-graves-empresario-demanda-lab-0462` |
| LAB-0463 | Extinción a instancia del trabajador por el art. 41.3 ET - demanda | `extincion-instancia-trabajador-art-41-3-et-demanda-lab-0463` |
| LAB-0464 | TRADE - demanda de extinción por incumplimiento de la empresa cliente | `trade-demanda-extincion-incumplimiento-empresa-cliente-lab-0464` |
| LAB-0465 | Extinción del contrato de artista por incumplimiento del empresario - demanda | `extincion-contrato-artista-incumplimiento-empresario-lab-0465` |
| LAB-0466 | Demanda por despido de un eventual por circunstancias de la producción, previa a la reforma de 2021 | `demanda-despido-eventual-circunstancias-produccion-lab-0466` |
| LAB-0470 | Demanda de despido del trabajador jubilado parcialmente que tenía un contrato a tiempo parcial | `demanda-despido-trabajador-jubilado-parcialmente-tenia-lab-0470` |
| LAB-0472 | Demanda de despido del representante de comercio con reclamación de la indemnización por clientela | `demanda-despido-representante-comercio-reclamacion-lab-0472` |
| LAB-0473 | Demanda de despido de un alto directivo | `demanda-despido-alto-directivo-lab-0473` |
| LAB-0474 | Demanda del socio cooperativista de trabajo asociado que impugna su expulsión | `demanda-socio-cooperativista-trabajo-asociado-impugna-lab-0474` |
| LAB-0475 | Demanda de despido de un trabajador cuyo contrato estaba suspendido | `demanda-despido-trabajador-cuyo-contrato-estaba-lab-0475` |
| LAB-0477 | Demanda por despido tácito derivado del cierre de la empresa | `demanda-despido-tacito-derivado-cierre-empresa-lab-0477` |
| LAB-0479 | Demanda principal de despido y subsidiaria de indemnización por extinción del contrato de TRADE | `demanda-principal-despido-subsidiaria-indemnizacion-lab-0479` |
| LAB-0480 | Demanda principal de indemnización por extinción del contrato de TRADE y subsidiaria de despido | `demanda-principal-indemnizacion-extincion-contrato-lab-0480` |
| LAB-0481 | Papeleta de conciliación previa por despido que pide su declaración de improcedencia | `papeleta-conciliacion-previa-despido-pide-declaracion-lab-0481` |
| LAB-0482 | Demanda del trabajador para extinguir el contrato por impago de salarios | `demanda-trabajador-extinguir-contrato-impago-salarios-lab-0482` |
| LAB-0483 | Solicitud de conciliación ante el SMAC de un trabajador extranjero por despido improcedente | `solicitud-conciliacion-ante-smac-trabajador-extranjero-lab-0483` |
| LAB-0484 | Demanda que acumula la acción de despido y la reclamación de la liquidación salarial | `demanda-acumula-accion-despido-reclamacion-liquidacion-lab-0484` |
| LAB-0486 | Carta del trabajador que denuncia su contrato temporal para extinguirlo a su vencimiento | `carta-trabajador-denuncia-contrato-temporal-lab-0486` |
| LAB-0489 | Carta de despido disciplinario a un trabajador no afiliado que reconoce la improcedencia | `carta-despido-disciplinario-trabajador-no-afiliado-lab-0489` |
| LAB-0490 | Carta de la empresa que denuncia el contrato temporal para extinguirlo a su vencimiento | `carta-empresa-denuncia-contrato-temporal-extinguirlo-lab-0490` |
| LAB-0491 | Carta de despido disciplinario a un trabajador no afiliado a ningún sindicato | `carta-despido-disciplinario-trabajador-no-afiliado-lab-0491` |
| LAB-0492 | Carta de despido objetivo por ineptitud sobrevenida al perder la titulación necesaria | `carta-despido-objetivo-ineptitud-sobrevenida-perder-lab-0492` |
| LAB-0493 | Carta de despido objetivo por insuficiencia de consignación presupuestaria | `carta-despido-objetivo-insuficiencia-consignacion-lab-0493` |
| LAB-0494 | Demanda de extinción del contrato por una modificación sustancial que menoscaba la dignidad | `demanda-extincion-contrato-modificacion-sustancial-lab-0494` |
| LAB-0495 | Demanda de extinción del contrato por impago de salarios acumulada a la reclamación de cantidad | `demanda-extincion-contrato-impago-salarios-acumulada-lab-0495` |
| LAB-0496 | Liquidación y finiquito del empleado del hogar familiar | `liquidacion-finiquito-empleado-hogar-familiar-lab-0496` |
| LAB-0497 | Demanda por despido al negar la empresa la reincorporación tras la excedencia por cuidado de hijo | `demanda-despido-negar-empresa-reincorporacion-tras-lab-0497` |
| LAB-0498 | Demanda contra el despido objetivo por ineptitud del trabajador | `demanda-contra-despido-objetivo-ineptitud-trabajador-lab-0498` |
| LAB-0499 | Demanda contra el despido objetivo por falta de adaptación a las modificaciones del puesto | `demanda-contra-despido-objetivo-falta-adaptacion-lab-0499` |
| LAB-0500 | Escrito de opción entre readmisión e indemnización tras declararse improcedente el despido | `escrito-opcion-entre-readmision-e-indemnizacion-tras-lab-0500` |
| LAB-0501 | Acuerdo de empresa y trabajador para extinguir el contrato de mutuo acuerdo | `acuerdo-empresa-trabajador-extinguir-contrato-mutuo-lab-0501` |
| LAB-0502 | Carta que extingue el contrato por incapacidad permanente o gran incapacidad del trabajador | `carta-extingue-contrato-incapacidad-permanente-gran-lab-0502` |
| LAB-0503 | Carta que resuelve el contrato por una causa válidamente pactada en él | `carta-resuelve-contrato-causa-validamente-pactada-lab-0503` |
| LAB-0505 | Escrito que pide extinguir el contrato por cierre de la empresa al ser imposible la readmisión | `escrito-pide-extinguir-contrato-cierre-empresa-ser-lab-0505` |
| LAB-0506 | Solicitud de ejecución de la sentencia de despido de un representante que opta por la readmisión | `solicitud-ejecucion-sentencia-despido-representante-lab-0506` |
| LAB-0507 | Comunicación del fin del contrato de duración determinada de una persona artista | `comunicacion-fin-contrato-duracion-determinada-persona-lab-0507` |
| LAB-0508 | Extinción del contrato de una persona empleada de hogar por no superar el periodo de prueba | `extincion-contrato-persona-empleada-hogar-no-superar-lab-0508` |
| LAB-0509 | Requerimiento al extrabajador para que devuelva los equipos y enseres de la empresa | `requerimiento-extrabajador-devuelva-equipos-enseres-lab-0509` |
| LAB-0510 | Comunicación de baja obligatoria del socio trabajador por perder los requisitos de admisión | `comunicacion-baja-obligatoria-socio-trabajador-perder-lab-0510` |
| LAB-0511 | Acuerdo que suspende cautelarmente los derechos del socio trabajador hasta que su baja sea ejecutiva | `acuerdo-suspende-cautelarmente-derechos-socio-lab-0511` |
| LAB-0512 | Acuerdo del consejo rector que califica como justificada la baja de un socio trabajador | `acuerdo-consejo-rector-califica-como-justificada-baja-lab-0512` |
| LAB-0513 | Petición de baja voluntaria del socio trabajador en la cooperativa | `peticion-baja-voluntaria-socio-trabajador-cooperativa-lab-0513` |
| LAB-0514 | Petición de baja justificada del socio trabajador disconforme con un acuerdo gravoso de la asamblea | `peticion-baja-justificada-socio-trabajador-disconforme-lab-0514` |
| LAB-0515 | Reclamación previa de la empresa al Estado por los salarios de tramitación abonados | `reclamacion-previa-empresa-estado-salarios-tramitacion-lab-0515` |
| LAB-0516 | Carta de la empresa que comunica al trabajador que opta por readmitirle | `carta-empresa-comunica-trabajador-opta-readmitirle-lab-0516` |
| LAB-0517 | Preaviso de la empresa de la finalización de un contrato de duración determinada | `preaviso-empresa-finalizacion-contrato-duracion-lab-0517` |
| LAB-0518 | Recibo de finiquito y liquidación de haberes al terminar la relación laboral | `recibo-finiquito-liquidacion-haberes-terminar-relacion-lab-0518` |
| LAB-0519 | Carta de la empresa que extingue el contrato durante el periodo de prueba | `carta-empresa-extingue-contrato-durante-periodo-prueba-lab-0519` |
| LAB-0520 | Carta del trabajador que extingue el contrato durante el periodo de prueba | `carta-trabajador-extingue-contrato-durante-periodo-lab-0520` |
| LAB-0521 | Carta de extinción del contrato por no alcanzar el rendimiento pactado | `carta-extincion-contrato-no-alcanzar-rendimiento-lab-0521` |
| LAB-0522 | Comunicación al trabajador de la fecha de reincorporación tras optar la empresa por readmitirle | `comunicacion-trabajador-fecha-reincorporacion-tras-lab-0522` |
| LAB-0523 | Carta de la empresa que denuncia el contrato temporal con quince días de preaviso | `carta-empresa-denuncia-contrato-temporal-quince-dias-lab-0523` |
| LAB-0524 | Carta de la empresa que denuncia el contrato temporal sin preaviso, indemnizando los días omitidos | `carta-empresa-denuncia-contrato-temporal-sin-preaviso-lab-0524` |
| LAB-0525 | Comunicación de la extinción del contrato por cumplirse la condición resolutoria | `comunicacion-extincion-contrato-cumplirse-condicion-lab-0525` |
| LAB-0526 | Comunicación a la empresa del cese del trabajador por jubilación, incapacidad o fallecimiento | `comunicacion-empresa-cese-trabajador-jubilacion-lab-0526` |
| LAB-0527 | Aviso al empresario de que se pedirá la resolución judicial del contrato por sus incumplimientos | `aviso-empresario-pedira-resolucion-judicial-contrato-lab-0527` |
| LAB-0528 | Audiencia previa al delegado sindical antes de despedir a un trabajador afiliado | `audiencia-previa-delegado-sindical-antes-despedir-lab-0528` |
| LAB-0529 | Carta de despido disciplinario a un representante legal de los trabajadores | `carta-despido-disciplinario-representante-legal-lab-0529` |

## Privacidad

Ver `PRIVACY.md`.
