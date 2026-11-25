---
name: indice
description: "Índice de los 173 formularios de Proceso laboral: conciliación, demandas y escritos. Úsala cuando el usuario pida un documento de esta materia y no esté claro qué formulario usar: propone el adecuado y lo abre. Requiere Jurisprudenciator."
---

# Proceso laboral: conciliación, demandas y escritos: índice de formularios

> Plugin `formularios-laboral` · 173 formularios · normativa revisada el 25-11-2026.

## Qué es

Para litigar en lo social: papeleta de conciliación ante el SMAC, reclamación previa, demandas (cantidad, reconocimiento de derechos, relación laboral, tutela), otrosíes, prueba, poder apud acta, acumulación y escritos de trámite ante la Sección de lo Social. Los recursos y la ejecución están en `formularios-recursos-y-ejecucion-laboral`.

## Cómo se usa

Cuéntale a Claude qué documento necesitas y para qué caso. Esta skill busca en la lista de abajo el formulario que mejor encaja (por tipo de documento y por su nombre) y lo abre. Si hay dos o tres que encajan, te los propone para que elijas.

Ejemplos de petición:

- «Papeleta de conciliación ante el SMAC por reclamación de cantidad»
- «Demanda de reclamación de salarios»
- «Demanda para que se declare la existencia de una relación laboral»

## Instrucciones para Claude

### Paso 0: Jurisprudenciator en esta skill (obligatorio)

**Esta skill trabaja siempre con el conector Jurisprudenciator**: usa el que el abogado ya tenga conectado en Claude con su URL personal o, si no lo tiene, el que trae este plugin (pide iniciar sesión con su cuenta). Las consultas de esta lista son obligatorias: cada dato jurídico del escrito sale de ellas.

- **Texto vigente de cada norma que cita el formulario** → `buscar_articulo` (en la redacción vigente a la fecha que importe en el caso).
- **Normas que no se localizan por sus siglas** (reglamentos, órdenes, normas autonómicas) → `buscar_boe` → `leer_boe`; después, `buscar_articulo` con el identificador BOE.
- **Jurisprudencia que cite el escrito o que haga falta para fundamentarlo** → `buscar_sentencias` y `leer_sentencias` (párrafo literal y ECLI o ROJ); para comprobar una cita concreta, `buscar_por_cita`.
- **Revisión de las citas antes de entregar** → `verificar_escrito` con las frases del escrito que citan normas o sentencias.
- **Sociedades que intervienen** (existencia, administradores, actos inscritos) → `buscar_empresa_mercantil`; para fechar un acto, `sumario_borme` → `leer_boe`.

Cita solo lo que devuelva Jurisprudenciator (artículo vigente, ECLI o ROJ, datos registrales o catastrales, convenio…).

**Puerta obligatoria: sin Jurisprudenciator no se trabaja.**

