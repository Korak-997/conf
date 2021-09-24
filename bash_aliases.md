# Bunch of usefull aliases for more productivity in linux terminal

First you need to run this command to create aliases file

```
$ sudo nano .bash_aliases 
```

Then you can create you aliases inside this file

```bash
  alias ALIAS_NAME = 'COMMAND'
```

After that you need to let Bash reload 

```
$ source .bashrc
```

Some aliases of my own : 

* To open Xampp GUI ( you need to install xampp first )
  ```bash
    alias xmapp='(cd /opt/lampp && sudo ./manager-linux-x64.run)'
  ```
* To Update and Upgrade all apt packages
  ```bash
    alias up_ud='(sudo apt update && sudo apt upgrade -y)'
  ```
