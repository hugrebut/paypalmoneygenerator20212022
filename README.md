# BuildTaskNuGetPackageTemplate
A template for creating a NuGet Package that runs an exec task at build based on the work done for [NuGetDefense](https://digitalcoyote.github.io/NuGetDefense/).

## How to use this Template
Using this template is as simple as writing a console app.
 1. Create a repo from this template or run `dotnet new nugetbuildtask`
 2. Write the console app
 3. Modify MyBuildTask.nuspec with your package info
 4. Modify MyBuildTask.targets to pass in any necessary arguments from msbuild
 5. Change the After/Before Targets if you want it to run any time other than after the build finishes
    - Default: `<Target Name="MyBuildTask" AfterTargets="Build">` See [MSBuild Docs for more info](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-targets)
