# SdkProject Extras for VS2017

<!-- Replace this badge with your own-->
[![Build status](https://ci.appveyor.com/api/projects/status/vr63sfhcc26yvdyx?svg=true)](https://ci.appveyor.com/project/robertmclaws/sdkprojects)
<!-- Update the VS Gallery link after you upload the VSIX-->
Download this extension from the [VS Marketplace](https://visualstudiogallery.msdn.microsoft.com/[GuidFromGallery])
or get the [CI build](http://vsixgallery.com/extension/2dd37380-7b86-413a-b26c-b6b2d5e067d4/).

---------------------------------------

A set of Item Templates to make writing legacy code with SdkProjects easier.

See the [change log](CHANGELOG.md) for changes and road map.

## Features

- EF6 EDMX ItemTemplate w/ Resource Generators.

### EF6 EDMX ItemTemplate w/ Resource Generators
Microsoft's Entity Framework build tasks aren't currently compatible with VS2017's new SDK projects.
So Microsoft doesn't even let you add new EDMX files to an SDK project. If you try to open an existing EDMX 
in a project that targets .NET Standard 2.0 first, they disable the EDMX designer.

In order to let developers upgrade to the new format to simplify their project files, the "Entity Framework 6 EDMX"
item template uses the standard EF ItemTemplate and Wizard, combined with a new T4 template that replaces the
EF MSBuild targets with a process you have more control over.

The new T4 template:
 - Removes the EDMX file from the project so it can be double-clicked and edited in the designer (stupid, I know...
   but it works).
 - Splits the EDMX file into separate CSDL, MSL, and SSDL resource files.
 - Sets the generated files as "EmbeddedResource" in the project so they get compiled into the assembly properly.
 - Sets the "LogicalName" property of each resource so they are namespaced in the assembly the way the EF6 Wizard
   generates connection strings.
 

## Contribute
Check out the [contribution guidelines](CONTRIBUTING.md)
if you want to contribute to this project.

For cloning and building this project yourself, make sure
to install the
[Extensibility Tools 2015](https://visualstudiogallery.msdn.microsoft.com/ab39a092-1343-46e2-b0f1-6a3f91155aa6)
extension for Visual Studio which enables some features
used by this project.

## License
[MIT](LICENSE)