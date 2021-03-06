# FIRST COMMANDS
## Update - Upgrade - Clean - Autoremove

```sh
$ sudo apt update -y && sudo apt upgrade -y && sudo apt autoremove -y && sudo apt install -f -y && sudo apt auto-clean -y
```

## Canonical software


Open "software and updates" and then "other software". Click and install.

## Language

In *settings/regions&languages* select *"manage installed languages and install them completely"*.

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

## OpenCV libs

```sh
$ sudo apt update && apt install -y libsm6 libxext6 libxrender1
```

## Radeontop (gpu utilization, after install amdgpu)

```sh
$ sudo apt install radeontop -y
```

## Nginx (proxy server)

```sh
$ sudo apt install nginx -y
```

## Synaptic Gdebi
#### Install:

```sh
$ sudo apt install synaptic gdebi -y
```

#### Synaptic search box:

```sh
$ sudo apt install apt-xapian-index -y && sudo update-apt-xapian-index -vf
```

#### FFmpeg:

Search, apply and install.

## Gnome Tweak Tool
#### Install:

```sh
$ sudo add-apt-repository universe -y
$ sudo apt install gnome-tweak-tool -y
```

#### Gnome Shell extensions, first:

```sh
$ sudo apt search gnome-shell-extension -y
$ sudo apt install  gnome-shell-extension-gsconnect -y 
$ sudo apt install $(apt search gnome-shell-extension | grep ^gnome | cut -d / -f1) -y
$ sudo apt install chrome-gnome-shell -y
$ sudo apt-get install adapta-gtk-theme -y 
$ sudo apt install arc-theme papirus-icon-theme -y
```

#### Second:

[User themes](https://extensions.gnome.org/extension/19/user-themes/)

Switch to **ON** and click *install*.

#### Restarts GNOME Shell:

<kbd>Alt</kbd> + <kbd>F2</kbd><br>
<kbd>r</kbd> + <kbd>ENTER</kbd>

#### Recommended configuration:

```sh
- Adwaita-dark
- Redglass
- Papirus-Dark
- Yaru-dark
- Yaru
```

## Sublime text (IDE, with Ubuntu software)

Search and install.

## Opera (browser, with Ubuntu software)

Search and install.

## VLC (media player, with Ubuntu software)

Search and install.

## Postman (API development)

Search and install.

## Visual Studio (IDE, with ubuntu software)

Search and install.

#### Extension: 

- Prettier - Code formatter. (Prettier)
- Python. (Microsoft)
- Django. (Baptiste Darthenay)
- React Native Tools. (Microsoft)
- ES7 React/Redux/GraphQL/React-Native snippets. (Dsznajder)
- JavaScript (ES6) code snippets. (Charalampos Karypidis) 

## GIT

```sh
$ sudo apt install git -y
```

## MySQL (database management)

```sh
$ sudo apt install mysql-server -y
```

## ZSH (powerful command interpreter, shell. As SUDO!!, this will install zsh on both user and sudo)

```sh
$ sudo apt install zsh -y
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
$ cd
$ sudo vim .zshrc
```

#### [.zshrc]

```sh
export ZSH="/opt/oh-my-zsh/.oh-my-zsh"
ZSH_THEME="essembeh"
```

#### Then ..

```sh
$ sudo mkdir /opt/oh-my-zsh
$ sudo cp -r /root/.oh-my-zsh /opt/oh-my-zsh
$ cp -r /root/.zshrc /home/<username>/
$ chsh --shell=`which zsh` ${<username>}
```

#### Two plugins:

```sh
$ sudo git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
$ sudo git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

#### [.zshrc]

For users and sudo.

```sh
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

#### Apply changes:

```sh
$ source $ZSH/oh-my-zsh.sh
```

## Curl (command line tool)

```sh
$ sudo apt install curl -y
```

## Anaconda (python distribution platform, As SUDO!!)

```sh
$ curl -O https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh
$ sudo bash ./Anaconda3-2020.11-Linux-x86_64.sh
```

<kbd>ENTER</kbd><br>

```sh
yes
```

#### Path:

```sh
/opt/anaconda3
```

#### Do you wish the installer to initialize Anaconda3:

```sh
yes # (Important)
```

#### Conda update:

Reset the terminal first.

```sh
$ conda update -n base -c defaults conda -y
```

#### To access Conda commands with any user, edit environment:

```sh
$ sudo vim /etc/environment
```

#### [environmnet]

```sh
PATH=/opt/anaconda3/bin:$PATH
```

Restart PC.

#### Create an env with some libs: (python 3.8)

```sh
$ conda create -n <envname> mysqlclient python==3.8 -y
$ source activate <envname>
$ pip install appdirs bokeh boto boto3 cython django django-allauth django-cors-headers django-filter django-rest-auth djangorestframework dtw==1.3.3 ec2-metadata gensim gunicorn imgaug ipykernel jupyter_console jupyter_contrib_nbextensions jupyter-themer jupyter_dashboards jupyter_full_width jupyterhub jupyterlab keras marshmallow matplotlib mysql-connector-python nltk numpy opencv-python openpyxl pandas pdf2image pypng regex scipy stop-words symspellpy tensorflow==2.4.0rc4 tqdm wazeroutecalculator wfdb xlrd xlwt
```