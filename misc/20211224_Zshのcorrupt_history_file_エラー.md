# Zshの corrupt history file エラー

    zsh: corrupt history file /home/hoge/.zhistory

みたいなエラーが出たときの対処法。

その1。

    mv .zhistory .zhistory_bad
    strings .zhistory_bad > .zhistory
    fc -R .zhistory

その2。

壊れた .zhistory ファイルをVimなどで開いて、

    ^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@^@: 1408035735:0;abababa

みたいな感じで壊れている行を削除。

