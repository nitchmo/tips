# ディスプレイの無い環境で Raspberry Pi OS をインストール

## インストールする環境

* MacBook Pro
* USB LAN
* Raspberry Pi 3+
* MicroSD 32GB
* USBカードリードライター（MicroSD対応）

## MicroSDの作成

今回は、32GBのMicroSDカードを使用しました。
↓から、OSをダウンロードしてSDカードへの書き込みまでしてくれるアプリをダウンロードします。
https://www.raspberrypi.org/downloads/

USBカードリードライターをMacに付けて、MicroSDカードを認識させます。

上記でダウンロードしたアプリを起動して、OSは、Raspberry Pi OS LITE を選択し、SDカードも選択したら、「WRITE」ボタンをクリックして書き込み開始。

書き込みが完了したら、一度USBカードリードライターを抜き差しして、再度 MicroSDカードを認識させます。
すると、/Volumes/boot とマウントされるので、空のsshファイルを作成します。

```
touch /Volumes/boot/ssh
```

## SSH接続

まず、回線の接続としては、Macと直接LAN接続するだけで、他には Wi-FiもLAN HUBにも接続しません。

そして、上記で作成したMicroSDを、Raspberry Piに付けて起動して１分ほど待って、起動したらSSH接続します。

```
ssh pi@raspberrypi.local
```

上記で起動すると、ネットワークの設定をするまでは再起動しないでください。
１度起動する時に touchコマンドで作成したsshファイルは削除されていて、今度は上記の様な raspberrypi.localの名前解決が出来ない状態になります。
