# 🇨🇴 OSINT Colombia

> **Recursos, fuentes y técnicas de inteligencia de fuentes abiertas aplicados al contexto colombiano.**  
> Enfoque ético para analistas de inteligencia, investigadores y periodistas.

---

## ⚠️ Aviso ético y legal

Este repositorio recopila **exclusivamente fuentes públicas y oficiales** del Estado colombiano y otros recursos de acceso abierto. Su propósito es académico, investigativo y de formación.

- El uso de estas fuentes sobre **funcionarios públicos en ejercicio** es legítimo dentro del marco del derecho al acceso a la información (Ley 1712 de 2014).
- Consultar estas fuentes sobre **ciudadanos privados sin propósito investigativo justificado** puede constituir una violación al habeas data (Ley 1581 de 2012).
- **La pregunta de inteligencia debe escribirse antes de iniciar cualquier búsqueda.** La recolección sin propósito definido no es inteligencia — es vigilancia.

---

## 📋 Tabla de contenidos

- [Cédula de ciudadanía](#-cédula-de-ciudadanía)
- [Registros judiciales y disciplinarios](#-registros-judiciales-y-disciplinarios)
- [Empresas y actividad económica](#-empresas-y-actividad-económica)
- [Salud y seguridad social](#-salud-y-seguridad-social)
- [Tránsito y transporte](#-tránsito-y-transporte)
- [Contratación pública](#-contratación-pública)
- [Transparencia y datos abiertos](#-transparencia-y-datos-abiertos)
- [Seguridad pública y conflicto](#-seguridad-pública-y-conflicto)
- [Registros electorales y políticos](#-registros-electorales-y-políticos)
- [Territorio y geografía](#-territorio-y-geografía)
- [Personas desaparecidas y fallecidas](#-personas-desaparecidas-y-fallecidas)
- [Sanciones internacionales](#-sanciones-internacionales)
- [Google Dorks para Colombia](#-google-dorks-para-colombia)
- [Herramientas OSINT aplicables](#-herramientas-osint-aplicables)
- [Casos prácticos documentados](#-casos-prácticos-documentados)
- [Recursos y referencias](#-recursos-y-referencias)

---

## 🪪 Cédula de ciudadanía

La cédula colombiana es el identificador central del ciudadano. Con el número de cédula es posible acceder a una superficie de información pública significativa a través de fuentes oficiales.

> 📌 **Superficie de exposición de una cédula colombiana** — ver diagrama en > 🚧 *Diagrama de fuentes por número de cédula — en construcción*


### Fuentes directas por número de cédula

| Fuente | Entidad | Qué entrega | Requisitos | URL |
|--------|---------|-------------|------------|-----|
| Estado de la cédula | Registraduría Nacional | Vigencia del documento, nombre, lugar de expedición | Nº cédula + fecha de expedición + captcha | https://certvigenciacedula.registraduria.gov.co/Datos.aspx |
| Lugar de votación | Registraduría Nacional | Municipio y puesto de votación | Por verificar | https://wsp.registraduria.gov.co/censo/consultar/ |
| Registro civil | Registraduría Nacional | Certificados de registro civil, nombre, apellido, oficina de registro, Nuip/Nip/Tarjeta de Identidad | Por verificar | https://consultasrc.registraduria.gov.co:28080/ProyectoSCCRC/ |
| Antecedentes judiciales | Policía Nacional | Récord judicial | Por verificar | https://antecedentes.policia.gov.co:7005/WebJudicial/ |
| Documentos recuperados | Policía Nacional | Documentos en custodia de la Policía | Por verificar | https://www.policia.gov.co/documentos-recuperados |
| Antecedentes disciplinarios | Procuraduría General | Sanciones disciplinarias | Por verificar | https://www.procuraduria.gov.co/Pages/Consulta-de-Antecedentes.aspx |
| Antecedentes fiscales | Contraloría General | Responsabilidades fiscales | Por verificar | https://www.contraloria.gov.co/control-fiscal/responsabilidad-fiscal/control-fiscal/responsabilidad-fiscal/certificado-de-antecedentes-fiscales/persona-natural |
| Sistema penal (SPOA) | Fiscalía General | Indagaciones e investigaciones | Por verificar | https://www.fiscalia.gov.co/colombia/servicios-de-informacion-al-ciudadano/consultas/ |
| Situación militar | Ejército Nacional | Estado de la libreta militar | Por verificar | https://www.libretamilitar.mil.co/modules/consult/militarysituation |
| Libreta militar (certificado) | Ejército Nacional | Certificado de la tarjeta militar | Por verificar | https://www.libretamilitar.mil.co/Modules/Consult/MilitaryCardCertificate |
| RUNT — Persona | Ministerio de Transporte | Licencias de conducción y trámites | Por verificar | https://www.runt.com.co/consultaCiudadana/#/consultaPersona |
| SISBEN | DNP | Grupo y puntaje de clasificación social | Por verificar | https://www.sisben.gov.co/Paginas/consulta-tu-grupo.aspx |
| EPS y afiliación en salud | ADRES | EPS a la que está afiliado | Por verificar | https://www.adres.gov.co/BDUA/Consulta-Afiliados-BDUA |
| RUAF — Seguridad social | SISPRO | Afiliaciones al sistema de seguridad social | Por verificar | https://ruaf.sispro.gov.co/TerminosCondiciones.aspx |
| SIMIT — Comparendos | FGCF | Multas e infracciones de tránsito | Por verificar | https://consulta.simit.org.co/Simit/indexA.jsp |
| SIGEP | DAFP | Hoja de vida de servidores públicos | Por verificar | https://www.sigep.gov.co/ |
| Colpensiones | Colpensiones | Certificado de afiliación / no pensión | Por verificar | https://www.colpensiones.gov.co |
| Verifíquese (app) | Privado | Consulta cruzada multi-fuente | App móvil | https://play.google.com/store/apps/details?id=se.verifique.app.cedula |

### Lo que revela cada fuente — análisis para el analista

| Dato | Valor para la inteligencia |
|------|--------------------------|
| **Vigencia cédula** | Confirma identidad activa. Una cédula cancelada puede indicar fallecimiento, suplantación o fraude. |
| **Lugar de votación** | Revela municipio de residencia real o de origen. Dato usado en campañas de geolocalización. |
| **SISBEN** | Indica nivel socioeconómico. Inconsistencia entre SISBEN y actividad económica visible = señal de alerta. |
| **RUNT** | Vehículos registrados, licencias vigentes, historial de trámites. |
| **Antecedentes** | Registro de condenas, medidas de aseguramiento, sanciones. |
| **SIGEP** | Para funcionarios: cargo, entidad, declaración de bienes y actividades. |
| **EPS** | Confirma lugar de residencia (régimen subsidiado = municipio de inscripción). |
| **SIMIT** | Comparendos por ciudad = patrón de movilidad de la persona. |
| **Situación militar** | Municipio de reclutamiento = municipio de origen. |

---

## ⚖️ Registros judiciales y disciplinarios

| Fuente | Entidad | URL |
|--------|---------|-----|
| Consulta de procesos (nacional unificada) | Rama Judicial | https://consultaprocesos.ramajudicial.gov.co/Procesos/Index |
| Procesos por ciudad — Bogotá | Rama Judicial | https://procesos.ramajudicial.gov.co/jepms/bogotajepms/conectar.asp |
| Procesos por ciudad — Medellín | Rama Judicial | https://procesos.ramajudicial.gov.co/jepms/medellinjepms/conectar.asp |
| Procesos por ciudad — Cali | Rama Judicial | https://procesos.ramajudicial.gov.co/jepms/calijepms/conectar.asp |
| Procesos por ciudad — Barranquilla | Rama Judicial | https://procesos.ramajudicial.gov.co/jepms/barranquillajepms/conectar.asp |
| Antecedentes disciplinarios abogados | Rama Judicial | https://antecedentesdisciplinarios.ramajudicial.gov.co/ |
| Vigencia de tarjeta profesional (abogados) | SIRNA | https://sirna.ramajudicial.gov.co/Paginas/Certificado.aspx |
| Sanciones a abogados | SIRNA | https://sirna.ramajudicial.gov.co/Paginas/Sanciones.aspx |
| Postulados Ley de Justicia y Paz | Fiscalía | https://www.fiscalia.gov.co/colombia/justicia-transicional-2/consulta-postulados/ |
| SPOA — denuncias Ley 906 | Fiscalía | https://www.fiscalia.gov.co/colombia/servicios-de-informacion-al-ciudadano/consultas/denuncias-ley-906-de-2004/ |
| Deudores morosos del Estado (BDME) | Contaduría General | https://eris.contaduria.gov.co/BDME/ |
| Antecedentes fiscales persona jurídica | Contraloría | https://www.contraloria.gov.co/control-fiscal/responsabilidad-fiscal/certificado-de-antecedentes-fiscales/certificado-de-antecedentes-fiscales/certificado-de-antecedentes-fiscales/persona-juridica |
| Privados de la libertad | INPEC | https://www.inpec.gov.co/registro-de-la-poblacion-privada-de-la-libertad |

---

## 🏢 Empresas y actividad económica

| Fuente | Entidad | Qué entrega | URL |
|--------|---------|-------------|-----|
| RUES | Cámaras de Comercio | Registro mercantil, proponentes, turismo — incluye cédula del representante legal | http://www.rues.org.co/ |
| Supersociedades | Supersociedades | Estados financieros, procesos ley 1116, bienes en venta | https://servicios.supersociedades.gov.co/barandaVirtual/#!/app/dashboard |
| Superfinanciera | SFC | Expedientes de entidades vigiladas | https://www.superfinanciera.gov.co/jsp/loader.jsf?lServicio=Publicaciones&lTipo=publicaciones&lFuncion=loadContenidoPublicacion&id=10083571 |
| DIAN — NIT | DIAN | Inconsistencias y estado del NIT | https://muisca.dian.gov.co/WebGestionmasiva/DefSelPublicacionesExterna.faces |
| SIC — Propiedad industrial | SIC | Patentes, marcas, diseños industriales | http://sipi.sic.gov.co/sipi/Extra/Default.aspx?sid=637483925925626831 |
| Supervigilancia — sanciones | Supervigilancia | Sanciones a empresas de vigilancia | https://www.supervigilancia.gov.co/documentos/buscar/?q=sanciones&genPagCat=1&genPag=1 |
| SuperSolidaria | SuperSolidaria | Cooperativas, entidades en liquidación | http://www.supersolidaria.gov.co/es/content/ventanilla |

---

## 🏥 Salud y seguridad social

| Fuente | Entidad | URL |
|--------|---------|-----|
| BDUA — afiliados | ADRES | https://www.adres.gov.co/BDUA/Consulta-Afiliados-BDUA |
| Verificación EPS Bogotá | Secretaría de Salud Capital | https://appb.saludcapital.gov.co/Comprobadordederechos/Consulta |
| Informes institucionales | Supersalud | https://www.supersalud.gov.co/es-co/nuestra-entidad/control/informes-institucionales |
| RUAF | SISPRO | https://ruaf.sispro.gov.co/TerminosCondiciones.aspx |
| Certificados SENA | SENA | https://certificados.sena.edu.co/CertificadoDigital/com.sena.consultacer |

---

## 🚗 Tránsito y transporte

| Fuente | Entidad | Qué entrega | URL |
|--------|---------|-------------|-----|
| RUNT — Persona | MinTransporte | Licencias, trámites por cédula | https://www.runt.com.co/consultaCiudadana/#/consultaPersona |
| RUNT — Vehículo | MinTransporte | Información del vehículo por placa | https://www.runt.com.co/consultaCiudadana/#/consultaVehiculo |
| SIMIT | FGCF | Multas e infracciones de tránsito | https://consulta.simit.org.co/Simit/indexA.jsp |
| DIMAR — Naves | DIMAR | Registro de embarcaciones marítimas | http://app.dimar.mil.co/zonadescarga/Formularios/frmConsultaRegistro.aspx |

---

## 📄 Contratación pública

| Fuente | Entidad | Qué entrega | URL |
|--------|---------|-------------|-----|
| SECOP I | Colombia Compra Eficiente | Contratos publicados hasta 2015 | https://www.contratos.gov.co/consultas/inicioConsulta.do |
| SECOP II | Colombia Compra Eficiente | Contratos y procesos desde 2015 | https://www.colombiacompra.gov.co/secop/secop-ii |
| RUP — Registro Único de Proponentes | RUES | Empresas habilitadas para contratar con el Estado | http://www.rues.org.co/ |

> 💡 **Nota para analistas:** El cruce entre RUES (representante legal por cédula) y SECOP (contratos adjudicados) es una de las técnicas más poderosas para detectar conflictos de interés y corrupción en contratación.

---

## 🌐 Transparencia y datos abiertos

| Fuente | Entidad | URL |
|--------|---------|-----|
| Portal de Datos Abiertos | Gobierno de Colombia | https://www.datos.gov.co/ |
| Portal de Transparencia | Función Pública | https://www.funcionpublica.gov.co/eva/es/transparencia |
| Monitor Ciudadano — Corrupción | Privado | https://www.monitorciudadano.co/hechos-corrupcion/visor |
| CHIP — Información fiscal territorial | Contaduría | https://www.chip.gov.co/ |
| Mapa Regalías | SGR | https://maparegalias.sgr.gov.co/ |
| SIGEP — Servidores públicos | DAFP | https://www.sigep.gov.co/ |

---

## 🔫 Seguridad pública y conflicto

| Fuente | Entidad | URL |
|--------|---------|-----|
| INPEC — Privados de la libertad | INPEC | https://www.inpec.gov.co/registro-de-la-poblacion-privada-de-la-libertad |
| Grupos armados — mapa ARCGIS | Terceros | https://www.arcgis.com/home/item.html?id=6930c4dbbffd4541a7c7a385fb4c75a3 |
| Mapa zonas de conflicto | Verdad Abierta | https://verdadabierta.carto.com/viz/e61e2a0a-e63a-11e5-8e65-0ecd1babdde5/public_map |
| ODC — Observatorio de Drogas | Min Justicia | https://www.minjusticia.gov.co/programas-co/ODC |
| ARN — Reintegración | ARN | https://www.reintegracion.gov.co/ |
| Víctimas del conflicto | UARIV | https://www.unidadvictimas.gov.co/ |
| SIEDCO — Criminalidad | Policía Nacional | https://www.policia.gov.co/estadistica-delictiva |

---

## 🗳️ Registros electorales y políticos

| Fuente | Entidad | URL |
|--------|---------|-----|
| Puesto de votación | Registraduría | https://wsp.registraduria.gov.co/censo/consultar/ |
| Candidatos y financiación | CNE | https://www.cne.gov.co/ |
| Declaraciones de bienes (SIGEP) | DAFP | https://www.sigep.gov.co/ |
| Votaciones congresistas | Senado / Cámara | https://www.senado.gov.co / https://www.camara.gov.co |
| Curul Visible | Privado | https://www.curulvisible.com/ |

---

## 🗺️ Territorio y geografía

| Fuente | Entidad | URL |
|--------|---------|-----|
| IGAC — Cartografía oficial | IGAC | https://www.igac.gov.co/ |
| DANE — Estadísticas y georreferenciación | DANE | https://www.dane.gov.co/ |
| Catastro rural (ANT) | ANT | https://www.agenciadetierras.gov.co/ |
| Consulta de predios (SNR) | Superintendencia de Notariado | https://www.supernotariado.gov.co/ |
| Vuelos en vivo | Flightradar24 | https://www.flightradar24.com/7.7,-71.28/5 |
| Tráfico marítimo | MarineTraffic | https://www.marinetraffic.com/es/ais/home/centerx:-12.1/centery:25.0/zoom:4 |
| Clima en tiempo real | Windy | https://www.windy.com/?4.598,-74.076,5 |

---

## 🔍 Personas desaparecidas y fallecidas

| Fuente | Entidad | URL |
|--------|---------|-----|
| Registro Nacional de Desaparecidos | Medicina Legal | https://www.medicinalegal.gov.co/rnd-registro-de-desaparecidos |
| Personas fallecidas sin reclamar (Bogotá) | Medicina Legal | https://www.medicinalegal.gov.co/personas-fallecidas-sin-reclamar-bogota |
| Circulares rojas INTERPOL (fugitivos) | INTERPOL | https://www.interpol.int/es/Como-trabajamos/Notificaciones/Ver-las-notificaciones-rojas |
| Circulares amarillas INTERPOL (desaparecidos) | INTERPOL | https://www.interpol.int/es/Como-trabajamos/Notificaciones/Ver-las-notificaciones-amarillas |

---

## 🌍 Sanciones internacionales

| Fuente | Organismo | URL |
|--------|-----------|-----|
| Lista OFAC (EE.UU.) | OFAC / Tesoro | https://sanctionssearch.ofac.treas.gov/ |
| Lista ONU — Consejo de Seguridad | ONU | https://scsanctions.un.org/search/ |
| Lista EUROPOL — más buscados | EUROPOL | https://eumostwanted.eu/es |
| Sanciones BID | BID | https://www.iadb.org/es/transparencia/empresas-y-personas-sancionadas |
| Panama Papers / ICIJ | ICIJ | https://offshoreleaks.icij.org/ |
| Sanciones DOJ (EE.UU.) | Dep. de Justicia | https://www.justice.gov/criminal-fraud/chronological-list |

---

## 🔎 Google Dorks para Colombia

```bash
# Buscar cédulas expuestas en documentos públicos
"cedula" filetype:pdf site:gov.co

# Buscar contratos específicos por nombre de persona
"[NOMBRE APELLIDO]" site:contratos.gov.co

# Buscar en la Procuraduría
"[NOMBRE]" site:procuraduria.gov.co

# Buscar en la Contraloría
"[NOMBRE]" site:contraloria.gov.co

# Buscar declaraciones de bienes
"[NOMBRE]" "declaracion de bienes" site:gov.co

# Buscar documentos con números de cédula de rangos específicos
"[NÚMERO]" filetype:pdf site:datos.gov.co

# Buscar en el portal de contratación
"[NOMBRE]" site:secop.gov.co

# Buscar en medios con cédula
"cedula [NÚMERO]" site:eltiempo.com OR site:elespectador.com

# Buscar RUT o NIT
"nit [NÚMERO]" site:gov.co
```

---

## 🛠️ Herramientas OSINT aplicables

| Herramienta | Uso | Enlace |
|-------------|-----|--------|
| Sherlock | Búsqueda de usernames en redes sociales | https://github.com/sherlock-project/sherlock |
| theHarvester | Recopilación de emails, subdominios, IPs | https://github.com/laramies/theHarvester |
| Maltego | Mapeo de relaciones y grafos de inteligencia | https://www.maltego.com/ |
| WHOIS — .co | Registro de dominios colombianos | https://www.nicco.co/ |
| Wayback Machine | Historial de páginas web | https://web.archive.org/ |
| ExifTool | Extracción de metadatos de archivos | https://exiftool.org/ |
| Google Colab + Python | Análisis de datos abiertos | https://colab.research.google.com/ |

---

## 📁 Estructura del repositorio

```
osint-colombia/
├── README.md                    ← Este archivo
├── cedula/
│   ├── README.md               ← Superficie de exposición de la cédula
│   └── flujo_cedula.png        ← Diagrama de fuentes por número de cédula
├── empresas/
│   └── README.md               ← Fuentes para personas jurídicas y NIT
├── contratacion/
│   └── README.md               ← SECOP, RUP y cruce con RUES
├── electoral/
│   └── README.md               ← Fuentes electorales y políticas
├── territorio/
│   └── README.md               ← Geografía, catastro y GEOINT
├── dorks/
│   └── colombia_dorks.md       ← Google Dorks contextualizados
├── herramientas/
│   └── README.md               ← Herramientas y entornos recomendados
└── casos/
    └── README.md               ← Casos prácticos documentados (anonimizados)
```

---

## 📚 Casos prácticos documentados

> *En construcción — se irán añadiendo casos reales anonimizados con metodología documentada.*

| Caso | Técnicas usadas | Fuentes principales |
|------|----------------|---------------------|
| Dominios electorales sospechosos (2023) | WHOIS, Google Dorks, SOCMINT | NIC.CO, RUES, redes sociales |
| Contratista con múltiples cédulas empresariales | RUES + SECOP cruzado | RUES, SECOP II, SIMIT |

---

## 🤝 Contribuciones

Este repositorio está en construcción activa. Si identificas una fuente pública que debería estar aquí, abre un *issue* o envía un *pull request*.

**Criterios para aceptar una fuente:**
- Debe ser de acceso público y gratuito
- Debe pertenecer a una entidad oficial o ser un recurso verificable
- Debe respetar el marco ético del OSINT legítimo

---

## 📖 Referencias y repositorios relacionados

- [osint-brazuca](https://github.com/osintbrazuca/osint-brazuca) — Referente brasileño que inspiró este repositorio
- [BeHackerPro/OSINT_in_Colombia](https://github.com/BeHackerPro/OSINT_in_Colombia) — Primer repositorio de OSINT colombiano
- [DragonJAR/OSINT-Notas](https://github.com/DragonJAR/OSINT-Notas) — Notas OSINT con fuentes colombianas por Jorge Coronado
- [jivoi/awesome-osint](https://github.com/jivoi/awesome-osint) — Lista curada de herramientas OSINT globales

---

## 📜 Licencia

Este repositorio se distribuye bajo licencia **MIT**. El contenido es de carácter educativo. El autor no se responsabiliza por usos indebidos de la información aquí recopilada.

---

*Mantenido por [@Hyperconectado] — 
