<p align="center">
  <img src="https://raw.githubusercontent.com/Choutes-Project/.github/main/assets/banner.png" alt="Choutes Project" width="100%">
</p>

<p align="center">
  <a href="https://choutes.com"><b>Website</b></a> &nbsp;&middot;&nbsp;
  <a href="https://packages.choutes.com"><b>Package server</b></a> &nbsp;&middot;&nbsp;
  <a href="https://help.choutes.com"><b>Help Center</b></a> &nbsp;&middot;&nbsp;
  <a href="https://discord.gg/nYdsKv7Fra"><b>Discord</b></a>
</p>

# Choutes Project package repository

The signed pacman repository of Choutes Project. Every installed system uses it automatically to receive new versions of the desktop, the applications, and the themes, together with the updates from the Arch Linux repositories. The packages that are published now are listed on [packages.choutes.com](https://packages.choutes.com).

> [!IMPORTANT]
> This repository is made for Choutes Project only. Do not add it to other Arch-based systems.

## How Choutes Project uses it

The packages and the repository database are published in the [`repo-x86_64`](https://github.com/Choutes-Project/packages/releases/tag/repo-x86_64) release of this repository. Choutes Project reads the address from `/etc/pacman.d/choutes-mirrorlist`, which comes with the `choutes-release` package:

```ini
# /etc/pacman.conf: the repository is moved before [core] by itself, so that a
# Choutes Project package always takes the place of a package with the same name
[choutes]
Include = /etc/pacman.d/choutes-mirrorlist

# /etc/pacman.d/choutes-mirrorlist
Server = https://github.com/Choutes-Project/packages/releases/download/repo-$arch
```

Software checks this repository in the background and installs its updates together with the other system updates. A new version of `choutes-release` is a new version of Choutes Project.

`choutes-plasma.json`, next to the database, names the KDE Plasma version that is released for Choutes Project. While the Arch Linux repositories have a newer Plasma that is still being tested, the system updates wait (at most 14 days) and only the Choutes Project packages are installed. `choutes-notes.json` holds the short notes that Software shows for each update.

## Packages

| Package | Contents |
| --- | --- |
| `choutes-keyring` | The key that signs the Choutes Project packages |
| `choutes-release` | The Choutes Project identity and version (`os-release`) and the address of this repository |
| `choutes-branding` | The Choutes Project logo, icons, and boot splash |
| `choutes-wallpapers` | The Choutes Project wallpapers, each in a light and a dark version |
| `choutes-plasma-theme` | The Choutes Dark and Choutes Light themes for KDE Plasma, the login screen, and the panel layout |
| `choutes-settings` | Kernel and gaming tuning, zram, defaults, Fastfetch, diagnostics (`choutes-diag`), and the order of the repositories |
| `choutes-app-base` | The shared parts of the Choutes Project applications, the KDE Plasma testing gate, and Reset System |
| `choutes-store` | Software: applications and games from Flathub and the AUR, and the updates of Choutes Project |
| `choutes-driver-manager` | Drivers: drivers for graphics, Wi-Fi, printers, and processors |
| `choutes-cleaner` | Cleaner: frees space, also by itself once a week |
| `choutes-welcome` | Welcome: the first steps after the installation |
| `choutes-calamares-config` | The configuration and artwork of the Choutes Project installer |
| `plasma-setup` | The KDE first start wizard, with the Choutes Project look, that creates the first account |

## Signatures

Every package and the database are signed with a dedicated signing subkey; pacman refuses files without a valid signature. The key is installed by `choutes-keyring`.

| | |
| --- | --- |
| **Fingerprint** | `45EE 66CD 70D6 F24F 3188  C04B 9E96 425D 7F3A 3F8A` |

## Security

Report security problems privately, as described in the [security policy](https://github.com/Choutes-Project/.github/blob/main/SECURITY.md).

## License

Each package carries the license of its contents. The Choutes Project packages are licensed under the GNU General Public License, version 3 or later; the Choutes Project name, logo, and artwork are not covered by that license.

---

<sub>&copy; 2026 Choutes Project. All rights reserved.<br>
The name and logo are trademarks. An independent project, not affiliated with Arch Linux.</sub>
