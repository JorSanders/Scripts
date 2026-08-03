# Scripts

These are some non-secret scripts/configs I use locally to develop. Since I tend to break things, or redo my local setup I place them in version control

## Fair warning

I highly recommend not running other people commands blindly on your machine. So I don't expect others to do the same with mine. Which is why the only documentation included; is meant for myself.

## Setup

Run the install script. It adds bin/ and bin/local/ (gitignored,
machine-local scripts) to PATH and sources every file under profile/ and
aliases/ from your shell rc file (~/.zshrc for Zsh, ~/.bashrc for Bash),
see `./install --help`:

```shell
./install
```

## Packages

`packages/` holds the packages I installed by hand, one list per machine,
so I don't have to remember them when I redo a setup. Dependencies and
whatever the base image shipped with are left out.

Regenerate a list on the machine it belongs to:

```shell
create_brewfile     # macOS, writes packages/Brewfile
create_apt_packages # Debian based, writes packages/apt-packages-<flavor>.txt
```

`create_apt_packages` names the file after the machine it detects (`wsl`,
`pi`, or the distribution ID); pass a flavor to write a different one. It
reads the apt history log, so installs older than the oldest log are
missed.

Install a list on a new machine:

```shell
brew bundle install --file=packages/Brewfile
xargs sudo apt install -y < packages/apt-packages-wsl.txt
```
