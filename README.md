# CLI template for C#

This is template app for making CLI application with C#.  
You can make CLI application by editing [src/App.cs](src/App.cs)

## How to get input parameters
The function Main have args parameter.

``` C#
public class App
{
    static public void Main(string[] args)
    {
        foreach (string arg in args) {
           Console.WriteLine(arg);
        }
    }
}
```

## How to output result
You can use `Console.WriteLine` method

``` C#
  Console.WriteLine("hoge")
```
