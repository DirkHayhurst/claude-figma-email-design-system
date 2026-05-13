# Email / Promo Creative Design System — The Art of Shaving (TAOS)

Source of truth: Figma file **"Claude Design Draft 1.0"** (`exTo8Ks2w49bEFIyDmutyJ`),
Page 4. These rules are reverse-engineered from the labeled Father's Day artboard
set and the four layout-pattern references (`T1 Block Below`, `T2 Bottom Band`,
`T3 Side by Side`, `T4 Polaroid`). Use them to spin up new seasonal/promo
versions by **copying a template and swapping copy only**.

## 1. Artboard

- **Size:** 600 × 800 px.
- **Name pattern:** `TAOS / Hero / {Layout Variant} / Export`
  (when deriving a campaign version, insert the campaign before `Export`, e.g.
  `TAOS / Hero / Upper Half / Memorial / Export`).
- **Layout variants in use** (these change *where* the text block + scrim sit, not
  the type system): `Upper Right`, `Upper Half`, `Upper Right Light`,
  `Left Half Light`, `Lower Half Light`.
- **Color modes:**
  | | Background | Image placeholder | Body text | Fine print |
  |---|---|---|---|---|
  | Dark  | `#000000` | `#1A1A1A` | white | white |
  | Light | `#E6E6E6` | `#D9D9D9` | black | black |

## 2. Layer stack (bottom → top) — keep these names

| # | Layer name | What it is | Style |
|---|---|---|---|
| 1 | `⬇ DROP IMAGE HERE` | 600×800 placeholder rect; the photo-swap target | fill = image placeholder color |
| 2 | *(photo layers)* | grayscale lifestyle photography, intentionally oversized & bled off-canvas | — |
| 3 | `⚡ GRADIENT — Toggle Visibility` | semi-transparent scrim that sits **behind the whole text block** for legibility | `rgba(0,0,0,.5–.55)` dark / `rgba(255,255,255,.5–.55)` light; sized/positioned per layout variant |
| 4 | `Hero / Eyebrow Rule` | 1px accent-colored rule (optional) | accent color, 1px |
| 5 | `Hero / Eyebrow` | campaign / holiday name | Inter Semi Bold 16, **accent color**, ALL CAPS |
| 6 | `Hero / Pre` | small lead-in line (optional) | Inter Regular 13, `#D9D9D9` on dark |
| 7 | `Hero / Big` | the headline; the **offer** is the dominant element | Inter Bold 40–64; an inline `%` is set ~24 against ~52; may split to two stacked lines, 2nd line ~28–32 |
| 8 | `Hero / Sub Line 1` + `Hero / Sub Line 2` | supporting lines (offer detail + value prop) | Inter Medium 18, white/black, ALL CAPS |
| 9 | `Hero / CTA Button BG` | solid rectangle button | 39px tall; width = label + ~28px L/R padding; 1px solid border (white on dark / black on light); **fill = campaign accent** |
| 10 | `Hero / CTA Label` | text inside the button | Inter Medium 16, white (or accent on a light-green button) |
| 11 | `Hero / Code` / `Hero / Code Note` | fine print under the CTA — either a promo-code line (**three runs**: `Use code` · **`CODE`** (bold) · `at checkout`, Inter Regular 14) **or** a single auto-discount line (e.g. `No code required · Valid M/D–M/D/YY`) set in **Inter Italic 12** | see left |

## 3. Type ramp (Inter)

| Element | Size | Weight | Case |
|---|---|---|---|
| Eyebrow | 16 | Semi Bold | UPPER |
| Pre | 13 | Regular | UPPER |
| Big / headline | 40–64 (offer dominant) | Bold | UPPER |
| Big / 2nd line | 28–32 | Bold | UPPER |
| Sub line 1 & 2 | 18 | Medium | UPPER |
| CTA label | 16 | Medium | UPPER |
| Fine print / code | 14 (code = Bold) | Regular | Sentence |

## 4. Campaign accent colors & promo codes

| Campaign | Accent / CTA fill | Accent text | Code |
|---|---|---|---|
| St. Patrick's Day | `#378B59` | `#7FBF7F` | `LUCKY26` |
| Spring sale | `#B3231E` | — | `SPRING26` |
| Father's Day | `#B3231E` | — | `DAD26` |
| Memorial Day | `#B3231E` (red already in palette; on-holiday) | — | none — automatic discount, fine print reads `No code required` |

Promo-code pattern (when a code is used): **`{CAMPAIGN}{YY}`**. Keep codes short
(≤6 chars) so the three-run fine print doesn't reflow. If the offer applies
automatically, drop the code entirely and use a single `No code required` line.

