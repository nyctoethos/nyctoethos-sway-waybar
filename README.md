# nyctoethos-sway-waybar
In the future ill have different statusbars so be on the look out for those!
Not yet finished configuring this is just here for a backup mainly but can also be used for others if they like it


preview of my waybar
https://github.com/user-attachments/assets/5b120bd4-84d2-4008-8edc-9b846eea3e8a

installation
Im gonna add a installation here for waybar and sway because i dont want any linux newb feeling left out! (just read the documentation please)

Step one
Install waybar using your distros packager 
Example 
arch:
pacman -S waybar
fedora: 
dnf install waybar

step two
From here execute waybar in the terminal to make sure it works
then go into your .config so .config/sway/config replace 
...
bar {
    position top

    # When the status_command prints a new line to stdout, swaybar updates.
    # The default just shows the current date and time.
    status_command while date +'%Y-%m-%d %X'; do sleep 1; done

    colors {
        statusline #ffffff
        background #323232
        inactive_workspace #32323200 #32323200 #5c5c5c
    }
}
...
with 

bar {
 swaybar_command waybar
}



step three
after waybar is installed and set in .config/sway go to your .config and mkdir ~/.config/waybar/
then cd into /etc/xdg/waybar/ the default config will be located there!
if not... use the config that i made!
while in /etc/xdg/waybar/ do cp config.jsonc ~/.config/waybar and again with the style.css

for easy copy%paste 
cp config.jsonc ~/.config/waybar
cp style.css ~/.config/waybar


step four 
replace these two files
style.css 
config.jsonc with my configs!
linked here




