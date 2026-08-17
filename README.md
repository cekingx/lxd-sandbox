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

Connect as the `ubuntu` user with password `root13`:

```bash
ssh ubuntu@<instance-ip>
```

If you have local SSH keys, the client may offer them before password auth and get disconnected with `Too many authentication failures`. Force password-only auth:

```bash
ssh -o PreferredAuthentications=password -o PubkeyAuthentication=no ubuntu@<instance-ip>
```
