# Command line application template for `C#`

Implement CLI application by editing [MainApp.cs](src/MainApp.cs)
You may add new files to keep your code clean, if it is allowed in your challenge.

## How to get input parameters
You can get arguments as `args` parameter, defined in Main method

```cs
public class MainApp
{
    static public void Main(string[] args)
    {
      // code to run
    }
}
```

## How to output result
You can use `Console.WriteLine` method to out put your results.

```cs
  Console.WriteLine("hoge")
```

## Install External Libraries
If you want to use external libraries, do the following:

- Add the following lines to [build.sh](build.sh), before the `mcs` line  
(You can have multiple libraries by adding more lines)

```
nuget [LibraryName]
```

You can add `-reference` option or some others, if these are required.

If you need to define env var `MONO_PATH`, please define it on Track UI.  
You can't define any environment variables in `build.sh`
