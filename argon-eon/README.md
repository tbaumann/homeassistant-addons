# Home Assistant Add-on: Argon eon support 


Preparation

Add to `/mnt/boot/config.txt`

```
dtparam=i2c_arm=on
dtparam=i2s=on

Uncomnent this if you want to run the lirc component
#dtoverlay=gpio-ir,gpio_pin=23
```

Creat this file `/mnt/overlay/etc/modules-load.d/i2c-dev.conf` 

```
i2c-dev
```


![Supports aarch64 Architecture][aarch64-shield]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
