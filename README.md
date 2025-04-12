# Steamdeck Scripts

A collection of scripts I use to automate installation of some components I use regularly after SteamOS updates

To run all scripts, simply execute
```bash
./install_all
```

## Scripts

### enable_jp_locale

Enables the japanese locale on the steamdeck. Useful for learners of japanese that have to interact with e.g. zip archives with japanese characters in file names
```bash
LANG=ja_JP 7zz x <zip-archive>
```

### install_lein

Installs [Leiningen](https://leiningen.org/) for clojure development. I suggest combining this with installing java via [SDKMAN](https://sdkman.io/).

### install_neovim

Installs [neovim](https://neovim.io/) in `${HOME}/bin/nvim`. By default the nightly version is chosen. You may want to install this via `distrobox` in a dedicated development container.

### install_podman-compose

Installs `aardvark-dns` and `podman-compose` for support of docker-compose files.

### install_xclip

Installs xclip, which is useful for copying and pasting in and out of [neovim](https://neovim.io/), [mpv](https://mpv.io/) with stuff like [mpvacious](https://github.com/Ajatt-Tools/mpvacious) etc.