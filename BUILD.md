# Building Pester

Pester is written in Powershell and C#.  The Microsoft .NET 4.5.2 Framework is required to build the Pester binaries.

Pester has a C# Solution which requires .Net Framework SDKs and Developer Packs in order to compile. The targetted frameworks can be found in `src\csharp\Pester\Pester.csproj`.

## Required Software

### Install .NET Core 3.1 SDK

[Download Link](https://dotnet.microsoft.com/download/dotnet-core/3.1)

### .Net Framework 4.5 Developer Pack

[Download Link](https://dotnet.microsoft.com/download/dotnet-framework/net452)
<https://aka.ms/msbuild/developerpacks>

## Running Tests

In Powershell, run test.ps1.  This defines the inherited function InPesterModuleScope and some types required for the tests.

Afterwards, each test can be run individually using Invoke-Pester.

Test.ps1 and optionally -skipPTests to skip the .ts.ps1 files.

## test.ps1

test.ps1 can be run with the following parameters

TODO document parameters, tests executed in pipelines.

```powershell
.\test.ps1 -CI -SkipPTests -NoBuild -File ${filename}
```

## Continuous Integration

The Azure Devops Pipeline azure-pipelines.yml file contains the code used for builds, unit and integration tests.

## Documentation

Documentation is available in the repo, the wiki, and at <https://pester.dev>

Documentation is written in Markdown. Comment-based Documentation and parts of the documentation web site are generated using Docusaurus Powershell.

Multi-line Examples added to comments should use fenced code.

<https://docusaurus-powershell.netlify.app/docs/faq/multi-line-examples>