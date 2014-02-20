# Chrome でアンチエイリアスを効かせる
* https://wiki.archlinux.org/index.php/chromium#Font_rendering
* ~/.config/fontconfig/fonts.conf

```
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
  <match target="font">
  <edit mode="assign" name="autohint"><bool>true</bool></edit>
  <edit mode="assign" name="hinting"><bool>true</bool></edit>
  <edit mode="assign" name="hintstyle"><const>hintslight</const></edit>
  </match>
</fontconfig>
```
