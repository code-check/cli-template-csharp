# Command line application template for C#

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

## For local exam using GitHub
To use codecheck command in your local environment, you need to modify [codecheck.yml](./codecheck.yml) in order to run test properly.

```yaml
# Before
build:
  - mcs src/*.cs -out:TheApp.exe
env:
  APP_COMMAND: mono TheApp.exe
main: src/MainApp.cs
test: mocha
```

```yaml
# After
build:
  - mcs "src/*.cs" -out:TheApp.exe
env:
  APP_COMMAND: mono TheApp.exe
main: src/MainApp.cs
test: mocha
```
