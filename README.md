```
         M"""""""`YM M""M          oo MM"""""""`MM M""M 
         M  mmmm.  M M  M             MM  mmmm,  M M  M 
.d8888b. M  MMMMM  M M  M .d8888b. dP M'        .M M  M 
88'  `88 M  MMMMM  M M  M 88'  `88 88 MM  MMMb. "M M  M 
88.  .88 M  MMMMM  M M  M 88.  .88 88 MM  MMMMM  M M  M 
`88888P' M  MMMMM  M M  M `8888P88 dP MM  MMMMM  M M  M 
         MMMMMMMMMMM MMMM      .88    MMMMMMMMMMMM MMMM 
                           d8888P                       
```

# Niri Omarchy Port

A port of the Omarchy OS user experience, aesthetics, and tooling to the Niri window manager on Wayland. This project aims to bring the curated, minimalist, and keyboard-driven workflow of Omarchy to Niri.

## Features

- **Custom Niri Configuration**: A tuned `config.kdl` with keybindings and window rules.
- **Screensaver System**: A custom screensaver implementation using `terminaltexteffects` (tte), compatible with Alacritty, Ghostty, and Kitty.
- **Application Management**: Helper scripts for launching and focusing applications (`niri-launch-or-focus`), supporting both GUI and TUI apps.
- **Branding**: Custom branding assets and text effects.

## Directory Structure

- `bin/`: Helper scripts for Niri (launchers, screensaver controls, etc.).
- `branding/`: Branding assets (e.g., screensaver text).
- `config/`: Application configurations (Alacritty, Ghostty, etc.).
- `niri/`: Main Niri configuration file (`config.kdl`).

## Installation & Usage

1. **Dependencies**: Ensure you have `niri`, `alacritty` (or `ghostty`/`kitty`), `swayidle`, and `terminaltexteffects` (tte) installed.
2. **Configuration**: Symlink or copy the `niri/config.kdl` to your Niri configuration directory (usually `~/.config/niri/config.kdl`).
3. **Scripts**: Add the `bin/` directory to your `$PATH` or ensure the scripts are accessible.
4. **Assets**: Place the `branding` and `config` directories in appropriate locations or update the paths in the scripts/config accordingly.

## Ported Scripts

1. **Screensaver Launcher**: Implements swayidle integration to launch the screensaver.

    The screensaver is handled by `niri-launch-screensaver` and `niri-cmd-screensaver`. It uses `terminaltexteffects` to display a visual effect.
    - **Manual Start**: Run `niri-launch-screensaver force`.
    - **Toggle**: Run `niri-toggle-screensaver`.
    - **Configuration**: Check `config/alacritty/screensaver.toml` or equivalent for other terminals.
    - **Swayidle Integration**: The screensaver is triggered by `swayidle` when the session is idle.

2. **Niri About Popup**: Displays the "About" window for the project.

## Credits

Ported from Omarchy OS.
