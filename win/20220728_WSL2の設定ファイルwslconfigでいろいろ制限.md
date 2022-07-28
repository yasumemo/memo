# WSL2の設定ファイル .wslconfig でいろいろ制限

https://ascii.jp/elem/000/004/044/4044122/

%UserProfile%¥.wslconfig でいろいろ設定できるらしい。

https://qiita.com/yoichiwo7/items/e3e13b6fe2f32c4c6120

WSL2がホストのメモリを枯渇させるなんてこともあるらしいので設定しておく。

    [wsl2]
    memory=4GB
    swap=0
    processors=4

メモリを4GBに、swapをゼロに、プロセッサ数を４つに制限してみる。

