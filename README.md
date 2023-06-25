# MultipleOsPlatform
Creating a FileHelper compatible with all Operation Systems. 
```CSharp
public static partial class FileHelper
{
    public static char GetDirectorySeparator()
    {
        return FileHelper.DirectorySeparator;
    }
}
```
The `FileHelper.Windows.cs` file:
```CSharp
public static partial class FileHelper
{
    public const char DirectorySeparator = '\\';
}
```
The `FileHelper.Unix.cs` file:
```CSharp
public static partial class FileHelper
{
    public const char DirectorySeparator = '/';
}
```
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
