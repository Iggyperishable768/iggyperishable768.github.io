# Open OCPP Trace Brand

## Identity

Open OCPP Trace is an open, vendor-neutral initiative defining a common, versioned and tool-independent format for exchanging, storing and analyzing OCPP traces. Its visual identity pairs a **symbol** — a signal/pulse waveform enclosed in square brackets — with an **OCPP-oriented wordmark**, "Open **OCPP** Trace". The brackets evoke inspection and structured data; the pulse evokes the trace/signal being captured; the emphasized monospaced `OCPP` anchors the mark in the protocol it serves. A single accent (`#33b1d4`) carries the symbol across light and dark surfaces.

## Assets

Paths are relative to this `assets/` directory.

| File | Purpose | Recommended usage | Background requirements |
| --- | --- | --- | --- |
| `logos/avatar-dark.svg` | Square avatar / app mark (512×512, `rx=96`) | GitHub org avatar, social profile | Self-contained dark tile (`#0d1117`); place on any background |
| `logos/avatar.svg` | Symbol only, no tile (512×512, transparent) | Overlays, custom backgrounds, single-color contexts | Requires a background with enough contrast against `#33b1d4` |
| `logos/logo-dark.svg` | Horizontal lockup, symbol + wordmark (760×220) | Docs headers, footers, dark UI | Dark surfaces (built-in `#0d1117` fill) |
| `logos/logo.svg` | Horizontal lockup, symbol + wordmark (760×220) | Docs, print, light UI | Light surfaces (built-in `#ffffff` fill) |
| `banners/banner.png` | README / repo banner (raster) | Top of README, landing pages | Self-contained dark banner |
| `banners/banner.svg` | README / repo banner (vector source) | Scalable banner, editing source | Self-contained dark banner |
| `favicons/favicon.svg` | Scalable favicon (dark tile, `rx=26`) | Browser tab icon (modern browsers) | Self-contained |
| `favicons/favicon-16.png`, `favicons/favicon-32.png`, `favicons/favicon-48.png` | Raster favicons | Legacy favicon fallbacks | Self-contained |
| `favicons/apple-touch-icon-180.png` | Apple touch icon (180×180) | iOS home-screen icon | Self-contained |
| `favicons/favicon-512.png` | Large raster mark | PWA / high-DPI icon slots | Self-contained |

## Logo usage

- **Avatar** — use where the brand appears as a small, square/circular slot with no accompanying text (org avatar, social profiles, favicons). Prefer `logos/avatar-dark.svg`; use `logos/avatar.svg` (transparent) only when placing the symbol on a controlled background.
- **Full lockup** — use where there is horizontal room and the brand name should be legible (documentation headers, site footers, presentations). Choose the variant that matches the surface.
- **README banner** — use once, at the top of a README or landing page, as the primary brand statement. It already includes symbol, wordmark, tagline and org URL, so it does not need an additional lockup beside it.

**Variant selection**

- **Dark** variants (`logos/logo-dark.svg`, `logos/avatar-dark.svg`) — for dark or neutral surfaces.
- **Light** variant (`logos/logo.svg`) — for white/light surfaces. Note the `OCPP` emphasis shifts to a darker teal (`#1f7d97`) for contrast on white.
- **Transparent** variant (`logos/avatar.svg`) — when you must composite the symbol over imagery or a brand color and can guarantee contrast.

## Usage rules

- Preserve the original aspect ratio of every asset.
- Do not stretch, squash, rotate or distort the logo.
- Do not recolor individual logo components (brackets, pulse, wordmark parts).
- Maintain sufficient contrast between the mark and its background (see `colors.md`).
- Do not add drop shadows, glows, outlines or other effects.
- Use the supplied asset files; do not recreate or trace the logo by hand.

## Clear space and minimum size

No formal clear-space or minimum-size rules have been defined yet. As a working guideline derived from the assets: the lockups place the symbol with roughly half a symbol-width of internal padding before the wordmark, which can serve as a reasonable minimum clear space around the whole lockup. Always check legibility at the target rendered size before shipping — the pulse detail inside the brackets is the first thing to break down when the mark is scaled down.

## Typography

Typography is referenced by name in the SVG source (not embedded as outlines):

- **Wordmark ("Open … Trace")** — `Space Grotesk`, weight 500, with `system-ui, sans-serif` fallback.
- **`OCPP` emphasis and supporting/monospaced text** (slug, tagline) — `JetBrains Mono`, weight 700 for `OCPP`, with `monospace` fallback.

Consumers should not rely on these fonts being available on a given system unless they are explicitly bundled or linked. For fixed-size brand rendering, prefer the provided raster assets (banner, favicons) or convert the SVG text to outlines. The exact licensing of the fonts is unspecified here and should be confirmed before redistribution.

## Colors

See [`colors.md`](./colors.md) for the full palette, background guidance, accessibility notes and CSS custom properties.

## Repository usage

These assets are the single source of truth and are hosted from the
`open-ocpp-trace.github.io` repository, served at
`https://open-ocpp-trace.github.io/assets/...`.

**From another repository or website** (e.g. the org profile README), reference
the hosted URLs so there is only one copy to maintain:

```markdown
![Open OCPP Trace](https://open-ocpp-trace.github.io/assets/banners/banner.png)
```

```markdown
![Open OCPP Trace](https://open-ocpp-trace.github.io/assets/logos/logo.svg)
```

```markdown
![Open OCPP Trace](https://open-ocpp-trace.github.io/assets/logos/logo-dark.svg)
```

Treat these paths as a stable public contract: GitHub proxies and caches README
images (via Camo), so moving or renaming a file silently breaks every consumer,
and replacing a file in place may not refresh immediately. To force a refresh,
publish under a new path (e.g. `assets/v2/...`).

**Within this repository**, relative paths work as usual (e.g.
`assets/banners/banner.png` from `index.html`).

## Changes

Any modification to the official brand assets (or to this documentation) should be proposed and reviewed through a pull request, so the identity stays consistent across the organization.
