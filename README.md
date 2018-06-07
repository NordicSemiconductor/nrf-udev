# nrf-udev

udev rules for nRF (Nordic Semiconductor) development kits


You probably are here because you have:

- A nRF development kit with USB support (e.g. nRF52840)
- Linux as a development environment

and one of the following problems:

- `LIBUSB_ERROR_ACCESS` errors when using any nRF Connect tools
- Missing permissions to read/write the serial ports at `/dev/ttyACM*`
- `ModemManager` thinks that your development kit is a modem, and sends AT commands when plugging it in


## Installation

For Debian-like systems, download the latest `.deb` file from https://github.com/NordicSemiconductor/nrf-udev/releases. Then, install the package using the following command in a console:

```
sudo dpkg -i nrf-udev_1.0.1-all.deb
```

## Caveats

These udev rules set all Nordic Semiconductor devices as readable/writable by all users. While this gets rid of the `LIBUSB_ERROR_ACCESS` errors with no further configuration, this also means that any user or background process can have complete access to these USB devices.


## Development

This repo contains the files needed for creating a .deb package for installing the udev rules for nRF devices. To create the package in a Debian-based linux system:

```
dpkg-deb -b nrf-udev_1.0.1-all
```
