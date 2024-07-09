# LizardByte's Pacman Repository

Repository of Arch Linux packages for LizardByte packages.

> [!CAUTION]
> LizardByte does not support packages hosted on the AUR. The platform is not secure, since anyone is able to
> become the packager of an AUR repo. If you use the AUR, please carefully inspect any PKGBUILDS for packages that you
> are using, before any installation. This repository is the only official source of LizardByte packages.

## Installation

Add the following code snippet to your `/etc/pacman.conf`:

```conf
[lizardbyte]
SigLevel = Optional
Server = https://app.lizardbyte.dev/pacman-repo
```

or:
```conf
[lizardbyte]
SigLevel = Optional
Server = https://raw.github.com/LizardByte/pacman-repo/gh-pages
```

Then, run `sudo pacman -Sy` to update repository.

## Considerations

- To account for changes to any dependencies, packages in this repo are rebuilt once per day.
- Packages may have optional run time dependencies, you can review the PKGBUILD files for more information.
