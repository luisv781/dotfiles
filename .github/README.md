<!--div align="center">
   <a href="#--------">
      <img src="assets/yoru.png" alt="Rice Preview">
   </a>
</div>

<br-->

## :snowflake: ‎ <samp>Information</samp>

- **OS:** [Arch Linux](https://archlinux.org)
- **WM:** [awesome](https://github.com/awesomeWM/awesome)
- **Terminal:** [wezterm](https://github.com/wez/wezterm)
- **Shell:** [zsh](https://www.zsh.org/)
- **Editor:** [neovim](https://github.com/neovim/neovim) / [vscode](https://github.com/microsoft/vscode)
- **Compositor:** [picom](https://github.com/yshui/picom)
- **Application Launcher:** [rofi](https://github.com/davatorium/rofi)
- **Music Player** [ncmpcpp](https://github.com/ncmpcpp/ncmpcpp)

AwesomeWM Modules:

- **[bling](https://github.com/blingcorp/bling)**
  - Adds new layouts, modules, and widgets that try to focus on window management primarily
- **[color](https://github.com/andOrlando/color)**
  - Clean and efficient api for color conversion in lua
- **[layout-machi](https://github.com/xinhaoyuan/layout-machi)**
  - Manual layout for Awesome with an interactive editor
- **[UPower](https://github.com/Aire-One/awesome-battery_widget)**
  - A UPowerGlib based battery widget for the Awesome WM

<br>

> This repo has a wiki! You can check it by clicking ~~[here](https://www.youtube.com/watch?v=UIp6_0kct_U)~~ [here](https://github.com/rxyhn/yoru/wiki).

<!-- SETUP -->

## :wrench: ‎ <samp>Setup</samp>


<details>
<summary><b>Dependencies</b></summary>
<br>

:warning: ‎ **This setup instructions only provided for Arch Linux (and other Arch-based distributions)**

Assuming your _AUR Helper_ is [paru](https://github.com/Morganamilo/paru).

> First of all you should install the [git version of AwesomeWM](https://github.com/awesomeWM/awesome/).

```sh
paru -S awesome-git
```

> Install necessary dependencies

```sh
paru -Sy picom-git wezterm rofi acpi acpid acpi_call upower lxappearance-gtk3 \
jq inotify-tools polkit-gnome xdotool xclip gpick ffmpeg blueman redshift \
pipewire pipewire-alsa pipewire-pulse alsa-utils brightnessctl feh maim \
mpv mpd mpc mpdris2 python-mutagen ncmpcpp playerctl --needed
```

> Enable Services

```sh
systemctl --user enable mpd.service
systemctl --user start mpd.service
```

</details>

<details>
<summary><b>Install</b></summary>
<br>

> Clone this repository

```sh
git clone --depth 1 --recurse-submodules https://github.com/rxyhn/yoru.git
cd yoru && git submodule update --remote --merge
```

> Copy config files

```sh
cp -r config/* ~/.config/
```

> Install a few fonts (mainly icon fonts) in order for text and icons to be rendered properly.

Necessary fonts:

- **Roboto** - [here](https://fonts.google.com/specimen/Roboto)
- **Material Design Icons** - [here](https://github.com/google/material-design-icons)
- **Icomoon** - [here](https://www.dropbox.com/s/hrkub2yo9iapljz/icomoon.zip?dl=0)

Optional fonts:

- **My custom Iosevka build(Aesthetic Iosevka)** - [here](https://github.com/rxyhn/yoru/tree/main/misc/fonts/Aesthetic%20Iosevka)
- **Azuki Font** - [here](https://www.freejapanesefont.com/azuki-font-あずきフォント)

Once you download them and unpack them, place them into `~/.fonts` or `~/.local/share/fonts`.

Or you can find the required fonts inside the `misc/fonts` folder of this repository.

```sh
cp -r misc/fonts/* ~/.fonts/
# or to ~/.local/share/fonts
cp -r misc/fonts/* ~/.local/share/fonts/
```

And run this command for your system to detect the newly installed fonts.

```sh
fc-cache -fv
```

> Finally, now you can login with AwesomeWM

</details>

<!-- Aesthetic Iosevka Font -->

## :bookmark_tabs: ‎ <samp>Fonts</samp>

<b>Font Preview:</b>

- <details>
  <summary>Regular</summary>
  <br>
  <a href="#--------">
  <img src="https://user-images.githubusercontent.com/93292023/179895783-e4e96572-821c-4684-8b22-886f508d5e8e.png" alt="font preview" width="500px">
  </a>
  </details>

- <details>
  <summary>Italic</summary>
  <br>
  <a href="#--------">
  <img src="https://user-images.githubusercontent.com/93292023/179895825-5dade677-4fc6-4345-a564-719a649c0f2d.png" alt="font preview" width="500px">
  </a>
  </details>

<b>Installation:</b>

1. Clone or Download this repository
2. Change the current directory to `yoru/misc/fonts/Aesthetic Iosevka`
3. Choose the variant you want, or choose both

<b>Usage:</b>

- Original:

  ```json
  "editor.fontFamily": "Aesthetic Iosevka Original",
  "editor.fontLigatures": true,
  ```

- Nerd Font:

  ```json
  "editor.fontFamily": "AestheticIosevka Nerd Font",
  "editor.fontLigatures": true,
  ```
