# wine

Wine 10.0: runs 64-bit Windows programs (console and windowed, with the X server of the xorg package: tos-x wine program.exe) and installs .msi packages (wine msiexec /i file.msi); no sound, no OpenGL or Direct3D

A package for [tOS](https://github.com/Artfical/tOS), installed with `tpkg`:

```
sudo tpkg install wine
```

| | |
|---|---|
| Version | 10.0 |
| Licence | LGPL-2.1-or-later (Wine); the libraries it carries are under zlib, libpng, IJG, MIT, BSD and LGPL licences |
| Upstream | https://www.winehq.org |
| Needs | [`xorg`](https://github.com/Artfical/tpkg-xorg), [`busybox`](https://github.com/Artfical/tpkg-busybox) |
| Needs tOS build | 634 or newer |
| Size | 73700471 bytes (231993651 unpacked) |
| SHA-256 of the `.tpkg` | `3811710bafc4f3d0682f4895ba5e8f7c3938e6d8b2b7cb38d1b447f45eaccc63` |

## Commands it adds

| Command | Runs |
|---|---|
| `wine` | `bin/tos-wine` |
| `wineserver` | `bin/tos-wineserver` |
| `msiexec` | `bin/tos-msiexec` |
| `winecfg` | `bin/tos-winecfg` |
| `regedit` | `bin/tos-regedit` |
| `winepath` | `bin/tos-winepath` |
| `wineconsole` | `bin/tos-wineconsole` |
| `wine-notepad` | `bin/tos-notepad` |

## Download

The package file (`wine-10.0.tpkg`) and the sources it was built from are the assets of the
[v10.0 release](https://github.com/Artfical/tpkg-wine/releases/tag/v10.0).
Git holds only the text: `meta.json`, the licences and `NOTICE.txt` (how it was built and what was changed).

Sources in the release:
- `wine-10.0.tar.xz`

Check a download: `sha256sum wine-10.0.tpkg` must give the hash above.

## Signatures

Packages are signed by Artfical's package server (Ed25519) and tOS checks the signature before it installs one.
The signature is made when the server hands a package out, so it is not kept here, and the signing key is never published.
`tpkg install` is the supported way to install; a `.tpkg` taken from here has the hash above but not the server's signature.

## Licence

The package is made of other people's software, under their licences: LGPL-2.1-or-later (Wine); the libraries it carries are under zlib, libpng, IJG, MIT, BSD and LGPL licences. The licence texts are in this
repository (`LICENSE*`, `UNLICENSE`), and `NOTICE.txt` says how it was built. The sources above are the
corresponding source. `meta.json` and this README are free to copy.

Package problems (build, files, versions): open an issue here. Problems in the software itself belong upstream.
Security reports: see [SECURITY.md](https://github.com/Artfical/tOS/blob/main/SECURITY.md).
