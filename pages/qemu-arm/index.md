---
title: The xPack QEMU Arm
permalink: /qemu-arm/

summary: "A binary distribution of QEMU Arm."

keywords:
  - qemu
  - arm
  - cortex-m
  - graphic

comments: true

date: 2015-09-07 21:31:00 +0300

redirect_to: https://xpack-dev-tools.github.io/qemu-arm-xpack/

---

## Quicklinks

If you already know the general facts about the xPack QEMU Arm, you can
directly skip to the desired pages.

User pages:

- [install]({{ site.baseurl }}/qemu-arm/install/)
- [support]({{ site.baseurl }}/qemu-arm/support/)
- [releases]({{ site.baseurl }}/qemu-arm/releases/)

Developer & maintainer pages:

- [GitHub](https://github.com/xpack-dev-tools/qemu-arm-xpack/)
- [README-MAINTAINER](https://github.com/xpack-dev-tools/qemu-arm-xpack/blob/xpack/README-MAINTAINER.md)

## Deprecated qemu-system-gnuarmeclipse

Starting with 2022, the custom QEMU known as `qemu-system-gnuarmeclipse`,
used initially with Eclipse, was
[deprecated]({{ site.baseurl }}/qemu-arm/gnuarmeclipse/),
and the project was updated to use the current upstream sources.

For compatibility reasons, `qemu-system-gnuarmeclipse` will still be
available for a while, but it is no longer recommended for new projects.

## Why QEMU?

[QEMU](https://www.qemu.org) is the long-standing open-source
cross-platform emulator. It is mature, it provides a good framework
for emulation, it implements a GDB server, it provides support for
semihosting, and although it does not intend to accurately simulate
processor time behaviour, it does keep a quite accurate track of
time when emulating timer interrupts, so it can also be used to
emulate applications using RTOS-es.

## Overview

**xPack QEMU Arm** is a cross-platform binary distribution of
the public open-source
[QEMU](https://www.qemu.org) project.

## Benefits

The main benefits of using the **xPack QEMU Arm** are:

- a convenient, uniform and portable install/uninstall/upgrade procedure,
  the same procedure is used for all major
  platforms (Intel Windows 64-bit, Intel GNU/Linux 64-bit, Arm GNU/Linux
  64/32-bit, Intel macOS 64-bit, Apple Silicon macOS 64-bit)
- a better integration with development environments
  like **Eclipse Embedded CDT**;
  users can run the _Hello World_ projects generated by the
  Eclipse templates immediately, without any specific hardware,
  neither development board nor JTAG programmer; all debugging
  features, like single stepping, inspecting variables, registers,
  etc. are supported
- a convenient integration with Continuous Integration environments,
  like GitHub Actions; the emulator provides a very convenient platform for running
  **unit tests**, fully supporting the **semihosting** features
  required for this.

All binaries are self-contained, they include all required libraries,
and can be installed in any location.

### Compatibility & peripherals

The xPack QEMU Arm is fully compatible with the original
`qemu-system-arm` and `qemu-system-aarch64`.

**xPack QEMU Arm** is generally intended for running tests, mainly
**unit tests**.

## Semihosting and ITM

The recommended method to display messages from the target is via
semihosting.

## Documentation

The official QEMU documentation is available
[online](https://wiki.qemu.org/Manual).

## Install

The details of installing the **xPack QEMU Arm** on various platforms are
presented in a dedicated
[install]({{ site.baseurl }}/qemu-arm/install) page.

## Testing

The recommended method to test QEMU is using the new Eclipse QEMU Arm Debugging
plug-in; create a test project using the _Hello World_ project template.

## Support

For the various support options, please read the separate
[support]({{ site.baseurl }}/qemu-arm/support/) page.

## Change log

The release and change log is available in the repository
[`CHANGELOG.md`](https://github.com/xpack-dev-tools/qemu-arm-xpack/blob/xpack/CHANGELOG.md) file.

## Build details

For those interested on the procedure used to build these packages,
please read the
[README-MAINTAINER](https://github.com/xpack-dev-tools/qemu-arm-xpack/blob/xpack/README-MAINTAINER.md)
page.
However, the ultimate source for details are the build scripts
themselves, all available from the
[`qemu-arm-xpack.git/scripts`](https://github.com/xpack-dev-tools/qemu-arm-xpack/tree/xpack/scripts/)
folder.

## Releases

See the [releases]({{ site.baseurl }}/qemu-arm/releases) pages.

## Other links

- [QEMU wiki](https://wiki.qemu.org/)
- the original [QEMU Windows build page](https://wiki.qemu.org/Hosts/W32)
