# Magisk Overlayfs

- Emulate your system partitions become read-write-able by using OverlayFS
- Make system partition (`/system`, `/vendor`, `/product`, `/system_ext`) become read-write.
- Use `/data` as upperdir for overlayfs. On some ROMs, loop ext4 image is needed when `/data` cannot be used directly.
- All modifications to overlayfs partition will not be made directly, but will be stored in upperdir, so it is easy to revert.

## Build

There is two way:
- Fork this repo and run github actions
- Run `bash build.sh` (On Linux/WSL)

## Without Magisk

- Possible to test:

```bash
mkdir -p /data/overlayfs
./overlayfs_system /data/overlayfs
```

## Source code

<https://github.com/HuskyDG/magisk_overlayfs>