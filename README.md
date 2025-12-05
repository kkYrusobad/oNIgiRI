```
         ███╗   ██╗██╗ ██████╗ ██╗██████╗ ██╗
  ██████╗████╗  ██║██║██╔════╝ ██║██╔══██╗██║
 ██╔═══██╗██╔██╗ ██║██║██║  ███╗██║██████╔╝██║
 ██║   ██║██║╚██╗██║██║██║   ██║██║██╔══██╗██║
 ╚██████╔╝██║ ╚████║██║╚██████╔╝██║██║  ██║██║
  ╚═════╝ ╚═╝  ╚═══╝╚═╝ ╚═════╝ ╚═╝╚═╝  ╚═╝╚═╝
```

# oNIgiRI - Niri Omarchy Port

A port of the Omarchy OS UX to the Niri window manager, integrated with Noctalia shell.

## Features

- **System Menu** (`MOD+M`): fuzzel-based menu with Noctalia styling
- **Screenshots**: Region, fullscreen, clipboard via grim/slurp
- **Toggles**: Screensaver, nightlight (gammastep/wlsunset)
- **Setup**: Audio, WiFi, Bluetooth, Power profiles via Noctalia
- **Screensaver**: terminaltexteffects with swayidle integration
- **Gum confirmations**: Styled dialogs for dangerous actions

## Dependencies

```bash
# Core
niri alacritty fuzzel gum swayidle

# Screenshot
grim slurp wl-copy satty

# Setup TUIs
impala bluetui

# Optional
gammastep terminaltexteffects
```

## Menu Structure

| Menu | Items |
|------|-------|
| **Learn** | Keybindings, Niri Wiki, Arch Wiki |
| **Trigger** | Screenshot, Toggle (Screensaver, Nightlight) |
| **Style** | Theme, Niri Config, Screensaver, About |
| **Setup** | Audio, WiFi, Bluetooth, Power, Settings, Dark Mode |
| **About** | System info |
| **System** | Lock, Screensaver, Suspend, Restart, Shutdown |

## Noctalia Integration

Uses Noctalia shell IPC for:

- `controlCenter toggle` - Audio controls
- `settings toggle` - Settings panel
- `powerProfile set/cycle` - Power profiles
- `darkMode toggle` - Theme switching
- `lockScreen lock` - Lock screen

## Directory Structure

```text
bin/          # Scripts (niri-menu, niri-cmd-screenshot, etc.)
branding/     # Assets (screensaver.txt, about.txt)
config/       # Terminal configs
niri/         # config.kdl
```

## Credits

Ported from Omarchy OS. Uses Noctalia shell.
