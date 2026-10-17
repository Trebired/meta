---
title: Handbook
updated: 2026-10-17
---

## Three shapes, and nothing else

There are three kinds of repository here and nothing else. An application holds a backend, a frontend, the code both share, its executables and its types. A package holds its source, its executable verification scripts and the gate that runs before it is published. A text repository holds documents that more than one repository has to agree on, one folder per document and one file per language, with no build of its own.

Each kind has one layout, and that layout is identical in every repository of that kind. Prose that only one repository reads stays in that repository; a text repository exists the moment two of them need the same words.

## Written by a person, or built by the build

The source holds code and the text a person wrote. Anything a build fetches, derives, renders or downloads is an artifact: a snapshot of a remote interface, an exchange rate file, a prerendered page. Artifacts are written into the build output on every run and are never committed.

A repository that keeps a generated file in its source is defective, and it stays defective when the file is small, when it changes once a year, and when committing it would make a build faster. The application reads generated data the way it reads any other build input, never as an import from the source tree.

## How a commit and a release read

A commit message is a subject and usually nothing else: imperative, sentence case, under seventy-two characters, describing the behaviour that changed rather than the files that changed. There are no type prefixes and no scopes. A commit that needs the word "and" twice is two commits.

A version bump is its own commit, its subject names the release and what changed in it, and the annotated tag carries that same line. The commit is pushed first and the tag second, because a tag that arrives first points at nothing. A published tag is never moved or deleted; a mistake is corrected by the next version.

## Whose name is on it

Every commit, tag, release and published package carries the name of the person who did the work. AI is used the way a compiler or an editor is used, as a tool in the hands of someone who remains answerable for the result, and it never appears as an author, because a model cannot answer for anything.

Nothing is handed over that the developer has not read, understood and is prepared to defend. That is the whole of the rule, and it is why the name on the commit means something.
