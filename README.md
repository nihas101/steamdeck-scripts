# Steamdeck Scripts

- [Steamdeck Scripts](#steamdeck-scripts)
  - [General Tools](#general-tools)
    - [./scripts/install\_xclip](#scriptsinstall_xclip)
    - [Insalling 7zz](#insalling-7zz)
  - [Japanese Learning](#japanese-learning)
    - [./scripts/enable\_jp\_locale](#scriptsenable_jp_locale)
    - [Installing game2text](#installing-game2text)
    - [Installing MPV and mpvacious](#installing-mpv-and-mpvacious)
    - [Japanese Input](#japanese-input)
    - [Anki](#anki)
  - [Development](#development)
    - [./scripts/install\_lein](#scriptsinstall_lein)
    - [./scripts/install\_neovim](#scriptsinstall_neovim)
    - [./scripts/install\_podman-compose](#scriptsinstall_podman-compose)

A collection of scripts I use to automate installation of some components and also just some general notes on installing and setting up things I use regularly.

To run all scripts, simply execute
```bash
./install_all
```

## General Tools

### ./scripts/install_xclip

Installs xclip, which is useful for copying and pasting in and out of [neovim](https://neovim.io/), [mpv](https://mpv.io/) with stuff like [mpvacious](https://github.com/Ajatt-Tools/mpvacious) etc.

### Insalling 7zz

1. Download the newest version from the [website](https://7-zip.org/download.html)
2. Run `tar -xf <7zz-file-name>.tar.xz`
3. Move `7zz` somewhere in your `$PATH`

## Japanese Learning

### ./scripts/enable_jp_locale

Enables the japanese locale on the steamdeck. Useful for learners of japanese that have to interact with e.g. zip archives with japanese characters in file names
```bash
LANG=ja_JP 7zz x <zip-archive>
```

### Installing game2text

[game2text](https://game2text.com/) can be used via [bottles](https://usebottles.com/).

1. Install bottles from the Software Center
2. Download [game2text for windows](https://github.com/mathewthe2/Game2Text/releases)
3. Unzip game2text `7zz x  win-game2text.zip `
4. Setup a bottle optimized for gaming
5. Run game2text inside the bottle you just created

### Installing MPV and mpvacious

1. Install MPV through the Software Center
2. Follow any of the tutorials out there to setup MPV and mpvacious exactly like you want. I believe the one by [Matt vs Japan](https://www.youtube.com/watch?v=bbg6ztWecbU) was the one I used as starting point.

### Japanese Input

You can use [Fcitx5](https://fcitx-im.org/wiki/Fcitx_5) and `mozc Fcitx5` from the Software Center for japanese input.

### Anki

[Anki](https://apps.ankiweb.net/) is available from the Software Center.

## Development

### ./scripts/install_lein

Installs [Leiningen](https://leiningen.org/) for clojure development. I suggest combining this with installing java via [SDKMAN](https://sdkman.io/).

### ./scripts/install_neovim

Installs [neovim](https://neovim.io/) in `${HOME}/bin/nvim`. By default the nightly version is chosen. You may want to install this via `distrobox` in a dedicated development container.

### ./scripts/install_podman-compose

Installs `aardvark-dns` and `podman-compose` for support of docker-compose files.
