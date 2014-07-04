Modified home directory, using: `git`, `mr`, `stow` (soon `vcsh`). The stow dir works with symlinks into `~/bin`, `~/etc` and `~/share`. Just some examples there.

```sh
# ~/etc/user-dirs.dirs

XDG_DESKTOP_DIR="$HOME/share/desktop"
XDG_DOWNLOAD_DIR="$HOME/var/tmp/downloads"
XDG_TEMPLATES_DIR="$HOME/share/templates"
XDG_PUBLICSHARE_DIR="$HOME/var/public"
XDG_DOCUMENTS_DIR="$HOME/var/documents"
XDG_MUSIC_DIR="$HOME/var/music"
XDG_PICTURES_DIR="$HOME/var/pictures"
XDG_VIDEOS_DIR="$HOME/var/videos"
```

```bash
# ~/.profile

# [...]

HOME="/home/${USER}"

PATH="/sbin:/usr/sbin:/usr/local/sbin:/usr/games:/usr/local/games:${PATH}"
[ -d "${HOME}/bin" ] && PATH="${HOME}/bin:${PATH}"

MAIL="${HOME}/var/mail/Maildir/system-mailspool"
XDG_CACHE_HOME="${HOME}/var/cache"
XDG_CONFIG_DIRS="/etc/xdg"
XDG_CONFIG_HOME="${HOME}/etc"
XDG_DATA_DIRS="/usr/local/share:/usr/share"
XDG_DATA_HOME="${HOME}/share"
#$XDG_RUNTIME_DIR
X_MAILDIR="${HOME}/var/mail/Maildir"
X_XDG_BACKUPS_DIR="${HOME}/var/backups"
X_XDG_CODE_DIR="${HOME}/var/code"
X_XDG_LOG_HOME="${HOME}/var/log"
X_XDG_MAIL_DIR="${HOME}/var/mail"
X_XDG_TMP_HOME="${HOME}/var/tmp"

[ -f "${XDG_CONFIG_HOME}/user-dirs.dirs" ] && source "${XDG_CONFIG_HOME}/user-dirs.dirs"

export HOME
export MAIL
export PATH
export XDG_CACHE_HOME
export XDG_CONFIG_DIRS
export XDG_CONFIG_HOME
export XDG_DATA_DIRS
export XDG_DATA_HOME
export XDG_DESKTOP_DIR
export XDG_DOCUMENTS_DIR
export XDG_DOWNLOAD_DIR
export XDG_MUSIC_DIR
export XDG_PICTURES_DIR
export XDG_PUBLICSHARE_DIR
export XDG_TEMPLATES_DIR
export XDG_VIDEOS_DIR
export X_MAILDIR
export X_XDG_BACKUPS_DIR
export X_XDG_CODE_DIR
export X_XDG_LOG_HOME
export X_XDG_TMP_HOME
export X_XDG_MAIL_DIR

# [...]

```

```
# $ tree  -a -P "*" -n --noreport -L 20 "$(pwd)" -o tree

/home/user
├── bin
├── .cache
├── .config
├── etc
│   ├── fontconfig
│   └── .git
├── .local
├── share
│   ├── applications
│   ├── desktop
│   ├── desktop-directories
│   ├── .git
│   ├── sounds
│   ├── templates
│   └── themes
├── stow
│   ├── bin
│   │   ├── bin
│   │   ├── gist-pub
│   │   ├── .git
│   │   ├── opt
│   │   └── sbin
│   └── local
│       ├── bash
│       │   ├── .bash_aliases
│       │   ├── .bash_color
│       │   ├── .bash_completion.d
│       │   │   ├── fzf-completion.bash
│       │   │   ├── git.sh
│       │   │   ├── task.sh
│       │   │   ├── tmuxinator.bash
│       │   │   └── tmux.sh
│       │   ├── .bash_function
│       │   ├── .bash_history
│       │   ├── .bash_history_pref
│       │   ├── .bash_integrations
│       │   ├── .bash_logout
│       │   ├── .bash_profile
│       │   ├── .bashrc
│       │   ├── .bash_tab-completion
│       │   └── .profile
│       ├── openbox
│       │   └── etc
│       │       └── openbox
│       │           ├── autostart.sh
│       │           ├── menu.xml
│       │           └── rc.xml
│       └── taskwarrior
│           ├── etc
│           │   └── tasknc
│           │       └── config
│           ├── share
│           │   └── taskwarrior
│           │       └── dark-pastels-256.theme
│           ├── .taskhelmrc
│           ├── .taskopenrc
│           ├── .taskrc
│           └── .taskreport
└── var
    ├── backups
    ├── cache
    ├── cloud
    ├── code
    │   ├── archiv
    │   ├── deb
    │   ├── emacs
    │   ├── fritzbox
    │   ├── java
    │   ├── mozilla
    │   ├── projects
    │   ├── vcs
    │   ├── virtualbox
    │   └── wine
    ├── documents
    ├── log
    │   └── .git
    ├── mail
    ├── music
    ├── pictures
    ├── public
    ├── src
    ├── tmp
    │   └── downloads
    ├── videos
    └── virtualization
```
