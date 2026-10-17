# Changelog

All notable changes to Trebired Meta will be documented here.

This repository follows semantic versioning.

## 2.7.0

- Added three roadmap entries. `roadmap-search-visibility` covers making the published pages legible to the machines that index them, without paying for placement. `roadmap-social-presence` covers holding the organization's name on the sites where software is discussed and announcing releases there. `roadmap-product-development` covers Operlorn and Sessionary resuming once the initial release is out.
- The Documents table names each roadmap entry by what it covers. One generic row described the shape of an entry, which the Format section already states and which stops being useful once there is more than one entry.

## 2.6.0

- Added `standards` in English and Czech: what every change has to pass before it ships, what the software itself has to be, what a reader is owed, and what happens when something fails any of it. The text was written in the website that rendered it, which is the wrong place for words another repository may need to quote.
- Added `handbook` in English and Czech: how the work is chosen, built and handed over, in the same four-section shape.
- Added the first roadmap entry, `roadmap-initial-release`. A roadmap entry is a document with two more front matter keys, `status` and `color`, and no sections: its body is the description. `status` says where the entry stands and `color` says what a consumer paints it, so the entry carries its own appearance instead of the page deciding. The Format section states both.

## 2.5.0

- A document can refuse the section navigator. `outline: false` in the front matter says the document is read straight through, and `faq` declares it: its sections are four groups of questions, not chapters to jump between.

## 2.4.0

- A document now says how it is presented. FAQ carries `parts: disclosure` in its front matter, so a consumer renders it as an accordion because the document asks for it rather than because the consumer recognises the folder name. Everything without the key is read as prose, which is every other document here.
- FAQ gained a lead paragraph. Paragraphs before the first section are the document's lead, and a consumer may show them under the title.

## 2.3.0

- Added FAQ in English and Czech: twelve questions in four sections, covering what a project costs, what a client owns, what is published, and what is kept about a reader.
- Documents may link to a page without showing anything to a reader of this repository. A span marked with a `<!--tbf:link /path-->` comment pair becomes a link in a consumer that understands it and plain words everywhere else, which a relative markdown link cannot do, because a repository page renders it as a link to a page that does not exist. The Format section states the whole of it.

## 2.2.0

- Added four chapters to philosophy in English and Czech: what the organization writes software in and why, what software is allowed to cost the machine it runs on, why the layer under the products is built in house, and who answers for work a model helped write.
- Changed the Windows chapter in philosophy in English and Czech. Compatibility is named as the one thing holding the system up, and consumer habit as what is left once it is set aside.

## 2.1.0

- Cookie policy now names accessibility settings among what a browser stores. The animation, text size and contrast choices offered in the site header are kept in the browser and never sent to Trebired, and the clearing paragraph says they go with site data.

## 2.0.0

**Breaking:** `ideology` is renamed to `philosophy`. The folder, and with it the route every consumer serves it at, changes from `/ideology` to `/philosophy`. A consumer that still asks for the old slug gets nothing back.

- Renamed ideology to philosophy in English and Czech. The text is unchanged.

## 1.2.0

- Added ideology in English and Czech, written in chapters.

## 1.1.1

- Conduct reports go to abuse@trebired.com instead of legal@trebired.com.

## 1.1.0

- Added code of conduct in English and Czech.

## 1.0.0

- Added privacy policy in English and Czech.
- Added cookie policy in English and Czech.
- Added terms of service in English and Czech.
- Added trademark policy in English and Czech.
- Added acceptable use policy in English and Czech.
- Added security policy in English and Czech.
