# Additional PKGBUILD files

The following files are required for this package. Due to legal reasons, these files are not provided here. Obtain these files from provided hyperlinks or existing Steam Proton file locations defined below. You can also extract these files directly from `proton_dist.tar.gz` archive.

### libsteam_api.so

**Alternative A)**

Link: [GitHub - ValveSoftware/Proton - libsteam_api.so](https://github.com/ValveSoftware/Proton/raw/proton_4.2/steam_helper/libsteam_api.so)

**Alternative B)**

Get the file either from...

```
$HOME/.local/share/Steam/steamapps/common/Proton <version>/dist/lib/libsteam_api.so
```

...or directly from `proton_dist.tar.gz` archive:

```
lib/libsteam_api.so
```

### steam.exe.so

Get the file either from...

```
$HOME/.local/share/Steam/steamapps/common/Proton <version>/dist/lib/wine/steam.exe.so
```

...or directly from `proton_dist.tar.gz` archive:

```
lib/wine/steam.exe.so
```

Put obtained files in the same directory along provided lib32-steamlibs `PKGBUILD` file. Build & install the package with `updpkgsums && makepkg -fi` command.

## Proton installation on Steam client

If you need to install specific Proton version, the easiest way is to use Steam client application. On the client, go to:

```
LIBRARY -> TOOLS -> Proton <version> -> Install Game...
```

Proton 4.2 or higher is required.
