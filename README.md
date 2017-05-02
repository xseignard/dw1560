# DW1560 WiFi + BT on Ubuntu 16.10

## For this given hardware

[http://www.ebay.com/itm/Dell-DW1560-Broadcom-BCM94352Z-M-2-NGFF-802-11AC-867Mbps-Bluetooth-4-0-WIFI-Card/262296628950?_trksid=p2047675.c100011.m1850&_trkparms=aid%3D222007%26algo%3DSIC.MBE%26ao%3D1%26asc%3D40130%26meid%3D45989c79177f4babb972000962324fc1%26pid%3D100011%26rk%3D3%26rkt%3D12%26sd%3D131573066893](http://www.ebay.com/itm/Dell-DW1560-Broadcom-BCM94352Z-M-2-NGFF-802-11AC-867Mbps-Bluetooth-4-0-WIFI-Card/262296628950?_trksid=p2047675.c100011.m1850&_trkparms=aid%3D222007%26algo%3DSIC.MBE%26ao%3D1%26asc%3D40130%26meid%3D45989c79177f4babb972000962324fc1%26pid%3D100011%26rk%3D3%26rkt%3D12%26sd%3D131573066893)

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
