configurations for i3, i3blocks, dmenu. Not intended to be used by others but, you are welcome to have a look. 
recaling basic steps to replicate this setup

Step 1)  
install i3 - the window manager
install i3status - the default "status bar" in i3
install i3blocks - a more customisable status bar. I use this.    
sudo apt install i3status i3lock i3

Step 2) 
two config files exist to configure i3 window manager and i3blocks
they are located in ~/.config/i3/config & ~/.config/i3blocks/config
if they don't exist, they can be created 
just find the 2 config files from my github replace your defaults.          
my i3 config will use i3blocks as status bar.     
press MODKEY + R to reload the configs     
its better to offer a restart upon the first install for dmenu to kick in.
