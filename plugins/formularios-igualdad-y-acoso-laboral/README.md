# Igualdad, acoso y canal de denuncias en la empresa

> Plugin de Claude Code `formularios-igualdad-y-acoso-laboral` · **36 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la igualdad en la empresa: plan de igualdad y su comisión negociadora, diagnóstico y cuestionarios, registro retributivo, protocolos frente al acoso sexual, por razón de sexo y laboral, medidas LGTBI, canal de denuncias y sanción del acoso.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 36 está al final):

- **Demandas, peticiones y solicitudes iniciales** (1). Por ejemplo: Demanda del trabajador acosado en el trabajo para tutelar sus derechos fundamentales.
- **Contratos, pactos y cláusulas** (3). Por ejemplo: Protocolo contra el acoso y la violencia hacia personas LGTBI; Acuerdo con la representación de los trabajadores sobre medidas de igualdad LGTBI; Protocolo contra el acoso sexual y por razón de sexo en el trabajo.
- **Estatutos, actas, certificaciones y escrituras** (5). Por ejemplo: Acta de reunión de la Comisión de seguimiento del Plan de Igualdad; Acta de constitución de la Comisión de seguimiento del plan de igualdad o plan LGTBI; Acta de aprobación del protocolo contra el acoso sexual o por razón de sexo.
- **Comunicaciones, requerimientos y cartas** (4). Por ejemplo: Aviso a la plantilla de la implantación del canal de denuncias; Carta para constituir la comisión negociadora del plan de igualdad; Aviso a la plantilla del inicio del Plan de Igualdad.
- **Escritos de trámite y otros** (23). Por ejemplo: Evaluación para la comisión de seguimiento - cuestionario; Cuestionario de evaluación del plan dirigido a la plantilla; Cuestionario de evaluación dirigido a la dirección.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Acta de constitución de la comisión negociadora del plan de igualdad»
   - «Protocolo para prevenir y actuar frente al acoso sexual»
   - «Carta de sanción por acoso»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-igualdad-y-acoso-laboral:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-igualdad-y-acoso-laboral:evaluacion-comision-seguimiento-cuestionario-lab-0319`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 2.068 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-igualdad-y-acoso-laboral@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-igualdad-y-acoso-laboral@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-igualdad-y-acoso-laboral.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (36)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0319 | Evaluación para la comisión de seguimiento - cuestionario | `evaluacion-comision-seguimiento-cuestionario-lab-0319` |
| LAB-0320 | Cuestionario de evaluación del plan dirigido a la plantilla | `cuestionario-evaluacion-plan-dirigido-plantilla-lab-0320` |
| LAB-0321 | Cuestionario de evaluación dirigido a la dirección | `cuestionario-evaluacion-dirigido-direccion-lab-0321` |
| LAB-0322 | Impulso por la empresa de la negociación del plan de igualdad o del plan LGTBI | `impulso-empresa-negociacion-plan-igualdad-plan-lgtbi-lab-0322` |
| LAB-0323 | Aviso a la plantilla de la implantación del canal de denuncias | `aviso-plantilla-implantacion-canal-denuncias-lab-0323` |
| LAB-0324 | Protocolo contra el acoso y la violencia hacia personas LGTBI | `protocolo-contra-acoso-violencia-hacia-personas-lgtbi-lab-0324` |
| LAB-0325 | Acuerdo con la representación de los trabajadores sobre medidas de igualdad LGTBI | `acuerdo-representacion-trabajadores-sobre-medidas-lab-0325` |
| LAB-0326 | Reglamento de la Comisión de seguimiento y evaluación | `reglamento-comision-seguimiento-evaluacion-lab-0326` |
| LAB-0327 | Acta de reunión de la Comisión de seguimiento del Plan de Igualdad | `acta-reunion-comision-seguimiento-plan-igualdad-lab-0327` |
| LAB-0328 | Acta de constitución de la Comisión de seguimiento del plan de igualdad o plan LGTBI | `acta-constitucion-comision-seguimiento-plan-igualdad-lab-0328` |
| LAB-0329 | Acta de aprobación del protocolo contra el acoso sexual o por razón de sexo | `acta-aprobacion-protocolo-contra-acoso-sexual-razon-lab-0329` |
| LAB-0330 | Diagnóstico del Plan de Igualdad - acta de aprobación | `diagnostico-plan-igualdad-acta-aprobacion-lab-0330` |
| LAB-0331 | Carta para constituir la comisión negociadora del plan de igualdad | `carta-constituir-comision-negociadora-plan-igualdad-lab-0331` |
| LAB-0332 | Acoso laboral (mobbing) - demanda por infracción de la normativa de prevención | `acoso-laboral-mobbing-demanda-infraccion-normativa-lab-0332` |
| LAB-0333 | Acta de aprobación del plan de igualdad o del plan LGTBI | `acta-aprobacion-plan-igualdad-plan-lgtbi-lab-0333` |
| LAB-0334 | Autorizar los trámites de inscripción del plan de igualdad o del protocolo de acoso | `autorizar-tramites-inscripcion-plan-igualdad-protocolo-lab-0334` |
| LAB-0335 | Plan de igualdad - hoja estadística | `plan-igualdad-hoja-estadistica-lab-0335` |
| LAB-0336 | Impulso por la representación de los trabajadores de la negociación del plan de igualdad | `impulso-representacion-trabajadores-negociacion-plan-lab-0336` |
| LAB-0337 | Cuestionario de igualdad para la plantilla | `cuestionario-igualdad-plantilla-lab-0337` |
| LAB-0338 | Cuestionario de igualdad para la dirección | `cuestionario-igualdad-direccion-lab-0338` |
| LAB-0339 | Criterios de selección de la empresa usuaria - comunicación a la empresa externa | `criterios-seleccion-empresa-usuaria-comunicacion-lab-0339` |
| LAB-0340 | Compromisos de la organización en selección y promoción | `compromisos-organizacion-seleccion-promocion-lab-0340` |
| LAB-0341 | Comisión negociadora del plan de igualdad - acta de reunión | `comision-negociadora-plan-igualdad-acta-reunion-lab-0341` |
| LAB-0342 | Acta de constitución de la comisión negociadora del plan de igualdad o plan LGTBI | `acta-constitucion-comision-negociadora-plan-igualdad-lab-0342` |
| LAB-0343 | Reunión con perspectiva de igualdad - convocatoria | `reunion-perspectiva-igualdad-convocatoria-lab-0343` |
| LAB-0344 | Aviso a la plantilla del inicio del Plan de Igualdad | `aviso-plantilla-inicio-plan-igualdad-lab-0344` |
| LAB-0345 | Compromiso de la empresa con la igualdad - carta | `compromiso-empresa-igualdad-carta-lab-0345` |
| LAB-0346 | Compromiso de la organización contra el acoso sexual y por razón de sexo | `compromiso-organizacion-contra-acoso-sexual-razon-sexo-lab-0346` |
| LAB-0347 | Protocolo contra el acoso sexual y por razón de sexo en el trabajo | `protocolo-contra-acoso-sexual-razon-sexo-trabajo-lab-0347` |
| LAB-0348 | Denuncia de acoso sexual o por razón de sexo | `denuncia-acoso-sexual-razon-sexo-lab-0348` |
| LAB-0349 | Compromiso con el plan de igualdad en el convenio colectivo - cláusula | `compromiso-plan-igualdad-convenio-colectivo-clausula-lab-0349` |
| LAB-0350 | Confidencialidad en la tramitación de denuncias de acoso - compromiso | `confidencialidad-tramitacion-denuncias-acoso-compromiso-lab-0350` |
| LAB-0351 | Sanción por acoso - carta | `sancion-acoso-carta-lab-0351` |
| LAB-0352 | Cargos por acoso sexual - pliego | `cargos-acoso-sexual-pliego-lab-0352` |
| LAB-0353 | Demanda del trabajador acosado en el trabajo para tutelar sus derechos fundamentales | `demanda-trabajador-acosado-trabajo-tutelar-derechos-lab-0353` |
| LAB-0354 | Autorización del trabajador a la sección sindical para denunciar un posible acoso | `autorizacion-trabajador-seccion-sindical-denunciar-lab-0354` |

## Privacidad

Ver `PRIVACY.md`.
