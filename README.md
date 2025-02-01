# After Installing Ubuntu
Ubuntuをインストールした後にやることの備忘録

## フォルダを英語名にする
```bash
$ LANG=C xdg-user-dirs-gtk-update
```

## CapsLock を Control にする
/etc/default/keyboard の内容を以下に変更する
```
XKBOPTIONS="ctrl:nocaps"
```

## sudoerの追加
/etc/sudoers.d/20-admin を作成して以下の内容にする
```
ユーザー名 ALL=(ALL:ALL) NOPASSWD:ALL
```

## i3のインストール
```
sudo apt install i3
```


