# nrf-udev

udev rules for nRF (Nordic Semiconductor) development kits


This repo contains the files needed for creating a .deb package for installing the udev rules for nRF devices.


To create the package in a Debian-based linux system:

```
dpkg-deb -b nrf-udev_1.0.0-all
```

To install the package use the following command:

```
sudo dpkg -i nrf-udev_1.0.0-all.deb
```

