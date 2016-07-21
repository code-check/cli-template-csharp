# CLIアプリケーション作成用テンプレート(C#)

C#でCLIアプリケーションを作成するためのテンプレートです。

[src/App.cs](src/App.cs)を編集することでCLIアプリケーションを作成することができます。

## コマンドライン引数の取得方法
Main関数の引数argsで配列として取得することができます。

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

## コマンド実行結果の標準出力への出力
標準の`Console.WriteLine`メソッドを使用してください。

``` C#
  Console.WriteLine("hoge")
```

