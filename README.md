<p align="center">
  <img src="https://raw.githubusercontent.com/ChoutesOS/.github/main/assets/banner.png" alt="ChoutesOS" width="100%">
</p>

<p align="center">
  <a href="https://choutes.com"><b>Website</b></a> &nbsp;&middot;&nbsp;
  <a href="https://discord.gg/nYdsKv7Fra"><b>Discord</b></a> &nbsp;&middot;&nbsp;
  <a href="https://sociabuzz.com/choutesos/donate"><b>Donate</b></a>
</p>

# ChoutesOS package repository

The signed pacman repository of ChoutesOS. Every ChoutesOS system uses it automatically to receive new versions of the ChoutesOS desktop, tools, and themes, next to the updates from the Arch repositories.

> [!IMPORTANT]
> This repository is made for ChoutesOS only. Do not add it to other Arch-based systems.

## How ChoutesOS uses it

The packages and the repository database are published in the [`repo-x86_64`](https://github.com/ChoutesOS/packages/releases/tag/repo-x86_64) release of this repository. ChoutesOS reads the address from `/etc/pacman.d/choutesos-mirrorlist`, which comes with the `choutesos-release` package:

```ini
[choutesos]
Include = /etc/pacman.d/choutesos-mirrorlist

# /etc/pacman.d/choutesos-mirrorlist
Server = https://github.com/ChoutesOS/packages/releases/download/repo-$arch
```

Software Update checks this repository every day and installs its updates together with the Arch updates.

## Packages

| Package | Contents |
| --- | --- |
| `choutesos-keyring` | The key that signs the ChoutesOS packages |
| `choutesos-release` | The ChoutesOS identity (`os-release`) and the address of this repository |
| `choutesos-branding` | ChoutesOS logos, application icon, and boot splash |
| `choutesos-wallpapers` | The ChoutesOS wallpaper collection |
| `choutesos-plasma-theme` | The ChoutesOS Dark and ChoutesOS Light themes for KDE Plasma |
| `choutesos-settings` | Kernel and gaming tuning, zram, and the default applications |
| `choutesos-welcome` | Welcome, Driver Manager, Software Update, and About ChoutesOS |
| `choutesos-calamares-config` | The configuration and artwork of the ChoutesOS installer |
| `plasma-setup` | The KDE first start wizard that creates the first user account |

## Signatures

Every package and the database are signed with a dedicated signing subkey; pacman refuses files without a valid signature. The key is installed by `choutesos-keyring`.

| | |
| --- | --- |
| **Key** | ChoutesOS Package Signing |
| **Fingerprint** | `45EE 66CD 70D6 F24F 3188  C04B 9E96 425D 7F3A 3F8A` |

## Security

Report security problems privately, as described in the [security policy](https://github.com/ChoutesOS/.github/blob/main/SECURITY.md).

## License

Each package carries the license of its contents. The ChoutesOS packages are licensed under the GNU General Public License, version 3 or later; the ChoutesOS name, logo, and artwork are not covered by that license.

---

<sub>© 2026 ChoutesOS. All rights reserved. ChoutesOS and the ChoutesOS logo are trademarks of ChoutesOS.<br>
Linux® is the registered trademark of Linus Torvalds in the U.S. and other countries. Arch Linux, KDE, and Plasma are trademarks of their respective owners.<br>
ChoutesOS is an independent project and is not affiliated with Arch Linux.</sub>
