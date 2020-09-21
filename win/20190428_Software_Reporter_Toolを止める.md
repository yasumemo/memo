# Software Reporter Toolを止める

Google Chrome を入れるとついてくる、Software Reporter ToolがCPUを食って煩わしいので止める。

https://support.graphisoft.co.jp/hc/ja/articles/360004830694-Chrome-Software-Reporter-Tool%E3%81%AE%E5%81%9C%E6%AD%A2%E6%96%B9%E6%B3%95

C:\Users\(USERNAME)\AppData\Local\Google\Chrome\User Data\SwReporter以下にバージョンに合わせて、software_reporter_tool.exe がある。

Google Chromeがアップデートされるたびに新しい物が入れられるのでうっとおしい。

software_reporter_tool.exe のプロパティを開いて、「セキュリティ」タブの「詳細設定」を開く。

「継承の無効化」をクリックし、「このオブジェクトから継承されたアクセス許可をすべて削除します。」を選択し「適用」をクリックすると、確認ウインドウが出るので「はい」を選択。

「OK」で終わり。

