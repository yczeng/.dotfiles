# .dotfiles

This is the setup for my ubuntu 20.04 system.

### i3
First install i3 because gnome sucks.

`sudo apt instal i3`

### Packages to install
- `sudo apt install acpi`
- `sudo apt install arandr`
- `sudo apt install feh`

### Installing Dropbox

***Make sure you sign into Dropbox on the web first!***

`cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -`

Next, install `nautilus-dropbox` with `sudo apt install nautilus-dropbox`

### Installing Chrome

`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`

`sudo apt install ./google-chrome-stable_current_amd64.deb`

### Natural Scrolling
I like natural scrolling. Change `/usr/share/X11/xorg.conf.d/40-libinput.conf`

```
# Match on all types of devices but joysticks
Section "InputClass"
        Identifier "libinput pointer catchall"
        MatchIsPointer "on"
        MatchDevicePath "/dev/input/event*"
        Driver "libinput"
        Option "NaturalScrolling" "True"
EndSection
```
