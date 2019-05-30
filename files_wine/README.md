# Steam Proton patches for system Wine

The included patch files hook necessary Steam libraries into Wine process, allowing Steam games to detect Steam client presence. Without these patches, it is impossible/difficult to run Steam client with system Wine.

Some patch code is developed by Valve Corporation. Respective source code links are provided in headers of these patch files.

Patch name syntax:

```
patch_steamproton_<number>_<dll-component>_wine<wine-version>_<staging|nostaging>.patch
```

For instance:

|                      Patch file                       |                                      Description                                       |
|-------------------------------------------------------|----------------------------------------------------------------------------------------|
| patch_steamproton_01_kernel32_wine4.9_staging.patch   | Patch file targeted to DLL component `kernel32`, Wine version 4.9, vanilla/non-staging |
| patch_steamproton_01_kernel32_wine4.9_nostaging.patch | Patch file targeted to DLL component `kernel32`, Wine version 4.9, staging             |

## How-to

Apply the provided patches directly to Wine source code, and compile + install Wine.

On Arch Linux, you can use helper scripts such as [Fincer/dxvk-wine-autobuilder](https://github.com/Fincer/dxvk-wine-autobuilder) or add patches manually to your Wine `PKGBUILD` file.

## LICENSE

Please see license information of [ValveSoftware/Wine/LICENSE](https://github.com/ValveSoftware/wine/blob/proton_4.2/LICENSE)
