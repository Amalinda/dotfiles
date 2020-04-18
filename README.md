### configurations for i3, i3blocks, dmenu. Not intended to be used by others but, you are welcome to have a look. 
recalling steps to replicate this setup
  I mostly followed the 3 tutorials on   https://www.youtube.com/watch?v=j1I63wGcvU4 . 

### Step 1)  
  install i3 - the window manager   
  install i3status - the default "status bar" in i3, its okay to have it.   
  install i3blocks - a more interesting status bar. I use this.   
  install dmenu - the mandatory application lancher.   
```
sudo apt install i3status i3blocks i3 dmenu
sudo reboot #dmenu requires reboot to kick-in.
```

  upon reboot, chose i3 window manager through log-in screen.   
  you will be served a first time wizard (or run i3-config-wizard in your terminal).  
  opt to create a config file & chose your modkey. I use ALT.   
  
### note: 
it's useful to know that modkey + enter will give you a terminal.     

### Step 2) 
  two config files exist to configure i3 window manager and i3blocks.   
  they should be located in ~/.config/i3/config & ~/.config/i3blocks/config   
  if they don't exist, you can always create them. Their defaults should be at /etc/i3/config & /etc/i3blocks.conf .   
  you may always find my config files in this repo, but its better to configure your own.             
  
#### configure i3 to use i3blocks as status bar. Edit that in to the .config/i3/config as follows: 
  ```
# Start i3bar to display a workspace bar (plus the system information i3status
# finds out, if available)
bar {
        position top
        status_command i3blocks
#       font pango: FontAwesome 10
#       status_command i3status
}
```
  press MODKEY + R to reload the configs to i3    
  
### enable tap-to-click for touchpads
if you did install on a laptop, i3 will not this feature by default. The following will add it in.   
courtesy : https://cravencode.com/post/essentials/enable-tap-to-click-in-i3wm/

```
sudo mkdir -p /etc/X11/xorg.conf.d && sudo tee <<'EOF' /etc/X11/xorg.conf.d/90-touchpad.conf 1> /dev/null
Section "InputClass"
        Identifier "touchpad"
        MatchIsTouchpad "on"
        Driver "libinput"
        Option "Tapping" "on"
EndSection

EOF
```

### Save your time with the following official docs.
  https://i3wm.org/docs/userguide.html is also a nice place.   
  and the rest of videos on  https://www.youtube.com/watch?v=j1I63wGcvU4   
  
