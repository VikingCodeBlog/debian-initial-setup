## Install base [debian](https://www.debian.org/)

Don't use the graphical installer

![Installer 1](./img/screenshot1.png)

Select only standard system utilities

![Installer 2](./img/screenshot2.png)

Add your usser to sudoers
```bash
su -l
apt-get install sudo
adduser {your-user-here} sudo
nano /etc/sudoers
```

Add this line after '%sudo' line
```
{your-user-here} ALL=(ALL:ALL) ALL
```
Example:
![Installer 3](./img/screenshot3.png)

Update system
```bash
sudo apt-get update
sudo apt-get upgrade
```

Install x window server [xorg](https://es.wikipedia.org/wiki/X.Org_Server)
```bash
sudo apt install xorg
```

Install window manager [i3](https://i3wm.org/)
I'm not going to install i3 directly, I prefer to use the [i3-gaps](https://github.com/Airblader/i3) fork, for that I need to install other tools like git, gcc and make

```bash
sudo apt-get install i3status i3lock dmenu git gcc make nitrogen lxappearance meson
```

Build i3-gaps

```bash
# clone the repository
git clone https://www.github.com/Airblader/i3 i3-gaps
cd i3-gaps

# compile
mkdir -p build && cd build
meson ..
ninja
meson install
```

i3-gaps dependences -> ([wiki](https://github.com/Airblader/i3/wiki/Building-from-source))

Intasll i3-gaps dependences (Debian)

```bash
apt install dh-autoreconf libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev xcb libxcb1-dev libxcb-icccm4-dev libyajl-dev libev-dev libxcb-xkb-dev libxcb-cursor-dev libxkbcommon-dev libxcb-xinerama0-dev libxkbcommon-x11-dev libstartup-notification0-dev libxcb-randr0-dev libxcb-xrm0 libxcb-xrm-dev libxcb-shape0 libxcb-shape0-dev
```
Install i3-gaps dependences (Ubuntu)

```bash
sudo apt install -y libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev \
libxcb-util0-dev libxcb-icccm4-dev libyajl-dev \
libstartup-notification0-dev libxcb-randr0-dev \
libev-dev libxcb-cursor-dev libxcb-xinerama0-dev \
libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev \
autoconf libxcb-xrm0 libxcb-xrm-dev automake libxcb-shape0-dev
```


Install [LightDM](https://github.com/canonical/lightdm) as a display manager

```bash
sudo shutdown -r now
```

### Actual status

Lockscreen

![Installer 4](./img/screenshot4.png)

Desktop

![Installer 5](./img/screenshot5.png)

## Config i3
Press the "enter" key to generate an i3 configuration file.

![Installer 6](./img/screenshot6.png)

Press the "win" key to select it as the default modifier and press enter again to save the setting.

![Installer 7](./img/screenshot7.png)
## Polybar
```bash
sudo apt install polybar
```
