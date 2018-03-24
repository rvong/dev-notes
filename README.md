# dev-notes

## Remote Desktop from Win/Mac to Linux
- Bitvise client for Windows (it will accept your .pem file client key import, even though the UI dropdown list doesn't say so)
- Remote Desktop client for Mac
- xrdp-vnc for Linux (make sure you set the passwd correctly
- Couldn't get x11rdp to work. And frankly, if they cannot compile and distribute a Debian package themselves, they do not want anyone using it.

```
xrdp_mm_process_login_response: login failed
```
Usually just means the wrong password for the account you're attempting to login with.

- Install tightvncserver over the default vnc4server
- sudo apt-get update && sudo apt-get upgrade
- sudo apt-get install xfce4 xfce4-goodies nautilus (nautilus has recursive search GUI which Thunar does not. xfce4-goodies will install xfce4-terminal, etc.)
- sudo apt-get install ~~tightvncserver~~ go to tigerVnc website and install the binary. tightvncserver doesn't support "Display" option because of missing RandR extension (check this with `Xrandr --version`)
- sudo apt-get install xrdp
- turn off screenservers etc. on startup

## AWS
- Create a snapshot of your ec2 volume before you screw everything up. This is the only way you can restore.
- You choose your AWS availability zone (AZ) by choosing your Subnet group.
- Create a Security Group for firewall-ing.

## Remote Desktop Client to Check for Linux
- NoMachine, FreeNX, X2Go
- Splashtop
- Teamviewer

## Best Linux Distros
- Manjaro XFCE
- Manjaro KDE
- pacman -S(yus) <arg>
- Reasonable choice https://www.linuxliteos.com/
- Elementary - Pretty and unusable.
- Deepin - Pretty and unusable.

## Distros to try
- MX Linux using xfce4 https://mxlinux.org/ Seems like Manjaro, except with apt-get.

## Strange
- Solus https://solus-project.com/ Wacky pkg manager (eopkg)

## Distro Notes
- Ubuntu: Debian, apt-get/aptitude, PPAs for community packages
- Manjaro: Arch, pacman, AUR for community packages
- CentOS/RedHat/AmazonLinux: Fedora, yum, basically no real support community packages. OpenSUSE build service? Has nothing in it. Fedora repos? Probably nothing in it, but I didn't check.
- Don't bother with anything else.
- https://distrowatch.com/

## WM Notes
- XFCE - Stable, light, least bugs.
- KDE - Nicest. Most buggy.
- Cinnamon - Usable and buggy.
