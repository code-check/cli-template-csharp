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

## 外部ライブラリの追加方法
外部ライブラリを使用する場合は以下の手順で実施してください。

- [build.sh](build.sh)に以下の内容を `mcs` の前に追加  
(複数のライブラリのインストールも行を追加していく事で可能です)

```
nuget [LibraryName]
```

必要に応じて`mcs`コマンドの`-reference`オプションを追加してください。

環境変数`MONO_PATH`が必要な場合は、TrackのUIより環境変数を設定してください。  
`build.sh`内でexportしても有効にはなりません。
