# Rule Institute

A layered legal-encoding ecosystem — the legal-domain peer of
[Swift Institute](https://github.com/swift-institute).

## What this is

Rule Institute encodes legal materials — statutes, case law, regulation — as
typed Swift packages, and composes them into executable legal reasoning. A
provision becomes a type whose construction proves the proposition holds;
unknown facts stay unknown (`Bool?`, Strong Kleene) instead of collapsing into
a premature verdict.

The architecture was ratified on 2026-08-03
([rule-institute/.github#1](https://github.com/rule-institute/.github/issues/1)).

## Structure — mirror by role

| Role | Organizations | License |
|---|---|---|
| Meta (skills, CI, inventory, control plane) | rule-institute | — |
| Raw authority encodings | swift-nl-wetgever, swift-nl-hoge-raad, swift-eu-legislature, swift-us-nv-legislature, … | Apache-2.0 |
| Composition (engine + per-jurisdiction) | rule-law; nl-rule-law, eu-rule-law, us-rule-law, … | AGPL-3.0-only + commercial |
| Application | rule-legal; nl-rule-legal, … | Closed |

- **Raw encodings are literal.** One repository per statute (named by its
  official register key) or per judgment (named by its ECLI), encoding the
  document as written — no interpretation, no invented vocabulary. Statute
  packages track dated consolidations of the official register; judgment
  packages are write-once. Judiciary packages never depend on legislature
  packages: a judgment states "does statute Y apply" as a proposition, and the
  binding happens one layer up.
- **Composition** is where legal reasoning lives: `rule-law` owns the
  jurisdiction-generic engine, `<jurisdiction>-rule-law` binds one
  jurisdiction's legislature and judiciary.
- **Applications** turn composed law into products.
- The encoding substrate (ternary logic, construction macros, test primitives)
  is Swift Institute infrastructure, composed rather than duplicated;
  dependencies between the institutes run one way, rule → swift.

## Naming

The jurisdiction identifier is an ordered ISO 3166 path, rendered in each
register's official form: big-endian in org names and ISO text
(`us-nv-rule-law`, `US-NV`), little-endian in DNS (`nv.us.rule.law`). Raw
authority orgs follow `swift-<jurisdiction>-<authority>`, with the authority
named in the jurisdiction's official language (wetgever, hoge-raad;
legislature where English is official).

## This organization

| Repo | Role |
|------|------|
| [.github](https://github.com/rule-institute/.github) | Org profile, control plane, and the org registry (`orgs.yaml`) |
| [Skills](https://github.com/rule-institute/Skills) | Canonical doctrine: rule-architecture, legal-encoding, legal-testing, dutch-law |
| [Internal](https://github.com/rule-institute/Internal) | Internal workspace documentation |

## Status

Architecture ratified; the vertical proof of concept (Burgerlijk Wetboek
Boek 2 — 698 articles as executable, three-valued Swift types) is in active
development in [swift-nl-wetgever](https://github.com/swift-nl-wetgever).
Programme state lives on the
[Rule Work project](https://github.com/orgs/rule-institute/projects/1).
