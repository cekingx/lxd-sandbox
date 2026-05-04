# cekingx-sandbox

Custom LXD image based on Ubuntu Noble (24.04) with Node.js 24 pre-installed.

## Build

```bash
sudo lxd-imagebuilder build-lxd src/cekingx-sandbox.yml ./out/cekingx-sandbox
```

## Import

```bash
sudo lxc image import ./out/cekingx-sandbox/lxd.tar.xz ./out/cekingx-sandbox/rootfs.squashfs --alias <some-name>
```
