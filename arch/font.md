# 強制的に Takao フォントを使う
* ~/.config/fontconfig/fonts.conf の fontconfig セクション

```
<match target="pattern">
    <test qual="any" name="lang" compare="contains">
        <string>ja</string>
    </test>
    <test name="family" qual="any">
        <string>serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
        <string>TakaoPMincho</string>
    </edit>
</match>
<match target="pattern">
    <test qual="any" name="lang" compare="contains">
        <string>ja</string>
    </test>
    <test name="family" qual="any">
        <string>sans-serif</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
        <string>TakaoPGothic</string>
    </edit>
</match>
<match target="pattern">
    <test qual="any" name="lang" compare="contains">
        <string>ja</string>
    </test>
    <test name="family" qual="any">
        <string>monospace</string>
    </test>
    <edit name="family" mode="prepend" binding="strong">
        <string>TakaoGothic</string>
    </edit>
</match>
```

* `fc-cache -rv`
* `fc-match :lang=ja:` で確認
