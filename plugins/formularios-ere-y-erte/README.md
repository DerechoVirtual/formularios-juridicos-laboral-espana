# Despido colectivo y ERTE

> Plugin de Claude Code `formularios-ere-y-erte` · **86 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para los procedimientos colectivos: despido colectivo y ERTE por causas económicas, técnicas, organizativas o de producción y por fuerza mayor, comisión negociadora, periodo de consultas y actas, comunicaciones a la autoridad laboral, Mecanismo RED y demandas contra el despido colectivo.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 86 está al final):

- **Demandas, peticiones y solicitudes iniciales** (8). Por ejemplo: Demanda contra la denegación de ERTE por fuerza mayor temporal o Mecanismo RED; Demanda contra la extinción del contrato por causas ETOP sin seguir el procedimiento legal; Demanda individual por falta de causa en un despido colectivo no impugnado por los representantes.
- **Contratos, pactos y cláusulas** (3). Por ejemplo: Acuerdo con los representantes que cierra el periodo de consultas de un ERTE por causas ETOP; Acuerdo de la empresa y los representantes en el periodo de consultas del despido colectivo; Acuerdo que designa al socio trabajador de cooperativa que causa baja por causas ETOP o fuerza mayor.
- **Estatutos, actas, certificaciones y escrituras** (11). Por ejemplo: Acta de consultas del despido colectivo; Acta en que la plantilla sin representantes elige la comisión negociadora del despido colectivo; Acta del periodo de consultas de un ERTE de reducción de jornada o suspensión de contratos.
- **Comunicaciones, requerimientos y cartas** (21). Por ejemplo: Aviso de la empresa a los representantes legales de que va a iniciar un despido colectivo; Aviso de la empresa a los trabajadores sin representantes de que va a iniciar un despido colectivo; Comunicación de la empresa que abre el periodo de consultas del despido colectivo.
- **Escritos de trámite y otros** (43). Por ejemplo: Mecanismo RED - inicio del procedimiento comunicado a la representación de los trabajadores; Mecanismo RED - acta final del periodo de consultas; Mecanismo RED - decisión sin acuerdo comunicada a la autoridad laboral.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Comunicación a los representantes del inicio del periodo de consultas del ERTE»
   - «Acta final con acuerdo en el despido colectivo»
   - «Comunicación a la autoridad laboral de la decisión final del ERTE»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-ere-y-erte:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-ere-y-erte:mecanismo-red-inicio-procedimiento-comunicado-lab-0530`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 5.302 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-ere-y-erte@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-ere-y-erte@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-ere-y-erte.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (86)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0530 | Mecanismo RED - inicio del procedimiento comunicado a la representación de los trabajadores | `mecanismo-red-inicio-procedimiento-comunicado-lab-0530` |
| LAB-0531 | Mecanismo RED - acta final del periodo de consultas | `mecanismo-red-acta-final-periodo-consultas-lab-0531` |
| LAB-0532 | Mecanismo RED - decisión sin acuerdo comunicada a la autoridad laboral | `mecanismo-red-decision-sin-acuerdo-comunicada-lab-0532` |
| LAB-0533 | Mecanismo RED - acuerdo comunicado a la autoridad laboral | `mecanismo-red-acuerdo-comunicado-autoridad-laboral-lab-0533` |
| LAB-0534 | Mecanismo RED - acuerdo en el periodo de consultas con la representación de los trabajadores | `mecanismo-red-acuerdo-periodo-consultas-representacion-lab-0534` |
| LAB-0535 | Mecanismo RED - inicio del periodo de consultas comunicado a la autoridad laboral | `mecanismo-red-inicio-periodo-consultas-comunicado-lab-0535` |
| LAB-0536 | Mecanismo RED - apertura del periodo de consultas comunicada a la plantilla | `mecanismo-red-apertura-periodo-consultas-comunicada-lab-0536` |
| LAB-0537 | Mecanismo RED - acta de designación de la comisión ad hoc | `mecanismo-red-acta-designacion-comision-ad-hoc-lab-0537` |
| LAB-0538 | Mecanismo RED - designación de miembros de la comisión negociadora comunicada a la empresa | `mecanismo-red-designacion-miembros-comision-lab-0538` |
| LAB-0539 | Mecanismo RED - petición de la empresa para constituir la comisión negociadora | `mecanismo-red-peticion-empresa-constituir-comision-lab-0539` |
| LAB-0540 | Cierre de centro en un despido colectivo - aviso a la autoridad laboral | `cierre-centro-despido-colectivo-aviso-autoridad-laboral-lab-0540` |
| LAB-0541 | Demanda contra la denegación de ERTE por fuerza mayor temporal o Mecanismo RED | `demanda-contra-denegacion-erte-fuerza-mayor-temporal-lab-0541` |
| LAB-0542 | Prórroga de la suspensión o reducción de jornada por ETOP (ERTE) - aviso al trabajador | `prorroga-suspension-reduccion-jornada-etop-erte-aviso-lab-0542` |
| LAB-0543 | Despido colectivo - acta de constitución de la comisión negociadora | `despido-colectivo-acta-constitucion-comision-lab-0543` |
| LAB-0544 | Despido colectivo - miembros de la comisión negociadora comunicados a la empresa | `despido-colectivo-miembros-comision-negociadora-lab-0544` |
| LAB-0545 | Despido colectivo - carta a la plantilla para nombrar la comisión negociadora | `despido-colectivo-carta-plantilla-nombrar-comision-lab-0545` |
| LAB-0546 | ERTE por ETOP - acta de designación de la comisión ad hoc | `erte-etop-acta-designacion-comision-ad-hoc-lab-0546` |
| LAB-0547 | Fin del ERTE y reincorporación al trabajo - carta al trabajador | `fin-erte-reincorporacion-trabajo-carta-trabajador-lab-0547` |
| LAB-0548 | Fin de las medidas de ERTE - comunicación a la autoridad laboral | `fin-medidas-erte-comunicacion-autoridad-laboral-lab-0548` |
| LAB-0549 | Calendario del expediente de regulación de empleo | `calendario-expediente-regulacion-empleo-lab-0549` |
| LAB-0550 | Lista de trabajadores afectados por expedientes de regulación de empleo | `lista-trabajadores-afectados-expedientes-regulacion-lab-0550` |
| LAB-0551 | ERTE por fuerza mayor temporal - comunicación al trabajador | `erte-fuerza-mayor-temporal-comunicacion-trabajador-lab-0551` |
| LAB-0552 | ERTE suspensivo por fuerza mayor temporal - acta de reunión con la representación | `erte-suspensivo-fuerza-mayor-temporal-acta-reunion-lab-0552` |
| LAB-0553 | Despido colectivo por fuerza mayor sin resolución administrativa - demanda | `despido-colectivo-fuerza-mayor-sin-resolucion-lab-0553` |
| LAB-0554 | ERTE por ETOP - apertura del periodo de consultas comunicada a los trabajadores | `erte-etop-apertura-periodo-consultas-comunicada-lab-0554` |
| LAB-0555 | ERTE por ETOP - suspensión o reducción de jornada comunicada al trabajador | `erte-etop-suspension-reduccion-jornada-comunicada-lab-0555` |
| LAB-0556 | Despido colectivo en grupo mercantil sin cuentas consolidadas - nulidad por falta de documentación | `despido-colectivo-grupo-mercantil-sin-cuentas-lab-0556` |
| LAB-0557 | Despido colectivo - demanda de nulidad por falta de documentación | `despido-colectivo-demanda-nulidad-falta-documentacion-lab-0557` |
| LAB-0558 | Despido colectivo en grupo mercantil con cuentas consolidadas - nulidad por falta de documentación | `despido-colectivo-grupo-mercantil-cuentas-consolidadas-lab-0558` |
| LAB-0559 | Despido colectivo con acuerdo - demanda de sindicatos que no lo firmaron | `despido-colectivo-acuerdo-demanda-sindicatos-no-lo-lab-0559` |
| LAB-0560 | Despido colectivo en grupo laboral - nulidad por tramitarse solo en una empresa | `despido-colectivo-grupo-laboral-nulidad-tramitarse-lab-0560` |
| LAB-0561 | Acta de consultas del despido colectivo | `acta-consultas-despido-colectivo-lab-0561` |
| LAB-0562 | Memoria de ejemplo sobre causa productiva en un despido colectivo | `memoria-ejemplo-sobre-causa-productiva-despido-lab-0562` |
| LAB-0563 | Despido colectivo - inicio del periodo de consultas comunicado a la autoridad laboral | `despido-colectivo-inicio-periodo-consultas-comunicado-lab-0563` |
| LAB-0564 | Reducción de jornada o suspensión de contratos sin representantes - aviso a todos los trabajadores | `reduccion-jornada-suspension-contratos-sin-lab-0564` |
| LAB-0565 | Aviso de la empresa a los representantes legales de que va a iniciar un despido colectivo | `aviso-empresa-representantes-legales-va-iniciar-lab-0565` |
| LAB-0566 | Aviso de la empresa a los trabajadores sin representantes de que va a iniciar un despido colectivo | `aviso-empresa-trabajadores-sin-representantes-va-lab-0566` |
| LAB-0567 | Respuesta de los representantes legales sobre la comisión representativa en el despido colectivo | `respuesta-representantes-legales-sobre-comision-lab-0567` |
| LAB-0568 | Respuesta de los trabajadores sin representantes sobre la comisión negociadora del despido colectivo | `respuesta-trabajadores-sin-representantes-sobre-lab-0568` |
| LAB-0569 | Acta en que la plantilla sin representantes elige la comisión negociadora del despido colectivo | `acta-plantilla-sin-representantes-elige-comision-lab-0569` |
| LAB-0570 | Comunicación de la empresa que abre el periodo de consultas del despido colectivo | `comunicacion-empresa-abre-periodo-consultas-despido-lab-0570` |
| LAB-0571 | Petición de la empresa al comité de su informe sobre el despido colectivo | `peticion-empresa-comite-informe-sobre-despido-colectivo-lab-0571` |
| LAB-0572 | Acta del periodo de consultas de un ERTE de reducción de jornada o suspensión de contratos | `acta-periodo-consultas-erte-reduccion-jornada-lab-0572` |
| LAB-0573 | Comunicación electrónica al SEPE de los datos del ERTE una vez terminada su tramitación | `comunicacion-electronica-sepe-datos-erte-vez-terminada-lab-0573` |
| LAB-0574 | Aviso de la empresa a los representantes de que va a iniciar un ERTE de reducción o suspensión | `aviso-empresa-representantes-va-iniciar-erte-reduccion-lab-0574` |
| LAB-0575 | Aviso fehaciente a los trabajadores sin representantes de un ERTE por causas ETOP | `aviso-fehaciente-trabajadores-sin-representantes-erte-lab-0575` |
| LAB-0576 | Respuesta de los representantes legales sobre la comisión representativa en un ERTE | `respuesta-representantes-legales-sobre-comision-lab-0576` |
| LAB-0577 | Petición de la empresa al comité de su informe sobre el ERTE de reducción o suspensión | `peticion-empresa-comite-informe-sobre-erte-reduccion-lab-0577` |
| LAB-0578 | Calendario de reuniones del periodo de consultas de un ERTE de reducción o suspensión | `calendario-reuniones-periodo-consultas-erte-reduccion-lab-0578` |
| LAB-0579 | Escrito a la empresa con los miembros designados para la comisión negociadora del ERTE por ETOP | `escrito-empresa-miembros-designados-comision-lab-0579` |
| LAB-0580 | Petición de la empresa a la plantilla para que constituya la comisión negociadora del ERTE por ETOP | `peticion-empresa-plantilla-constituya-comision-lab-0580` |
| LAB-0581 | Demanda contra la extinción del contrato por causas ETOP sin seguir el procedimiento legal | `demanda-contra-extincion-contrato-causas-etop-sin-lab-0581` |
| LAB-0582 | Demanda individual por falta de causa en un despido colectivo no impugnado por los representantes | `demanda-individual-falta-causa-despido-colectivo-no-lab-0582` |
| LAB-0583 | Demanda individual contra un despido colectivo por no respetar la prioridad de permanencia | `demanda-individual-contra-despido-colectivo-no-lab-0583` |
| LAB-0584 | Acta de apertura del periodo de consultas en el despido colectivo | `acta-apertura-periodo-consultas-despido-colectivo-lab-0584` |
| LAB-0585 | Memoria explicativa del ERTE por causas económicas, técnicas, organizativas o de producción | `memoria-explicativa-erte-causas-economicas-tecnicas-lab-0585` |
| LAB-0586 | Acta del calendario de reuniones del periodo de consultas en el despido colectivo | `acta-calendario-reuniones-periodo-consultas-despido-lab-0586` |
| LAB-0587 | Comunicación a la autoridad laboral del inicio del periodo de consultas del despido colectivo | `comunicacion-autoridad-laboral-inicio-periodo-lab-0587` |
| LAB-0588 | Certificado de que la empresa no está obligada a auditar sus cuentas, para el periodo de consultas | `certificado-empresa-no-esta-obligada-auditar-cuentas-lab-0588` |
| LAB-0589 | Demanda de la empresa para que se declare ajustado a derecho su despido colectivo | `demanda-empresa-declare-ajustado-derecho-despido-lab-0589` |
| LAB-0590 | Demanda individual contra el despido producido en un despido colectivo por causas ETOP | `demanda-individual-contra-despido-producido-despido-lab-0590` |
| LAB-0591 | Memoria explicativa de la causa económica en el despido colectivo | `memoria-explicativa-causa-economica-despido-colectivo-lab-0591` |
| LAB-0592 | Comunicación a la autoridad laboral del inicio de consultas de un ERTE por causas ETOP | `comunicacion-autoridad-laboral-inicio-consultas-erte-lab-0592` |
| LAB-0593 | Comunicación a la autoridad laboral del fin de las consultas con acuerdo en un ERTE por causas ETOP | `comunicacion-autoridad-laboral-fin-consultas-acuerdo-lab-0593` |
| LAB-0594 | Acta final del periodo de consultas de un ERTE por causas ETOP | `acta-final-periodo-consultas-erte-causas-etop-lab-0594` |
| LAB-0595 | Demanda individual contra la suspensión o reducción de jornada de un ERTE por causas ETOP | `demanda-individual-contra-suspension-reduccion-jornada-lab-0595` |
| LAB-0596 | Comunicación a la autoridad laboral de la decisión final sin acuerdo en un ERTE por causas ETOP | `comunicacion-autoridad-laboral-decision-final-sin-lab-0596` |
| LAB-0597 | Solicitud a la autoridad laboral para que constate la fuerza mayor temporal en un ERTE | `solicitud-autoridad-laboral-constate-fuerza-mayor-lab-0597` |
| LAB-0598 | Comunicación a los representantes de la solicitud de ERTE por fuerza mayor temporal | `comunicacion-representantes-solicitud-erte-fuerza-lab-0598` |
| LAB-0599 | Acuerdo con los representantes que cierra el periodo de consultas de un ERTE por causas ETOP | `acuerdo-representantes-cierra-periodo-consultas-erte-lab-0599` |
| LAB-0600 | Solicitud de la empresa a la autoridad laboral para extinguir contratos por fuerza mayor | `solicitud-empresa-autoridad-laboral-extinguir-lab-0600` |
| LAB-0601 | Comunicación a los representantes de la solicitud de extinción de contratos por fuerza mayor | `comunicacion-representantes-solicitud-extincion-lab-0601` |
| LAB-0602 | Carta individual de despido a cada trabajador afectado por el despido colectivo | `carta-individual-despido-cada-trabajador-afectado-lab-0602` |
| LAB-0603 | Demanda de los representantes legales o sindicales que impugna el despido colectivo | `demanda-representantes-legales-sindicales-impugna-lab-0603` |
| LAB-0604 | Comunicación a los representantes de la decisión final y las condiciones del despido colectivo | `comunicacion-representantes-decision-final-condiciones-lab-0604` |
| LAB-0605 | Comunicación de la empresa a los representantes de la apertura de consultas del despido colectivo | `comunicacion-empresa-representantes-apertura-consultas-lab-0605` |
| LAB-0606 | Comunicación a la autoridad laboral del acuerdo alcanzado en las consultas del despido colectivo | `comunicacion-autoridad-laboral-acuerdo-alcanzado-lab-0606` |
| LAB-0607 | Acuerdo de la empresa y los representantes en el periodo de consultas del despido colectivo | `acuerdo-empresa-representantes-periodo-consultas-lab-0607` |
| LAB-0608 | Comunicación a la autoridad laboral de la decisión final y las condiciones del despido colectivo | `comunicacion-autoridad-laboral-decision-final-lab-0608` |
| LAB-0609 | Acta final sin acuerdo de las consultas de un ERTE de reducción de jornada o suspensión | `acta-final-sin-acuerdo-consultas-erte-reduccion-lab-0609` |
| LAB-0610 | Acta que cierra sin acuerdo el periodo de consultas del despido colectivo | `acta-cierra-sin-acuerdo-periodo-consultas-despido-lab-0610` |
| LAB-0611 | Acta que cierra con acuerdo el periodo de consultas del despido colectivo | `acta-cierra-acuerdo-periodo-consultas-despido-colectivo-lab-0611` |
| LAB-0612 | Acuerdo que designa al socio trabajador de cooperativa que causa baja por causas ETOP o fuerza mayor | `acuerdo-designa-socio-trabajador-cooperativa-causa-lab-0612` |
| LAB-0613 | Acta de reunión de consultas en un ERTE de suspensión de contratos o reducción de jornada | `acta-reunion-consultas-erte-suspension-contratos-lab-0613` |
| LAB-0614 | Comunicación de la empresa a la autoridad laboral de la apertura de consultas del despido colectivo | `comunicacion-empresa-autoridad-laboral-apertura-lab-0614` |
| LAB-0615 | Comunicación a la autoridad laboral del resultado de las consultas del despido colectivo | `comunicacion-autoridad-laboral-resultado-consultas-lab-0615` |

## Privacidad

Ver `PRIVACY.md`.
