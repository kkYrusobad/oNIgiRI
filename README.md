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
- **App Launcher**: Browse and launch all apps with icons
- **My Apps**: Custom web apps and TUI apps you create
- **Web App Creator**: Turn any website into a PWA-style app
- **TUI App Creator**: Create launcher shortcuts for terminal tools
- **Screenshots**: Region, fullscreen, clipboard via grim/slurp
- **Toggles**: Screensaver, nightlight (gammastep/wlsunset)
- **Setup**: Audio, WiFi, Bluetooth, Power profiles via Noctalia
- **Screensaver**: terminaltexteffects with swayidle integration

## Menu Structure

| Menu | Items |
|------|-------|
| **My Apps** | Your custom web/TUI apps |
| **Learn** | Keybindings, Niri Wiki, Arch Wiki |
| **Trigger** | Screenshot, Toggle (Screensaver, Nightlight) |
| **Style** | Theme, Niri Config, Screensaver, About |
| **Setup** | Audio, WiFi, Bluetooth, Power, Settings, Dark Mode |
| **Install** | Web App, TUI App |
| **About** | System info |
| **System** | Lock, Screensaver, Suspend, Restart, Shutdown |

## Creating Apps

### Web Apps

Create PWA-style web apps that open in a minimal browser window:

```bash
niri-webapp-install  # Interactive mode
# Or: niri-webapp-install "Gmail" "https://mail.google.com" "https://icon-url.png"
```

### TUI Apps

Create launcher entries for terminal tools with float/tile window options:

```bash
niri-tui-install  # Interactive mode
# Or: niri-tui-install "Docker" "lazydocker" "float" "https://icon-url.png"
```

## Dependencies

```bash
# Core
niri alacritty fuzzel gum swayidle curl

# Screenshot
grim slurp wl-copy satty

# Setup TUIs
impala bluetui

# Optional
gammastep terminaltexteffects papirus-icon-theme
```

## Noctalia Integration

Uses Noctalia shell IPC for:

- `controlCenter toggle` - Audio controls
- `settings toggle` - Settings panel
- `powerProfile set/cycle` - Power profiles
- `darkMode toggle` - Theme switching
- `lockScreen lock` - Lock screen

## Directory Structure

```text
bin/          # Scripts (niri-menu, niri-webapp-install, etc.)
branding/     # Assets (screensaver.txt, about.txt)
config/       # Terminal configs
niri/         # config.kdl with TUI window rules
```

## Credits

Ported from Omarchy OS. Uses Noctalia shell.
