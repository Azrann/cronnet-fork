# cronnet-fork

Copia histórica de CronNET, biblioteca de tareas programadas para .NET.

<!-- BEGIN project-context -->

## Antigüedad y evidencia

**Año de referencia de esta versión: 2017.** Se toma el archivo de código o configuración más reciente con una fecha histórica recuperable; no se ha podido confirmar la fecha exacta de creación.

- Archivo más reciente datable: **2017-11-13**, [`CronNET/CronNETTests/packages.config`](CronNET/CronNETTests/packages.config); fecha de modificación conservada.
- Primer registro del repositorio Git original que contiene este código: **2012-01-05**. Puede corresponder a una importación; no prueba cuándo se escribió por primera vez.
- Dependencia fechada más reciente entre las comprobadas: [NUnit 2.6.3](https://www.nuget.org/packages/NUnit/2.6.3), publicada el **2013-10-11** (versión declarada), en [`CronNET/CronNETTests/packages.config`](CronNET/CronNETTests/packages.config).
- Referencia adicional: destino `v4.0` en [`CronNET/CronNET/CronNET.csproj`](CronNET/CronNET/CronNET.csproj); su [versión estable se publicó el 2010-04-12](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-framework). Es una pista de generación tecnológica; pudieron existir versiones preliminares anteriores.

La publicación de una dependencia sitúa la configuración conservada a partir de esa versión, si la referencia es válida. Una actualización de paquetes puede ser mucho más reciente que el inicio del proyecto. No se restauraron paquetes para comprobarlo.

## Por qué merece la pena mirarlo

CronSchedule convierte expresiones cron en decisiones de ejecución, y CronDaemon coordina los trabajos. Es una biblioteca pequeña donde se puede seguir el planificador completo y contrastar sus decisiones con las pruebas del calendario.

Puntos de entrada al código:

- [`CronNET/CronSchedule.cs`](CronNET/CronNET/CronSchedule.cs)
- [`CronNET/CronDaemon.cs`](CronNET/CronNET/CronDaemon.cs)
- [`CronNETTests/CronScheduleTests.cs`](CronNET/CronNETTests/CronScheduleTests.cs)

<!-- END project-context -->

## Contenido

| Directorio | Función |
| --- | --- |
| [`CronNET/`](CronNET/) | Biblioteca C# para ejecutar acciones según expresiones cron, con un planificador en memoria, trabajos en hilos y pruebas del análisis de horarios. |

Derivación importada de kevincolyar/CronNET. Se conserva LICENSE.md. El historial local anterior no se publica.

## Requisitos y preparación

.NET Framework, NuGet y NUnit.

Esta es una copia histórica. Consultar los archivos de proyecto y los README de cada componente para sus versiones y dependencias. Restaurar NuGet/npm desde la carpeta correspondiente; las bibliotecas internas pueden necesitar reconstrucción. Preparar las bases de datos y los servicios externos con cuentas propias.

Soluciones conservadas:

- `CronNET/CronNET.sln`

## Configuración y seguridad

Los secretos originales se han eliminado o sustituido por `REPLACE_WITH_YOUR_VALUE`. Buscar este marcador antes de ejecutar y aportar los valores mediante configuración local o variables de entorno. Las sesiones, claves privadas, certificados de firma, bases de datos, registros, perfiles de despliegue y paquetes binarios no se publican. El `.gitignore` protege estos archivos locales.

Se publica un historial nuevo: los commits antiguos permanecen únicamente en la copia local original. Los valores de ejemplo no permiten conectarse a los servicios originales.

## Estado de validación

Se realizó una revisión estática y un escaneo de secretos antes de publicar. No se ejecutaron aplicaciones, operaciones de trading, despliegues ni pruebas que contacten servicios externos. No se garantiza la compilación con herramientas actuales. Algunos proyectos necesitan dependencias históricas y activos que no están incluidos.

## Licencias y procedencia

Se conservan las licencias y atribuciones de terceros presentes en el código. No se añade una licencia global a los componentes que no la tenían. Esta importación conserva fuentes locales y no afirma ser una versión actual del proyecto original.

Proyecto de procedencia: [código original](https://github.com/kevincolyar/CronNET). Esta es una importación independiente de la copia local, con historial nuevo.
