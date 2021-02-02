# WindowsでSylpheedのUIフォントを弄る

Windows10上のSylpheed3.7での話。

    style "font"
    {
      font_name="Yu Gothic UI 12"
    }
    widget_class "*" style "font"

みたいな感じのファイルを

    C:\Users\hoge\AppData\Roaming\Sylpheed\gtkrc

として保存。

- https://www.aq-m08.com/2016/02/sylpheed.html
- http://sylpheed-support.good-day.net/bbs_article_body.php?pthread_id=95

