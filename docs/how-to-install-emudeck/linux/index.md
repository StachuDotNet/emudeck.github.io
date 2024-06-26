# How to Install EmuDeck for Linux

> ⚠️ These are for x86_64 devices **ONLY** ⚠️

[TOC]

***

## Prerequisites

### Arch based (Includes Endeavour, Manjaro, etc.)

```sh
sudo pacman -Sy bash flatpak fuse2 git jq steam unzip zenity
```

### Bazzite

[https://github.com/ublue-os/bazzite](https://github.com/ublue-os/bazzite)

[https://universal-blue.org/images/bazzite/installation/](https://universal-blue.org/images/bazzite/installation/)

No additional prerequisites need to be installed.

Install EmuDeck through Bazzite's portal.

### ChimeraOS

[https://chimeraos.org/](https://chimeraos.org/)

No additional prerequisites need to be installed. For ChimeraOS tweaks to ensure EmuDeck works properly, see [ChimeraOS Tweaks](#chimeraos-tweaks).

### Debian based (Includes Ubuntu, Pop!_OS, Mint, etc.)

```sh
sudo apt-get install bash flatpak git jq libfuse2 rsync unzip zenity
```

Install Steam as directed by your OS.

### Fedora based (Includes RHEL, CentOS, Nobara, etc.)

```sh
sudo dnf install bash flatpak fuse git jq rsync unzip zenity
```

Install Steam as directed by your OS.

### OpenSUSE based

```sh
sudo zypper install bash flatpak git jq libfuse2 unzip rsync steam zenity
```

### Void based

```sh
sudo xbps-install -Syv void-repo-nonfree void-repo-multilib
sudo xbps-install -Syv libgcc-32bit libstdc++-32bit libdrm-32bit libglvnd-32bit mesa-dri-32bit
sudo xbps-install -Syv bash flatpak fuse git jq rsync steam unzip zenity jq xmlstarlet
```

### Gentoo

```sh
sudo emerge -av app-shells/bash sys-apps/flatpak dev-vcs/git net-misc/rsync gnome-extra/zenity
sudo emerge -av app-arch/unzip app-misc/jq app-text/xmlstarlet
```

It's required to install the FUSE file system on slot 0 (the default is slot 2):

```sh
sudo emerge -av sys-fs/fuse:0
```

For installing Steam, follow the [wiki article](https://wiki.gentoo.org/wiki/Steam).

***

## Text Guides

### Distro Agnostic

1. Open a terminal and enter the following:

```sh
curl -L https://raw.githubusercontent.com/dragoonDorise/EmuDeck/main/install.sh | bash
```

### Arch

Either use the [Distro Agnostic](#distro-agnostic) guide or use the [AUR Package](https://aur.archlinux.org/packages/emudeck) with the AUR helper of your choice.

### Bazzite

Install EmuDeck through Bazzite's portal.

***

## Distro Specific Guides

### ChimeraOS Tweaks

[https://github.com/ChimeraOS/chimeraos/wiki/EmuDeck](https://github.com/ChimeraOS/chimeraos/wiki/EmuDeck)

***

## Tested and Working Linux Distros

Any distro **not listed** in the table below **has not** been tested.

**Key**

* Check mark/✓: Works great without any issue
* Tilde/~: Works but requires additional set up
* X mark/x: Does not work

| Distro      | Compatibility                 |
|-------------|-------------------------------|
| Arch        | ✓                             |
| ChimeraOS   | ~ See [ChimeraOS Tweaks](#chimeraos-tweaks) |
| EndeavourOS | ✓                             |
| Fedora      | ✓                             |
| Nobara      | ✓                             |
| Ubuntu      | ✓                             |
| Void Linux  | ✓                             |

***
