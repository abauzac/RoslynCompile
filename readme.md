
Hello

This small project is just a test to show how you can compile C# Code into an assembly (or whatever)

Note that this work as I'm writing this using `1.0.0-preview2-1-003177`

As many things are changing releases after releases, this may not work in a futur .NET core version

The main things to look at are the project.json file for dependencies :
* System.Runtime.Loader
* Microsoft.CodeAnalysis

And also the imports (still in project.json) :
* dnxcore50
* portable-net45+win8

For now, loading an assembly through a stream is done using `AssemblyLoadContext.Default.LoadFromStream` method but it may change in futur releases of .NET Core

Finally, the base code is inspired from this [Stackoverflow post](http://stackoverflow.com/a/29417053/4739462)
