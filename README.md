<h1 align="center">Arch Install Scripts</h1>

Custom scripts made in order to automate Arch-Linux's installation & configuration. :ice_cube:

## Note :memo:

* You can first try it in a `VirtualMachine`

## Obtaining The Repository :bangbang:

- Increase cowspace partition: `mount -o remount,size=2G /run/archiso/cowspace`
- Get list of packages and install git: `pacman -Sy git`
- Get the script: `git clone git://github.com/vol0s/ais`

## How to use AIS :ice_cube:

The Repository will consist of 4 scripts: 

- ais [Arch Install Script]
- acs [Arch Config Script]
- aps [Arch Pentest Script]
- shared [Shared Code]

### AIS [Arch Install Script] Installation :mag:

First of all we need to edit some variables inside the `shared` script, so as to satisfy our personal needs. Ex:

```bash
KEYMAP="es"
MIRROR_COUNTRY="Spain"
TIMEZONE_PATH="Europe/Madrid"
LOCALE_GEN="es_ES.UTF-8"
NTP_STRING="0.es.pool.ntp.org 1.es.pool.ntp.org"
USERNAME="user"
HOSTNAME="arch"
EDITOR="vi"
```

Once we've edited these variables we will be ready to launch our `ais` script, which will ask us for the rest of specifications. For the moment it has only been tested with DOS partitioning, and the Default Mode needs a SWAP partition. This Script will also configure the network via `NetworkManager` service's DHCP and grant sudo to our created user.

```bash
./ais
```

### ACS [Arch Config Script] Configuration :mag:

The next step will be configuring our freshly installed Arch Installation. It will handle the following configs. It will also ask for Ricing Dotfiles if a Tiling WM is selected.

- [X] Base Extra libs
- [X] AUR Helper (yay)
- [X] Colored Utils
- [X] Audio (alsa/pulseaudio)
- [X] Bluetooth (bluez/blueman)
- [X] NFS/NTFS
- [X] Desktop Env
  - [X] KDE
  - [ ] i3-gaps
  - [X] Sway
  - [ ] Wayfire
- [X] Display Manager (sddm)
- [X] Browsers (firefox/qutebrowser)
- [X] GPU Drivers (amdgpu)
- [ ] Virtualization
- [X] Containers

- [X] RICING :rice_ball:
  - [X] sway-violet-rice
  - [ ] sway-dracula-rice

The installation process is simple, just follow the steps until oh-my-zsh plugins are installed and a zsh shell is opened. Then exit this shell and the installation process will continue. Just press Enter when its needed, and make your choices when asked. It also will install several applications like Spotify. It's recommended to modify the `acs` script and add the utilities you want.

```bash
./acs
```
### APS [Arch Pentest Script] Pentesting :mag:

This script will set a full pentest environment for our Arch-Linux installation. ### WORK IN PROGRESS ###

```bash
./aps
```
## Roadmap :calendar:

- [X] AIS [Arch Install Script]
- [X] ACS [Arch Config Script]
- [ ] APS [Arch Pentest Script]

## Thanx helmuthdu :kissing_heart:

I've gathered lots of inspiration from helmuthdu's (<a href="https://github.com/helmuthdu/aui">aui</a>) in preparation for making my own scripts, please consider sending him a small Paypal donation at helmuthdu@gmail.com :)

## License :scroll:

This project is licenced under the GNU General Public License V3. For more information, see the `LICENSE` file or visit https://www.gnu.org/licenses/gpl-3.0.en.html

