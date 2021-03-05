# PiBoyControls
Modified PiBoy DMG Controls driver  
original author : Nathan Scherdin  
License : GPL 
PiBoy DMG https://www.experimentalpi.com/
Firmware & script https://www.experimentalpi.com/downloads.html



## Install
```
cd /home/pi
git clone https://github.com/losernator/PiBoyControls.git
cd PiBoyControls
sudo cp -a * /usr/src/xpi_gamecon-1.0/
sudo dkms uninstall -m xpi_gamecon -v 1.0
sudo dkms build -m xpi_gamecon -v 1.0
# Check the make log:
cat /var/lib/dkms/xpi_gamecon/1.0/5.4.51-v7l+/armv7l/log/make.log
sudo dkms install -m xpi_gamecon -v 1.0
```
You need to reboot for changes

## Restore from a (previously compiled) backup
```
sudo cp ~/dev/piboydmg/xpi_gamecon_module_backup/root/lib/modules/5.4.51-v7l+/updates/dkms/xpi_gamecon.ko /run/media/arlanthir/retropie/lib/modules/5.4.51-v7l+/updates/dkms
sudo cp ~/dev/piboydmg/xpi_gamecon_module_backup/root/var/lib/dkms/xpi_gamecon/1.0/5.4.51-v7l+/armv7l/module/xpi_gamecon.ko /run/media/arlanthir/retropie/var/lib/dkms/xpi_gamecon/1.0/5.4.51-v7l+/armv7l/module/xpi_gamecon.ko
```

**Change log** 
change DPAD control to HAT
add bulky deadzone setting to analog stick
