# Premium Container — Brand Palette

Sampled from the Instagram logo (canvas pixel sampling of the profile avatar) and from the
product photography in the feed. Hex values are measured, not guessed.

## Core (from the logo)
| Role | Hex | Notes |
|---|---|---|
| Brand orange (primary) | `#ED7310` | The house/container mark. Cluster measured #DE7218–#F67206; #ED7310 is the centre |
| Ink (wordmark) | `#0A0A0A` | "PREMIUM CONTAINER" text, near-black |
| Base | `#FFFFFF` | Logo background |

## Supporting neutrals (from product photos)
| Role | Hex | Where it comes from |
|---|---|---|
| Anthracite | `#2E3234` | Container frames, window joinery, dark-clad units |
| Steel grey | `#8A8A8D` | Roller shutters, sheet-metal panels |
| Warm wood | `#6F4B2A` | Wood/cedar cladding on the flagship units |
| Sky | `#6090C0` | Outdoor photo backgrounds — use only as a photo tone, not UI |

## Suggested UI ramp for the build
```
--brand-500: #ED7310;   /* CTAs, links, accents */
--brand-600: #D4650B;   /* hover */
--brand-100: #FDEBDA;   /* tint backgrounds */
--ink-900:   #0A0A0A;   /* headings */
--ink-700:   #2E3234;   /* body text, dark sections */
--ink-400:   #8A8A8D;   /* muted text, borders */
--paper-50:  #FAF9F7;   /* page background */
--paper-0:   #FFFFFF;   /* cards */
--wood-600:  #6F4B2A;   /* optional warm accent, used sparingly */
```

## Usage notes
- Orange is a small-area accent: buttons, active states, icon strokes, section eyebrows. Large
  orange fills will fight the product photography, which is already warm (wood) and high-contrast.
- Dark sections should use `--ink-700` (#2E3234), not pure black — it matches the anthracite
  cladding in the photos and keeps photo edges from disappearing into the background.
- Contrast: #ED7310 on white is ~3.0:1 — fine for large text and UI, NOT for body copy.
  For orange text on white use `#B8560A` or darker. White text on #ED7310 is ~3.3:1, so use it
  only at 18px+/bold on buttons; otherwise put `#0A0A0A` text on the orange button.
- Logo has a white circular ground on IG. Get the original file before placing it on any dark
  section — otherwise it needs a white pill behind it.

## Status
- Logo source file: NOT RECEIVED. Colours above were sampled from a 150×150 avatar, so treat
  #ED7310 as accurate to within a couple of points until the vector arrives.
