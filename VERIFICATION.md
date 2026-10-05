# USA Version Verification

Public verification phrase: `KURU`

Fork: <https://github.com/moswald14/app-foldingathome>

Branch: `usa-version`

Verification tag: `usa-real-real-v0.1.0`

Upstream source: <https://github.com/hassio-addons/app-foldingathome>

## What This Means

This file makes the USA version fork verifiable in public. The word `KURU` is a
public marker that should appear in both `README.md` and `foldingathome/DOCS.md`.

This marker is not a password, Folding@home passkey, account token, GitHub token,
or Home Assistant credential.

## How To Verify

Clone the fork and fetch tags:

```sh
git clone https://github.com/moswald14/app-foldingathome.git
cd app-foldingathome
git fetch --tags
```

Check the pinned USA version tag:

```sh
git rev-parse usa-real-real-v0.1.0^{commit}
```

Check that the public marker is present:

```sh
git grep -n "Verification code: `KURU`" usa-real-real-v0.1.0 -- README.md foldingathome/DOCS.md
```

Check the SHA-256 checksums recorded in `REAL-REAL.sha256`:

```sh
sha256sum -c REAL-REAL.sha256
```

## Trust Model

The real proof is the public Git history, the pinned tag, and the SHA-256
checksums. The `KURU` phrase is only a human-readable marker.
