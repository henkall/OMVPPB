# OMVPPB
Openmediavault Plex Plugin backup files. <br>
This is just a place where i put some backup files so it is available to everyone.

This is only a backup of the files I have been using to rewrite the openmediavault-plexmediacenter plugin and a way to repackage the deb again

I Like to share. :P

# Notes

If using OMV-Extras and having Plex reposistory turned on in Openmediavault then skip Step 1 

Step 1.
- Run these two commands in ssh before installing deb
```
echo deb https://downloads.plex.tv/repo/deb/ ./public main | sudo tee -a /etc/apt/sources.list.d/plexrep.list
apt update.
```

Step 2.
- Install the plugin throug the plugin section in the web gui.

# OBS
This plugin is only been tested on a clean install and I don't take any responsiblility for any dataloss you are having.

# Warning
If already using Tautulli from github don't enable Tautulli in this plugin.<br> 
As I said "I don't take any responsiblility for any dataloss you are having"

# Extras 
Only for checking if repository is there:
```
find /etc/apt/ -name *.list | xargs cat | grep  ^[[:space:]]*deb | grep plex
```

Extract backup:
```
tar -zxvf backup.tar.gz
```

Making backup:
```
tar -zcvf backup.tar.gz working
```

Repakaging deb
```
dpkg-deb -Z xz -b oldpack/ newpack/
```
