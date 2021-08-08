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
```bash
sudo apt-get install i3 i3status i3lock dmenu
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