# OMVPPB
Openmediavault Plex Plugin Backup files. <br>
This is just a place where i put some backup files so it is awailible to everyone.

I Like to share. :P

# Notes

If using OMV-Extras and having Plex reposistory turned on in Openmediavault then skip Step 1 

Step 1
Run these two commands in ssh before installing deb
```
echo deb https://downloads.plex.tv/repo/deb/ ./public main | sudo tee -a /etc/apt/sources.list.d/plexrep.list
apt update.
```

Step 2
Install the pluging throug the web gui in the plugin section.

# OBS
This plugin is only been tested on a clean install and I don't take any responsiblility for any dataloss you are having.

# Ekstras 
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
