# customUbuntuISO

# Steps to reproduce

# in cubic shell



```bash

apt update

apt install firefox -y



mkdir temp

cd temp



# use the copy feature to copy all files



# custom branding

cp logo.png /usr/share/plymouth/ubuntu-logo.png

cp logo.png /usr/share/plymouth/themes/spinner/bgrt-fallback.png

cp watermark.png /usr/share/plymouth/themes/spinner/watermark.png



# change default wallpaper

cp /usr/share/backgrounds/warty-final-ubuntu.png /usr/share/backgrounds/warty-final-ubuntu-old.png

cp wallpaper.png /usr/share/backgrounds/warty-final-ubuntu.png



# make firefox open page on startup

mkdir /etc/skel/startpage

cp index.html /etc/skel/startpage

cp style.css /etc/skel/startpage

cp script.js /etc/skel/startpage



cd /etc/skel/

mkdir -p .conf/autostart

nano .conf/autostart/startup.desktop



# paste this into that file

[Desktop Entry]

Name=Firefox_Startpage

Type=Application

Exec=sh -c "firefox /home/$USER/startpage/index.html; $SHELL"

Terminal=false

# end of copy



# and done

# - replaced branding

# - changed wallpaper

# - added firefox to startup and open that page```
