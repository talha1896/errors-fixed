# errors fixed

This repo contain some files and solutions that i faced using linux.So, instead of searching same working solution, i decided to make this repository.
### xbacklight no output device
This error is when i try to adjust brightness with xbacklight of xorg,it say no output device.


## soloution
create new file by using this command

```javascript
sudo nano /etc/X11/xorg.conf
```
then copy this code into file
```javascript
Section "Device"
    Identifier  "Intel Graphics" 
    Driver      "intel"
    Option      "Backlight"  "intel_backlight"
EndSection
```
then save and reboot.fixed

### xbacklight no output device
Touchpad tap on click not working.
## soloution
create new file by using this command

```javascript
sudo nano /etc/X11/xorg.conf.d/30-touchpad.conf
```
then copy this code into file
```javascript
Section "InputClass"
    Identifier "touchpad"
    Driver "libinput"
    MatchIsTouchpad "on"
    Option "Tapping" "on"
    Option "TappingButtonMap" "lmr"
EndSection
```
then save and reboot.fixed
### lxappearance Segmentation fault

## soloution
Run 
```javascript
sudo apt remove lxappearance-obconf
```
fixed


