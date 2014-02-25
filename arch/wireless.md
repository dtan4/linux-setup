# 無線通信
## NetworkManager & dhcpcd
* /etc/NetworkManager/NetworkManager.conf
    * `dhcp=dhcpcd`
* gnome-keyring をインストール
* .xinitrc

```sh
source /etc/X11/xinit/xinitrc.d/30-dbus
eval $(/usr/bin/gnome-keyring-daemon --start --components=gpg,pkcs11,secrets,ssh)
export GNOME_KEYRING_CONTROL GNOME_KEYRING_PID GPG_AGENT_INFO SSH_AUTH_SOCK
```


## (obsoluted) wicd & dhclient
* dhcpcd だと IP アドレス取得に失敗した
* wicd の設定画面で dhclient を明示的に指定する
