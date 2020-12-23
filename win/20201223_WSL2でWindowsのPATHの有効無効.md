# WSL2でWindowsのPATHの有効無効

WSL2のUbuntu上では

    $ echo $PATH
    /home/hoge/.zsh/zplug/repos/zplug/zplug/bin:/home/hoge/.zsh/zplug/bin:/usr/local/bin:/usr/local/sbin:/bin:/sbin:/usr/bin:/usr/sbin:/usr/games:/usr/local/games:/mnt/c/Windows/system32:/mnt/c/Windows:/mnt/c/Windows/System32/Wbem:/mnt/c/Windows/System32/WindowsPowerShell/v1.0/:/mnt/c/Windows/System32/OpenSSH/:/mnt/c/Users/fuga/AppData/Local/Microsoft/WindowsApps

となっており、WindowsなPATHが沢山。

これが悪さをすることがあったりなかったりするらしい。

https://qiita.com/ysd_marrrr/items/e22dec510755a8230c07

WSL2上のUbuntu内の/etc/wsl.confで有効無効が切り替えられるらしい。

    [interop]
    appendWindowsPath = false

手元の環境では/etc/wsl.confは無かったので作成する必要があった。

