# CSU_CS_VNC
A short tutorial detailing how to VNC into the CS department at CSU.




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
