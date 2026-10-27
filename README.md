# Trebired Meta

The published documents and the brand of the Trebired organization, as the single source every consuming site reads at build time. The documents are in English and Czech; the brand is the logos and colours.

This repository owns the wording, the structure, and the effective date of each policy in it, and the logos and colours of the brand. Consumers own their routing, their rendering, and their fallback behaviour. It does not own licence texts, which ship in the repository of the software they cover, and it does not own client contracts, which exist per engagement and are not published.

## Documents

| Folder | Covers |
| --- | --- |
| `privacy` | What personal data the organization handles, why, for how long, and the rights that apply to it |
| `cookies` | What the sites store in a browser and how to clear it |
| `terms` | The terms covering every site, product, and server the organization runs |
| `trademark` | The marks the organization claims and the conditions for using them |
| `acceptable-use` | What is and is not allowed on the services the organization operates |
| `code-of-conduct` | What is expected of everyone in the organization's spaces, and what happens when it is breached |
| `philosophy` | What the organization believes, why everything it writes is public, and which machines it builds for |
| `faq` | The questions that arrive most often about working with the organization, what a client gets, and what is kept |
| `roadmap/initial-release` | A roadmap entry: the organization and its website going public together |
| `roadmap/search-visibility` | A roadmap entry: making the published pages findable without buying placement |
| `roadmap/social-presence` | A roadmap entry: holding the organization's name where software is discussed, and announcing releases there |
| `roadmap/product-development` | A roadmap entry: Operlorn and Sessionary resuming once the initial release is out |

## Structure

```txt
<document>/
  en.md
  cs.md
roadmap/
  <entry>/
    en.md
    cs.md
brand/
  brand.json
  logos/
```

Everything of one kind lives in one folder. Roadmap entries are folders inside `roadmap/`, and the brand is `brand/`.

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

`parts` is optional and says how a consumer presents the `###` parts of this document: `prose`, the default, for articles that are read in order, or `disclosure` for an accordion, where each part is a question the reader opens. A document states this itself so that no consumer has to recognise it by its folder name.

`outline` is optional and takes `false` when a document does not want the section navigator a consumer puts beside long documents. A document whose sections are read one by one, such as a list of questions, says so here rather than leaving the decision to the page that renders it.

`status` and `color` belong to a roadmap entry and to nothing else. `status` is one of `in-progress`, `next`, `later` or `done`, and a consumer renders the word in its own language. `color` is a hex colour the consumer paints that status in, so the entry decides how it reads rather than the page it appears on. A roadmap entry is the one document shape with no `##` at all: its whole body is the lead, which is the description, and it lives in `roadmap/<entry>/` because an entry is not served at a route of its own.

Paragraphs written before the first `##` are the document's lead, and a consumer may show them under the title.

`##` opens a section. A blank line separates paragraphs, and each paragraph becomes one rendered block.

`###` opens a part inside a section, for a document long enough to read in chapters. A section either holds paragraphs of its own or holds parts, never both, and parts do not nest further.

The rendered subset is headings and paragraphs. Lists, tables, bold, italics, images, and code blocks are dropped silently, so nothing outside the subset ships.

A link is the one exception, and it is written so that it shows nothing here. A markdown link cannot be used: a path like `/privacy` is relative, so a repository page renders it as a visible link to a page that does not exist there. A span is marked with a comment pair instead, which every markdown renderer hides:

```md
Read <!--tbf:link /philosophy-->the philosophy page<!--/tbf:link--> for why.
Get it from <!--tbf:link https://github.com/Trebired tab-->GitHub<!--/tbf:link-->.
Start at <!--tbf:link /downloads reload-->the downloads page<!--/tbf:link-->.
```

The first token after the marker is the destination and is required. `tab` opens the link in a new tab; `reload` makes the consumer navigate fully instead of swapping the page in place. A missing destination, an unknown flag or an unclosed pair drops the link and renders the words plainly, so a mistake costs a link and never a sentence. Consumers that do not understand the markers show the text and nothing else, which is the same thing a reader of this repository sees.

## Brand

`brand/brand.json` names the brand, its two colours and every logo, by path inside `brand/`:

```json
{
  "name": "Trebired",
  "colors": { "dark": "#000000ff", "light": "#f5f5f5ff" },
  "logos": {
    "full": { "dark": "logos/full/dark.svg", "light": "logos/full/light.svg" },
    "full-tm": { "dark": "logos/full/tm/dark.svg", "light": "logos/full/tm/light.svg" },
    "minimal": { "dark": "logos/minimal/dark.svg", "light": "logos/minimal/light.svg" }
  }
}
```

The colours are hex with alpha. `full` is the mark with the name, `full-tm` the same with the trademark sign, and `minimal` the mark alone. A logo's `dark` file is drawn for a dark background and its `light` file for a light one. Consumers read the logos from here at build time and keep no copy of their own, so a logo changes everywhere by changing it here.

## Language

Every document ships in English and Czech, carrying the same sections in the same order.

A section present in one language and missing in the other disappears for the readers of that language rather than falling back, so parity is a correctness rule.

Each language is written, never translated from the other. An idiom that works in one language is replaced in the other, not carried across.

## Consumption

Consuming sites read the raw files at build time and fall back to what their last build fetched when the fetch fails, so a network failure never breaks a build.

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
