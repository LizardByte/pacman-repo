# LizardByte's Pacman Repository

[![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/LizardByte/pacman-repo/build-repo.yml?branch=master&event=schedule&style=for-the-badge&logo=github)](https://github.com/LizardByte/pacman-repo/actions/workflows/build-repo.yml?query=event%3Aschedule+branch%3Amaster)
[![GitHub Downloads (all assets, specific tag)](https://img.shields.io/github/downloads/LizardByte/pacman-repo/beta/total?style=for-the-badge&logo=archlinux&label=daily%20downloads%40beta)](https://github.com/LizardByte/pacman-repo/releases/tag/beta)
[![GitHub Downloads (all assets, specific tag)](https://img.shields.io/github/downloads/LizardByte/pacman-repo/latest/total?style=for-the-badge&logo=archlinux&label=daily%20downloads%40latest)](https://github.com/LizardByte/pacman-repo/releases/latest)

Repository of Arch Linux packages for LizardByte packages.

> [!CAUTION]
> LizardByte does not support packages hosted on the AUR. The platform is not secure, since anyone is able to
> become the packager of an AUR repo. If you use the AUR, please carefully inspect any PKGBUILDS for packages that you
> are using, before any installation. This repository is the only official source of LizardByte packages.

## Repo Installation

Add the following code snippet to your `/etc/pacman.conf`:

```conf
[lizardbyte]
SigLevel = Optional
Server = https://github.com/LizardByte/pacman-repo/releases/latest/download
```

```conf
[lizardbyte-beta]
SigLevel = Optional
Server = https://github.com/LizardByte/pacman-repo/releases/beta/download
```

Then, run `sudo pacman -Sy` to update repository.

## Packages

### List repo packages

```bash
pacman -Sl lizardbyte
pacman -Sl lizardbyte-beta
```

### Install repo packages

```bash
sudo pacman -S lizardbyte/<package-name>
sudo pacman -S lizardbyte-beta/<package-name>
```

e.g.
```bash
sudo pacman -S lizardbyte/sunshine
sudo pacman -S lizardbyte-beta/sunshine-git
```

## Considerations

- To account for changes to any dependencies, packages in this repo are rebuilt once per day.
- Packages may have optional run time dependencies, you can review the PKGBUILD files for more information.
