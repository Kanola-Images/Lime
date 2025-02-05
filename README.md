# Lime LabWM Image

Containerfile for building Lime, an unofficial Vanilla OS LabWM image.

This image is based on top of [`vanillaos/core`](https://github.com/Vanilla-OS/core-image/pkgs/container/core) and offers the default
Unofficial Vanilla OS Desktop Experience with LabWM.

## Switch your Installation to this image

> [!CAUTION]
> This WIP image is experimental and isn't suitable for production. If you encounter any bugs during testing, please report them in this repository.

- Edit the `/etc/abroot/abroot.json` file with the `host-shell pkexec nano /etc/abroot/abroot.json` command.
- Change the "name" entry from something like `vanilla-os/desktop` to `kanola-images/labwm` (**Note**: All characters must be in lowercase).
- Now, Run `abroot upgrade` to switch to your custom image.

## Build

```bash
vib build recipe.yml
podman image build -t kanola-images/labwm .
```
