# .dotfiles

This is the setup for my ubuntu 20.04 system.

### Leave Gnome
First install i3 because gnome sucks.

`sudo apt install i3`

Then login to i3 and import `.bashrc` and the `i3` and `i3status` folders from the `.config` folder into the home directory.

Also save the `wallpaper.jpg` file into the `Pictures` folder so that you can look at a dope LOTR background for some Feng Shui.

### Packages to install
```
sudo apt install acpi
sudo apt install arandr
sudo apt install feh
sudo apt install thunar
sudo snap install vlc
sudo snap install spotify
```

### Installing Dropbox

***Make sure you sign into Dropbox on the web first!***

`cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -`

Next, install `nautilus-dropbox` with `sudo apt install nautilus-dropbox`

### Installing Chrome

`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`

`sudo apt install ./google-chrome-stable_current_amd64.deb`

### Installing Sublime
Try:

```
sudo snap install sublime-text
```

or else do this:

```
sudo apt update
sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common curl
curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"
sudo apt install sublime-text
```

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
