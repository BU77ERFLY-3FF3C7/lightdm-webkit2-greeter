## LightDM-webkit2-greeter (forked from [Antergos/web-greeter](https://github.com/antergos/web-greeter/))


### Installation

#### Official Distro Packages (Dismissed)
|Distro|Install Command/Links|
|:---:|:---:|
|![antergos][antergos]|`sudo pacman -S lightdm-webkit2-greeter`|

#### Unofficial Distro Packages
|Distro|Install Command/Links|
|:---:|:---:|
|![arch][arch] ![manjaro][manjaro] ![endeavour][endeavour]|`yay -S lightdm-webkit2-greeter`|
|![fedora][fedora] |[copr](https://copr.fedorainfracloud.org/coprs/antergos/lightdm-webkit2-greeter/) &nbsp;|
|![openSUSE][openSUSE]| Not available|
|![Debian][debian] ![ubuntu][ubuntu]| [latest release](https://github.com/MerkeX/Lightdm-webkit2-greeter/releases/download/v2.2.5-1/lightdm-webkit2-greeter_2.2.5-1_amd64.deb)|
### Building

### Dependencies
|                       | ![antergos][antergos] &nbsp; ![arch][arch] &nbsp; ![manjaro][manjaro] &nbsp;![endeavour][endeavour] | ![debian][debian] &nbsp; ![mint][mint] &nbsp; ![ubuntu][ubuntu] &nbsp; ![zorin][zorin] | ![fedora][fedora]     | ![opensuse][opensuse]  | 
|-----------------------|--------------------------------------------------|--------------------------------------------------|-----------------------|------------------------|
|**liblightdm-gobject-1** |lightdm                                         |liblightdm-gobject-dev                            | lightdm-gobject-devel | liblightdm-gobject-1-0 |
|**gtk+ 3**               |gtk3                                            |libgtk-3-0                                        | gtk3                  | gtk3                   |
|**webkit2gtk-4.0**       |webkit2gtk                                      |libwebkit2gtk-4.0-dev                             | webkitgtk4            | libwebkit2gtk-4_0-37   |
|**dbus-glib-1**          |dbus-glib                                       |libdbus-glib-1-dev                                | dbus-glib             | dbus-1-glib            |

#### Build Deps
|                   | ![antergos][antergos] &nbsp;&nbsp; ![arch][arch] &nbsp;&nbsp; ![endeavour] &nbsp;&nbsp; ![manjaro] &nbsp;&nbsp; ![debian][debian] &nbsp;&nbsp; ![mint] &nbsp;&nbsp; ![ubuntu][ubuntu] &nbsp;&nbsp; ![zorin] &nbsp;&nbsp; ![fedora][fedora] &nbsp;&nbsp; ![opensuse][opensuse] |
|-------------------|--------------------------------------------------|
|**Meson Build System**|meson v0.37+|

#### Antergos / Arch / Manjaro / EndeavourOS
    sudo pacman -S meson lightdm gtk3 webkit2gtk dbus-glib -y

#### Debian / Ubuntu / Linux Mint / Zorin OS
    sudo apt install meson liblightdm-gobject-dev libgtk-3-0 libwebkit2gtk-4.0-dev libdbus-glib-1-dev -y

#### Fedora
    sudo dnf install meson lighdm-gobject-devel gtk3 webkitgtk4 dbus-glib -y

#### OpenSUSE
    sudo zypper -n install meson lightdm-gobject-devel gtk3-devel libwebkit2gtk-4_0-37 dbus-1-glib-devel \
    webkit2gtk3-devel  webkit2gtk3-soup2-devel


### How To Build
```sh
git clone https://github.com/MerkeX/lightdm-webkit2-greeter.git /tmp/greeter
cd /tmp/greeter/build
#git checkout ${LATEST_RELEASE_TAG} # eg. git checkout 2.2
git checkout stable
meson --prefix=/usr --libdir=lib ..
ninja
```

### How To Install
```sh
sudo ninja install
```

#### One liner
```sh
git clone https://github.com/Antergos/lightdm-webkit2-greeter.git /tmp/greeter && cd /tmp/greeter/build && git checkout stable && meson --prefix=/usr --libdir=lib .. && ninja && sudo ninja install
```

## Theme JavaScript API:
The greeter exposes a JavaScript API to themes which they must use to interact with the greeter (in order to facilitate the user login process). For more details, check out the [API Documentation](https://doclets.io/Antergos/lightdm-webkit2-greeter/stable). 

Personally, I recommend the [litarvan theme](https://github.com/Litarvan/lightdm-webkit-theme-litarvan).



[antergos]: /.distro_logo/antergos.png "antergos"
[arch]: /.distro_logo/arch.png "arch"
[debian]: /.distro_logo/debian.png "debian"
[endeavour]: /.distro_logo/endeavour.png "endeavour"
[fedora]: /.distro_logo/fedora.png "fedora"
[manjaro]: /.distro_logo/manjaro.png "manjaro"
[mint]: /.distro_logo/mint.png "mint"
[openSUSE]: /.distro_logo/opensuse.png "openSUSE"
[ubuntu]: /.distro_logo/ubuntu.png "ubuntu"
[zorin]: /.distro_logo/zorin.png "zorin"

[release]: https://img.shields.io/github/release/Antergos/web-greeter.svg?style=flat-square "Latest Release"
[codacy]: https://img.shields.io/codacy/grade/43c95c8c0e3749b8afa3bfd2b6edf541.svg?style=flat-square "Codacy Grade"
[circleci]: https://img.shields.io/circleci/project/Antergos/web-greeter/master.svg?style=flat-square "CI Status"
[api]: https://img.shields.io/badge/API--Docs-ready-brightgreen.svg?style=flat-square "Theme API Docs"
[aur]: https://img.shields.io/aur/votes/lightdm-webkit2-greeter.svg?maxAge=604800&style=flat-square "AUR Votes"

[whither]: https://github.com/Antergos/whither "Whither"
