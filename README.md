# Vanilla OS Desktop Base Image

Containerfile for building a Vanilla OS Desktop Base Image.

> [!IMPORTANT]
> This image is not intended to be used directly. It is used as a base image for other images.
> Like the Vanilla Kipferl image, etc.
>
> This image is NOT officially regulated by Vanilla OS.

This image is based on top of [`vanillaos/core`](https://github.com/Vanilla-OS/core-image/pkgs/container/core) and offers most packages for desktop experience.

## Build

```bash
vib build recipe.yml
podman image build -t vanillakde/base .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-KDE/base-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-kde/base:latest --owner Vanilla-KDE
```
