# My Configs

## Auto Mounting Drives

use gnome-disks

## Application Launcher Shortcuts Path

`~/.local/share/applications`

## Changing Login Screen Background

```
To change the login screen wallpaper go to
/usr/share/gnome-shell/theme >> and edit >> gdm3.css
find lockDialogGroup
```

## Connecting to another linux machine with x2x

`ssh -X [computer name]@[ip gateway] -l [user name] x2x -east -to :0.0` 

## Editing unity animation with Dconf (ubuntu 16.04)

```
open dconf
com > canonical > unity
minimize-speed-threshold 0 - 100
minimize-slow-duration
```

## Increasing File Monitoring Amount of System Files

Modify the number of system monitoring files

in Ubuntu

`sudo gedit /etc/sysctl.conf`

Add a line at the bottom

`fs.inotify.max_user_watches=524288`

Then save and exit!

`sudo sysctl -p`

to check it

> [Stackoverflow post URL](https://stackoverflow.com/questions/55763428/react-native-error-enospc-system-limit-for-number-of-file-watchers-reached)

## Mouse Sensivity

`xset m default`

## Changing nautilus search to typeahed (tested in ubuntu 18.04)

Type Ahead search was removed completely from Nautilus, aka GNOME Files, since Artful. Luckily, there is a patch on GitHub that adds this functionality back to Nautilus 3.26.3, the version installed by default in Ubuntu 18.04. Now if you want to apply the patch and build Nautilus from source, go ahead, but there is a guy that did the job for us and provided a PPA to install the patched Nautilus directly:

`sudo add-apt-repository ppa:lubomir-brindza/nautilus-typeahead`

Then upgrade using

`sudo apt full-upgrade` and kill Files `nautilus -q`

> [Stackoverflow post URL](https://askubuntu.com/questions/1037732/type-ahead-search-using-nautilus-on-ubuntu-18-04)

## Using Xbindkeys for my logitech mx master

it opens the xbindkeysrc config file

`xdg-open .xbindkeysrc`

Mouse buttons | Action detected as
------- | -------
Left button | button 1
Press to wheel | button 2
Right button | button 3
Scroll wheel up | button 4
Scroll wheel down | button 5
Press "i" button under wheel undetectable in linux | 
Scroll hor_wheel right (up) | button 6
Scroll hor_wheel left (down) | button 7
Side-bottom button | button 8
Side-top button | button 9
Thumb button | Ctrl+Alt+Tab

>[ArchWiki URL](https://wiki.archlinux.org/index.php/Logitech_MX_Master)