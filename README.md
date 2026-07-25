# Scripts
These are some non-secret scripts/configs I use locally to develop. Since I tend to break things, or redo my local setup I place them in version control

## Fair warning
I highly recommend not running other people commands blindly on your machine. So I don't expect others to do the same with mine. Which is why the only documentation included; is meant for myself.


## Setup

Run the install script. It adds bin/ and bin/local/ (gitignored,
machine-local scripts) to PATH and sources every file under profile/ and
aliasses/ from your shell rc file (~/.zshrc for zsh, ~/.bashrc for bash),
see `./install --help`:
```shell
./install
```
