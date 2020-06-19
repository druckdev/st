# st - simple terminal
st is a simple terminal emulator for X which sucks less.


## About this fork
### Patches applied
 - [st-alpha-0.8.2.diff](https://st.suckless.org/patches/alpha/)
 - [st-anysize-0.8.1.diff](https://st.suckless.org/patches/anysize/)
 - [st-desktopentry-0.8.2.diff](https://st.suckless.org/patches/desktopentry/)
 - [st-hidecursor-0.8.3.diff](https://st.suckless.org/patches/hidecursor/)
 - [st-scrollback-20200419-72e3f6c.diff](https://st.suckless.org/patches/scrollback/)
 - [st-scrollback-mouse-20191024-a2c479c.diff](https://st.suckless.org/patches/scrollback/)
 - [st-scrollback-mouse-altscreen-20200416-5703aa0.diff](https://st.suckless.org/patches/scrollback/)
 - [st-w3m-0.8.3.diff](https://st.suckless.org/patches/w3m/)
 - [st-workingdir-20200317-51e19ea.diff](https://st.suckless.org/patches/workingdir/)

### Bindings
#### Scrolling
```
          MouseWheel  -  move by line
  Shift + MouseWheel  -  move by 3 lines
Control + MouseWheel  -  move by page

        Alt + {k, j}  -  move {up, down} by line
Shift + Alt + {k, j}  -  move {up, down} by 3 lines
        Alt + {u, d}  -  move {up, down} by page
```

### Upstream
To pull changes from upstream:
```
if not already done:
$ git remote add upstream 'https://git.suckless.org/st'

$ git fetch upstream
$ git checkout custom
$ git merge upstream/master
```


## Requirements
In order to build st you need the Xlib header files.\
For the transparency to work you need a composite manager (e.g. picom,
xcompmgr).


## Installation
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install


## Running st
If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -sx st.info

See the man page for additional details.

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.

