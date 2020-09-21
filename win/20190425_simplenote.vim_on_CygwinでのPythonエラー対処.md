# simplenote.vim on Cygwin でのPythonエラー対処

CygwinのVimでsimplenote.vimを実行するとエラーが出てうまく動かない。エラーメッセージの最後に、

    UnicodeDecodeError: 'ascii' codec can't decode byte 0xe6 in position 6: ordinal not in range(128)

こんなのが出ている。

http://shu223.hatenablog.com/entry/20111201/1328334689 を参考に

    $ python
    Python 2.7.16 (default, Mar 20 2019, 12:15:19)
    [GCC 7.4.0] on cygwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> import sys
    >>> sys.getdefaultencoding()
    'ascii'

となったので、

    import sys
    sys.setdefaultencoding('utf-8')

な中身の sitecustomize.py を

    /usr/lib/python2.7/site-packages

以下に作成するとうまくいく。

