# USB Storage
* `yaourt -S gvfs udisks2`
* 設定 -> リムーバブルメディア でオートマウント
* .xinitrc に以下を追記
    * `exec dbus-launch`
