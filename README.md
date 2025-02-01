# After Installing Ubuntu
Ubuntuをインストールした後にやることの備忘録

## フォルダを英語名にする
```bash
$ LANG=C xdg-user-dirs-gtk-update
```
### バックアップを戻す
user-dirs.dirs
user-dirs.locale

## CapsLock を Control にする
/etc/default/keyboard の内容を以下に変更する
```
XKBOPTIONS="ctrl:nocaps"
```

## ナチュラルスクロールにする
/usr/share/X11/xorg.conf.d/40-libinput.conf の内容を一部修正する
```
[Identifier "libinput pointer catchall"]
 Option "NaturalScrolling" "True"
```
および
```
[Identifier "libinput touchpad catchall"]
 Option "NaturalScrolling" "True"
 Option "Tapping" "on"
```

## sudoerを追加する
/etc/sudoers.d/20-admin を作成して以下の内容にする
```
ユーザー名 ALL=(ALL:ALL) NOPASSWD:ALL
```

## i3 をインストールする
```
sudo apt install i3 i3status
```
### バックアップを戻す
.confi/i3/
.i3status.conf

## 日本語関係＆mozc をインストールする
```
sudo apt install language-pack-ja-base language-pack-ja fonts-noto-cjk-extra fcitx5-mozc
```
### バックアップを戻す
~/.fonts
```
fc-cache -fv
```

## Firefox & Thunderbird をインストールする
```
sudo apt install firefox thunderbird
```
### バックアップを戻す
.thunderbird/

## syncthing をインストールする
```
sudo apt install syncthing
```
### バックアップを戻す
~/.config/syncthing/
### /etc/sysctl.conf の最後に以下を追加する
```
fs.inotify.max_user_watches=204800
```
### サービスを登録・実行する
```
sudo systemctl start syncthing@ユーザー名.service
sudo systemctl enable syncthing@ユーザー名.service
```
## emacs をインストールする
```
sudo apt install emacs emacs-mozc
```
### バックアップを戻す
.emacs.d/init.el

### libreoffice をインストールする
```
sudo apt install libreoffice libreoffice-l10n-ja libreoffice-help-ja
```

## その他をインストールする
```
sudo apt install feh ntpdate rsnapshot kmix flameshot openssh-server
```

## バックアップを元にもどす
.fehbg
.bashrc
~/.ssh
/etc/rsnapshot.conf
~/bin
~/working
~/Research
~/Dropbox
~/Downloads
~/Music
~/landisk
~/Pharo
~/Pictures
~/Videos

