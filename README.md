# rastaf
raspberrypi stuff

burn os
-------

`sudo dd bs=4M if=/media/vicky/Data/iso/2017-03-02-raspbian-jessie-lite.img of=/dev/sdb conv=fsync`


ssh
----

`touch ssh` to config partition

interfaces
----------

```
# interfaces(5) file used by ifup(8) and ifdown(8)

# Please note that this file is written to be used with dhcpcd
# For static IP, consult /etc/dhcpcd.conf and 'man dhcpcd.conf'

# Include files from /etc/network/interfaces.d:
source-directory /etc/network/interfaces.d

auto wlan0
auto lo
iface lo inet loopback

iface eth0 inet manual

allow-hotplug wlan0
iface wlan0 inet manual
wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf

allow-hotplug wlan1
iface wlan1 inet manual
wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf

```

wpa_supplicant config
---------------------
```
network = {
   ssid=
   psk=
}
```


