# ThunarでWebP画像ファイルのサムネイルを表示する

新し目の画像フォーマットであるWebPはデフォルトではThunarにおいてサムネイルが表示されないので表示させる。

https://spacebums.co.uk/thunar-webp-thumbnails/

以下の内容を

    [Thumbnailer Entry]
    Version=1.0
    Encoding=UTF-8
    Type=X-Thumbnailer
    Name=webp Thumbnailer
    MimeType=image/webp;
    Exec=/usr/bin/convert -thumbnail %s %i %o
    /usr/share/thumbnails

/usr/share/thumbnails/webp.thumbnailer として保存する。

MIMEタイプは

    $ file -i sample_webp.webp
    sample_webp.webp: image/webp; charset=binary

登録されているようなのでThunarを再起動すればサムネイルが表示される。

