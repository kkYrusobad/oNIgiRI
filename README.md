```text
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
- **Package Manager**: Install/remove packages with fzf + animated globe spinner
- **My Apps**: Custom web apps and TUI apps you create
- **Web App Creator**: Turn any website into a PWA-style app
- **TUI App Creator**: Create launcher shortcuts for terminal tools
- **Screenshots**: Region, fullscreen, clipboard via grim/slurp
- **Toggles**: Screensaver, nightlight (gammastep/wlsunset)

## Menu Structure

| Menu | Items |
|------|-------|
| **󱍕 My Apps** | Your custom web/TUI apps |
| **󰠮 Learn** | Keybindings, Niri Wiki, Arch Wiki |
| **󰹑 Trigger** | Screenshot, Toggle (Screensaver, Nightlight) |
| **󰃣 Style** | Theme, Niri Config, Screensaver, About |
| **󰒓 Setup** | Audio, WiFi, Bluetooth, Power, Settings |
| **󰏔 Install** | Package, AUR Package, Web App, TUI App |
| **󱧖 Remove** | Package, My App |
| **󰋽 About** | System info |
| **󱩊 System** | Lock, Screensaver, Suspend, Restart, Shutdown |

## Dependencies

```bash
# Core
niri alacritty fuzzel gum fzf swayidle curl yay

# Screenshot
grim slurp wl-copy satty

# Setup TUIs
impala bluetui

# Optional
gammastep terminaltexteffects papirus-icon-theme
```

## Credits

Ported from Omarchy OS. Uses Noctalia shell.
