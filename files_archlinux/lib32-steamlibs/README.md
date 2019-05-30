# Additional PKGBUILD files

The following files are required for this package. Due to legal reasons, these files are not provided here. Obtain these files from provided hyperlinks or existing Steam Proton file locations defined below. You can also extract these files directly from `proton_dist.tar.gz` archive.

The easiest way to install Proton is to use Steam client application. On the client, go to:

```
LIBRARY -> TOOLS -> Proton <version> -> Install Game...
```

Proton 4.2 or higher is required.

## libsteam_api.so

**Alternative A)**

Link: [GitHub - ValveSoftware/Proton - libsteam_api.so](https://github.com/ValveSoftware/Proton/raw/proton_4.2/steam_helper/libsteam_api.so)

**Alternative B)**

```
$HOME/.local/share/Steam/steamapps/common/Proton <version>/dist/lib/libsteam_api.so
```

## steam.exe.so

```
$HOME/.local/share/Steam/steamapps/common/Proton <version>/dist/lib/wine/steam.exe.so
```

ut these files in the same directory along provided lib32-steamlibs `PKGBUILD` file, after which you can build & install the package with `updpkgsums && makepkg -fi` command.
