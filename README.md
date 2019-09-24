# Rotate Ubuntu Wallpaper
Rotates an ubuntu desktop's wallpaper using jpg files in the Pictures folder.
<img src="https://github.com/edendekker/Rotate_Ubuntu_Wallpaper/blob/master/wallpaper_rotator.jpeg" />

## Limitations
- Can only be executed upon user session startup and not crontab
 - Maybe i can create a systemd install script that runs at startup for the current user
- Hardcoded to search for jpg files in the /home/user/Pictures folder

## Motivation
I just happen to like transparent windows and forever changing backgrounds.

## Installation
### Unix
Download to your machine.
```
apt install wget
wget "https://github.com/edendekker/Rotate_Ubuntu_Wallpaper/archive/master.zip"
```
If you have git on your development machine.
```
git clone https://github.com/edendekker/Rotate_Ubuntu_Wallpaper.git
```
Install in you home directory and make sure you, the owner can execute it.
```
chmod 750 rotate_ubuntu_wallpaper
ls -lrtah
-rwxr-x---  1 ubuntu    ubuntu     805 Sep 23 19:19 rotate_ubuntu_wallpaper
```
Add startup entry in your home directory. Change 60 to how many seconds you want to wait before it changes to another picture.
```
vi .bashrc
...
...
nohup /home/e/rotate_ubuntu_wallpaper 60 &>/dev/null &
```
### Windows 
Sorry.
