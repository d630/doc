Modified home directory, using: `git`, `mr`, `stow` (soon `vcsh`). The stow dir works with symlinks into `~/bin`, `~/etc`, `~/share` and `~/var`.

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

```sh
# ~/.profile.d/11-evars-user.sh

[ -f "${XDG_CONFIG_HOME}/vars.priv" ]  && . "${XDG_CONFIG_HOME}/vars.priv"

X_MAILDIR="${HOME}/var/mail/Maildir"
X_XCLIENT=openbox
X_XDG_BACKUPS_DIR="${HOME}/var/backups"
X_XDG_CODE_DIR="${HOME}/var/code"
X_XDG_LIB_DIR="${HOME}/var/lib"
X_XDG_LOG_HOME="${HOME}/var/log"
X_XDG_MAIL_DIR="${HOME}/var/mail"
X_XDG_SOURCE_DIR="${HOME}/src"
X_XDG_TMP_HOME="${HOME}/var/tmp"

# [...]
```

```
# $ tree  -a -P "*" -n --noreport -L 20 --charset=ascii "$PWD"

/home/user
|-- bin
|-- .cache
|-- .config
|-- etc
|   `-- .git
|-- .local
|-- share
|   |-- applications
|   |-- cert
|   |-- desktop
|   |-- desktop-directories
|   |-- fonts
|   |-- .git
|   |-- gvfs-metadata
|   |-- sounds
|   |-- templates
|   |-- themes
|   |-- Trash
|   `-- recently-used.xbel
|-- src
|-- stow
|   |-- bin
|   |   |-- bin
|   |   |-- gist-pub
|   |   |-- .git
|   |   |-- opt
|   |   `-- sbin
|   `-- local
|       |-- bash
|       |   |-- .bash_completion.d
|       |   |   |-- fzf-completion.bash
|       |   |   |-- git.sh
|       |   |   |-- git-prompt.sh
|       |   |   `-- task.sh
|       |   |-- .bashrc.d
|       |   |   |-- alias.sh
|       |   |   |-- applications.sh
|       |   |   |-- color.sh
|       |   |   |-- completion.sh
|       |   |   |-- function.sh
|       |   |   `-- history.sh
|       |   |-- .bash_history
|       |   |-- .bash_logout
|       |   |-- .bash_profile
|       |   `-- .bashrc
|       |-- .git
|       |-- .gitignore
|       |-- openbox
|       |   `-- etc
|       |       `-- openbox
|       |           |-- menu.xml
|       |           |-- rc.xml
|       |           |-- rc-applications.xml
|       |           |-- rc-desktops.xml
|       |           |-- rc-dock.xml
|       |           |-- rc-focus.xml
|       |           |-- rc-keyboard.xml
|       |           |-- rc-margins.xml
|       |           |-- rc-menu.xml
|       |           |-- rc-mouse.xml
|       |           |-- rc-placement.xml
|       |           |-- rc-resistance.xml
|       |           |-- rc-resize.xml
|       |           `-- rc-theme.xml
|       `-- taskwarrior
|           |-- etc
|           |   `-- tasknc
|           |       `-- config
|           |-- var
|           |   `-- lib
|           |       `-- taskwarrior
|           |           `-- dark-pastels-256.theme
|           |-- .taskhelmrc
|           |-- .taskopenrc
|           |-- .taskrc
|           `-- .taskreport
`-- var
    |-- backups
    |-- cache
    |-- cloud
    |-- code
    |   |-- archiv
    |   |-- deb
    |   |-- emacs
    |   |-- fritzbox
    |   |-- java
    |   |-- mozilla
    |   |-- projects
    |   |-- vcs
    |   |-- virtualbox
    |   `-- wine
    |-- documents
    |-- lib
    |-- log
    |   `-- .git
    |-- mail
    |-- music
    |-- pictures
    |-- public
    |-- tmp
    |   `-- downloads
    |-- videos
    `-- virtualization
```
