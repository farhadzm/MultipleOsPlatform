# MultipleOsPlatform
This way, in the `GetDirectorySeparator` method, when the operating system is Linux, the character "/" is returned, and when the operating system is Windows, the character "\\" is returned.
```CSharp
var directorySeparator = FileHelper.DirectorySeparator;
Console.WriteLine(".{0}Data{0}uploads{0}fileName", directorySeparator);
```
In the Windows operating system, you would see the following output:
```
.\Data\uploads\fileName
```
And when executed on the Linux operating system, you would see the following output:
```
./Data/uploads/fileName
```
