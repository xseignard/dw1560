# DW1560 WiFi + BT on Ubuntu 16.10

## Required installations

See: [http://www.dell.com/support/article/us/en/19/HOW10806/how-to-install-broadcom-wireless-driver-on-xps-13-9343-from-ubuntu-1504-install-media?lang=EN](http://www.dell.com/support/article/us/en/19/HOW10806/how-to-install-broadcom-wireless-driver-on-xps-13-9343-from-ubuntu-1504-install-media?lang=EN)

```
sudo apt-get install dkms bcmwl-kernel-source
```

You should have a working WiFi, and recognized bluetooth.

## You cannot pair bluetooth

You need to add the bluetooth firmware.

```
wget https://raw.githubusercontent.com/xseignard/dw1560/master/BCM20702A1-0a5c-216f.hcd
sudo cp BCM20702A1-0a5c-216f.hcd /lib/firmware/brcm
```

Now you should be good!
