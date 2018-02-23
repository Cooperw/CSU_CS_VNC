# CSU_CS_VNC
A short tutorial detailing how to VNC into the CS department at CSU.

I use chrome apps to ssh and vnc so that I can access everything with a chrome book but feel free to use any programs you like. The chrome apps need almost no configuration. (See links below)

[Secure Shell](https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo?hl=en) 

[VNC® Viewer for Google Chrome™](https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla/related?hl=en) 



First ssh into a CS dept machine using Secure Shell. I will be using the computer named "Cooper" in my examples but you may use any CS machine. To find the name of a machine look for a white label on the front of the machine next time you are in the CSB.
```
Userame: {your cs username}
Hostname: cooper.cs.colostate.edu
```

If you have never used vnc before you may need to modify the startup file.
First make a backup copy of your old startup file and then open up the origional file.
```
cp /s/bach/k/under/{your cs username}/.vnc/xstartup  /s/bach/k/under/{your cs username}/.vnc/xstartup.old
nano /s/bach/k/under/{your cs username}/.vnc/xstartup
```

Replace everything in the new file with the text below.
```
!/bin/sh

#unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS
#exec /etc/X11/xinit/xinitrc

startxfce4 &
```

Press CTRL-X then Y then ENTER to save your changes
```
CTRL-X
Y
ENTER
```

Now start the VNC server that you will eventually be connecting to. The 5 below specifies the display number to use. It doesn't matter too much which one you use, I generally just grab 5. Only one student may occupy a display at a time.
```
vncserver :5
```
*use vncserver -kill :5 to stop the server when you are done

Your halfway done! Now switch over to your regular personal desktop.
When off campus I sometimes use Pulse Secure to establish a vpn with CSU.

Once you are ready to connect to the VNC server open up [VNC® Viewer for Google Chrome™](https://chrome.google.com/webstore/detail/vnc%C2%AE-viewer-for-google-ch/iabmpiboiopbgfabjmgeedhcmjenhbla/related?hl=en).
Type your computer address into the address box.
```
Address: cooper.cs.colostate.edu:5
Picture Quality: Automatic
```

Then click connect and you may get a warning about an uncrypted connection. Click Connect again.
Enter you CS password.
You should now be able to see the familiar CS desktop. 
Enjoy and don't forget to run the -kill command when you are done.
