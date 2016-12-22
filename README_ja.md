# コマンドラインアプリケーション(CLI アプリ)作成用テンプレート(C#)

[MainApp.cs](src/MainApp.cs)を編集して、CLIアプリを実装してください。
チャレンジ内でファイルの作成が許可されていれば、可読性等のためにファイルを分割する事も可能です。

## コマンドライン引数の取得方法
Main関数の引数 `args` で配列として取得することができます。

```cs
public class MainApp
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

## GitHub を用いたローカル受験の場合
codecheck コマンドでテストを行う場合、次のように [codecheck.yml](codecheck.yml) を修正する必要があります。  
（提出時にはもとに戻すことを忘れないでください！）

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
