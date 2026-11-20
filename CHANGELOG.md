# Changelog

## 1.0.1 - 2026-11-20

### Fixes
- `rgb-primary-text-color` and `rgb-text-primary-color` are set in both modes, so the parts of Home Assistant that tint with them (hovers, ripples, text on the accent) match the theme's text colors instead of the default ones.

### Maintenance
- Validate: `setup-python` pinned to a commit, and a new check that every `rgb-*` variable matches the color it shadows.

## 1.0.0 - 2026-11-18

### Features
- Neutral theme for Home Assistant, matching the ha-* cards: flat neutral gray page, opaque white (light) or charcoal (dark) cards, soft gray inner tiles.
- Light and dark modes in one theme (`modes:`); the dark mode also switches the ha-* illustrated headers to their night scene.
- Status palette of the ha-* cards applied to Home Assistant's color variables, so built-in state colors follow it: green OK, amber active, blue open, cyan cold, purple media, red alert, gray idle.
- 14px rounded cards with a hairline border and no shadow, calm app header and side panel with a blue accent.