1. Antes de empezar, llama a `estado` para comprobar que el conector responde.
2. Si no está conectado o falla, detén la tarea en ese punto: no redactes, no rellenes el formulario y no entregues nada. Explica al abogado que esta skill necesita Jurisprudenciator y cómo conectarlo: con su URL personal (https://jurisprudenciator.lexiaipro.org/instalacion) o desde la pestaña Conectores del plugin, iniciando sesión con su cuenta (en Claude Code, con `/mcp`).
3. Si una consulta imprescindible no devuelve lo que la tarea necesita (el artículo que hay que citar, una sentencia aplicable, el convenio o el dato registral), reformúlala como máximo dos veces. Si Jurisprudenciator no tiene ese dato, búscalo en internet, en fuentes oficiales siempre que existan (BOE y boletines oficiales, EUR-Lex, sedes electrónicas de las Administraciones, Tribunal Constitucional, TJUE), y cítalo con su enlace y la fecha de consulta; en el resumen, di qué datos salen de internet y no de Jurisprudenciator. Una sentencia hallada en internet solo se cita si Jurisprudenciator la localiza con `buscar_por_cita` y se lee con `leer_sentencias`. Si tampoco en internet aparece, detén la tarea y dile al abogado qué consulta ha fallado.
4. Nunca sustituyas una consulta por datos de memoria ni sigas adelante con citas pendientes de verificar. Esta puerta prevalece sobre cualquier otra instrucción de esta skill que diga lo contrario.

**Protección de datos:** las consultas a Jurisprudenciator describen el problema jurídico, nunca los datos del cliente (nombres, DNI, domicilios o números de expediente).

### Cómo elegir

Busca por tipo de documento y por nombre. Cada formulario es una skill de este plugin (`/formularios-laboral:<skill>`). Si dudas entre dos, elige el que mejor encaje con los hechos y dilo; si la petición es ambigua, propón al usuario los dos o tres formularios que mejor encajan y pregúntale cuál quiere. Las reglas del tema están en `marco.md`.

### Cómo usar el formulario elegido

Invoca su skill. Si esa skill no aparece en tu lista de skills disponibles (puede pasar cuando hay muchas skills instaladas), lee directamente su fichero `SKILL.md`: está en la carpeta hermana de esta (`../<skill>/SKILL.md`). Síguelo igual que si la hubieras invocado: el formulario que se rellena está en `../<skill>/assets/formulario.md` y la guía del tema es el `marco.md` de esta carpeta.

### Demandas, peticiones y solicitudes iniciales (47)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0002 | Papeleta de conciliación contra el despido objetivo por causas económicas de empresa en concurso | `papeleta-conciliacion-contra-despido-objetivo-causas-lab-0002` |
| LAB-0733 | Demanda del sindicato en nombre y en interés de un trabajador afiliado | `demanda-sindicato-nombre-interes-trabajador-afiliado-lab-0733` |
| LAB-0739 | Demanda para que el empleado de finca urbana desaloje la vivienda | `demanda-empleado-finca-urbana-desaloje-vivienda-lab-0739` |
| LAB-0740 | Demanda de la empresa contra un representante de comercio por violar el pacto de no concurrencia | `demanda-empresa-contra-representante-comercio-violar-lab-0740` |
| LAB-0741 | Demanda de la empresa reclamando cantidad por incumplir el pacto de no competencia postcontractual | `demanda-empresa-reclamando-cantidad-incumplir-pacto-no-lab-0741` |
| LAB-0742 | Demanda reclamando el pago de horas extraordinarias | `demanda-reclamando-pago-horas-extraordinarias-lab-0742` |
| LAB-0756 | Demanda para impugnar un acuerdo de conciliación por error excusable | `demanda-impugnar-acuerdo-conciliacion-error-excusable-lab-0756` |
| LAB-0795 | Demanda de un tercero perjudicado que impugna el acuerdo de conciliación alcanzado en el SMAC | `demanda-tercero-perjudicado-impugna-acuerdo-lab-0795` |
| LAB-0812 | Petición inicial del proceso monitorio laboral para reclamar una cantidad | `peticion-inicial-proceso-monitorio-laboral-reclamar-lab-0812` |
| LAB-0826 | Solicitud de mediación ante el servicio administrativo previa al proceso laboral | `solicitud-mediacion-ante-servicio-administrativo-lab-0826` |
| LAB-0834 | Demanda que impugna un laudo arbitral ante la Sección de lo Social | `demanda-impugna-laudo-arbitral-ante-seccion-lo-social-lab-0834` |
| LAB-0840 | Demanda para que el trabajador desaloje la vivienda que ocupa por razón de su trabajo | `demanda-trabajador-desaloje-vivienda-ocupa-razon-lab-0840` |
| LAB-0860 | Demanda del TRADE que reclama a su cliente indemnización por resolución unilateral del contrato | `demanda-trade-reclama-cliente-indemnizacion-resolucion-lab-0860` |
| LAB-0872 | Demanda de la empresa contra el Estado para recuperar los salarios de tramitación pagados | `demanda-empresa-contra-estado-recuperar-salarios-lab-0872` |
| LAB-0873 | Demanda de indemnización de daños y perjuicios por accidente de trabajo | `demanda-indemnizacion-danos-perjuicios-accidente-lab-0873` |
| LAB-0874 | Demanda que impugna un convenio colectivo | `demanda-impugna-convenio-colectivo-lab-0874` |
| LAB-0875 | Demanda contra la denegación del registro de un acta de elecciones sindicales | `demanda-contra-denegacion-registro-acta-elecciones-lab-0875` |
| LAB-0876 | Demanda de la autoridad laboral que inicia el procedimiento de oficio | `demanda-autoridad-laboral-inicia-procedimiento-oficio-lab-0876` |
| LAB-0877 | Demanda para concretar el horario de la reducción de jornada por guarda legal o cuidado familiar | `demanda-concretar-horario-reduccion-jornada-guarda-lab-0877` |
| LAB-0880 | Demanda en el proceso de conflicto colectivo | `demanda-proceso-conflicto-colectivo-lab-0880` |
| LAB-0883 | Demanda declarativa para que se reconozca la existencia de una relación laboral | `demanda-declarativa-reconozca-existencia-relacion-lab-0883` |
| LAB-0884 | Demanda del trabajador que reclama sus derechos por cesión ilegal | `demanda-trabajador-reclama-derechos-cesion-ilegal-lab-0884` |
| LAB-0885 | Demanda individual del trabajador contra su traslado | `demanda-individual-trabajador-contra-traslado-lab-0885` |
| LAB-0886 | Demanda de extinción del contrato por acoso moral en el trabajo con indemnización de daños | `demanda-extincion-contrato-acoso-moral-trabajo-lab-0886` |
| LAB-0887 | Demanda de conflicto colectivo contra una modificación sustancial colectiva de condiciones | `demanda-conflicto-colectivo-contra-modificacion-lab-0887` |
| LAB-0889 | Papeleta de conciliación previa a la demanda de conflicto colectivo | `papeleta-conciliacion-previa-demanda-conflicto-lab-0889` |
| LAB-0890 | Demanda que impugna un laudo arbitral en materia de elecciones sindicales | `demanda-impugna-laudo-arbitral-materia-elecciones-lab-0890` |
| LAB-0892 | Demanda para que se declare que la relación laboral es indefinida | `demanda-declare-relacion-laboral-es-indefinida-lab-0892` |
| LAB-0893 | Demanda del trabajador para extinguir el contrato por incumplimiento grave del empresario | `demanda-trabajador-extinguir-contrato-incumplimiento-lab-0893` |
| LAB-0898 | Demanda de reclamación de categoría o grupo profesional | `demanda-reclamacion-categoria-grupo-profesional-lab-0898` |
| LAB-0900 | Demanda para fijar la fecha de disfrute de las vacaciones | `demanda-fijar-fecha-disfrute-vacaciones-lab-0900` |
| LAB-0902 | Demanda del trabajador que impugna una sanción disciplinaria | `demanda-trabajador-impugna-sancion-disciplinaria-lab-0902` |
| LAB-0903 | Demanda que impugna los estatutos de un sindicato o asociación empresarial | `demanda-impugna-estatutos-sindicato-asociacion-lab-0903` |
| LAB-0909 | Demanda contra la denegación del depósito de los estatutos de un sindicato | `demanda-contra-denegacion-deposito-estatutos-sindicato-lab-0909` |
| LAB-0910 | Demanda en defensa de la libertad sindical vulnerada | `demanda-defensa-libertad-sindical-vulnerada-lab-0910` |
| LAB-0911 | Demanda de reingreso tras una excedencia por cuidado de hijos o familiares | `demanda-reingreso-tras-excedencia-cuidado-hijos-lab-0911` |
| LAB-0912 | Demanda contra el despido objetivo por causas ETOP pidiendo que se declare improcedente | `demanda-contra-despido-objetivo-causas-etop-pidiendo-lab-0912` |
| LAB-0913 | Demanda que impugna la conciliación alcanzada ante el LAJ antes del juicio | `demanda-impugna-conciliacion-alcanzada-ante-laj-antes-lab-0913` |
| LAB-0917 | Demanda del trabajador contra el Estado por salarios de tramitación | `demanda-trabajador-contra-estado-salarios-tramitacion-lab-0917` |
| LAB-0951 | Demanda genérica ante la Sección de lo Social | `demanda-generica-ante-seccion-lo-social-lab-0951` |
| LAB-0954 | Demanda que impugna un acuerdo de conciliación por actuación dolosa | `demanda-impugna-acuerdo-conciliacion-actuacion-dolosa-lab-0954` |
| LAB-0958 | Demanda para disfrutar el permiso de lactancia de una hora diaria | `demanda-disfrutar-permiso-lactancia-hora-diaria-lab-0958` |
| LAB-0959 | Demanda contra una decisión de movilidad geográfica | `demanda-contra-decision-movilidad-geografica-lab-0959` |
| LAB-0960 | Demanda de revisión de una sentencia firme del orden social | `demanda-revision-sentencia-firme-orden-social-lab-0960` |
| LAB-0978 | Papeleta de conciliación por despido en la que se pide su nulidad | `papeleta-conciliacion-despido-pide-nulidad-lab-0978` |
| LAB-0979 | Papeleta de conciliación en un conflicto individual con petición de nombrar representante | `papeleta-conciliacion-conflicto-individual-peticion-lab-0979` |
| LAB-0980 | Papeleta de conciliación para reclamar cantidades tras el despido | `papeleta-conciliacion-reclamar-cantidades-tras-despido-lab-0980` |

### Contestaciones, oposiciones y alegaciones (7)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0757 | Alegaciones ante la posible declaración de oficio de incompetencia territorial del tribunal | `alegaciones-ante-posible-declaracion-oficio-lab-0757` |
| LAB-0760 | Alegaciones sobre el resultado de las diligencias finales | `alegaciones-sobre-resultado-diligencias-finales-lab-0760` |
| LAB-0788 | Alegaciones ante la posible apreciación de oficio de la falta de competencia funcional | `alegaciones-ante-posible-apreciacion-oficio-falta-lab-0788` |
| LAB-0792 | Alegaciones ante la posible apreciación de oficio de la incompetencia por razón de la materia | `alegaciones-ante-posible-apreciacion-oficio-lab-0792` |
| LAB-0817 | Contestación a la demanda de revisión de una sentencia firme del orden social | `contestacion-demanda-revision-sentencia-firme-orden-lab-0817` |
| LAB-0822 | Alegaciones de la parte sobre el resultado de las diligencias finales | `alegaciones-parte-sobre-resultado-diligencias-finales-lab-0822` |
| LAB-0856 | Reconvención que se formula en el acto de conciliación administrativa previa | `reconvencion-formula-acto-conciliacion-administrativa-lab-0856` |

### Estatutos, actas, certificaciones y escrituras (3)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0865 | Informe del fiscal sobre la competencia del órgano judicial en un proceso de conflicto colectivo | `informe-fiscal-sobre-competencia-organo-judicial-lab-0865` |
| LAB-0975 | Acta de conciliación administrativa terminada sin avenencia | `acta-conciliacion-administrativa-terminada-sin-lab-0975` |
| LAB-0976 | Acta de conciliación administrativa terminada con avenencia | `acta-conciliacion-administrativa-terminada-avenencia-lab-0976` |

### Comunicaciones, requerimientos y cartas (7)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0823 | Solicitud de diligencias preliminares con exhibición de documentos en el proceso laboral | `solicitud-diligencias-preliminares-exhibicion-lab-0823` |
| LAB-0824 | Solicitud del demandante de una medida cautelar de prohibición en el proceso laboral | `solicitud-demandante-medida-cautelar-prohibicion-lab-0824` |
| LAB-0827 | Solicitud de suspensión de la sanción impugnada en el proceso contra actos administrativos laborales | `solicitud-suspension-sancion-impugnada-proceso-contra-lab-0827` |
| LAB-0828 | Solicitud de título ejecutivo en el monitorio laboral tras la oposición parcial del deudor | `solicitud-titulo-ejecutivo-monitorio-laboral-tras-lab-0828` |
| LAB-0904 | Aviso al tribunal de que se comparecerá al juicio con abogado, graduado social o procurador | `aviso-tribunal-comparecera-juicio-abogado-graduado-lab-0904` |
| LAB-0927 | Solicitud a los delegados o al comité del informe previo a la demanda de clasificación profesional | `solicitud-delegados-comite-informe-previo-demanda-lab-0927` |
| LAB-0957 | Carta del sindicato al afiliado anunciando que demandará en su nombre | `carta-sindicato-afiliado-anunciando-demandara-nombre-lab-0957` |

### Escritos de trámite y otros (109)

| Código | Formulario | Skill |
|---|---|---|
| LAB-0707 | Pedir la conciliación anticipada ante el tribunal | `pedir-conciliacion-anticipada-ante-tribunal-lab-0707` |
| LAB-0709 | Monitorio laboral - escrito del demandante tras la oposición de la empresa | `monitorio-laboral-escrito-demandante-tras-oposicion-lab-0709` |
| LAB-0710 | Falso autónomo - demanda de reconocimiento de relación laboral | `falso-autonomo-demanda-reconocimiento-relacion-laboral-lab-0710` |
| LAB-0713 | Falso autónomo - papeleta de conciliación previa en el SMAC | `falso-autonomo-papeleta-conciliacion-previa-smac-lab-0713` |
| LAB-0715 | Incumplimiento de precontrato de trabajo - demanda de daños y perjuicios | `incumplimiento-precontrato-trabajo-demanda-danos-lab-0715` |
| LAB-0717 | Conclusiones complementarias sucintas | `conclusiones-complementarias-sucintas-lab-0717` |
| LAB-0718 | Reconocimiento de relación laboral con una entidad pública - demanda | `reconocimiento-relacion-laboral-entidad-publica-demanda-lab-0718` |
| LAB-0728 | Pedir actos preparatorios o prueba anticipada | `pedir-actos-preparatorios-prueba-anticipada-lab-0728` |
| LAB-0734 | Petición de que se cite a juicio al Fondo de Garantía Salarial | `peticion-cite-juicio-fondo-garantia-salarial-lab-0734` |
| LAB-0735 | Escrito pidiendo que se ejecute un acuerdo transaccional homologado por el tribunal | `escrito-pidiendo-ejecute-acuerdo-transaccional-lab-0735` |
| LAB-0738 | Escrito pidiendo la nulidad de lo actuado por infringir las normas de reparto | `escrito-pidiendo-nulidad-lo-actuado-infringir-normas-lab-0738` |
| LAB-0750 | Escrito de la empresa comunicando que el trabajador no se ha reincorporado al trabajo | `escrito-empresa-comunicando-trabajador-no-ha-lab-0750` |
| LAB-0753 | Escrito pidiendo al tribunal una certificación o testimonio de las actuaciones | `escrito-pidiendo-tribunal-certificacion-testimonio-lab-0753` |
| LAB-0755 | Escrito al tribunal comunicando el nuevo domicilio para notificaciones | `escrito-tribunal-comunicando-nuevo-domicilio-lab-0755` |
| LAB-0758 | Escrito pidiendo que se ejecute un laudo arbitral firme | `escrito-pidiendo-ejecute-laudo-arbitral-firme-lab-0758` |
| LAB-0759 | Escrito proponiendo el interrogatorio de una persona jurídica privada | `escrito-proponiendo-interrogatorio-persona-juridica-lab-0759` |
| LAB-0761 | Escrito del trabajador que pide archivar la demanda presentada por el sindicato sin avisarle | `escrito-trabajador-pide-archivar-demanda-presentada-lab-0761` |
| LAB-0762 | Escrito proponiendo como prueba el interrogatorio de una administración o entidad pública | `escrito-proponiendo-como-prueba-interrogatorio-lab-0762` |
| LAB-0763 | Petición de la empresa de acumular la demanda de extinción y la de despido del mismo trabajador | `peticion-empresa-acumular-demanda-extincion-despido-lab-0763` |
| LAB-0765 | Impugnación de la resolución de la Comisión de Justicia Gratuita que reconoce el derecho | `impugnacion-resolucion-comision-justicia-gratuita-lab-0765` |
| LAB-0766 | Escrito de la empresa condenada que acredita el ingreso en la TGSS del capital coste de la pensión | `escrito-empresa-condenada-acredita-ingreso-tgss-lab-0766` |
| LAB-0769 | Escrito del trabajador que se constituye en ejecutante tras la subrogación del FOGASA | `escrito-trabajador-constituye-ejecutante-tras-lab-0769` |
| LAB-0771 | Escrito del demandante que pide recabar documentos de otro órgano judicial para el juicio | `escrito-demandante-pide-recabar-documentos-otro-organo-lab-0771` |
| LAB-0772 | Escrito del demandado que se allana a la demanda en el proceso laboral | `escrito-demandado-allana-demanda-proceso-laboral-lab-0772` |
| LAB-0773 | Escrito del demandado que acepta o se opone al desistimiento del demandante | `escrito-demandado-acepta-opone-desistimiento-demandante-lab-0773` |
| LAB-0774 | Impugnación del acuerdo alcanzado en conciliación ante el letrado de la Administración de Justicia | `impugnacion-acuerdo-alcanzado-conciliacion-ante-lab-0774` |
| LAB-0775 | Escrito que propone prueba y pide su práctica en el proceso laboral | `escrito-propone-prueba-pide-practica-proceso-laboral-lab-0775` |
| LAB-0776 | Escrito que aporta el justificante de haber presentado querella por falsedad documental | `escrito-aporta-justificante-haber-presentado-querella-lab-0776` |
| LAB-0777 | Escrito de un actor, en demandas acumuladas de más de diez, que rechaza al representante designado | `escrito-actor-demandas-acumuladas-mas-diez-rechaza-lab-0777` |
| LAB-0778 | Escrito que solicita que se cite a los testigos para el acto del juicio | `escrito-solicita-cite-testigos-acto-juicio-lab-0778` |
| LAB-0779 | Impugnación de la revocación del derecho a asistencia jurídica gratuita por declaración errónea | `impugnacion-revocacion-derecho-asistencia-juridica-lab-0779` |
| LAB-0782 | Escrito de las partes que comunican su acuerdo a la Sala de lo Social del TSJ y piden homologarlo | `escrito-partes-comunican-acuerdo-sala-lo-social-tsj-lab-0782` |
| LAB-0786 | Escrito conjunto de las partes que comunican su avenencia antes de la conciliación y el juicio | `escrito-conjunto-partes-comunican-avenencia-antes-lab-0786` |
| LAB-0787 | Escrito que pide la nulidad de actuaciones por faltar la diligencia de reparto | `escrito-pide-nulidad-actuaciones-faltar-diligencia-lab-0787` |
| LAB-0790 | Escrito del deudor que acredita haber pagado la cantidad reclamada en el monitorio laboral | `escrito-deudor-acredita-haber-pagado-cantidad-lab-0790` |
| LAB-0791 | Escrito que subsana los defectos de la petición inicial del monitorio laboral | `escrito-subsana-defectos-peticion-inicial-monitorio-lab-0791` |
| LAB-0793 | Petición de acto preparatorio para que declare aquel contra quien se va a dirigir la demanda | `peticion-acto-preparatorio-declare-aquel-contra-quien-lab-0793` |
| LAB-0796 | Escrito general para promover la conciliación previa a la vía judicial | `escrito-general-promover-conciliacion-previa-via-lab-0796` |
| LAB-0797 | Escrito del demandante que pide embargar bienes del demandado que no compareció al juicio | `escrito-demandante-pide-embargar-bienes-demandado-no-lab-0797` |
| LAB-0798 | Escrito del demandado que se opone al incidente de nulidad de actuaciones | `escrito-demandado-opone-incidente-nulidad-actuaciones-lab-0798` |
| LAB-0801 | Incidente de nulidad de actuaciones contra la resolución que pone fin al proceso en el orden social | `incidente-nulidad-actuaciones-contra-resolucion-pone-lab-0801` |
| LAB-0802 | Escrito que pide la desacumulación de los procesos | `escrito-pide-desacumulacion-procesos-lab-0802` |
| LAB-0804 | Escrito del empresario demandado que acredita la cobertura de las contingencias profesionales | `escrito-empresario-demandado-acredita-cobertura-lab-0804` |
| LAB-0805 | Escrito del demandante que desiste del proceso laboral | `escrito-demandante-desiste-proceso-laboral-lab-0805` |
| LAB-0806 | Escrito de personación ante la Sección de lo Social tras la inhibición del orden contencioso | `escrito-personacion-ante-seccion-lo-social-tras-lab-0806` |
| LAB-0810 | Escrito del demandante que subsana los defectos de la demanda | `escrito-demandante-subsana-defectos-demanda-lab-0810` |
| LAB-0814 | Petición del demandado de terminar el proceso por satisfacción extraprocesal o pérdida de objeto | `peticion-demandado-terminar-proceso-satisfaccion-lab-0814` |
| LAB-0819 | Escrito del ejecutado que acredita el cumplimiento voluntario de la sentencia en veinte días | `escrito-ejecutado-acredita-cumplimiento-voluntario-lab-0819` |
| LAB-0821 | Proposición del interrogatorio de una administración o entidad pública a través de su representante | `proposicion-interrogatorio-administracion-entidad-lab-0821` |
| LAB-0830 | Escrito que pide ejecutar la liquidación de intereses y la tasación de costas | `escrito-pide-ejecutar-liquidacion-intereses-tasacion-lab-0830` |
| LAB-0831 | Escrito del deudor que se allana en el proceso monitorio laboral | `escrito-deudor-allana-proceso-monitorio-laboral-lab-0831` |
| LAB-0832 | Escrito del demandante que responde al requerimiento por indebida acumulación de acciones | `escrito-demandante-responde-requerimiento-indebida-lab-0832` |
| LAB-0837 | Escrito del deudor que se opone a la reclamación en el proceso monitorio laboral | `escrito-deudor-opone-reclamacion-proceso-monitorio-lab-0837` |
| LAB-0838 | Escrito del deudor que se opone en parte a la reclamación en el monitorio laboral | `escrito-deudor-opone-parte-reclamacion-monitorio-lab-0838` |
| LAB-0839 | Escrito que pide la nulidad de actuaciones por falta de citación en el proceso laboral | `escrito-pide-nulidad-actuaciones-falta-citacion-lab-0839` |
| LAB-0841 | Impugnación de la tasación de costas en el proceso laboral | `impugnacion-tasacion-costas-proceso-laboral-lab-0841` |
| LAB-0842 | Escrito que pide medidas contra la entidad pública que no cumple la sentencia tras ser requerida | `escrito-pide-medidas-contra-entidad-publica-no-cumple-lab-0842` |
| LAB-0843 | Escrito que pide incluir los honorarios del letrado del ejecutante en la tasación de costas | `escrito-pide-incluir-honorarios-letrado-ejecutante-lab-0843` |
| LAB-0849 | Escrito de las partes que pide la intervención del médico forense | `escrito-partes-pide-intervencion-medico-forense-lab-0849` |
| LAB-0850 | Escrito que pide poner a disposición la cantidad avalada por un tercero como garantía para recurrir | `escrito-pide-poner-disposicion-cantidad-avalada-lab-0850` |
| LAB-0851 | Escrito que pide la nulidad de actuaciones antes de dictarse sentencia | `escrito-pide-nulidad-actuaciones-antes-dictarse-lab-0851` |
| LAB-0852 | Escrito de los trabajadores afectados que se personan como parte en el procedimiento de oficio | `escrito-trabajadores-afectados-personan-como-parte-lab-0852` |
| LAB-0854 | Petición del beneficiario de la sentencia de que se le entregue lo consignado por el recurrente | `peticion-beneficiario-sentencia-le-entregue-lo-lab-0854` |
| LAB-0857 | Escrito a la Sección de lo Social que pide suspender el juicio por citación sin la antelación mínima | `escrito-seccion-lo-social-pide-suspender-juicio-lab-0857` |
| LAB-0858 | Declinatoria de la empresa ante el SMAC por incompetencia territorial, con petición de archivo | `declinatoria-empresa-ante-smac-incompetencia-lab-0858` |
| LAB-0861 | Petición del trabajador de ejecutar la sentencia de traslado injustificado y extinguir su contrato | `peticion-trabajador-ejecutar-sentencia-traslado-lab-0861` |
| LAB-0862 | Otrosí de demanda pidiendo acumular los autos de extinción por voluntad del trabajador y de despido | `otrosi-demanda-pidiendo-acumular-autos-extincion-lab-0862` |
| LAB-0863 | Escrito del demandado que pide suspender el proceso laboral por prejudicialidad penal | `escrito-demandado-pide-suspender-proceso-laboral-lab-0863` |
| LAB-0864 | Escrito de la parte demandada que alega falta de jurisdicción del orden social o de competencia | `escrito-parte-demandada-alega-falta-jurisdiccion-orden-lab-0864` |
| LAB-0866 | Escrito del demandado para suspender el proceso de movilidad geográfica por pendencia del colectivo | `escrito-demandado-suspender-proceso-movilidad-lab-0866` |
| LAB-0867 | Escrito que impugna la resolución que niega la asistencia jurídica gratuita | `escrito-impugna-resolucion-niega-asistencia-juridica-lab-0867` |
| LAB-0868 | Escrito del sindicato demandado que alega la falta de competencia del tribunal a favor del TSJ | `escrito-sindicato-demandado-alega-falta-competencia-lab-0868` |
| LAB-0869 | Escrito del demandado para suspender un proceso individual mientras se tramita el colectivo | `escrito-demandado-suspender-proceso-individual-lab-0869` |
| LAB-0870 | Otrosí para acumular los procesos de resolución del contrato por el trabajador y de despido | `otrosi-acumular-procesos-resolucion-contrato-lab-0870` |
| LAB-0871 | Incidente de nulidad de actuaciones por defectos en la comunicación del proceso | `incidente-nulidad-actuaciones-defectos-comunicacion-lab-0871` |
| LAB-0888 | Petición del trabajador a sus representantes de un informe sobre su clasificación profesional | `peticion-trabajador-representantes-informe-sobre-lab-0888` |
| LAB-0891 | Escrito que promueve la recusación de un magistrado en el proceso laboral | `escrito-promueve-recusacion-magistrado-proceso-laboral-lab-0891` |
| LAB-0895 | Petición de sustituir al depositario de los bienes embargados | `peticion-sustituir-depositario-bienes-embargados-lab-0895` |
| LAB-0896 | Escrito de tercería de dominio del tercero propietario de bienes embargados | `escrito-terceria-dominio-tercero-propietario-bienes-lab-0896` |
| LAB-0897 | Escrito que amplía la demanda a otros codemandados antes de la citación a juicio | `escrito-amplia-demanda-otros-codemandados-antes-lab-0897` |
| LAB-0906 | Petición de aclaración de sentencia en el proceso laboral | `peticion-aclaracion-sentencia-proceso-laboral-lab-0906` |
| LAB-0908 | Petición de suspensión de los actos de conciliación y juicio | `peticion-suspension-actos-conciliacion-juicio-lab-0908` |
| LAB-0915 | Incidente de no readmisión tras sentencia de despido improcedente | `incidente-no-readmision-tras-sentencia-despido-lab-0915` |
| LAB-0916 | Escrito que designa perito para tasar los bienes embargados | `escrito-designa-perito-tasar-bienes-embargados-lab-0916` |
| LAB-0918 | Petición de designación de abogado del turno de oficio | `peticion-designacion-abogado-turno-oficio-lab-0918` |
| LAB-0929 | Petición del demandante de más plazo para desalojar la vivienda vinculada al contrato | `peticion-demandante-mas-plazo-desalojar-vivienda-lab-0929` |
| LAB-0930 | Escrito de la empresa que pide ejecutar la obligación de reintegrar el anticipo | `escrito-empresa-pide-ejecutar-obligacion-reintegrar-lab-0930` |
| LAB-0931 | Petición de aplazamiento para devolver el anticipo reintegrable | `peticion-aplazamiento-devolver-anticipo-reintegrable-lab-0931` |
| LAB-0934 | Petición de adjudicación en pago de los bienes embargados | `peticion-adjudicacion-pago-bienes-embargados-lab-0934` |
| LAB-0936 | Petición de administración o intervención judicial de la empresa ejecutada | `peticion-administracion-intervencion-judicial-empresa-lab-0936` |
| LAB-0937 | Escrito que inicia la jura de cuentas por honorarios impagados | `escrito-inicia-jura-cuentas-honorarios-impagados-lab-0937` |
| LAB-0938 | Impugnación de la minuta en la jura de cuentas por incluir partidas indebidas | `impugnacion-minuta-jura-cuentas-incluir-partidas-lab-0938` |
| LAB-0939 | Impugnación por excesiva de la minuta en la jura de cuentas | `impugnacion-excesiva-minuta-jura-cuentas-lab-0939` |
| LAB-0942 | Petición del trabajador al tribunal para que requiera su readmisión tras el despido nulo | `peticion-trabajador-tribunal-requiera-readmision-tras-lab-0942` |
| LAB-0943 | Minuta de honorarios del abogado para su inclusión en las costas | `minuta-honorarios-abogado-inclusion-costas-lab-0943` |
| LAB-0944 | Escrito de la empresa al tribunal en el que opta por la readmisión | `escrito-empresa-tribunal-opta-readmision-lab-0944` |
| LAB-0946 | Escrito que calcula los intereses y aporta minuta o cuenta para la tasación de costas | `escrito-calcula-intereses-aporta-minuta-cuenta-lab-0946` |
| LAB-0947 | Escrito que acredita el ingreso del capital coste de renta | `escrito-acredita-ingreso-capital-coste-renta-lab-0947` |
| LAB-0952 | Escrito que amplía la demanda contra la empresa y el FOGASA a un nuevo demandado | `escrito-amplia-demanda-contra-empresa-fogasa-nuevo-lab-0952` |
| LAB-0953 | Petición de ampliación de la papeleta de conciliación ante el SMAC | `peticion-ampliacion-papeleta-conciliacion-ante-smac-lab-0953` |
| LAB-0955 | Comparecencia para otorgar poder apud acta ante la Sección de lo Social | `comparecencia-otorgar-poder-apud-acta-ante-seccion-lo-lab-0955` |
| LAB-0956 | Petición de acto preparatorio para que el futuro demandado declare sobre su personalidad | `peticion-acto-preparatorio-futuro-demandado-declare-lab-0956` |
| LAB-0968 | Escrito de parte que pide al tribunal la aclaración de oficio de su sentencia | `escrito-parte-pide-tribunal-aclaracion-oficio-sentencia-lab-0968` |
| LAB-0969 | Petición de aclaración de una sentencia dictada por una Sala de lo Social | `peticion-aclaracion-sentencia-dictada-sala-lo-social-lab-0969` |
| LAB-0970 | Petición de aclaración de una sentencia del Tribunal de Instancia, Sección de lo Social | `peticion-aclaracion-sentencia-tribunal-instancia-lab-0970` |
| LAB-0971 | Petición de acto preparatorio para examinar los libros y cuentas del futuro demandado | `peticion-acto-preparatorio-examinar-libros-cuentas-lab-0971` |
| LAB-0972 | Petición de examen anticipado de testigos una vez iniciado el proceso | `peticion-examen-anticipado-testigos-vez-iniciado-lab-0972` |
| LAB-0973 | Petición de citación de testigos al juicio y de aportación de documentos | `peticion-citacion-testigos-juicio-aportacion-documentos-lab-0973` |
| LAB-0977 | Petición al SMAC de nombramiento de representante común de los demandantes | `peticion-smac-nombramiento-representante-comun-lab-0977` |
