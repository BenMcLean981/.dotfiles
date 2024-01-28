# .dotfiles

This is my repository for storing my .dotfiles. When I setup a new PC with Linux for myself, I use these files. This assumes that [VSCode](https://code.visualstudio.com/) has been installed.

## Setup

All setup will assume you have cloned this repo to `~/.dotfiles`.

### Create symbolic links:

```
ln -s ~/.dotfiles/.bashrc ~/.bashrc
ln -s ~/.dotfiles/.gitconfig ~/.gitconfig
ln -s ~/.dotfiles/.git-prompt.sh ~/.git-prompt.sh
ln -s ~/.dotfiles/alacritty.yml ~/.config/alacritty/alacritty.yml
```

### Install DNF Packages

```
dnf install $(cat ~/packages.txt)
```

### Adding DNF Packages

View all installed packages:

```
dnf repoquery --userinstalled
```

Search for currently installed package:

```
dnf repoquery --userinstalled | grep "[name]"
```

Simply add a line to the packages.txt.