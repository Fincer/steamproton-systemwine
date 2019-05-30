# Steam games with system Wine, DXVK & D9VK

Use system-wide Wine, DXVK & D9VK for Steam Play/Proton (Windows) games, directly from Steam client.

## Contents

- [files_wine](files_wine) = Necessary source code patches for Wine to make it Steam-compatible

- [files_archlinux](files_archlinux) = Necessary packages & installation scripts for system-wide, Steam-compatible Wine + DXVK + D9VK. **NOTE:** Wine files are provided in [files_wine](files_wine).

- [files_proton](files_proton) = Modified Python 3 launch script for Steam Play. The script is modified to use system-wide Wine + DXVK + D9VK + OpenVR libraries & executables instead of Steam-provided, bundled ones.

## Usage

-----

**STEAM CLIENT PREPARATION**

**1)** Install Steam Client.

**2)** On Steam Client, install `Proton 4.2`: `Steam Client -> LIBRARY -> Tools -> Proton 4.2 -> Install Game...`

-----

**SYSTEM PACKAGES**

**3)** Compile & install Wine using patch files in [files_wine](files_wine). See [files_wine/README](files_wine/README.md) for additional information.

**4)** Compile & install all packages in [files_archlinux](files_archlinux). If provided, see `README.md` file of each package for additional information.

-----

**PROTON CONFIGURATION**

**5.A)** Apply modified [files_proton](files_proton/proton) Steam Play launch script. Put this file into `$HOME/.local/share/Steam/steamapps/common/Proton <version>/` where `<version>` is `4.2` or higher (depending on your configuration).

**5.B)** Select this specific Proton version in Steam client configuration menu (`Steam Client -> Settings -> Steam Play`). _This means system-wide Wine, DXVK & D9VK are used for your Steam Play games._ **Only selected version works**

-----

## Recommendations & Notes

- **Backup your _proton_ script**. It is known that Steam client likes to apply automatic patches. Have a backup of your _proton_ script file in case the client decides to overwrite it.

- **Games may not work**. Games which work on Steam-bundled Proton may not work on this modified Wine/DXVK/D9VK configuration. In this case, either **A)** choose different Proton version for non-working game titles or **B)** revert _proton_ script changes.

Original _proton_ script version `4.2` can be downloaded from [ValveSoftware/Proton - proton](https://github.com/ValveSoftware/Proton/blob/proton_4.2/proton). This script file restores original Steam Proton original functionality for the selected Proton version.

## LICENSE

Parts of this repository use various licenses:

- [License (files_wine): ValveSoftware/Wine](https://github.com/ValveSoftware/wine/blob/proton_4.2/LICENSE)

- License ([files_proton](files_proton)):

  - [ValveSoftware/Proton/LICENSE](https://github.com/ValveSoftware/Proton/blob/proton_4.2/LICENSE)

  - [ValveSoftware/Proton/LICENSE.proton](https://github.com/ValveSoftware/Proton/blob/proton_4.2/LICENSE.proton)

- License ([files_archlinux](files_archlinux)):

  - Subdirectories here provide only `PKGBUILD` compilation scripts for various packages. Licenses for these packages are listed in their respective `PKGBUILD` files.
