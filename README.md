<h1 align="center">Arch Install Scripts</h1>

Custom script made in order to automate Arch-Linux's configuration. :ice_cube:

## Obtaining The Repository :bangbang:

- Get list of packages and install git: `pacman -Sy git`
- Get the scripts: `git clone git://github.com/vol0s/ais`

### ACS [Arch Config Script] Configuration :mag:

First of all we need to edit some variables inside the `acs` script, so as to satisfy our personal needs. Ex:

```bash
USERNAME="user"
```

The next step will be configuring our freshly installed Arch Installation. It will handle the following configs. It will also ask for Ricing Dotfiles if a Tiling WM is selected.

- [X] Base Extra libs
- [X] AUR Helper (yay)
- [X] Colored Utils
- [X] Bluetooth (bluez/blueman)
- [X] Desktop Env
  - [X] KDE
  - [ ] i3-gaps
  - [X] Sway
  - [ ] Wayfire
- [X] Display Manager (sddm)
- [X] Browsers (firefox/qutebrowser)
- [X] Virtualization
- [X] Containers
- [X] Hardening Tools
- [X] Hacking Tools

- [X] RICING :rice_ball:
  - [X] sway-violet-rice
  - [ ] sway-dracula-rice
  - [ ] i3-violet-rice
  - [ ] i3-dracula-rice

The installation process is simple, just follow the steps until oh-my-zsh plugins are installed and a zsh shell is opened. Then exit this shell and the installation process will continue. Just press Enter when its needed, and make your choices when asked. It also will install several applications like Spotify. It's recommended to modify the `acs` script and add the utilities you want.

```bash
./acs
```

## License :scroll:

This project is licenced under the GNU General Public License V3. For more information, see the `LICENSE` file or visit https://www.gnu.org/licenses/gpl-3.0.en.html