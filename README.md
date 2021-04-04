ODROID C1 Gentoo Overlay
========================

This overlay includes ebuilds for the following packages:

* `app-misc/lcdproc`: lcdproc + Odroid-C1 patch
* `app-misc/odroidc1-remote`: Odroid C1 remote control setup (https://github.com/mdrjr/c1_irremote)
* `dev-embedded/u-boot-tools-odroidc1`: Odroid C1 U-Boot (https://github.com/hardkernel/u-boot)
* `dev-libs/wiringPi`: Fork of the wiringPi library with Odroid-C1 support
* `media-libs/aml-odroidc1`: Odroid C1 Amlogic Libraries (https://github.com/mdrjr/c1_aml_libs)
* `sys-kernel/odroidc1-sources`: Linux source for Odroid devices (https://github.com/hardkernel/linux)
* `x11-drivers/xf86-video-odroidc1`: Xorg DDX driver for Odroid-C1 (https://github.com/mdrjr/c1_mali_ddx)
* `x11-libs/odroidc1-mali`: Closed source drivers for Mali (https://github.com/mdrjr/c1_mali_libs)


Usage with Layman
-----------------

```
mkdir -p /etc/portage/package.use
echo "app-portage/layman sync-plugin-portage" > /etc/portage/package.use/layman
emerge -av dev-util/git app-portage/layman

pico /etc/layman/layman.cfg
|   overlays  :
|       https://api.gentoo.org/overlays/repositories.xml
| +     https://github.com/svoop/odroidc1-overlay/raw/main/repositories.xml
layman -S
layman -a odroidc1
```

