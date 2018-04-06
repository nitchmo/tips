# gitコマンドの補完

## GitHubサイトにある、git-completion.bashを利用する。

このファイル、よく設置場所が変わりますよね・・・  
2018-04-06現在では、下記にあります。  

https://github.com/git/git/tree/master/contrib/completion

## 設置方法

補完スクリプトのファイルさえ手に入れば、今までの導入方法はいっしょです。
```
wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
source git-completion.bash
```

私は必要になった時だけ、`source git-completion.bash` を実行するのですが  
それが面倒くさい方は、.bashrc に追記しておくのが一般的です。
```
> vim .bashrc

# 下記を追記
source ~/git-completion.bash
```
