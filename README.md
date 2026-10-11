# Trebired Meta

The published documents of the Trebired organization, in English and Czech, as the single source every consuming site reads at build time.

This repository owns the wording, the structure, and the effective date of each policy in it. Consumers own their routing, their rendering, and their fallback behaviour. It does not own licence texts, which ship in the repository of the software they cover, and it does not own client contracts, which exist per engagement and are not published.

## Documents

| Folder | Covers |
| --- | --- |
| `privacy` | What personal data the organization handles, why, for how long, and the rights that apply to it |
| `cookies` | What the sites store in a browser and how to clear it |
| `terms` | The terms covering every site, product, and server the organization runs |
| `trademark` | The marks the organization claims and the conditions for using them |
| `acceptable-use` | What is and is not allowed on the services the organization operates |
| `security` | How to report a vulnerability and what the reporter receives in return |
| `code-of-conduct` | What is expected of everyone in the organization's spaces, and what happens when it is breached |
| `philosophy` | What the organization believes, why everything it writes is public, and which machines it builds for |

## Structure

```txt
<document>/
  en.md
  cs.md
```

The folder name is the consumer-facing slug in kebab-case. `privacy/` is served at `/privacy`, `acceptable-use/` at `/acceptable-use`. Renaming a folder breaks every consumer route that points at it.

Language files are named by ISO 639-1 code. There is no `index.md`, no locale suffix, and no document file at the repository root.

## Format

Every file opens with front matter and then sections.

```md
---
title: Privacy policy
updated: 2026-10-04
---

## The short version

One paragraph.

Another paragraph.
```

`title` is the rendered page heading. `updated` is an ISO date and is rendered as the last-updated line. Both are required.

`##` opens a section. A blank line separates paragraphs, and each paragraph becomes one rendered block.

`###` opens a part inside a section, for a document long enough to read in chapters. A section either holds paragraphs of its own or holds parts, never both, and parts do not nest further.

The rendered subset is headings and paragraphs. Lists, tables, bold, italics, links, images, and code blocks are dropped silently, so nothing outside the subset ships.

## Language

Every document ships in English and Czech, carrying the same sections in the same order.

A section present in one language and missing in the other disappears for the readers of that language rather than falling back, so parity is a correctness rule.

Each language is written, never translated from the other. An idiom that works in one language is replaced in the other, not carried across.

## Consumption

Consuming sites read the raw files at build time and fall back to their committed snapshot when the fetch fails, so a network failure never breaks a build.

A change reaches a site on its next deploy, not immediately. A document that must take effect on a date is merged before that date, not on it.

## Authoring

Changes are made by the founder and maintainer, Miroslav Machynka. A change to the substance of a document moves its `updated` date and gets a changelog bullet naming the document. A typo fix does neither.

Renaming or removing a document folder is a breaking change, because it breaks consumer routes, and is recorded as one.

## What It Does Not Do

This repository does not:

- Ship a runtime, a build, a package, or any configuration. There is nothing to install.
- Hold licence texts. Those ship in the repository of the software they cover.
- Hold client contracts, proposals, or correspondence. Those are per engagement and are not published.
- Render anything. Consumers own rendering, and the format exists to keep that simple.
- Guarantee that a published site is current. A site shows the text as of its last deploy.
