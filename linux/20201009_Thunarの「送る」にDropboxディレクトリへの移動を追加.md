# Thunarの「送る」にDropboxディレクトリへの移動を追加

    [Desktop Entry]
    Type=Application
    Version=1.0
    Encoding=UTF-8
    Exec=mv %f /home/hoge/Dropbox
    Icon=/home/hoge/Dropbox/Picture/dropboxstatus-logo.png
    Name=Dropbox

上の内容でファイルを作成し、適当に`dropbox-folder.desktop`とでも名付けて`$HOME/.local/share/Thunar/sendto/`に保存。

2021年1月24日追記

Xfceが4.16に上がってから、あるファイルをDropboxに「送る」と、そのファイルタイプの「アプリケーションで開く」メニューの候補に「送る」を実行した回数分の「Dropbox」というエントリーが羅列されるようになった。

よく分からない挙動なので、この設定は諦めてカスタムアクションで代替した。

