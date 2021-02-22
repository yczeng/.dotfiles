# .dotfiles
### Packages to install
- `sudo apt install acpi`
- `sudo apt install arandr`
- `sudo apt install feh`

### Installing Dropbox

***Make sure you sign into Dropbox on the web first!***

`cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -`

Next, install `nautilus-dropbox` with `sudo apt install nautilus-dropbox`

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
