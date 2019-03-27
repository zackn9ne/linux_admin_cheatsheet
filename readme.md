### common commands
```
w # show logged in
whoami #show me
netstat -TulPn #network
nmtui #activate connection or
nmcli c s
nmcli c up en0
iostat

gpasswd -a escallateduser wheel

timedatectl
```
### run command as another user
```
sudo -u anotherperson -i pwd
```

### usb
```
lsusb
dmesg
fdisk -l #best choice shows filesystem type
mount
umount
lsof
```

### server related
```
apachect -S #check apache conf
IncludeOptional sites-enabled/*.conf  #add this to your conf file to do /sites-available /sites-enabled schema
```
### desktop related
#### get wifi working on a macbook air (fedora)
```
# Enable RPM fusion repo
dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

# Install packages
dnf install -y broadcom-wl akmods "kernel-devel-uname-r == $(uname -r)"

# Rebuild driver for your kernel
akmods

# Load the new driver
modprobe wl
```
