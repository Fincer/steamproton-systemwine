# Additional PKGBUILD files

The following files are required for this package. Due to legal reasons, these files are not provided here. Obtain these files from existing Steam Proton file locations defined below or from other sources. You can also extract these files directly from `proton_dist.tar.gz` archive.

**1)** From `proton_dist.tar.gz` archive, obtain the files listed in `DLL file` column:

|               DLL file               |      Target location      |
|--------------------------------------|---------------------------|
| lib/wine/fakedlls/vrclient.dll       | lib32/vrclient.dll        |
| lib/wine/dxvk/openvr_api_dxvk.dll    | lib32/openvr_api_dxvk.dll |
| lib64/wine/fakedlls/vrclient_x64.dll | lib64/vrclient_x64.dll    |
| lib64/wine/dxvk/openvr_api_dxvk.dll  | lib64/openvr_api_dxvk.dll |


**2)** Create two new subdirectories: `lib32`, `lib64`. Insert copied DLL files into respective locations defined in `Target location` column above.

**3)** Put these directories in the same location with your `openvr-proton` PKGBUILD.

**4)** Run `updpkgsums && makepkg -fi`

----------

# Configuration files

You should create file `` with the following contents:

```
{
  "config" : [ "/home/<username>/.local/share/Steam/config/" ],
  "external_drivers" : null,
  "log" : [ "/home/<username>/.local/share/Steam/logs/" ],
  "runtime" : [ "/home/<username>/.local/share/Steam/SteamApps/common/SteamVR" ]
}
```

where `<username>` is user name of the Unix user which uses Steam client.
