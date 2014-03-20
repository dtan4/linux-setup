# SLiM
* /etc/slim.conf
    * `current_theme archlinux`
* テーマの確認
    * `slim -p /usr/share/slim/themes/<theme name>`

## 蓋を占めた時に slimlock
* `pacman -S acpid`
* acpid を enable
* /etc/acpi/handler.sh の button/lid を編集
    * `/usr/bin/pm-suspend &` は余分。二重にサスペンドが掛かる？

```
button/lid)
    case $3 in
        close)
            #echo "LID switched!">/dev/tty5
            #/usr/bin/pm-suspend &
	        DISPLAY=:0.0 su -c - dtan4 /usr/bin/slimlock
            ;;
```
