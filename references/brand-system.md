# Yan Er Ding brand system

Read this reference for every use of the skill. It records the current reusable brand decisions extracted from the owner's design source files. A task-specific brief overrides layout choices, but it does not silently replace the brand identity.

## Identity

**Brand:** 言二丁 / YAN ERDING<br>
**Category:** handcrafted women's shoes<br>
**Tagline:** 古典主义的浪漫复兴 / Classy & Romantic<br>
**Character:** classical, romantic, restrained, handcrafted, editorial

One-sentence test:

> Deep burgundy is the paper, champagne gold is the foil, Chinese serif type is the structure, and product photography is the only large field of full color.

The work should resemble a boutique shoe window, a brand lookbook, or a couture workshop. It should not resemble a promotion-heavy marketplace page or a gray-white SaaS template.

## Five governing principles

1. **Restraint creates luxury.** Burgundy and gold carry the identity; hierarchy comes from lightness, opacity, type, and spacing rather than extra hues.
2. **The product is the protagonist.** Give shoes enough scale and preserve their shape. Avoid promotional stickers and decorative competition.
3. **Elements form composed groups.** Lock marks, headlines, supporting copy, and actions into intentional units instead of scattering them.
4. **The voice stays quiet.** Copy is visual, specific, and editorial. Imply craft and confidence instead of shouting claims.
5. **Square geometry carries character.** Default corners are 2px and never exceed 4px except for avatars, status dots, and circular icon controls.

## Color tokens

Use burgundy as the dominant field and champagne gold for type, rules, controls, and emphasis.

| Role | Token | Value |
|---|---|---|
| Immersive background | `burgundy-950` | `#1e0605` |
| Footer / overlay | `burgundy-900` | `#28090c` |
| Header / sidebar / deep surface | `burgundy-800` | `#3a0a10` |
| Main page field | `burgundy-700` | `#431014` |
| Hover / raised field | `burgundy-600` | `#51141b` |
| Active state | `burgundy-500` | `#591e23` |
| Strong title | `gold-200` | `#c69c79` |
| Primary text / hover | `gold-300` | `#c69c79` |
| Default accent / button / selected | `gold-400` | `#c69c79` |
| Muted text | `gold-500` | `#b39172` |
| Disabled / placeholder | `gold-600` | `#a08369` |
| Logo, icons, gold rules | `gold-mark` | `#ac8461` |
| Light paper, print only | `surface-light` | `#fbf6ec` |

Gold has two tiers (since 2026-10-28, same as the WeChat mini program, the website and cc-design): text and buttons use the lifted `gold-200`–`600`; logo, icons and gold rules stay on `gold-mark` `#ac8461`, one step darker. Do not lift icons or the logo to text gold, and do not drop text back to `gold-mark`. Gold rules use `rgba(172, 132, 97, 0.08)` through `rgba(172, 132, 97, 0.58)`. Shadows should carry a burgundy cast rather than pure black.

Semantic colors are exceptions, not palette extensions:

- Success `#5a8c6f`
- Warning `#997556`
- Danger `#b34940`
- Info `#8d6c4f`

Use them only for genuine states, at restrained area and saturation. Do not use them decoratively.

## Typography

- **Chinese:** Noto Serif SC, Source Han Serif SC, Songti SC, then `serif`.
- **English, numerals, prices:** Cormorant Garamond, Garamond, Times New Roman, then `serif`.
- **Script:** Parisienne only for the short `Classy & Romantic` signature or an equivalent approved micro-mark.
- Chinese body copy has line-height at least `1.75`; the system default is `1.82`.
- Chinese title tracking usually sits between `0.05em` and `0.15em`.
- A rare English eyebrow may reach `0.28em`; do not place one above every section.
- Prices use old-style numerals when the font supports them.
- Never use Inter, Arial, or a generic sans serif as a brand headline.

## Logo assets

All paths are relative to the skill root.

| Asset | Use |
|---|---|
| `assets/brand/badge.png` | Preferred compact brand appearance; tightly cropped oval swallow badge |
| `assets/brand/brandmark-lockup.png` | Preferred full lockup: badge, script line, and Chinese subtitle |

The source brand system also has gold, white, black, and wordmark variants. Use those only when the rights holder supplies them for the current task; do not derive new variants from the two packaged files.

Keep clear space of at least one quarter of the rendered logo height on every side. On a complex photograph, place the logo on a restrained burgundy backing. Preserve transparency and aspect ratio. Never use a product-level mark as the navigation identity.

## Product imagery

- Product photography is the only element allowed to occupy a large area in full color.
- Default product ratio is `3:4`; `4:5` is acceptable for a deliberate focal composition.
- Never stretch or compress a shoe. `object-fit: cover` is the default for consistent grids, but adjust `object-position` or the crop if the shoe silhouette is lost.
- Prefer real authorized product photos over stock or generated substitutes.
- Do not infer or fabricate model names, prices, materials, sizes, stock, delivery promises, or campaign labels from an image.

## Composition and geometry

- Base spacing scale: `4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128`.
- Maximum digital shell width: `1200px`; comfortable prose width: at most `640px`.
- Aim for full but breathable composition: grouped content, deliberate rhythm, and useful image scale. Avoid both sparse scattering and cramped repetition.
- Cards are a functional affordance, not the default composition. A card is a translucent gold film on burgundy with a fine gold rule—not a white rounded tile.
- Default radius is `2px`, maximum `4px`. Use one meaningful divider rather than stacked decorative rules.
- Motion should be quiet and purposeful. Avoid bounce and elastic movement; support reduced motion.

## Copy voice

Customer-facing copy is calm, visual, and confident.

Good patterns:

- `一双鞋，一段不急不缓的日子。`
- `浏览本季全部款式`
- `白月光` / `朱砂痣` / `黑美人` / `栗壳棕`
- A specific fulfillment statement only when the source data supports it.

Avoid:

- `爆款秒杀`
- `全网最低`
- `姐妹们冲`
- Emoji, repeated exclamation points, or unsupported performance claims

Staff and admin copy may be direct, but should remain precise and restrained. Prefer concrete labels such as `搜索款号、名称、颜色…` over vague placeholders.

## Hard exclusions

Remove or redesign these when they appear:

- Purple/blue gradients, neon technology styling, or decorative glassmorphism
- Large rounded cards, generic Tailwind/Material SaaS layouts, or gray-white admin templates
- Emoji icons, multicolor icon sets, or icons with no consistent source
- Gradient text, loud promotional badges, and repeated metric-hero templates
- A tiny uppercase tracked eyebrow above every section
- Repeated `01 / 02 / 03` section scaffolding unless the content is a real sequence
- Excessive whitespace, disconnected elements, duplicate dividers, or repeated content
- Distorted or unrecognizable product images
- Text overflow at tablet or mobile widths
