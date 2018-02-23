# CSU_CS_VNC
A short tutorial detailing how to VNC into the CS department at CSU.

I use chrome apps to ssh and vnc so that I can access everything with a chrome book but feel free to use any programs you like. The chrome apps need almost no configuration. (See links below)

[Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo?hl=en) 

[VNC® Viewer for Google Chrome™](https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla/related?hl=en) 



First ssh into a CS dept machine using 
```
nano /s/bach/k/under/cwiegand/.vnc/xstartup
```

```
!/bin/sh

#unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
#exec /etc/X11/xinit/xinitrc

startxfce4 &
```

```
CTRL-X
Y
ENTER
```
