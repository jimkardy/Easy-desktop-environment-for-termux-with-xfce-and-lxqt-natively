# Easy-desktop-environment-for-termux-with-xfce-and-lxqt-natively
## install it with one click here :
```bash
curl -sSL -o txgui https://github.com/jimkardy/Easy-desktop-environment-for-termux-with-xfce-and-lxqt-natively/releases/latest/download/txgui.txt && chmod +x txgui && ./txgui help
 ```


TXGUI - a full desktop on your phone
  (XFCE or LXQt, seen over VNC)

  FIRST TIME
    ./txgui install        installs the desktop
                           (asks which one you want)

  EVERYDAY USE
    ./txgui start          starts desktop + VNC
    ./txgui stop           stops desktop + VNC
    ./txgui status         shows what is running

  WHICH DESKTOP
    ./txgui start xfce       start the xfce desktop
    ./txgui start lxqt       start the lxqt desktop
    ./txgui stop xfce        stop xfce + VNC
    ./txgui stop lxqt        stop lxqt + VNC
    (plain start/stop use
     the desktop you installed)

  NOTES
    * The VNC password is asked
      once, at first start.
    * Connect any VNC app to:
      <your-ip>:5901
    * Answers "y" to everything,
      so it can run unattended.
## it doesn't contains any remove/delete subcommands, but here's how to delete the CLI and the desktop environment's if needed:

### 1 the cli/script 

``` bash 
rm txgui 
```
### 2 the xfce desktop

``` bash 
apt remove xfce4
```

### 3 the lxqt desktop

``` bash 
apt remove lxqt
```

## additionally the vnc server is necessarily

``` bash 
apt remove tigervnc
```

