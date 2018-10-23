# Arc Deep Theme

**This theme is forked from [NicoHood/arc-theme](https://github.com/NicoHood/arc-theme) and made colors to more black.**

Arc is a flat theme with transparent elements for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Pantheon, Xfce, MATE, Cinnamon (>=3.4), Budgie Desktop (10.4 for GTK+3.22) etc.

The NicoHood/arc-theme repository is a fork of the horst3180/arc-theme repository  which as been umaintained since March 2017.
Its aim is to continue the maintenance of arc-theme. The two maintainers are the Arch-Linux and Debian & Ubuntu packaging maintainers.

It is strongly encouraged to submit pull-requests to suggest fixes and enhancements.

## Arc Deep is available in three variants

##### Arc-Deep

![A screenshot of the Arc-Deep theme](https://i.imgur.com/lnPlGe9.png)

##### Arc-Deep-Darker

![A screenshot of the Arc-Deep-Darker theme](https://i.imgur.com/XrwvcwA.png)

##### Arc-Deep-Dark

![A screenshot of the Arc-Deep-Dark theme](https://i.imgur.com/odgvsJq.png)

## Installation

### Packages

Not available right now

--

### Manual Installation

To build the theme the following packages are required
* `autoconf`
* `automake`
* `sassc` for GTK 3, Cinnamon, or GNOME Shell
* `pkg-config` or `pkgconfig` for Fedora
* `git` to clone the source directory
* `optipng` for GTK 2, GTK 3, or XFWM
* `inkscape` for GTK 2, GTK 3, or XFWM

The following packages are optionally required
* `gnome-shell`for auto-detecting the GNOME Shell version
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros, for auto-detecting the GTK3 version

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.18 - 3.30, GTK 3.18 - 3.24
* The `gnome-themes-extra` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/bilguun0203/arc-deep-theme --depth 1 && cd arc-deep-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency         disable transparency in the GTK3 theme
    --disable-light                disable Arc Deep Light support
    --disable-darker               disable Arc Deep Darker support
    --disable-dark                 disable Arc Deep Dark support
    --disable-cinnamon             disable Cinnamon support
    --disable-gnome-shell          disable GNOME Shell support
    --disable-gtk2                 disable GTK2 support
    --disable-gtk3                 disable GTK3 support
    --disable-metacity             disable Metacity support
    --disable-unity                disable Unity support
    --disable-xfwm                 disable XFWM support
    --disable-plank                disable Plank theme support
    --disable-openbox              disable Openbox support

    --with-gnome-shell=<version>   build the gnome-shell theme for a specific version
    --with-gtk3=<version>          build the GTK3 theme for a specific version
                                   Note: Normally the correct version is detected automatically
                                   and these options should not be needed.
    --with-custom=<script>         run the executable script file in the custom subfolder

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `Arc`, `Arc-Darker` or `Arc-Dark` as Window/GTK+ theme and `Arc` or `Arc-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `Arc-solid`, `Arc-Darker-solid` and `Arc-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{Arc-Deep,Arc-Deep-Darker,Arc-Deep-Dark}

## Extras

### Arc icon theme
The Arc icon theme is available at https://github.com/NicoHood/arc-icon-theme

### Plank theme
As of version `20180114` the plank theme will be installed along with the normal arc gtk theme. You can disable the install by passing `disable-plank` to the autogen command.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Gtk+` as the theme.

## Troubleshooting

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal


## Bugs
If you find a bug, please report it at https://github.com/bilguun0203/arc-deep-theme/issues

## License
Arc Deep is available under the terms of the GPL-3.0. See `COPYING` for details.
