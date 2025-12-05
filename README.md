```
         ███╗   ██╗██╗ ██████╗ ██╗██████╗ ██╗
  ██████╗████╗  ██║██║██╔════╝ ██║██╔══██╗██║
 ██╔═══██╗██╔██╗ ██║██║██║  ███╗██║██████╔╝██║
 ██║   ██║██║╚██╗██║██║██║   ██║██║██╔══██╗██║
 ╚██████╔╝██║ ╚████║██║╚██████╔╝██║██║  ██║██║
  ╚═════╝ ╚═╝  ╚═══╝╚═╝ ╚═════╝ ╚═╝╚═╝  ╚═╝╚═╝
```

# Niri Omarchy Port

A port of the Omarchy OS user experience, aesthetics, and tooling to the Niri window manager on Wayland. This project aims to bring the curated, minimalist, and keyboard-driven workflow of Omarchy to Niri.

## Features

- **Custom Niri Configuration**: A tuned `config.kdl` with keybindings and window rules.
- **System Menu**: Omarchy-style system menu (`niri-menu`) using fuzzel with Noctalia color scheme.
- **Screensaver System**: A custom screensaver implementation using `terminaltexteffects` (tte), compatible with Alacritty, Ghostty, and Kitty.
- **Application Management**: Helper scripts for launching and focusing applications (`niri-launch-or-focus`), supporting both GUI and TUI apps.
- **Branding**: Custom branding assets and text effects.

## Directory Structure

- `bin/`: Helper scripts for Niri (launchers, menu, screensaver controls, etc.).
- `branding/`: Branding assets (e.g., screensaver text).
- `config/`: Application configurations (Alacritty, Ghostty, etc.).
- `niri/`: Main Niri configuration file (`config.kdl`).

## Installation & Usage

1. **Dependencies**: Ensure you have `niri`, `alacritty` (or `ghostty`/`kitty`), `swayidle`, `fuzzel`, and `terminaltexteffects` (tte) installed.
2. **Configuration**: Symlink or copy the `niri/config.kdl` to your Niri configuration directory (usually `~/.config/niri/config.kdl`).
3. **Scripts**: Add the `bin/` directory to your `$PATH` or ensure the scripts are accessible.
4. **Assets**: Place the `branding` and `config` directories in appropriate locations or update the paths in the scripts/config accordingly.

## Ported Scripts

### System Menu

The system menu provides quick access to common actions via `MOD+M`.

| Script | Description |
|--------|-------------|
| `niri-menu` | Main menu with Learn, Style, About, System submenus |
| `niri-menu-keybindings` | Displays current Niri keybindings |

**Menu Structure:**

- **Learn**: Keybindings, Niri Wiki, Arch Wiki, Neovim, Bash
- **Style**: Theme, Niri Config, Screensaver, About Text
- **About**: System info via fastfetch
- **System**: Lock, Screensaver, Suspend, Restart, Shutdown

Uses **fuzzel** with the Noctalia Gruvbox color scheme and JetBrainsMono Nerd Font.

### Screensaver

The screensaver is handled by `niri-launch-screensaver` and `niri-cmd-screensaver`. It uses `terminaltexteffects` to display a visual effect.

- **Manual Start**: Run `niri-launch-screensaver force`
- **Toggle**: Run `niri-toggle-screensaver`
- **Configuration**: Check `config/alacritty/screensaver.toml` for terminal settings
- **Swayidle Integration**: Triggered automatically when the session is idle

### About Popup

Displays system info via `niri-launch-about`.

## Credits

Ported from Omarchy OS.
