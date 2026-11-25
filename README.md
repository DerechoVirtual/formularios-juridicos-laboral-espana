# Formularios jurídicos de España para Claude · Laboral

15 plugins de formularios de Laboral, uno por materia. Cada formulario es una skill que Claude rellena paso a paso con los datos del caso y entrega en Word tal cual es el formulario (Times New Roman 11, interlineado 1,15 y texto justificado): 1019 skills en total, contando la skill `indice` de cada plugin, que sirve para encontrar el formulario adecuado.

Todas las skills trabajan con **Jurisprudenciator** (https://jurisprudenciator.lexiaipro.org): antes de redactar comprueban que el conector responde y verifican en fuentes oficiales las normas que cita el formulario. Sin Jurisprudenciator conectado, las skills no redactan. Normativa revisada el 25-11-2026.

Las demás jurisdicciones están en repositorios propios: [Mercantil](https://github.com/DerechoVirtual/formularios-juridicos-mercantil-espana), [Civil](https://github.com/DerechoVirtual/formularios-juridicos-civil-espana), [Seguridad Social](https://github.com/DerechoVirtual/formularios-juridicos-seguridad-social-espana), [Administrativo y Tributario](https://github.com/DerechoVirtual/formularios-juridicos-administrativo-tributario-espana), [Penal](https://github.com/DerechoVirtual/formularios-juridicos-penal-espana).

## Instalación

En Claude Code:

```
/plugin marketplace add DerechoVirtual/formularios-juridicos-laboral-espana
/plugin install formularios-contratos-de-trabajo@formularios-juridicos-laboral-espana
```

Cada plugin ocupa contexto en la conversación, así que conviene instalar solo los de las materias con las que se trabaja.

En Claude (web, escritorio y Cowork) se puede añadir este repositorio desde **Personalizar → Plugins → Añadir marketplace** con la dirección `https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana`, o subir cada plugin como ZIP. Los ZIP están en la página de [versiones](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest).

## Plugins

| Plugin | Contenido | Skills | ZIP |
|---|---|---:|---|
| `formularios-contratos-de-trabajo` | Contratos de trabajo y contratación laboral | 137 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-contratos-de-trabajo.zip) |
| `formularios-salario-y-condiciones-de-trabajo` | Salario, movilidad y condiciones de trabajo | 90 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-salario-y-condiciones-de-trabajo.zip) |
| `formularios-jornada-vacaciones-y-permisos` | Jornada, vacaciones, permisos y conciliación | 88 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-jornada-vacaciones-y-permisos.zip) |
| `formularios-igualdad-y-acoso-laboral` | Igualdad, acoso y canal de denuncias en la empresa | 37 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-igualdad-y-acoso-laboral.zip) |
| `formularios-datos-y-control-del-trabajador` | Protección de datos y control empresarial | 12 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-datos-y-control-del-trabajador.zip) |
| `formularios-prevencion-de-riesgos-laborales` | Prevención de riesgos laborales | 8 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-prevencion-de-riesgos-laborales.zip) |
| `formularios-comite-sindicatos-y-convenios` | Representantes de los trabajadores, sindicatos y convenios | 15 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-comite-sindicatos-y-convenios.zip) |
| `formularios-faltas-y-sanciones-laborales` | Faltas y sanciones laborales | 43 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-faltas-y-sanciones-laborales.zip) |
| `formularios-despidos` | Despido y extinción del contrato de trabajo | 90 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-despidos.zip) |
| `formularios-ere-y-erte` | Despido colectivo y ERTE | 87 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-ere-y-erte.zip) |
| `formularios-seguridad-social-en-la-empresa` | Seguridad Social en la empresa, incapacidad y accidentes de trabajo | 28 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-seguridad-social-en-la-empresa.zip) |
| `formularios-inspeccion-de-trabajo` | Inspección de Trabajo y sanciones administrativas | 63 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-inspeccion-de-trabajo.zip) |
| `formularios-recursos-y-ejecucion-laboral` | Recursos, ejecución y resoluciones en el proceso laboral | 103 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-recursos-y-ejecucion-laboral.zip) |
| `formularios-laboral` | Proceso laboral: conciliación, demandas y escritos | 174 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-laboral.zip) |
| `formularios-extranjeria-y-trabajo` | Extranjería y movilidad internacional de trabajadores | 44 | [descargar](https://github.com/DerechoVirtual/formularios-juridicos-laboral-espana/releases/latest/download/formularios-extranjeria-y-trabajo.zip) |

## Estructura

```
.claude-plugin/marketplace.json  catálogo del marketplace
plugins/<plugin>/                .claude-plugin/plugin.json, .mcp.json, skills/<skill>/SKILL.md y assets/formulario.md, README.md, PRIVACY.md, LICENSE
```

## Aviso

Los documentos que se generan son borradores que debe revisar un abogado; no constituyen asesoramiento jurídico. Las skills no guardan datos del cliente y las consultas a Jurisprudenciator describen el problema jurídico, no los datos personales.

Soporte: https://jurisprudenciator.lexiaipro.org/incidencias · Licencia: ver [LICENSE](LICENSE).
