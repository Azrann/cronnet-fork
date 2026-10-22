**Languages:** [English](README.md) · [Español](README.es.md)

# cronnet-fork

Historical copy of CronNET, a scheduled task library for .NET.

<!-- BEGIN project-context -->

## Historical dates and evidence

**Reference year for this version: 2017.** This uses the most recent source or configuration file with a recoverable historical date; the exact creation date could not be confirmed.

- Most recent datable file: **2017-11-13**, [`CronNET/CronNETTests/packages.config`](CronNET/CronNETTests/packages.config); preserved modification timestamp.
- First record in the original Git repository containing this code: **2012-01-05**. This may be an import and does not establish when the code was first written.
- Most recently published dependency among those checked: [NUnit 2.6.3](https://www.nuget.org/packages/NUnit/2.6.3), published on **2013-10-11** (declared version), in [`CronNET/CronNETTests/packages.config`](CronNET/CronNETTests/packages.config).
- Additional reference: target `v4.0` in [`CronNET/CronNET/CronNET.csproj`](CronNET/CronNET/CronNET.csproj); its [stable release was published on 2010-04-12](https://dotnet.microsoft.com/en-us/platform/support/policy/dotnet-framework). This indicates the technology generation; earlier preview releases may have existed.

A dependency's publication places the preserved configuration at or after that version, if the reference is valid. Package updates may be much newer than the project's beginnings. Packages were not restored to verify this.

## Why this is worth exploring

CronSchedule turns cron expressions into execution decisions, while CronDaemon coordinates jobs. This small library lets you follow the entire scheduler and compare its decisions with schedule tests.

Code entry points:

- [`CronNET/CronSchedule.cs`](CronNET/CronNET/CronSchedule.cs)
- [`CronNET/CronDaemon.cs`](CronNET/CronNET/CronDaemon.cs)
- [`CronNETTests/CronScheduleTests.cs`](CronNET/CronNETTests/CronScheduleTests.cs)

<!-- END project-context -->

## Contents

| Directory | Function |
| --- | --- |
| [`CronNET/`](CronNET/) | C# library for running actions based on cron expressions, with an in-memory scheduler, threaded jobs, and schedule parsing tests. |

Imported derivative of kevincolyar/CronNET. LICENSE.md is retained. The previous local history is not published.

## Requirements and setup

.NET Framework, NuGet, and NUnit.

This is a historical copy. Consult each component's project files and README for versions and dependencies. Restore NuGet/npm from the appropriate folder; internal libraries may need rebuilding. Prepare databases and external services using your own accounts.

Preserved solutions:

- `CronNET/CronNET.sln`

## Configuration and security

Original secrets have been removed or replaced with `REPLACE_WITH_YOUR_VALUE`. Search for this marker before running and provide values through local configuration or environment variables. Sessions, private keys, signing certificates, databases, logs, deployment profiles, and binary packages are not published. The `.gitignore` protects these local files.

A fresh history is published: old commits remain only in the original local copy. Example values cannot connect to the original services.

## Validation status

A static review and secret scan were performed before publication. Applications, trading operations, deployments, and tests contacting external services were not run. Building with current tools is not guaranteed. Some projects need historical dependencies and assets that are not included.

## Licenses and provenance

Third-party licenses and attributions present in the code are retained. No blanket license is added to components that lacked one. This import preserves local sources and does not claim to be a current version of the original project.

Upstream project: [original source](https://github.com/kevincolyar/CronNET). This is an independent import of the local copy, with a fresh history.
