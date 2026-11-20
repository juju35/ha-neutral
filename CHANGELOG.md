# Changelog

## 1.0.2 - 2026-11-20

### Fixes
- Status colors are readable as text in light and dark mode: every one of them (`green`, `amber`, `orange`, `yellow`, `blue`, `light-blue`, `cyan`, `teal`, `purple`, `deep-purple`, `red`, `grey`, and `success`/`warning`/`error`/`info`) now reaches a 4.5:1 contrast on the card and on the inner tiles, and 3:1 as an icon on its tinted pastille. Light mode: green, amber, orange, yellow, blue, light-blue, cyan, teal and grey are darker. Dark mode: orange, blue, light-blue, purple, deep-purple, red and grey are lighter. Hues are unchanged, and ha-liquid-glass uses the same palette.
- The blue accent (`primary`, `accent`, selected side-panel item) follows the new blue, and the active state icon the new amber.
- Every status color has its `rgb-*` variable, so translucent tints (icon pastilles, state badges) match the color instead of Home Assistant's default palette.

### Maintenance
- Validate: a new check computes the contrast of every status color on the theme's card, tile and dialog backgrounds, in light and dark, and fails below 4.5:1 (text) or 3:1 (icon on its pastille).

## 1.0.1 - 2026-11-20

### Fixes
- `rgb-primary-text-color` and `rgb-text-primary-color` are set in both modes, so the parts of Home Assistant that tint with them (hovers, ripples, text on the accent) match the theme's text colors instead of the default ones.
- Light mode: amber (`amber-color`, `warning-color`, `state-icon-active-color`) and yellow are darker — `#9f691b` and `#8e7109`, 4.6:1 on the white card instead of 3.6:1 and 3.45:1 — so a coloured state line ("Heating", "Charging"…) reads as text, not only as an icon.
- README: the validation badge is named after the Marketplace, as in the rest of the README.

### Maintenance
- Repository guide: the release reads the version from the top CHANGELOG entry (a theme has no `package.json`).
- Validate: `setup-python` pinned to a commit, and a new check that every `rgb-*` variable matches the color it shadows.

## 1.0.0 - 2026-11-18

### Features
- Neutral theme for Home Assistant, matching the ha-* cards: flat neutral gray page, opaque white (light) or charcoal (dark) cards, soft gray inner tiles.
- Light and dark modes in one theme (`modes:`); the dark mode also switches the ha-* illustrated headers to their night scene.
- Status palette of the ha-* cards applied to Home Assistant's color variables, so built-in state colors follow it: green OK, amber active, blue open, cyan cold, purple media, red alert, gray idle.
- 14px rounded cards with a hairline border and no shadow, calm app header and side panel with a blue accent.
