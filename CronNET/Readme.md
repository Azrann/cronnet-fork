**Languages:** [English](Readme.md) · [Español](README.es.md)

# CronNET

C# library for running actions based on cron expressions, with an in-memory scheduler, threaded jobs, and schedule parsing tests.

Documentation based on local files reviewed on 21 October 2026.

<!-- BEGIN project-context -->

## Historical dates and evidence

**Reference year for this version: 2017.** This uses the most recent source or configuration file with a recoverable historical date; the exact creation date could not be confirmed.

- Most recent datable file: **2017-11-13**, [`CronNET/CronNETTests/packages.config`](CronNETTests/packages.config); preserved modification timestamp.
- First record in the original Git repository containing this code: **2012-01-05**. This may be an import and does not establish when the code was first written.
- Most recently published dependency among those checked: [NUnit 2.6.3](https://www.nuget.org/packages/NUnit/2.6.3), published on **2013-10-11** (declared version), in [`CronNET/CronNETTests/packages.config`](CronNETTests/packages.config).
- Additional reference: target `v4.0` in [`CronNET/CronNET/CronNET.csproj`](CronNET/CronNET.csproj); its [stable release was published on 2010-04-12](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-framework). This indicates the technology generation; earlier preview releases may have existed.

A dependency's publication places the preserved configuration at or after that version, if the reference is valid. Package updates may be much newer than the project's beginnings. Packages were not restored to verify this.

## Why this is worth exploring

CronSchedule turns cron expressions into execution decisions, while CronDaemon coordinates jobs. This small library lets you follow the entire scheduler and compare its decisions with schedule tests.

Code entry points:

- [`CronNET/CronSchedule.cs`](CronNET/CronSchedule.cs)
- [`CronNET/CronDaemon.cs`](CronNET/CronDaemon.cs)
- [`CronNETTests/CronScheduleTests.cs`](CronNETTests/CronScheduleTests.cs)

<!-- END project-context -->

## Structure and responsibilities

| Path | Responsibility |
| --- | --- |
| `CronNET/CronDaemon.cs` | Registers jobs and checks for minute changes using a timer running every 30 seconds. |
| `CronNET/CronJob.cs` | Checks the schedule and starts the action in a Thread. |
| `CronNET/CronSchedule.cs` | Parses and evaluates schedule expressions. |
| `CronNETTests/` | NUnit schedule tests. |
| `LICENSE.md, Readme.md` | Original license and documentation, both retained. |

## Technologies and requirements

Windows or tools compatible with .NET Framework 4.0, Visual Studio/MSBuild, and NUnit 2.6.3 for tests.

Targets read from project files: `v4.0`.

## Setup and startup

Open CronNET.sln, restore NuGet packages, and build the library. A consuming application creates CronDaemon, calls AddJob and Start, and keeps its process running. The project is not an installed service on its own.

Solutions present: `CronNET.sln`.

## Configuration and integrations

No project-specific private configuration was identified. Actions and schedules are provided by the consuming process.

## Status of this copy

IcoReaderService in cryptomarketanalysis uses the CronNET API. This implementation calls Thread.Abort when stopping jobs, so review compatibility and behavior before migrating it to other runtimes.

The review was static: dependencies were not restored, and applications and tests were neither built nor run. The commands above are setup instructions, not validation results. Listed versions describe the preserved code.


## Public copy

Original credentials have been removed or replaced with `REPLACE_WITH_YOUR_VALUE`. Local data, sessions, private certificates, and deployment profiles are omitted. Configure your own services and credentials before running. Building and operation with external services have not been validated.
