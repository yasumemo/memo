# FirefoxのUIフォント

https://www.bugbugnow.net/2018/04/firefox-userchromecss.html

FirefoxのUIフォントサイズが小さいので大きくする。

about:config で

    toolkit.legacyUserProfileCustomizations.stylesheets

を true にして、about:profilesで見えるルートディレクトリにある chrome という名のディレクトリ、なければ作成して、そこに

    @charset "UTF-8";
    
    @-moz-document url(chrome://browser/content/browser.xhtml) {
    
      * {
        font-size: 12pt;
      }
    
    }

という内容で userChrome.css を作る。

### UIのDOMの確認方法。

開発ツールを表示して、その設定から

- ブラウザとアドオンのデバッガーを有効化
- リモートデバッガーを有効化

の二つをオンにして、メニューから「ウェブ開発」の中にある「ブラウザツールボックス」を立ち上げる。

