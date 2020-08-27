# st - simple terminal
st is a simple terminal emulator for X which sucks less.


## About this fork
### Patches applied
 - [alpha](https://st.suckless.org/patches/alpha/)
 ([0.8.2](https://st.suckless.org/patches/alpha/st-alpha-0.8.2.diff))
 - [anysize](https://st.suckless.org/patches/anysize/)
 ([0.8.1](https://st.suckless.org/patches/anysize/st-anysize-0.8.1.diff))
 - [desktopentry](https://st.suckless.org/patches/desktopentry/)
 ([0.8.2](https://st.suckless.org/patches/desktopentry/st-desktopentry-0.8.2.diff))
 - [hidecursor](https://st.suckless.org/patches/hidecursor/)
 ([0.8.3](https://st.suckless.org/patches/hidecursor/st-hidecursor-0.8.3.diff))
 - [w3m](https://st.suckless.org/patches/w3m/)
 ([0.8.3](https://st.suckless.org/patches/w3m/st-w3m-0.8.3.diff))
 - [workingdir](https://st.suckless.org/patches/workingdir/)
 ([20200317](https://st.suckless.org/patches/workingdir/st-workingdir-20200317-51e19ea.diff))

### Upstream
To pull changes from upstream:
```
if not already done:
$ git remote add upstream 'https://git.suckless.org/st'

$ git fetch upstream
$ git checkout custom
$ git merge upstream/master

To push the upstream tags:
$ git push origin --tags
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

