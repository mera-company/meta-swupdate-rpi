# meta-swupdate-rpi
The project allows to include swupdate in the yocto build for the Raspberry Pi3 and use it in pair with update-server feature.
See update-server repository for details

This project is based on the  https://github.com/sbabic/meta-swupdate-boards

## Getting Started
This layer depends on:

* URI: git://git.yoctoproject.org/poky
  * branch: master
  * revision: HEAD

* URI: git://github.com/agherzan/meta-raspberrypi.git
  * branch: master
  * revision: HEAD

To build run:

```
	bitbake update-image
```

Above will generate a `swu` file suitable for usage with SWUpdate on
your device.

Note that `update-image` depends on `ext4.gz` and you must make sure
that it is part of `IMAGE_FSTYPES`.

For usage with Raspberry Pi one must add the following to `local.conf`

	RPI_USE_U_BOOT = "1"

## Prerequisites

## Installing

## Built With
* [SW Update](https://sbabic.github.io/swupdate/) - Update client for embedded linux
* [Raspberry Pi](https://www.raspberrypi.org) - Raspberry Pi 4 adapted kernel and firmware

## Limitations
## Versioning

We use [SemVer](http://semver.org/) for versioning. 

## Authors

Leonid Lazarev <leonid.lazarev@orioninc.com>

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License

This project is licensed under the MIT license. See the [COPYING.MIT](COPYING.MIT) file for details.
