# Windows 10 Home でローカルグループポリシーエディターを使えるようにする

Proでは普通に使えるローカルグループポリシーエディターをHomeでも使えるようになるらしい。

https://www.japan-secure.com/entry/how-to-use-local-group-policy-editor-in-windows-10-home.html

まず

    @echo off
    pushd "%~dp0"
    
    dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientExtensions-Package~3*.mum >List.txt
    dir /b %SystemRoot%\servicing\Packages\Microsoft-Windows-GroupPolicy-ClientTools-Package~3*.mum >>List.txt
    
    for /f %%i in ('findstr /i . List.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"
    pause

という内容で、hobe.batなど適当な名前のバッチファイルを作成して保存して、管理者として実行する。

終わったら再起動して、 gpedit.msc をファイル名を指定して実行すればローカルグループポリシーエディターが起動する。

https://0ut3r.space/2022/03/06/windows-defender/

によるとローカルグループポリシーエディターでMicrosoft Defenderを強化できるらしい。

