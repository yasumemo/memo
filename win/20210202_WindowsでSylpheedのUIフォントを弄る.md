# WindowsでSylpheedのUIフォントを弄る

https://www.aq-m08.com/2016/02/sylpheed.html

Windows10上のSylpheed3.7での話。

    style "user-font"
    {
      font_name="Yu Gothic UI 12"
    }
    widget_class "*" style "user-font"

みたいな感じのファイルを

    C:\Users\hoge\AppData\Roaming\Sylpheed\gtkrc

として保存。

