# Themes

Qt Stylesheets and community-made themes for GameModManager.

## Theme Format

Each theme consists of:
- `tokens.json` - Color tokens (variables) used by the stylesheet
- `*.qss` - Qt Stylesheet with token references

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
4. Use the default.qss as a reference for the complete stylesheet structure

## Included Themes

- **Dark** - Dark theme with blue accents
- **Nord** - Inspired by Nord color palette