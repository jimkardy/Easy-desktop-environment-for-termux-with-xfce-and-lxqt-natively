# Easy-desktop-environment-for-termux-with-xfce-and-lxqt-natively
## install it with one click here :
```bash
curl -sSL -o txgui https://github.com/jimkardy/txgui/releases/latest/download/txgui.txt && chmod +x txgui && ./txgui help
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

## for people that hate scripts, try manually here:


``` bash 
apt update && apt upgrade -y
```


``` bash 
pkg install x11-repo
```

``` bash 
apt install xfce4 tigervnc xfce4-terminal chromium
```

``` bash 
nano ~/.bashrc
```

``` bash 
vncserver :1 -localhost no -interface 0.0.0.0
export DISPLAY=":1"
startxfce4

```
then restart termux.

## This method is not recommended, use the script instead. it's easyer and effortless.

## what vnc app should you use ? 

open play store 

search for avnc 

download it 

use your local IP and port e.g 

127.0.0.1:5901


### good luck! you now got a mini PC inside your phone at a touch of a finger :) 


## this script is intended for older 32 bit devices to give them a new purpose.

i also recommend doing

``` bash 
apt install synaptic
```
