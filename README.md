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

## SSH Access

Connect as the `ubuntu` user using the `~/.ssh/lxd` key:

```bash
ssh ubuntu@<instance-ip> -i ~/.ssh/lxd
```

> **Note:** The SSH public key (`~/.ssh/lxd.pub`) is hardcoded in `src/cekingx-sandbox.yml` under `/home/ubuntu/.ssh/authorized_keys`. To use a different key, update that file before building the image.
