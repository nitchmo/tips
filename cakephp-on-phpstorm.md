# PhpStormにて、CakePHP開発する時に、コード補完させる。

OSは、macOS High Sierra  
CakePHPのバージョンは、2.7  
PhpStormのバージョンは、2018.1  
です。

## ConsoleとTestsディレクトリをプロジェクトの対象からはずす。

⌘+,でPreferences画面を表示して、左メニューのDirectoriesを選択します。  
あとは、下記のディレクトリを選択して、Excludedをクリックします。  
```
/lib/Cake/Console
/lib/Cake/Test
```
Excluded後は、OKボタンをクリックして保存。

## /lib/Cake/Core/Object.phpをプレーンテキスト化

これは、Winと手順がいっしょ。

1. プロジェクトビューから/lib/Cake/Core/Object.phpを右クリックします。
1. 右クリックメニューのMark as Plain Textを選択します。

## PHPDocを編集するらしい・・・

[参考元](https://happyquality.com/2012/06/11/2276.htm)では、PHPDocの編集をすると保管が有効になるらしいのだが・・・
私の環境では、すでに保管が効いていた。  

