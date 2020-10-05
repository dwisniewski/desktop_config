# desktop_config
Configuration of i3wm and others


# Requirements:
sudo pacman -S [...]
- i3 (should provide: i3-wm, dunst (dmenu notification), i3lock (lock screen), i3status (status line), suckless-tools (simple commands for minimalistic wm))
- picom - provides desktop effects
- hsetroot - provides wallpaper handling
- rxvt-unicode - terminal emulator
- xsel - X clipboard in terminal (alt+c to copy / alt+v to paste)
- rofi - program launcher, replaces dmenu
- fonts-noto - fonts
- fonts-mplus - fonts
- xsettingsd - improved fonts rendering
- lxappearance - change GTK themes
- scrot - screenshots
- viewnior - image viewer


`i3config` should be placed in `~/.config/i3/config`


# picom configuration
once installed, make sure that NVidia drivers are also installed (inxi -G -- check drivers, sudo mhwd -a pci nonfree 0300 -- install drivers)
`mkdir ~/.config/picom`
`cp /etc/xdg/picom.conf ~/.config/picom/`

Autorun picom from i3:
Add `exec picom &` to `~/.config/i3/config`

# Urxvt configuration
Copy `config/dotXresources` to `~/.Xresources` to set terminal fonts and colors
Copy `config/dotXdefaults` to `~/.Xdefaults` to set terminal opacity
