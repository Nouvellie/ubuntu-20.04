# FIRST COMMANDS
## Update - Upgrade - Clean - Autoremove

```sh
$ sudo apt update -y && sudo apt upgrade -y && sudo apt autoremove -y && sudo apt install -f -y && sudo apt auto-clean -y
```

## Canonical software


Open "software and updates" and then "other software". Click and install.

## Htop (ncurses-based process viewer)

```sh
$ sudo apt install htop -y
```

## Vim (text editor)

```sh
$ sudo apt install vim -y
```

## Inxi (server information)

```sh
$ sudo apt install inxi -y
```

## Ncdu (ncurses disk usage analyzer)

```sh
$ sudo apt install ncdu -y
```

## Radeontop (gpu utilization, after install amdgpu)

```sh
$ sudo apt install radeontop -y
```

## Sublime text (IDE, with Ubuntu software)

Search and install.

## Opera (browser, with Ubuntu software)

Search and install.

## VLC (media player, with Ubuntu software)

Search and install.

## GIT

```sh
$ sudo apt install git -y
```

## MySQL (database management)

```sh
$ sudo apt install mysql-server -y
```

## ZSH (powerful command interpreter, shell. As SUDO!!)

```sh
$ sudo apt install zsh -y
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
$ sudo mkdir /opt/oh-my-zsh
$ sudo cp -r /root/.oh-my-zsh /opt/oh-my-zsh
$ cp -r /root/.zshrc /home/<username>/
$ chsh --shell=`which zsh` ${nouvellie}
```

Check /root/.oh-my-zsh/

## Curl (command line tool)

```sh
$ sudo apt install curl -y
```