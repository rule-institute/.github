# Issue #4 design proposal — UNRATIFIED

Working renders supporting the design proposal on
[#4](https://github.com/rule-institute/.github/issues/4). Nothing here is
ratified brand; on ratification the accepted sources are promoted into
`brand/` and this directory is pruned (issue links are pinned to the
introducing commit and survive the pruning).

| File | What it is |
|------|------------|
| `avatar-application.svg` | Proposed application avatar: gold mark, plane `#121024`, floor shadows proportionally darkened (`#080714`, `#0d0b1e`). |
| `avatar-application-alt.svg` | Named alternative plane `#1d1a33` (slate–navy midpoint). |
| `sheet-collision.png` | Institute vs application at 200/96/24 px, full 24 px tier row, alternative plane. |
| `sheet-jurisdiction.png` | Jurisdiction-accent exploration (rejected): NL glyph mock at 200/24 px. |
| `card-*.png` | Sample social cards through swift-institute's parametric chassis, `render.py` unchanged. |
| `card-institute-ring.png` | Same card with the left-pane glyph swapped to the ring silhouette — demo of the proposed `{{GLYPH}}` chassis parameter (post-substituted locally; not a chassis change). |

Card render inputs (chassis = swift-institute/.github `social-preview/`):

```
render.py --namespace "RuleInstitute"        --package-name rule-institute            --accent-from "#f3c309" --accent-to "#dd981c" --accent-text "#924c24" --caption INSTITUTE
render.py --namespace "Burgerlijk|Wetboek 2" --package-name burgerlijk-wetboek-boek-2 --accent-from "#bf6a22" --accent-to "#924c24" --accent-text "#924c24" --caption STATUTE
render.py --namespace "RuleLaw"              --package-name rule-law                  --accent-from "#464a5e" --accent-to "#121024" --accent-text "#464a5e" --caption COMPOSITION
render.py --namespace "RuleLegal"            --package-name rule-legal                --accent-from "#dd981c" --accent-to "#121024" --accent-text "#901d0f" --caption APPLICATION
```

Raster caveat: these samples were rasterized locally (WebKit; Inter not
installed, system-font fallback). Production cards come from the pinned-font
resvg path; glyph metrics will differ slightly.
