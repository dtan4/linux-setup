# VAIO Pro でのスピーカー
* スピーカーアイコンのサウンドカード変更
* /usr/share/alsa/alsa.conf を修正

```
defaults.ctl.card 1
defaults.pcm.card 1
```

* キーボード -> ショートカット
    * `amixer set Master 5%+`
    * `amixer set Master 5%-`
    * `amixer set Master toggle`
