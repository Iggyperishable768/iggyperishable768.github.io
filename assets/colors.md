# Open OCPP Trace Colors

All values below were extracted directly from the current official SVG assets (`logos/logo.svg`, `logos/logo-dark.svg`, `logos/avatar-dark.svg`, and the banner source). Colors are reported as authored; no new colors were introduced.

## Core palette

| Semantic name | HEX | RGB | Observed use |
| --- | --- | --- | --- |
| Accent | `#33b1d4` | `51, 177, 212` | Symbol stroke (brackets + pulse) on all variants; `OCPP` emphasis on dark |
| Accent (on light) | `#1f7d97` | `31, 125, 151` | `OCPP` emphasis in the light lockup (darker teal for contrast on white) |
| Background — dark | `#0d1117` | `13, 17, 23` | Dark tile / lockup / banner background |
| Background — light | `#ffffff` | `255, 255, 255` | Light lockup background |
| Foreground — dark | `#e6edf3` | `230, 237, 243` | Wordmark text on dark |
| Foreground — light | `#1f2328` | `31, 35, 40` | Wordmark text on light |
| Muted — light | `#8b949e` | `139, 148, 158` | Slug text (`open-ocpp-trace`) on light |
| Muted — dark | `#7d8590` | `125, 133, 144` | Slug/tagline text on dark |
| Banner divider | `#161b22` | `22, 27, 34` | Horizontal baseline in the README banner |
| Banner trace (faint) | `#1d3a44` | `29, 58, 68` | Decorative background pulse in the README banner |

## Backgrounds

- **Light lockup** — designed for `#ffffff` and other light, low-saturation surfaces.
- **Dark lockup** — designed for `#0d1117` and other dark/neutral surfaces.
- **Transparent avatar** — has no background of its own; place only on surfaces that keep enough contrast against the `#33b1d4` symbol (avoid mid-tone teals/cyans).
- **README banner** — self-contained on `#0d1117`; do not place it on an additional colored panel.

## Accessibility

Contrast ratios are calculated per WCAG 2.x (relative luminance). "Decorative" means the logo symbol itself, which is exempt from text contrast requirements; "text" means wordmark/supporting copy.

| Foreground | Background | Ratio | Assessment |
| --- | --- | --- | --- |
| `#e6edf3` (text) | `#0d1117` | ~16.0:1 | Passes AA and AAA for normal text |
| `#1f2328` (text) | `#ffffff` | ~15.8:1 | Passes AA and AAA for normal text |
| `#33b1d4` (decorative / `OCPP` on dark) | `#0d1117` | ~7.5:1 | Passes AA (all) and AAA for normal text |
| `#1f7d97` (`OCPP` on light) | `#ffffff` | ~4.7:1 | Passes AA for normal text; does not reach AAA |
| `#7d8590` (supporting text) | `#0d1117` | ~5.1:1 | Passes AA for normal text |
| `#8b949e` (supporting text) | `#ffffff` | ~3.1:1 | Large text only (≥18.66px bold / ≥24px); do **not** use for small text |
| `#33b1d4` | `#ffffff` | ~2.5:1 | Decorative only — do **not** use for text of any size |

Notes:
- The accent (`#33b1d4`) has sufficient contrast for text on the dark background but not on white; that is why the light lockup uses `#1f7d97` for the `OCPP` emphasis.
- `#8b949e` on white and `#33b1d4` on white should not be used for small body text.
- These ratios describe the brand assets as authored; they are not a blanket claim of WCAG compliance for any product UI built on top of them.

## CSS custom properties

```css
:root {
  --oot-color-accent: #33b1d4;
  --oot-color-accent-on-light: #1f7d97;
  --oot-color-background-dark: #0d1117;
  --oot-color-background-light: #ffffff;
  --oot-color-foreground-dark: #e6edf3;
  --oot-color-foreground-light: #1f2328;
  --oot-color-muted-dark: #7d8590;
  --oot-color-muted-light: #8b949e;
}
```
