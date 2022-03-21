# Scripts
These are some non-secret scripts/configs I use locally to develop. Since I tend to break things, or redo my local setup I place them in version control

## Fair warning
I highly recommend not running other people commands blindly on your machine. So I don't expect others to do the same with mine. Which is why the only documentation included; is meant for myself.


## Setup

### .bashrc
Add the following to your .bashrc
```shell
# Jor bin in PATH
export PATH="$HOME/Projects/Scripts/bin:$PATH"

# Jor .profile
for f in  $HOME/Projects/Scripts/profile/*; do
  . "$f"
done

# Jor aliasses
for f in  $HOME/Projects/Scripts/aliasses/*; do
  . "$f"
done
```

### Config
```shell
mkdir -p ~/.ssh
cp config/ssh/config ~/.ssh/config
chmod 600 ~/.ssh/config
```
