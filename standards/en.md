---
title: Standards
updated: 2026-10-17
---

## What every change has to pass

Types check with no errors, the discipline tool approves the shape of the code, the verification scripts run, and the whole thing builds. A change that fails any of them is not merged and not released. The gate is a program, not a reviewer in a good mood.

The discipline tool enforces what review is bad at: file length, function length, line length, dead comments, import paths, and where a thing is allowed to live. It refuses the commit rather than leaving the mess for later.

## What the software has to be

Open source, under MIT or the AGPL, with no held back core. Desktop software runs on Linux. Anything built for a browser works wherever a browser does.

An application runs under a hard cap of 500 MB of resident memory and aims at 200 MB, measured under real use rather than at a fresh idle boot. Graphics work is the only exception, and it states its own number instead of being excused from having one.

## What a reader is owed

Every site and every interface we publish is held to WCAG 2.2 AA: operable from a keyboard alone, readable by a screen reader, legible at 200% text, and honest about reduced motion. The accessibility page says what that covers and what it does not.

No tracking, no analytics, no behavioural profiling, and no third party watching the reader on anything the organization runs.

## What happens when something fails it

The cause gets fixed. A limit that moves whenever it is inconvenient was never a limit, so memory overruns are fixed at the cause rather than by raising the cap, and a rule is never switched off to get a commit through.

When a standard turns out to be wrong, it is changed in the open, in writing, and everything already shipped is brought up to it. That is slower than an exception and it is the only version that holds.
