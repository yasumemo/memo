# xfce4-screensaverが動かない

Xfce4でxfce4-screensaverを有効にしても、再起動すると、プロセスは起動しているにも関わらず設定時間が経過しても何も反応しない。

設定画面で何かしら設定を弄った後は正しく反応する。

ので、

    #!/bin/sh
    sleep 20
    xfconf-query --channel xfce4-screensaver --property /saver/enabled --set false
    sleep 5
    xfconf-query --channel xfce4-screensaver --property /saver/enabled --set true

みたいなシェルスクリプトを作成して自動開始アプリケーションに登録した。

一応動いている。

