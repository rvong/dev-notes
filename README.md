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

- You choose your AWS availability zone (AZ) by choosing your Subnet group.
- Install tightvncserver over the default vnc4server
- sudo apt-get update && sudo apt-get upgrade
- sudo apt-get install xfce4 xfce4-goodies nautilus (nautilus has recursive search GUI which Thunar does not. xfce4-goodies will install xfce4-terminal, etc.)
- sudo apt-get install tightvncserver
- sudo apt-get install xrdp
- turn off screenservers etc. on startup
