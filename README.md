# Scripts
These are some non-secret scripts/configs I use locally to develop. Since I tend to break things, or redo my local setup I place them in version control

## Fair warning
I highly recommend not running other people commandos blindly on your machine. So I don't expect others to do the same with mine. Which is why the only documentation included; is only for myself.

## Setup

### profile
Add the following to your .bashrc
```shell
for f in  /mnt/c/Users/Jor/Projects/Scripts/profile/*; do
  . "$f" 
done
```

### Bin
Add the following to your .bashrc
```shell
export PATH="$WINHOME/Projects/Scripts/bin:$PATH"
```

### Aliasses
Add the following to your .bashrc
```shell
for f in  /mnt/c/Users/Jor/Projects/Scripts/aliasses/*; do
  . "$f" 
done
```

### Config
```shell
mkdir -p ~/.ssh/config
cp config/ssh/config ~/.ssh/config
chmod 600 ~/.ssh/config 
```