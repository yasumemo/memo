# DropboxをUbuntu 16.04で自動起動させる

https://www.dropbox.com/download?dl=packages/dropbox.py を落として、/usr/local/bin/dropboxとして、

    $ sudo chmod a+x /usr/local/bin/dropbox

で実行属性を付加。

ユーザーhogeの場合、以下の内容

    [Unit]
    Description=Dropbox Service
    After=network.target
    
    [Service]
    ExecStart=/bin/sh -c '/usr/local/bin/dropbox start'
    ExecStop=/bin/sh -c '/usr/local/bin/dropbox stop'
    PIDFile=/home/hoge/.dropbox/dropbox.pid
    User=hoge
    Group=hoge
    Type=forking
    Restart=on-failure
    RestartSec=5
    StartLimitInterval=60s
    StartLimitBurst=3
    
    [Install]
    WantedBy=multi-user.target

を/etc/systemd/system/dropbox.serviceとして保存。

    $ sudo systemctl daemon-reload
    $ sudo systemctl enable dropbox.service

で登録完了。

    $ sudo systemctl start dropbox.service

で始める。

