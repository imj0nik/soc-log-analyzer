# SOC Log Analyzer

Aplicación web de una sola página para analistas SOC N2. Carga un Excel exportado de un SIEM y genera automáticamente el análisis, la correlación de incidentes y un informe técnico.

## Qué hace
- Valida las columnas del archivo y la ventana de tiempo de los eventos.
- Correlaciona eventos en incidentes por IP externa, cuenta o equipo.
- Calcula un puntaje de riesgo con los factores que lo justifican.
- Mapea técnicas MITRE ATT&CK, lista indicadores de compromiso y propone acciones de respuesta.
- Genera un informe técnico descargable en PDF.

## Privacidad
Todo el procesamiento ocurre en el navegador. El archivo no se envía a ningún servidor.

## Uso

**Opción 1: en línea (recomendada)**
Abre https://imj0nik.github.io/soc-log-analyzer/ y carga tu archivo. No requiere instalar nada.

**Opción 2: local**
1. Descarga `index.html` (botón **Download raw file** en GitHub) o clona el repositorio.
2. Ábrelo con doble clic en Chrome, Edge o Firefox. Requiere conexión a internet para cargar las librerías.

**Pasos en la aplicación**
1. En "Carga de logs", arrastra tu `.xlsx` exportado del SIEM.
2. Revisa Dashboard, Incidentes e Informe.
3. Pulsa "Descargar PDF" para obtener el informe técnico.

## Columnas esperadas
`Log_ID, Timestamp, Hostname, Event_ID, User, Source_IP, Destination, Log_Source, Event_Description, Process_CommandLine, Result, Severity`

`Timestamp` y `Event_ID` son obligatorias.

## Detecciones cubiertas
Eventos de Windows (4625, 4624, 4672, 4688, 4698, 7045, entre otros), proxy, firewall e IIS: password spraying, acceso exitoso tras fallos, ejecución sospechosa, persistencia y movimiento lateral.

## Tecnologías
HTML, CSS y JavaScript sin dependencias de servidor.

## Autor
**Juan Medina**
Proyecto final del bootcamp Analista SOC nivel 2 de Comunidad Dojo, octubre 2026.
GitHub: [@imj0nik](https://github.com/imj0nik)
