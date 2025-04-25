# sddm-astronaut-theme

![Stars](https://img.shields.io/github/stars/kakawait/sddm-astronaut-theme?color=dd864a&labelColor=1b1b25&style=for-the-badge)
![Forks](https://img.shields.io/github/forks/kakawait/sddm-astronaut-theme?color=bf616a&labelColor=1b1b25&style=for-the-badge)

![island_animation_24h.webp](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/island_animation_24h.webp?raw=true)

[sddm-astronaut-theme](https://github.com/kakawait/sddm-astronaut-theme) is a series of themes for the [SDDM](https://github.com/sddm/sddm/) display manager made by **[Keyitdev](https://github.com/Keyitdev)** and forked by myself **[Kakawait](https://github.com/kakawait)**.

It's written using the latest version of Qt, which is **Qt6**. Its key features include **virtual keyboard support** and an **installation script**. This theme also support **animated wallpapers**. You can easily change its appearance by choosing another of the ten pre-made themes or creating your own. Each of these themes was created by modifying just one file - **[config](./Themes/astronaut.conf)**.

Most themes were created for 1080p. However, they should work well in other resolutions.

## Preview of other themes

![all_themes.gif](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/all_themes.gif?raw=true)

## Preview of animated themes

https://github.com/user-attachments/assets/2cfc947e-4621-4e98-b5f3-07d5e224b80c

<h2><a href="https://youtu.be/4tQ56xh7wBc" target="_blank">Watch more on Youtube!</a></h2>
<details>
<summary><h2>Detailed previews</h2></summary>

**Astronaut**|**Black hole**
|:--:|:--:|
![astronaut](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/astronaut.png?raw=true)|![black_hole](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/black_hole.png?raw=true)
**Japanese aesthetic**|**Pixel sakura static**
![japanese_aesthetic](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/japanese_aesthetic.png?raw=true)|![pixel_sakura_static](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/pixel_sakura_static.png?raw=true)
**Purple leaves**|**Cyberpunk**
![purple_leaves](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/purple_leaves.png?raw=true)|![cyberpunk](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/cyberpunk.png?raw=true)
**Post-apocalyptic hacker**|**xxx**
![post-apocalyptic_hacker](https://github.com/kakawait/sddm-astronaut-theme/blob/master/Previews/post-apocalyptic_hacker.png?raw=true)|

**Hyprland Kath**

https://github.com/user-attachments/assets/1d926e76-44f7-4d99-ac6d-d1abcd7ed688

**Pixel sakura**

https://github.com/user-attachments/assets/ea004765-7e84-4a0d-90cd-aaac97679f62

**Jake the dog**

https://github.com/user-attachments/assets/181d48c2-f152-45f5-b568-21145be180f6

</details>

## Installation

### Automatic Installation

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/kakawait/sddm-astronaut-theme/master/setup.sh)"
```
> Works on distributions using pacman, xbps-install, dnf, zypper.
> Remember to always read the scripts you run from the internet.

### Manual Installation

1. Install **dependencies**

[`sddm >= 0.21.0`](https://github.com/sddm/sddm), [`qt6 >= 6.8`](https://doc.qt.io/qt-6/index.html), [`qt6-svg >= 6.8`](https://doc.qt.io/qt-6/qtsvg-index.html), [`qt6-virtualkeyboard >= 6.8`](https://doc.qt.io/qt-6/qtvirtualkeyboard-index.html), [`qt6-multimedia >= 6.8`](https://doc.qt.io/qt-6/qtmultimedia-index.html)

You may also want to install additional video codecs like h.264.

```sh
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia-ffmpeg     # Arch
sddm qt6-svg qt6-virtualkeyboard qt6-multimedia            # Void
sddm qt6-qtsvg qt6-qtvirtualkeyboard qt6-qtmultimedia      # Fedora
sddm-qt6 libQt6Svg6 qt6-virtualkeyboard qt6-virtualkeyboard-imports qt6-multimedia qt6-multimedia-imports        # OpenSUSE
```

2. Clone this repository
```sh
sudo git clone -b master --depth 1 https://github.com/kakawait/sddm-astronaut-theme.git /usr/share/sddm/themes/sddm-astronaut-theme
```
3. Copy fonts to `/usr/share/fonts/`
```sh
sudo cp -r /usr/share/sddm/themes/sddm-astronaut-theme/Fonts/* /usr/share/fonts/
```
4. Edit `/etc/sddm.conf`
```sh
echo "[Theme]
Current=sddm-astronaut-theme" | sudo tee /etc/sddm.conf
```
5. Edit `/etc/sddm.conf.d/virtualkbd.conf`
```sh
echo "[General]
InputMethod=qtvirtualkeyboard" | sudo tee /etc/sddm.conf.d/virtualkbd.conf
```

## Selecting a theme

You can select theme by editing [metadata](./metadata.desktop) (`/usr/share/sddm/themes/sddm-astronaut-theme/metadata.desktop`).

Just edit this line:
```
ConfigFile=Themes/astronaut.conf
```
All available configs are in [Themes](./Themes/) directory.

## Previewing a theme

You can preview the set theme without logging out by runnning:
```sh
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/sddm-astronaut-theme/
```
> Note that depending on the system configuration, the preview may differ slightly from the actual login screen.

## Sources

Initially the theme was independed fork of [MarianArlt's theme](https://github.com/MarianArlt/sddm-sugar-dark) but now the project has come a long way and started to significantly deviate from the original.
Many of the wallpapers and fonts used in this project are very popular and copied from one user to another, so I don't know who the original creator is.
I also redesigned many of them, but here are links to some of the orginal artists who created these wonderful wallpapers:

- Astronaut: [wallpaper](https://wallhaven.cc/w/e76pew), [font](https://fonts.google.com/specimen/Open+Sans/about)
- Black hole: [wallpaper](https://images2.alphacoders.com/114/1141632.jpg), [font](https://www.1001fonts.com/espacion-font.html)
- Japanese aesthetic: [wallpaper](https://imgur.com/a/pua0dYx) by [gharly](https://www.artstation.com/gharly), [font](https://www.1001fonts.com/electroharmonix-font.html)
- Purple leaves: [wallpaper](https://wallha.com/wallpaper/artwork-abstract-leaves-purple-texture-pattern-1414432), [font](https://fonts.google.com/specimen/Open+Sans/about)
- Cyberpunk: [wallpaper](https://images5.alphacoders.com/133/1330479.png) by [patrika](https://alphacoders.com/users/profile/227699/patrika), [font](https://www.1001fonts.com/kognigear-font.html)
- Post-apocalyptic hacker:  [wallpaper](https://images.alphacoders.com/137/thumb-1920-1375178.png) by [patrika](https://alphacoders.com/users/profile/227699/patrika), [font](https://www.1001fonts.com/fragile-bombers-font.html)
- Hyprland Kath: [wallpaper](https://motionbgs.com/andvari-last-origin), [font](https://www.1001fonts.com/pixelon-font.html)
- Pixel sakura: [wallpaper](https://imgur.com/gallery/sakura-tree-with-petals-flying-off-t5tg4N8), [font](https://www.1001fonts.com/arcadeclassic-font.html)
- Jake the dog: [wallpaper](https://motionbgs.com/jake-the-dog), [font](https://fontmeme.com/fonts/thunderman-font/)
- Island: [wallpaper](https://www.reddit.com/r/wallpaper/comments/k02una/outset_island_throughout_the_day_3840x2160/) (source image from [google drive](https://drive.google.com/file/d/1G22S-b5aeksYqIe-tO9vl5y1OlTvQLxv/view)), [font](https://fonts.google.com/specimen/Open+Sans/about)

## Supporting project

You can support me simply by dropping a **star** on **[github](https://github.com/kakawait/sddm-astronaut-theme)**.

Distributed under the **[GPLv3+](https://www.gnu.org/licenses/gpl-3.0.html) License**.
Copyright (C) 2022-2025 Keyitdev.
Copyright (C) 2025 kakawait.
