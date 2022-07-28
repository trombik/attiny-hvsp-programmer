# AVR High-voltage Serial Fuse Reprogrammer with Chip Erase function

Check out the full story behind this: [Removing a curse from ATtiny85 Fuses](https://blog.wokwi.com/removing-a-curse-from-attiny85-fuses).

If you want to make your own, take a look at [the wiring tutorial](https://www.hackster.io/sbinder/attiny85-powered-high-voltage-avr-programmer-3324e1).

## Schematic

![Schematic](kicad/attiny-hvsp-programmer.svg)

## Requirements

* python 3 and [tox](https://tox.wiki/en/latest/install.html)

## Building

`tox.ini` install all the dependencies, including `platformio` and necessary
toolchains.

```console
tox
```

## Activating `tox` environment

In `tox` environment, you can run `platformio`.

```console
source .tox/python/bin/activate
```

```console
> pio --version
PlatformIO Core, version 6.1.3
```

To build, run:

```console
pio run
```

## Uploading the firmware

```console
pio run -t upload --upload-port ${SERIAL_PORT}
```

Replace `${SERIAL_PORT}` with the serial port on local machine.
`/dev/ttyUSB${N}` for Linux, `/dev/cuaU${N}` for FreeBSD, `COM${N}` for
Windows.

## License

License: GPL 3+

