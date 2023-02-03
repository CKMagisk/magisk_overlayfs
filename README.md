# Magisk Overlayfs

- Emulate your system partitions become read-write-able by using OverlayFS
- Make system partition (`/system`, `/vendor`, `/product`, `/system_ext`) become read-write.
- Use `/data` as upperdir for overlayfs. On some ROMs, loop ext4 image is needed when `/data` cannot be used directly.
- All modifications to overlayfs partition will not be made directly, but will be stored in upperdir, so it is easy to revert.

## Without Magisk

- Possible to test:

```bash
mkdir -p /data/overlayfs
./overlayfs_system /data/overlayfs
```

## Bugreport

- Please include `/cache/overlayfs.log`

## Source code

<https://github.com/HuskyDG/magisk_overlayfs>