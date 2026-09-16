# Heplon CLI releases

This repository hosts the official prebuilt binaries of the Heplon CLI
(`heplon`).

## License

The Heplon-owned portions of the binary are licensed under the
[PolyForm Internal Use License 1.0.0](https://polyformproject.org/licenses/internal-use/1.0.0/),
which permits internal use and internal changes but does not permit
distribution, sublicensing, or access to source code. The precise permission
notice is bundled in every release archive as `HEPLON-CLI-LICENSE.txt`.

Third-party components included in the binary remain under their own original
licenses. Their complete notices are bundled in every release archive as
`THIRD-PARTY-LICENSES.html`.

## Supported artifact

Currently published: **Linux x86_64 (musl, statically linked)**.

Download the attached `.tar.gz` asset from a release.

## Install

Replace `<VERSION>` with the release version, for example `0.1.0`.

```sh
VERSION=<VERSION>
BASE="https://github.com/heplonhq/heplon-client/releases/download/heplon-v${VERSION}"
ARCHIVE="heplon-${VERSION}-x86_64-unknown-linux-musl.tar.gz"

curl -fLO "${BASE}/${ARCHIVE}"
curl -fLO "${BASE}/SHA256SUMS"

# Verify the download before running it.
sha256sum --check --ignore-missing SHA256SUMS

tar -xzf "${ARCHIVE}"
sudo install -m 0755 "heplon-${VERSION}-x86_64-unknown-linux-musl/heplon" /usr/local/bin/heplon

heplon --version
```

## Support

For questions and support, please contact hello@heplon.com.

## Security

Please do not report security issues by email or in public. Use GitHub's
private vulnerability reporting on this repository
("Security" tab → "Report a vulnerability").
