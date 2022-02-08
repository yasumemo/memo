# ManjaroでHHKB Hybridのペアリング

HHKB Hybridを購入したのでManjaroとペアリングしようと思ったらGUIから出来なかったので

https://wiki.archlinux.jp/index.php/Bluetooth

を参考に手動で設定する。

まず、 bluez-utils パッケージをインストールして、

    $ bluetoothctl

で対話形式のプロンプトに入るので、

    # default-agent
    # scan on

でずらずらと表示される中でHHKBを見つけて、

    # pair 00:12:34:56:78:90

な感じでMACアドレスを入力するとPINコードの入力を促されるので、HHKBからそのコードを入力すればペアリング終了。

    # exit

で終了。

ログイン画面でもHHKBが使えるように /etc/bluetooth/main.conf の [Policy] セクションに

    AutoEnable=true

な設定を追加しておく。

