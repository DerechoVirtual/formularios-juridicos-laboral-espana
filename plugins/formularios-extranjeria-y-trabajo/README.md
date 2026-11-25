# Extranjería y movilidad internacional de trabajadores

> Plugin de Claude Code `formularios-extranjeria-y-trabajo` · **43 formularios** · Laboral · normativa revisada el 25-11-2026 · requiere Jurisprudenciator

## Para qué sirve

Para la extranjería laboral: autorizaciones de residencia y trabajo, arraigo, residencia de larga duración, visados y movilidad internacional (Ley 14/2013), desplazamiento de trabajadores, TIE, recursos y contencioso en materia de extranjería, expulsión y medidas cautelares.

Cada formulario es una skill: Claude lo rellena contigo paso a paso y te entrega el documento en Word, con las normas comprobadas en el BOE. Cada skill explica en su `SKILL.md` qué es el formulario, para qué sirve, cómo se usa, qué datos necesita y qué avisos normativos lleva; el formulario seco, listo para rellenar, está en `assets/formulario.md` dentro de la carpeta de la skill.

## Qué puedes hacer con él

Estos son los tipos de documento que trae, con algunos ejemplos (la lista completa de los 43 está al final):

- **Demandas, peticiones y solicitudes iniciales** (5). Por ejemplo: Recurso contencioso-administrativo contra la denegación del visado de reagrupación familiar; Solicitud de ejecución forzosa de sentencia firme en un procedimiento abreviado de extranjería; Solicitud de ejecución forzosa de la sentencia que reconoce la renovación de residencia y trabajo.
- **Contestaciones, oposiciones y alegaciones** (1). Por ejemplo: Alegaciones contra el acta de infracción a un extranjero por trabajar por cuenta propia en España.
- **Recursos** (2). Por ejemplo: Recurso de reposición para que se reconozca por silencio positivo la residencia de larga duración; Recurso de reposición contra la sanción a un extranjero por trabajar por cuenta propia en España.
- **Contratos, pactos y cláusulas** (1). Por ejemplo: Acuerdo entre la empresa y un alto directivo para su desplazamiento al extranjero.
- **Estatutos, actas, certificaciones y escrituras** (1). Por ejemplo: Acta notarial de manifestaciones de los cónyuges para el visado de reagrupación familiar.
- **Comunicaciones, requerimientos y cartas** (12). Por ejemplo: Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013; Solicitud de medida cautelar en el recurso contencioso sobre reagrupación familiar; Carta poder para gestiones consulares de reagrupación familiar y autorización de salida del menor.
- **Escritos de trámite y otros** (21). Por ejemplo: Memoria de actividad de la empresa y perfil del puesto para desplazar y contratar extranjeros; Silencio positivo en la modificación de autorización - certificado; Silencio positivo en la residencia de larga duración - certificado.

## Cómo se usa

1. **Pídelo con tus palabras.** Cuéntale a Claude qué documento necesitas y para qué caso; él elige el formulario. Por ejemplo:
   - «Solicitud de autorización de residencia y trabajo por arraigo»
   - «Recurso de reposición por silencio positivo en la residencia de larga duración»
   - «Solicitud de suspensión cautelar de una expulsión»
2. **Si no da con el formulario**, empieza por el índice del plugin: escribe `/formularios-extranjeria-y-trabajo:indice` y cuéntale lo que necesitas. Te propondrá el formulario que mejor encaja (o dos o tres para que elijas).
3. **Si ya sabes cuál quieres**, llámalo por su nombre de skill, por ejemplo `/formularios-extranjeria-y-trabajo:memoria-actividad-empresa-perfil-puesto-desplazar-lab-0981`. Los nombres están en la lista de formularios de abajo.

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
- **Espacio que ocupa:** unos 2.688 tokens en cada conversación mientras esté activado, porque Claude lleva en memoria la descripción de cada skill. Activa solo los plugins que vayas a usar; los demás puedes desactivarlos sin desinstalarlos (`claude plugin disable formularios-extranjeria-y-trabajo@formularios-juridicos-laboral-espana`).

## Instalación

