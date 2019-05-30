# Arch Linux packages for system-wide Steam-compatible Wine/DXVK/D9VK

This folder contains necessary packages for Steam-compatible Wine/DXVK/D9VK. **NOTE:** Required Wine files are located at [files_wine](../files_wine).

## Contents

- **[d9vk-git](d9vk-git):** D9VK build files. Applies custom `patch` and `diff` files if provided. Package script not found in the official package repositories

- **[dxvk-git](dxvk-git):** DXVK build files. Applies custom `patch` and `diff` files if provided. Package script not found in the official package repositories

- **[lib32-steamlibs](lib32-steamlibs):** Build files of proprietary Steam libraries for Wine (library files are not provided due to legal reasons). Package script not found in the official package repositories

- **[openvr-git](openvr-git):** OpenVR build files. See updated version [here](https://aur.archlinux.org/packages/openvr-git/)

- **[openvr-proton](openvr-proton):** Build files of OpenVR dll libraries (library files are not provided). Package script not found in the official package repositories

- **[proton-git](proton-git):** Proton build files. See updated version [here](https://aur.archlinux.org/packages/proton-git/)

- **[steam](steam):** Steam client build files & modified `PKGBUILD` with added packages in `depends` array. See updated version number [here](https://www.archlinux.org/packages/multilib/x86_64/steam/).

Some subdirectories include `README.md` file for additional instructions/information.
