# Themes

Qt Stylesheets and community-made themes for GameModManager.

## Theme Format

Each theme consists of:
- `tokens.json` - Color tokens (variables) used by the stylesheet
- `*.qss` - Qt Stylesheet with token references
- `theme.json` (optional) - Theme metadata (see below)

### Theme Metadata

`theme.json` is an optional metadata file. The only supported field is
`base_style`, the Qt style the theme should be rendered with:

```json
{
  "base_style": "Fusion"
}
```

When present, GameModManager applies that Qt style before the QSS so the
theme renders consistently on platforms whose native style (Breeze, adwaita,
...) does not fully respect QSS. If the style is not available on the system,
a warning is logged and the theme is applied with the active style. Themes
without `theme.json` are style-agnostic and keep the current style.

### Token Variables

Themes use a token-based color system. Tokens are defined in `tokens.json` and referenced in QSS files using `$` prefix:

```json
{
  "$bg": "#2e3440",
  "$bgAlt": "#3b4252",
  "$bgInput": "#232831",
  "$fg": "#d8dee9",
  "$fgMuted": "#7b88a1",
  "$accent": "#88c0d0",
  "$accentHover": "#a5cde0",
  "$accentFg": "#2e3440",
  "$border": "#434c5e",
  "$selected": "#5e81ac",
  "$danger": "#bf616a",
  "$dangerBg": "#8b0000"
}
```

### Available Tokens

| Token | Description |
|-------|-------------|
| `$bg` | Main background color |
| `$bgAlt` | Alternative background (buttons, panels) |
| `$bgInput` | Input field backgrounds |
| `$fg` | Primary foreground text |
| `$fgMuted` | Muted/disabled text |
| `$accent` | Primary accent color (links, highlights) |
| `$accentHover` | Hover state accent |
| `$accentFg` | Text color on accent backgrounds |
| `$border` | Border color |
| `$selected` | Selection highlight |
| `$danger` | Error/danger color |
| `$dangerBg` | Danger background |

### Creating a Theme

1. Create a new directory with your theme name
2. Create `tokens.json` with the required color tokens
3. Create a `.qss` file using `$token` references
4. Optionally create `theme.json` declaring a `base_style` (e.g. `"Fusion"`)
5. Use the default.qss as a reference for the complete stylesheet structure

## Included Themes

- **Dark** - Dark theme with blue accents
- **Nord** - Inspired by Nord color palette