En Claude Code, añade el catálogo (solo la primera vez) e instala el plugin:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-extranjeria-y-trabajo@formularios-juridicos-laboral-espana
```

En Claude (web, escritorio o Cowork): **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o sube el ZIP del plugin ([descargar ZIP](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-extranjeria-y-trabajo.zip)).

Para comprobar que está instalado: `claude plugin list`.

## Lista completa de formularios (43)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0981 | Memoria de actividad de la empresa y perfil del puesto para desplazar y contratar extranjeros | `memoria-actividad-empresa-perfil-puesto-desplazar-lab-0981` |
| LAB-0982 | Silencio positivo en la modificación de autorización - certificado | `silencio-positivo-modificacion-autorizacion-certificado-lab-0982` |
| LAB-0983 | Silencio positivo en la residencia de larga duración - certificado | `silencio-positivo-residencia-larga-duracion-certificado-lab-0983` |
| LAB-0985 | Revocar la resolución de expulsión - solicitud | `revocar-resolucion-expulsion-solicitud-lab-0985` |
| LAB-0986 | Designar representante para tramitar visados | `designar-representante-tramitar-visados-lab-0986` |
| LAB-0987 | Solicitud de movilidad internacional para el familiar del titular, Ley 14 de 2013 | `solicitud-movilidad-internacional-familiar-titular-ley-lab-0987` |
| LAB-0988 | Recurso contencioso-administrativo contra la denegación del visado de reagrupación familiar | `recurso-contencioso-administrativo-contra-denegacion-lab-0988` |
| LAB-0989 | Acuerdo entre la empresa y un alto directivo para su desplazamiento al extranjero | `acuerdo-entre-empresa-alto-directivo-desplazamiento-lab-0989` |
| LAB-0991 | Escrito de alegaciones del extranjero frente a la propuesta de expulsión por estancia irregular | `escrito-alegaciones-extranjero-frente-propuesta-lab-0991` |
| LAB-0992 | Solicitud de medida cautelar en el recurso contencioso sobre reagrupación familiar | `solicitud-medida-cautelar-recurso-contencioso-sobre-lab-0992` |
| LAB-0993 | Solicitud de ejecución forzosa de sentencia firme en un procedimiento abreviado de extranjería | `solicitud-ejecucion-forzosa-sentencia-firme-lab-0993` |
| LAB-0994 | Solicitud de ejecución forzosa de la sentencia que reconoce la renovación de residencia y trabajo | `solicitud-ejecucion-forzosa-sentencia-reconoce-lab-0994` |
| LAB-0995 | Carta poder para gestiones consulares de reagrupación familiar y autorización de salida del menor | `carta-poder-gestiones-consulares-reagrupacion-familiar-lab-0995` |
| LAB-0996 | Solicitud de residencia y trabajo por arraigo con limitación sectorial y geográfica | `solicitud-residencia-trabajo-arraigo-limitacion-lab-0996` |
| LAB-0997 | Recurso de reposición para que se reconozca por silencio positivo la residencia de larga duración | `recurso-reposicion-reconozca-silencio-positivo-lab-0997` |
| LAB-0998 | Solicitud para que se certifique la concesión por silencio de la residencia de larga duración | `solicitud-certifique-concesion-silencio-residencia-lab-0998` |
| LAB-0999 | Recurso contencioso contra la denegación consular del visado de residencia | `recurso-contencioso-contra-denegacion-consular-visado-lab-0999` |
| LAB-1000 | Demanda contencioso-administrativa por la denegación de un visado exento de autorización de trabajo | `demanda-contencioso-administrativa-denegacion-visado-lab-1000` |
| LAB-1001 | Solicitud de autorización de trabajo para extranjeros penados en tercer grado o libertad condicional | `solicitud-autorizacion-trabajo-extranjeros-penados-lab-1001` |
| LAB-1002 | Escrito de desistimiento de la solicitud de residencia y trabajo por cuenta ajena | `escrito-desistimiento-solicitud-residencia-trabajo-lab-1002` |
| LAB-1003 | Acta notarial de manifestaciones de los cónyuges para el visado de reagrupación familiar | `acta-notarial-manifestaciones-conyuges-visado-lab-1003` |
| LAB-1004 | Cuestionario de denuncia ante el Relator Especial de la ONU sobre derechos de los migrantes | `cuestionario-denuncia-ante-relator-especial-onu-sobre-lab-1004` |
| LAB-1005 | Comunicación individual de denuncia ante el Comité de Derechos Humanos de la ONU | `comunicacion-individual-denuncia-ante-comite-derechos-lab-1005` |
| LAB-1006 | Escrito a la Comisaría que revoca el poder otorgado en un expediente de extranjería | `escrito-comisaria-revoca-poder-otorgado-expediente-lab-1006` |
| LAB-1008 | Solicitud de residencia por razones humanitarias en el expediente de asilo | `solicitud-residencia-razones-humanitarias-expediente-lab-1008` |
| LAB-1009 | Solicitud de revocación de la orden de expulsión por arraigo | `solicitud-revocacion-orden-expulsion-arraigo-lab-1009` |
| LAB-1010 | Memoria de la empresa para la residencia y trabajo en el marco de prestaciones transnacionales | `memoria-empresa-residencia-trabajo-marco-prestaciones-lab-1010` |
| LAB-1011 | Memoria del puesto que ocupará el trabajador extranjero | `memoria-puesto-ocupara-trabajador-extranjero-lab-1011` |
| LAB-1012 | Solicitud de suspensión cautelar de la expulsión de un extranjero en centro de internamiento | `solicitud-suspension-cautelar-expulsion-extranjero-lab-1012` |
| LAB-1013 | Solicitud urgente al juzgado de guardia de medida cautelar contra la denegación de entrada | `solicitud-urgente-juzgado-guardia-medida-cautelar-lab-1013` |
| LAB-1014 | Autorización del titular de la vivienda para la reagrupación familiar | `autorizacion-titular-vivienda-reagrupacion-familiar-lab-1014` |
| LAB-1015 | Escrito que amplía las alegaciones en el expediente de expulsión | `escrito-amplia-alegaciones-expediente-expulsion-lab-1015` |
| LAB-1016 | Escrito del extranjero que apodera a su letrado para recurrir en vía administrativa | `escrito-extranjero-apodera-letrado-recurrir-via-lab-1016` |
| LAB-1017 | Escrito que reclama la asistencia sanitaria gratuita de un menor extranjero | `escrito-reclama-asistencia-sanitaria-gratuita-menor-lab-1017` |
| LAB-1018 | Escrito que reclama la asistencia sanitaria gratuita de una extranjera en el embarazo y el parto | `escrito-reclama-asistencia-sanitaria-gratuita-lab-1018` |
| LAB-1019 | Solicitud de reexamen de la inadmisión a trámite de la protección internacional en frontera | `solicitud-reexamen-inadmision-tramite-proteccion-lab-1019` |
| LAB-1020 | Petición de un documento que acredite que la autorización de trabajo sigue vigente | `peticion-documento-acredite-autorizacion-trabajo-sigue-lab-1020` |
| LAB-1022 | Impreso EX11 para pedir la residencia de larga duración o de larga duración UE | `impreso-ex11-pedir-residencia-larga-duracion-larga-lab-1022` |
| LAB-1023 | Impresos oficiales para iniciar procedimientos de documentación de extranjeros en España | `impresos-oficiales-iniciar-procedimientos-lab-1023` |
| LAB-1024 | Impreso EX13 para pedir la autorización de regreso a España | `impreso-ex13-pedir-autorizacion-regreso-espana-lab-1024` |
| LAB-1025 | Impreso EX17 para pedir la Tarjeta de Identidad de Extranjero | `impreso-ex17-pedir-tarjeta-identidad-extranjero-lab-1025` |
| LAB-1026 | Recurso de reposición contra la sanción a un extranjero por trabajar por cuenta propia en España | `recurso-reposicion-contra-sancion-extranjero-trabajar-lab-1026` |
| LAB-1027 | Alegaciones contra el acta de infracción a un extranjero por trabajar por cuenta propia en España | `alegaciones-contra-acta-infraccion-extranjero-trabajar-lab-1027` |

## Privacidad

Ver `PRIVACY.md`.
