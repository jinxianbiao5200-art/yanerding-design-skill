# Yan Er Ding Design Skill

<img src="assets/brand/brandmark-lockup.png" alt="Yan Er Ding brandmark" width="360">

A portable Agent Skill for creating and restyling authorized **言二丁 / YAN ERDING** interfaces and brand materials. It packages the brand's deep-burgundy and champagne-gold visual system, typography, logo usage, responsive guidance, reusable CSS tokens, and delivery checks.

## What it handles

- Storefronts, product pages, and branded campaigns
- Staff tools and admin interfaces without generic SaaS styling
- Posters, packaging, presentations, contracts, and other fixed layouts
- Visual review of existing Yan Er Ding work

The repository intentionally excludes private ERP data, the full product-photo catalog, business projections, exported project deliverables, dependency folders, and source artwork that agents do not need.

## Install

Clone the repository into the skill directory used by your AI client. Common locations are:

```bash
# Codex
git clone https://github.com/jinxianbiao5200-art/yanerding-design-skill.git ~/.codex/skills/yanerding-design

# Claude Code
git clone https://github.com/jinxianbiao5200-art/yanerding-design-skill.git ~/.claude/skills/yanerding-design

# Cursor, project-scoped
git clone https://github.com/jinxianbiao5200-art/yanerding-design-skill.git .cursor/skills/yanerding-design
```

For another Agent Skills-compatible client, copy this repository into that client's skills search path. The folder name should remain `yanerding-design` so it matches the name in `SKILL.md`.

## Invoke

```text
Use $yanerding-design to restyle this storefront while preserving its checkout flow.
```

```text
使用 $yanerding-design，把这张开箱须知卡做成言二丁品牌风格，并输出可印刷 PDF。
```

The description supports automatic discovery in clients that allow implicit skill invocation. Explicit `$yanerding-design` invocation is the most portable option.

## Repository map

```text
SKILL.md                         Agent entrypoint and routing
agents/openai.yaml               Codex UI metadata
references/brand-system.md       Identity, palette, typography, imagery, red lines
references/digital-implementation.md
references/print-and-copy.md
assets/css/                      Reusable CSS tokens and component classes
assets/brand/                    Approved core logo files
```

## License

The skill instructions and CSS are available under the [MIT License](LICENSE). Brand names, logos, and other files under `assets/brand/` remain protected brand assets and are governed by [BRAND_ASSETS_LICENSE.md](BRAND_ASSETS_LICENSE.md).

The CSS references three open fonts from Google Fonts at runtime; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). No third-party font binary is included in this repository.
