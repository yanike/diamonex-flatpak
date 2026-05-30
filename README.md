# Diamonex Flatpak

This repository contains public Flatpak packaging for Diamonex.

The Diamonex application source is maintained separately. The Flatpak manifest
uses `extra-data` to download the packaged application payload at install time.

## Local build

```bash
flatpak-builder --force-clean --user --install --install-deps-from=flathub flatpak-build io.github.yanike.diamonex-flatpak.yml
flatpak run io.github.yanike.diamonex-flatpak
```

If `flatpak-builder` fails locally with a `rofiles-fuse` error, add:

```bash
--disable-rofiles-fuse
```
