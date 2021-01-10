# Sound Blaster Play! 3 の音量

Sound Blaster Play! 3 は安いし、繋げばLinuxですぐ使えるし、ノイズを拾わないしで良いことが沢山あるのだが、音量が大きすぎたり、ボリュームを下げていくとある時点で急にミュートされたりするのが嫌。

https://chrisjean.com/fix-for-usb-audio-is-too-loud-and-mutes-at-low-volume-in-ubuntu/

手元の環境では /usr/share/alsa-card-profile/mixer/paths/analog-output.conf.common の該当部分を、

    [Element PCM]
    switch = mute
    volume = merge
    override-map.1 = all
    override-map.2 = all-left,all-right

から

    [Element PCM]
    switch = mute
    volume = ignore
    volume-limit = 0.01
    override-map.1 = all
    override-map.2 = all-left,all-right

に変更する。

後は、

    pulseaudio -k

で Pulseaudio を再起動。

