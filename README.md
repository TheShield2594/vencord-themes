# Vencord Themes

Seven full Discord themes for [Vencord](https://vencord.dev) (also works in Vesktop and BetterDiscord).
All of them support dark, light, Darker and Midnight, and Discord's 2025 visual refresh.

| Theme | Look |
| --- | --- |
| **Clarity** (`Clarity.theme.css`) | visionOS-inspired and minimal. Neutral glass lit from above, neutral selection instead of colored fills, capsule controls, accent used only for actions. |
| **Orchard** (`Orchard.theme.css`) | Apple-style. Liquid Glass materials, SF typography, iOS switches, macOS menus, a Dock-style server rail, iMessage bubbles. |
| **Nothing** (`Nothing.theme.css`) | Nothing OS-inspired. Monochrome, dot-matrix type, a dot-grid backdrop, floating cards, one red accent. |
| **Mica** (`Mica.theme.css`) | Windows 11 / Fluent-inspired. Mica backdrop, Acrylic flyouts, the accent pill on selected items, Segoe UI Variable, Win11 controls. |
| **Tonal** (`Tonal.theme.css`) | Material You-inspired. One seed colour builds the whole tonal palette; expressive shapes, pill indicators, icons that morph and bounce. |
| **Operator** (`Operator.theme.css`) | Inspired by boutique synth hardware. Brushed-aluminium chassis (graphite in dark), an LCD channel header, knob buttons, LEDs, four key colours. |
| **Encore** (`Encore.theme.css`) | Spotify-inspired. Black frame with floating panels, bold Figtree type, green pill buttons, a Now Playing user panel with an equalizer in voice. |

## Install

**Online (auto-updates):** open Vencord Settings → Themes → Online Themes, and paste one of these:

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Clarity.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Orchard.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Nothing.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Mica.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Tonal.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Operator.theme.css
```

```
https://raw.githubusercontent.com/TheShield2594/vencord-themes/main/Encore.theme.css
```

**Local (to customise):** download the `.css` file, open Vencord Settings → Themes → Open Themes Folder, drop it in, and enable it.

**BetterDiscord:** download the `.css` file, open Settings → Themes → Open Themes Folder, drop it in, and enable it. All files already use the `.theme.css` name BetterDiscord needs.

## Customise

Each theme has a settings block at the top of the file. To change a setting, edit the value in your local copy, or set it in Vencord's QuickCSS so it survives updates:

```css
:root {
  --clarity-radius: 16px;           /* Clarity: tighter corners */
  --orchard-accent-dark: #BF5AF2;   /* Orchard: purple accent */
  --orchard-bubbles: off;           /* Orchard: plain messages */
  --n-accent: #c2410c;              /* Nothing: burnt orange (5.2:1 with white text) */
  --tonal-seed: #006A60;            /* Tonal: a teal palette */
  --encore-eq: 0;                   /* Encore: still equalizer bars */
}
```

### Clarity

| Variable | Default | What it does |
| --- | --- | --- |
| `--clarity-accent-dark` / `-light` | `#0A84FF` / `#007AFF` | Accent for buttons, links, focus rings and checkboxes. Selection stays neutral |
| `--clarity-wallpaper-dark` / `-light` | gradients | The environment behind the glass; use `url(...) center / cover` for a photo |
| `--clarity-blur`, `--clarity-saturate` | `48px`, `160%` | Glass strength |
| `--clarity-gap` | `10px` | Space between floating panes |
| `--clarity-radius` | `22px` | Pane corners. Menus, rows, cards and chips scale from it |

Clarity has no on/off switches, so it looks the same in every Chromium and Firefox build. It respects *Reduce motion* and *Reduce transparency* the same way Orchard does.

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

### Mica

| Variable | Default | What it does |
| --- | --- | --- |
| `--mica-accent-dark` / `-light` | `#60CDFF` / `#005FB8` | Accent for buttons, toggles, selection pills, focus underlines and links. Dark mode puts black text on it and light mode white, so keep the dark accent light and the light accent deep |
| `--mica-wallpaper-dark` / `-light` | gradients | The "desktop" Mica tints itself from; use `url(...) center / cover` for a photo |
| `--mica-radius` | `8px` | Corners of cards, flyouts and dialogs. Controls use half of it |
| `--mica-gap` | `6px` | Space around the chat card; `0px` for edge-to-edge |
| `--mica-blur` | `30px` | Acrylic blur strength for menus, popouts and the user panel |

Mica loads no web fonts; it uses Segoe UI Variable when your system has it, and falls back to Inter or the system font. It respects *Reduce motion* and *Reduce transparency*; with reduced transparency, Mica and Acrylic become solid.

### Tonal

| Variable | Default | What it does |
| --- | --- | --- |
| `--tonal-seed` | `#6750A4` | The one colour the whole palette is built from (primary, containers, tinted surfaces). Medium-to-dark colours work best |
| `--tonal-tertiary` | `#7D5260` | Companion accent for mentions, the "new mentions" bar and highlights |
| `--tonal-radius` | `28px` | Pane and dialog corners; cards, fields, chips and tooltips scale from it |
| `--tonal-gap` | `8px` | Space between floating panes; `0px` for flush |
| `--tonal-expressive` | `1` | Squish-and-overshoot spring on icons, reactions and menus; `0` keeps the shape changes without the bounce |

Tonal loads Google Sans Flex, Roboto Flex and Roboto Mono from Google Fonts.

### Operator

| Variable | Default | What it does |
| --- | --- | --- |
| `--op-accent` | `#ff5a00` | Main accent: buttons, selection LED, focus, sliders. Black text sits on it, so keep it bright |
| `--op-blue` | `#0071bb` | Links, embed edge, bot tags, mic knob |
| `--op-green` | `#00a85a` | Online status, unread LEDs, switches, typing dots, headset knob |
| `--op-white` | `#e8e8e4` | Neutral key colour, settings knob |
| `--op-orange` | `#ff5a00` | Mentions, badges, danger, muted and deafened knobs |
| `--op-texture` | `1` | Brushed-metal grain; `0` for flat surfaces |
| `--op-radius` | `6px` | Key and module corners |
| `--op-gap` | `8px` | Space between modules; `0px` for a flush layout |

Operator loads Inter and JetBrains Mono from Google Fonts.

### Encore

| Variable | Default | What it does |
| --- | --- | --- |
| `--encore-accent` | `#1ED760` | Accent for buttons, the active channel, toggles, badges and the equalizer. Black text and icons sit on it, so keep it bright |
| `--encore-header-tint` | `var(--encore-accent)` | Colour of the gradient at the top of the chat, Friends and settings views |
| `--encore-radius` | `8px` | Panel corners. Rows, cards and modals scale from it |
| `--encore-gap` | `8px` | Space between the floating panels; `0px` makes them flush |
| `--encore-eq` | `1` | Animated equalizer while you're in voice; `0` shows still bars |

Encore loads Figtree from Google Fonts.

## Notes

- Orchard's on/off switches use CSS style queries, which need Chromium 111 or newer. That covers the Discord desktop app, Vesktop and Chrome. In Firefox the switchable features stay off.
- A few rules match Discord's English button labels (Orchard's traffic lights; the mute, deafen and disconnect buttons in Nothing, Mica, Tonal, Operator and Encore). In other languages those parts fall back to Discord's own styling.
- Discord renames its CSS classes now and then. If something looks off after a Discord update, please open an issue.
