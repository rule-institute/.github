# Brand

The Rule Institute mark: the rule.law golden ring, as pixel-exact vector
graphics (32×32 grid, `crispEdges` — sharp at every size).

| File | Use |
|------|-----|
| `logo.svg` | The canonical mark (gold), transparent background. |
| `logo-bronze.svg` | Raw-encoding role variant (bronze). |
| `logo-silver.svg` | Composition role variant (silver). |
| `avatar.svg` | Gold on slate (`#464a5e`) with shadow — the institute avatar source. |
| `avatar-bronze.svg` / `avatar-silver.svg` | Tier avatars on slate — raw and composition orgs. |
| `avatar-application.svg` | Gold on navy (`#121024`) — application orgs (rule-legal, nl-rule-legal). |
| `avatar-{1024,512,400,256,128,64,32}.png` | Raster exports of the institute avatar. GitHub org avatar: 1024 (uploader takes raster only). X/Twitter profile: 400. Favicons: 64/32. |
| `avatar-{bronze,silver,application}-1024.png` | Uploader exports for the tier avatars. |
| `glyph-ring.svg` | White-on-accent ring silhouette fragment for the social-card chassis (`--glyph-file`). |

Role tiers (ratified 2026-08-03,
[#4](https://github.com/rule-institute/.github/issues/4)): bronze = raw
encoding orgs, silver = composition orgs, gold = the institute and the
application orgs — distinguished by plane: the institute sits on slate
(`#464a5e`), applications on navy (`#121024`), both from the core palette.
Family invariants across all variants: the warm-white highlights and the navy
outline (`#121024`) never recolor. Jurisdiction orgs wear the canonical
silver mark with no per-jurisdiction accents (ratified: differentiation lives
in the org name and repo captions, not the avatar).

**Placement rule:** the logo lives in each org's avatar, never embedded in
READMEs — the avatar is the canonical display surface.

## Social cards

Cards render through swift-institute/.github `social-preview/`
(`chassis.svg.tmpl` + `render.py`); every brand input is an argument,
including the left-pane glyph (`--glyph-file brand/glyph-ring.svg`).
Ratified per-role accents and captions:

| Role | Accent from → to | Caption color | Caption |
|------|------------------|---------------|---------|
| meta | `#f3c309` → `#dd981c` | `#924c24` | `INSTITUTE` |
| raw, legislature branch | `#bf6a22` → `#924c24` | `#924c24` | `STATUTE` |
| raw, judiciary branch | `#bf6a22` → `#924c24` | `#924c24` | `JUDGMENT` |
| composition | `#464a5e` → `#121024` | `#464a5e` | `COMPOSITION` |
| application | `#dd981c` → `#121024` | `#901d0f` | `APPLICATION` |

Core palette: outline `#121024` · golds `#f3c309` / `#dd981c` · ambers
`#bf6a22` / `#924c24` · deep red `#901d0f` · pale gold `#efd978` · warm white
`#f6f3e6` · slate `#464a5e`.

Provenance: faithful conversion of the original rule.law pixel-art ring
(per-cell extraction on the verified 32×32 grid, cluster quantization,
white-highlight recovery, outline completion; converged 2026-08-03).
