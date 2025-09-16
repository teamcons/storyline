# ![icon](data/images/icon.png) storyline

## Focus on your writing

[![Get it on AppCenter](https://appcenter.elementary.io/badge.svg)](https://appcenter.elementary.io/io.github.teamcons.storyline)

[![Build Status](https://travis-ci.org/lainsce/storyline.svg?branch=master)](https://travis-ci.org/lainsce/storyline)
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](http://www.gnu.org/licenses/gpl-3.0)

![Screenshot](data/images/shot.png)

## License

Fonts under the `/data/font` directory are under [License: SIL OFL 1.1](http://scripts.sil.org/OFL), also copied there in full.

## Donations

Would you like to support the development of this app to new heights? Then:

[Be my backer on Patreon](https://www.patreon.com/lainsce)

## Dependencies

Please make sure you have these dependencies first before building.

```bash
valac
libgranite-dev
gtk+-3.0
gtksourceview-4-dev
libwebkit2gtk-4.0-dev
libmarkdown2-dev
libgtkspell3-3-dev
libhandy-1-dev >= 0.80.0
meson
```

## Building

Simply clone this repo, then:

```bash
meson build --prefix=/usr && cd build
sudo ninja install
```

## Arch Linux

Arch Linux users can find storyline under the name [storyline-git](https://aur.archlinux.org/packages/storyline-git/) in the **AUR**:

`$ <aur_helper> -S storyline-git`

## Fedora

Fedora users can find storyline under the name [storyline](https://src.fedoraproject.org/rpms/storyline) in official repository:

`$ sudo dnf install storyline`
