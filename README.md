<div align="center">
  <img
    src="https://raw.githubusercontent.com/LizardByte/.github/refs/heads/master/branding/logos/logo.svg"
    alt="LizardByte icon"
    width="256"
  />
  <h1 align="center">pacman-repo</h1>
  <h4 align="center">ArchLinux packages for LizardByte applications.</h4>
</div>

<div align="center">
  <a href="https://github.com/LizardByte/pacman-repo/actions/workflows/build-repo.yml?query=branch%3Amaster"><img src="https://img.shields.io/github/actions/workflow/status/lizardbyte/pacman-repo/build-repo.yml.svg?branch=master&label=build&logo=github&style=for-the-badge" alt="GitHub Workflow Status"></a>
  <a href="https://github.com/LizardByte/pacman-repo/releases/tag/stable"><img src="https://img.shields.io/github/downloads/LizardByte/pacman-repo/stable/lizardbyte.db.svg?style=for-the-badge&logo=archlinux&label=current%20db%20downloads%40stable&displayAssetName=false" alt="Stable database downloads since publish"></a>
  <a href="https://github.com/LizardByte/pacman-repo/releases/tag/beta"><img src="https://img.shields.io/github/downloads/LizardByte/pacman-repo/beta/lizardbyte-beta.db.svg?style=for-the-badge&logo=archlinux&label=current%20db%20downloads%40beta&displayAssetName=false" alt="Beta database downloads since publish"></a>
  <a href="https://sonarcloud.io/project/overview?id=LizardByte_pacman-repo"><img src="https://img.shields.io/sonar/quality_gate/LizardByte_pacman-repo.svg?server=https%3A%2F%2Fsonarcloud.io&style=for-the-badge&logo=sonarqubecloud&label=sonarcloud" alt="SonarCloud"></a>
</div>

# LizardByte's Pacman Repository

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
Server = https://github.com/LizardByte/pacman-repo/releases/download/beta
```

Then, run `sudo pacman -Syu` to update the system.

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

## License

This repository is licensed under the [MIT License](LICENSE); however, individual packages may have their own licenses.
Please refer to the `.SRCINFO` or `PKGBUILD` files for more information.
