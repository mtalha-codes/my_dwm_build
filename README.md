# My Build of DWM
This repository include my own build of the dynamic window manager also known as dwm and is based on the configuration crafted by Christ Titus yes the main behind the famous Windows utility and Linux Utility.

## How to install

> [!WARNING]
> This mini wiki is designed for those, who as already installed arch linux many times via the archinstall script

1. First, Install a fresh copy of arch linux minimal.
2. So take your usb installer and plug it into your machine and boot into it
3. Upon booting into the arch installer, assuming you are connected to ethernet which is the best method to install arch easily, you will have this interface 
```bash
# bunch of text printed by arch iso
root@archiso> | # | is cursor
```
4. Enter these commands
```bash
lsblk # identify your target drive
```

```bash
gdisk /dev/[s/v]dX
# in my case it is currently 
# gdisk /dev/sda
# then press x and then press z and then press y two times to erase the whole disk
```

```bash
sudo pacman -Sy archlinux-keyring archinstall && archinstall 
```
5. Set user, password and time zone inside the script according to your choice, but make sure to select the following choices as specified below:
- **Bootloader** == Grub
- **Profile** == Minimal
6. After the installation is done, reboot the system, unplug the usb, and i am still assuming you're connected to ethernet 
7. Run this command
```bash
curl -fsSL christitus.com/linux | sh
```
8. press v to enter multi select mode and press tab on the following options
- DWM-Titus
- Bash Prompt
- Alacritty 
- and other options according to your needs, but for this setup these three are enough 
8. After that, run this command
```bash
cd .local/share/dwm-titus && rm -r * && git clone https://github.com/mtalha-codes/my_dwm_build.git . 
```