## 5. Copy-swap discipline (how to derive a new campaign correctly)

**Do:**
- Duplicate an existing campaign's frame set; rename `… / Export` →
  `… / {NewCampaign} / Export`.
- Change **text-layer contents only**, plus the CTA Button BG fill color and the
  promo code, to match the new campaign accent.
- Keep the headline hierarchy: the discount % stays the dominant `Hero / Big`
  element; details/dates go in `Hero / Sub Line 1/2` (and the 2nd big line if the
  template has one).
- After swapping copy, confirm the `⚡ GRADIENT` scrim still fully covers the
  headline + sub lines + CTA + code.

**Don't:**
- Don't move, rename, regroup, or resize layers; don't change the 600×800 artboard.
- Don't reflow or re-letter-space — accept minor width changes.
- Don't propagate the known bug where some Father's Day layers use
  `rgba(255,128,0,0.3)` (a leftover orange placeholder) for text — those should be
  white (dark mode) or black (light mode).

## 6. Layout-pattern references

The `T1`–`T4` artboards at the bottom of Page 4 are the canonical compositions:
- **T1 – Block Below:** text block sits below the image area.
- **T2 – Bottom Band:** solid accent band across the bottom carrying the CTA.
- **T3 – Side by Side:** image one side, text the other.
- **T4 – Polaroid:** image framed as a polaroid with copy around it.

---

## 7. v2 — creative-director upgrade (what "good" looks like)

The original templates work; v2 raises the bar. Principles applied (see the
`… / Memorial / v2 / Export` frames in the Figma file):

1. **One dominant element.** The headline (the offer % or the urgency line) is the
   hero — `~80–90px` Inter Bold, sized to fill the text zone. Nothing else competes.
2. **Four zones, max.** `wordmark → occasion eyebrow → giant headline → one
   detail+date line → CTA → fine print`. No duplicated numbers, no stacked sub-lines.
3. **Brand mark always present.** `THE ART OF SHAVING` wordmark, 12px Inter Medium,
   +14% tracking, top of the text block.
4. **Bigger CTA.** Solid accent button, **50px** tall, ≥230px wide, no border,
   label 17px Inter Semi Bold +4% tracking, white — comfortably tappable on mobile.
5. **Real gradient scrim, not a flat tint.** Linear gradient from ~92% opaque on
   the copy side to 0% on the far side (vertical for top/bottom-anchored layouts,
   horizontal for side-anchored), so contrast is guaranteed at any crop.
6. **Wide text zone.** Side-anchored layouts (`Upper Right*`) are re-anchored to a
   left column with the gradient covering ~70% of the width, so the headline gets
   room to be big.
7. **Detail line carries offer + dates** in one beat, e.g.
   `20% OFF SITEWIDE  ·  ENDS SUNDAY` (timed sends) or `SITEWIDE SAVINGS  ·  MAY 21–25`.
8. **Fine print** = `No code required — applied automatically`, 11px Inter Italic, 70% opacity.

### Still on the roadmap (not yet built)
- Ship as **responsive HTML email modules** (live text + bulletproof VML buttons),
  not sliced flat PNGs — better deliverability, accessibility, dark-mode.
- A real **product-grid module** so the email merchandises, not just announces.
- A **live countdown** treatment for last-chance sends.
- A dedicated **mobile-stacked** layout.

Memorial Day 2026 = **Mon May 25**; "Memorial Day weekend" = **May 23–25, 2026**.
Standard copy applied across the set (red accent `#B3231E`, code `MDW26`):

- `Hero / Eyebrow` → `MEMORIAL DAY SALE`
- `Hero / Big` → `20% OFF` (2nd line, if present → `STOREWIDE`)
- `Hero / Sub Line 1` → `20% OFF SITEWIDE`
- `Hero / Sub Line 2` → `THROUGH MEMORIAL DAY WEEKEND`
- `Hero / CTA Label` → `SHOP THE SALE`
- `Hero / Code Note` → `No code required · Valid 5/21–5/25/26` (Inter Italic 12; promo is automatic)

**Timed-urgency variants** (same templates, headline-only swaps — keep everything
else; tag the frame name e.g. `… / Memorial — 24HR LEFT / Export`):
- *Sunday send* — `Hero / Big` → `ONLY 24 HOURS` (use digits, not words)
- *Final day* — keep/lead with `Hero / Eyebrow` = `MEMORIAL DAY SALE`; `Hero / Big` → `FINAL DAY`; `Hero / Sub Line 2` → `ENDS TONIGHT`
- *Last hours* — `Hero / Big` → `6 HOURS LEFT`
