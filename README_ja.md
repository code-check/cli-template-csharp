# コマンドラインアプリケーション(CLI アプリ)作成用テンプレート(C#)

[src/App.cs](src/App.cs)を編集して、CLIアプリを実装してください。

## コマンドライン引数の取得方法
Main関数の引数argsで配列として取得することができます。

```cs
public class App
{
    static public void Main(string[] args)
    {
        // code to run
    }
}
```

## コマンド実行結果の標準出力への出力
標準の `Console.WriteLine` メソッド等が使用可能です。

```cs
  Console.WriteLine("hoge")
```
