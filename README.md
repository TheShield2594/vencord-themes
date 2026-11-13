# Vencord Themes

Two full Discord themes for [Vencord](https://vencord.dev) (also works in Vesktop and BetterDiscord).
Both support dark, light, Darker and Midnight, and Discord's 2025 visual refresh.

| Theme | Look |
| --- | --- |
| **Orchard** (`Orchard.theme.css`) | Apple-style. Liquid Glass materials, SF typography, iOS switches, macOS menus, a Dock-style server rail, iMessage bubbles. |
| **Nothing** (`Nothing.theme.css`) | Nothing OS-inspired. Monochrome, dot-matrix type, a dot-grid backdrop, floating cards, one red accent. |

## Install

**Online (auto-updates):** open Vencord Settings → Themes → Online Themes, and paste one of these:

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Orchard.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Nothing.theme.css
```

**Local (to customise):** download the `.css` file, open Vencord Settings → Themes → Open Themes Folder, drop it in, and enable it.

**BetterDiscord:** download the `.css` file, open Settings → Themes → Open Themes Folder, drop it in, and enable it. Both files already use the `.theme.css` name BetterDiscord needs.

## Customise

Each theme has a settings block at the top of the file. To change a setting, edit the value in your local copy, or set it in Vencord's QuickCSS so it survives updates:

```css
:root {
  --orchard-accent-dark: #BF5AF2;   /* Orchard: purple accent */
  --orchard-bubbles: off;           /* Orchard: plain messages */
  --n-accent: #ff6a00;              /* Nothing: orange accent */
}
```

### Orchard

| Variable | Default | What it does |
| --- | --- | --- |
| `--orchard-dock` | `on` | Turns the server rail into a macOS Dock with magnification |
| `--orchard-traffic-lights` | `on` | Shows red, yellow and green window buttons (Windows/Linux) |
| `--orchard-liquid-glass` | `on` | Adds a prismatic rim and top sheen to glass panels |
| `--orchard-bubbles` | `on` | Shows iMessage-style bubbles (cozy display mode only) |
| `--orchard-accent-dark` / `-light` | `#0A84FF` / `#007AFF` | Accent color; the wallpaper glow follows it |
| `--orchard-wallpaper-dark` / `-light` | gradients | Background behind the glass; use `url(...) center / cover` for a photo |
| `--orchard-blur`, `--orchard-saturate` | `40px`, `180%` | Glass strength |
| `--orchard-gap` | `8px` | Space between floating panels |

Orchard respects the OS settings *Reduce motion* and *Reduce transparency*, and Discord's own *Reduced Motion* setting. With reduced transparency, the glass switches to solid surfaces.

### Nothing

| Variable | Default | What it does |
| --- | --- | --- |
| `--n-accent` | `#d71921` | Accent color. Pick a saturated color: white text and icons sit on it, so very light colors become unreadable |
| `--n-dot-opacity` | `1` | Dot-grid strength; `0` turns it off |
| `--n-dot-size` | `14px` | Dot-grid spacing |
| `--n-gray-icons` | `1` | Shows server icons in grayscale until you hover them; `0` for color |
| `--n-blink` | `1` | Blinks the red dot on the active channel; `0` for a static dot |
| `--n-gap` | `8px` | Card spacing; `0px` makes the panels flush |
| `--n-radius`, `--n-radius-sm` | `20px`, `12px` | Corner roundness |

Nothing loads Doto, Space Grotesk and Space Mono from Google Fonts.

## Notes

- Orchard's on/off switches use CSS style queries, which need Chromium 111 or newer. That covers the Discord desktop app, Vesktop and Chrome. In Firefox the switchable features stay off.
- A few rules match Discord's English button labels (traffic lights, the mute and deafen buttons in Nothing). In other languages those parts fall back to Discord's own styling.
- Discord renames its CSS classes now and then. If something looks off after a Discord update, please open an issue.
