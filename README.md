# .dotfiles
### Packages to install
- `sudo apt-get install acpi`
- `sudo apt-get install arandr`
- `sudo apt-get install feh`

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
