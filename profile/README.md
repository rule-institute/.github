# Rule Institute

A layered legal-encoding ecosystem — the legal-domain counterpart to [Swift Institute](https://github.com/swift-institute).

## What this is

Rule Institute is a working space for encoding legal materials (statutes, case
law, regulations) as typed Swift packages. Where Swift Institute organizes
infrastructure into atomic primitives → specifications → composed foundations,
Rule Institute applies the same layering discipline to legal artifacts: the
text of a statute, the structure of a judgment, the composition of a regulatory
regime.

The work is early. The org currently hosts the canonical legal-domain skill
definitions (naming conventions, encoding rules, testing patterns) and serves
as the home for legal artifacts that don't belong in any single jurisdiction's
package.

## Layout

| Repo | Role |
|------|------|
| [Skills](https://github.com/rule-institute/Skills) | Canonical legal-domain skill definitions: encoding rules, testing patterns, jurisdiction lookup |
| [.github](https://github.com/rule-institute/.github) | This org-profile repo plus shared workflows for legal-domain CI |

Jurisdiction-specific encoding work lives in sibling organizations and standalone
repositories — Rule Institute is the cross-jurisdiction ecosystem home, not a
container for every legal package.

## Status

Pre-release. The org and its repos are being shaped; expect structural change
before the first stable tag.
