---
title: Download
subtitle: Your world is about to change. Welcome to the best programming language in the world.
---

(*) For Linux 64-bit distros, you need to install 32-bit supporting libraries. So, for Debian-based distros, install them using:

```
sudo apt-get install ia32-libs libc6-i386 libcurl3
```

If you are using a Debian 7+ or Ubuntu 13.10+ version, you should use the multiarch way:

```
dpkg --add-architecture i386
apt-get update
apt-get install libc6:i386 libcurl3:i386
```

For Fedora/Redhat/Centos distros:

```
sudo yum install glibc.i686
sudo yum install libcurl.i686
```

For FreeBSD, no prebuilt binaries yet, you need to cross-compile, or get the Red sources, a Rebol interpreter ([here](http://www.rebol.com/downloads/v278/rebol-core-278-7-2.tar.gz)) and a couple packages: `libcrypto.so.8`, which can be found in the openssl package, and `libcurl.so.4` (temporary dependency):

```
pkg install openssl
pkg install fpc-libcurl-3.0.2
```

For ArchLinux, there is a Red package [there](https://aur.archlinux.org/packages/red/).

For step by step instructions on compiling your first script, please find them [here](https://github.com/dockimbel/Red/blob/master/README.md).

## Install Red using a package manager

* [Chocolatey](https://chocolatey.org/packages/red): `choco install red`

## Direct links to latest builds

* Windows: [raw binary](https://static.red-lang.org/dl/auto/win/red-latest.exe), [zipped](https://static.red-lang.org/dl/auto/win/red-latest.zip)
* Linux: [raw binary](https://static.red-lang.org/dl/auto/linux/red-latest), [zipped](https://static.red-lang.org/dl/auto/linux/red-latest.zip)
* macOS: [raw binary](https://static.red-lang.org/dl/auto/mac/red-latest), [zipped](https://static.red-lang.org/dl/auto/mac/red-latest.zip)


