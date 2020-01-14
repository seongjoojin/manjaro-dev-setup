# manjaro-dev-setup

manjaro linux 환경 설정 저장용 레포 (gnome 기준)

## 패키지 업그레이드

```bash
$ sudo pacman -Syu
```

## 한글 설정

uim를 설치해줍니다

```bash
# uim 설치
$ sudo pacman -Sy uim

# xprofile 수정
$ nano ~/.xprofile
```

.xprofile은 아래의 내용으로 수정하여 줍니다.

```text
export GTK_IM_MODULE='uim'
export QT_IM_MODULE='uim'
uim-xim &
export XMODIFIERS='@im=uim'
```

다음으로는 입력기를 설정합니다.
만약 아래 명령어로 나오지 않는다면 시작메뉴에서 uim을 입력하면 나오게 됩니다.

```bash
$ uim-pref-gtk
```
위의 설정에서는 기본 입력기를 벼루로 설정해줍니다.

```bash
$ sudo pacman -Sy noto-fonts-cjk
```

마지막으로 한글 폰트를 설치하고 마무리합니다.


## 저장소 설정 

```bash
$ sudo pacman-mirrors --fasttrack
```
