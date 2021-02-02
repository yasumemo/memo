# FirefoxのUIフォント

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

