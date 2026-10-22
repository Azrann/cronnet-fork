**Languages:** [English](Readme.md) · [Español](README.es.md)

# CronNET

Biblioteca C# para ejecutar acciones según expresiones cron, con un planificador en memoria, trabajos en hilos y pruebas del análisis de horarios.

Documentación basada en los archivos locales revisados el 21 de octubre de 2026.

<!-- BEGIN project-context -->

## Antigüedad y evidencia

**Año de referencia de esta versión: 2017.** Se toma el archivo de código o configuración más reciente con una fecha histórica recuperable; no se ha podido confirmar la fecha exacta de creación.

- Archivo más reciente datable: **2017-11-13**, [`CronNET/CronNETTests/packages.config`](CronNETTests/packages.config); fecha de modificación conservada.
- Primer registro del repositorio Git original que contiene este código: **2012-01-05**. Puede corresponder a una importación; no prueba cuándo se escribió por primera vez.
- Dependencia fechada más reciente entre las comprobadas: [NUnit 2.6.3](https://www.nuget.org/packages/NUnit/2.6.3), publicada el **2013-10-11** (versión declarada), en [`CronNET/CronNETTests/packages.config`](CronNETTests/packages.config).
- Referencia adicional: destino `v4.0` en [`CronNET/CronNET/CronNET.csproj`](CronNET/CronNET.csproj); su [versión estable se publicó el 2010-04-12](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-framework). Es una pista de generación tecnológica; pudieron existir versiones preliminares anteriores.

La publicación de una dependencia sitúa la configuración conservada a partir de esa versión, si la referencia es válida. Una actualización de paquetes puede ser mucho más reciente que el inicio del proyecto. No se restauraron paquetes para comprobarlo.

## Por qué merece la pena mirarlo

CronSchedule convierte expresiones cron en decisiones de ejecución, y CronDaemon coordina los trabajos. Es una biblioteca pequeña donde se puede seguir el planificador completo y contrastar sus decisiones con las pruebas del calendario.

Puntos de entrada al código:

- [`CronNET/CronSchedule.cs`](CronNET/CronSchedule.cs)
- [`CronNET/CronDaemon.cs`](CronNET/CronDaemon.cs)
- [`CronNETTests/CronScheduleTests.cs`](CronNETTests/CronScheduleTests.cs)

<!-- END project-context -->

## Estructura y responsabilidades

| Ruta | Responsabilidad |
| --- | --- |
| `CronNET/CronDaemon.cs` | Registra trabajos y revisa el cambio de minuto mediante un temporizador de 30 segundos. |
| `CronNET/CronJob.cs` | Comprueba el horario e inicia la acción en un Thread. |
| `CronNET/CronSchedule.cs` | Interpreta y evalúa la expresión de calendario. |
| `CronNETTests/` | Pruebas NUnit del calendario. |
| `LICENSE.md, Readme.md` | Licencia y documentación original, que se conservan. |

## Tecnologías y requisitos

Windows o herramientas compatibles con .NET Framework 4.0, Visual Studio/MSBuild y NUnit 2.6.3 para las pruebas.

Destinos leídos de los proyectos: `v4.0`.

## Preparación y arranque

Abrir CronNET.sln, restaurar los paquetes NuGet y compilar la biblioteca. Un consumidor crea CronDaemon, llama AddJob y Start, y mantiene su proceso en ejecución. El proyecto no es un servicio instalado por sí mismo.

Soluciones presentes: `CronNET.sln`.

## Configuración e integraciones

No se identificó configuración privada propia. Las acciones y horarios los proporciona el proceso consumidor.

## Estado de esta copia

IcoReaderService, en cryptomarketanalysis, utiliza la API CronNET. La implementación usa Thread.Abort al detener trabajos, por lo que requiere revisar compatibilidad y comportamiento antes de migrarla a runtimes distintos.

La revisión fue estática: no se restauraron dependencias, no se compiló ni se ejecutaron aplicaciones o pruebas. Los comandos anteriores son instrucciones de preparación, no resultados de validación. Las versiones indicadas son las del código conservado.


## Copia pública

Las credenciales originales se han retirado o sustituido por `REPLACE_WITH_YOUR_VALUE`. Los datos locales, sesiones, certificados privados y perfiles de despliegue se omiten. Configurar servicios y credenciales propios antes de ejecutar. La compilación y el funcionamiento con servicios externos no se han validado.
