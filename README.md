# st - simple terminal
st is a simple terminal emulator for X which sucks less.


## Bindings
### Scrolling
```
          MouseWheel  -  move by line
  Shift + MouseWheel  -  move by 3 lines
Control + MouseWheel  -  move by page

        Alt + {k, j}  -  move {up, down} by line
Shift + Alt + {k, j}  -  move {up, down} by 3 lines
        Alt + {u, d}  -  move {up, down} by page
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

