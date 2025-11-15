# check if port is availabe or already in use
sudo ss -tuln | grep :80
sudo ss -tulnp4 | awk '!seen[$5]++'


# Stop Process
pgrep dmenu



# Find


find ~ -type f -name ".env"


find . -type d -name "__pycache__" -print
find . -type d -name "__pycache__" -exec rm -r {} +



tmux

split screen vertical
Ctrl+b then %


Ctrl+b then o

Ctrl+b then ← →

# File Manager: Yazi
yazi




# iptables

sudo iptables-save > iptab
vim iptab
sudo iptables-restore < iptab






# Tmux

`Ctrl+b` followed by `s`. tabbing between sessions

Ctrl+b` (backtick)














whoami
ifconfig
sshd


#

Open Home Filenamager	Super (Windows Key) + E	Opens the file explorer (Nautilus on GNOME).



l for ls -l



# Setup 

```
bash install.sh
```




# Unistall

```
bash uninstall.sh
```



## see all available shortcuts and set values:

```
gsettings list-recursively org.gnome.settings-daemon.plugins.media-keys
```


# Other

chmod +x /home/user/Nextcloud/PATH/utils/yt.py

sudo ln -s /home/user/Nextcloud/PATH/utils/yt.py /usr/local/bin/yt

sudo rm /usr/local/bin/yt




#

nano ~/bin/g

#!/bin/bash
git add . && git commit -m "+" && git push

chmod +x ~/bin/g
export PATH="$HOME/bin:$PATH"
source ~/.bashrc 



# KDE Send Files over local Network.

kdeconnect-cli --list-devices

kdeconnect-cli --device a1b2c3d4e5f6g7h8 --send /path/to/your/file.txt











# ZSH
Extensions:




# fish
nice for quick edits but not compatible with posix




# Bash

|Keys|Description|
|--|--|
|Ctrl + R |reverse search|

