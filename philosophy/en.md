---
title: Philosophy
updated: 2026-10-13
---

## Why all of it is public

### We are dispensable

Nobody in this organization is rare. Building software is a learned skill held by a large number of people, and every one of us can be replaced by someone who will do it as well or better. The organization is no different. Trebired exists because a few decisions went one way rather than another, and it will stop existing the same way.

We say that plainly because the opposite belief is the one thing we refuse to build on. An organization that treats its own continuation as the point starts protecting itself. It keeps the source closed so that leaving costs something, it ties the software to a service only it can run, and it makes the people who depend on it depend on its survival. That is a reasonable way to stay alive. It also means that on the day the organization ends, everything it made ends with it.

### The work can outlast us

Source code is one of the few things a person can make that has no natural end. It does not wear out, it costs nothing to copy, and anyone who finds it can read it, correct it and extend it, in a year or in a century. Published, it is independent of whoever wrote it. Closed, it has exactly the lifespan of the organization holding the password.

So we publish all of it. Every product, every package, and every tool we wrote to build them, under the AGPL or MIT, in public repositories, with no held back core and no paid tier that unlocks what we kept. If Trebired closes tomorrow, nothing here has to be rescued, because nothing was ever locked up. The license already grants the rights and the code is already on other people's disks.

### For people we will never meet

This is not generosity and it is not a marketing position. It follows from the two sections above. If we are dispensable and the work is not, the only honest thing to do with the work is to put it somewhere our disappearance cannot reach.

What anyone does with it afterwards is not ours to decide. It can be run, forked, learned from, or taken somewhere we never thought of, without asking us and without owing us anything. That is the point. We would rather leave behind something that keeps being useful than an organization that was careful to remain necessary.

## Which machines we build for

### An operating system should be boring

An operating system has the most basic job in computing. It starts the machine, it moves data between programs, and then it gets out of the way. Nothing in that job requires a secret, and nothing in it is worth a company watching a billion people to do it.

Windows keeps the secret anyway. Nobody outside the company selling it can read what it does, correct what it gets wrong, or check a single claim made about it. On top of that it reports what its users do back to that same company, on terms the user did not write and cannot inspect. That is not a flaw in an otherwise fine system. It is what the system is for.

### So we do not build for it

Desktop software from this organization runs on Linux. Windows is not on the list and will not be added, and neither will macOS. This is not about effort, and it is not about how many people use them. Shipping onto a closed platform would mean accepting its terms on behalf of everyone who uses what we make, and then calling our own code open.

Anything we build for a browser works wherever a browser does, including on Windows and on a Mac. The line is drawn at the software we write for a machine, because that is the part where the platform gets a say in what the user is subjected to.

### We expect it to end

Windows runs almost everywhere, and that is the part we find genuinely sad. It is there because of preinstalls, purchasing agreements and habit, not because anyone compared it with the alternatives and picked it.

One thing holds it up, and it is not quality. It is compatibility: the programs people need were written for Windows because Windows is what people were sold, and people stay on Windows because that is where those programs are. Set that circle aside and look at the system on its own, and there is very little left to defend. Everything underneath it, the kernel, the file systems, the networking, the machines that actually run the internet, is already done in the open, by more people, in the light. What remains is a consumer habit with a telemetry service attached, and habits are replaceable.

So we think it should not survive, and we do not think it will. Linux already runs the servers, the networks and the phones in people's pockets; the desktop is the last place it has not taken, and it is closer every year. We build for that desktop on purpose, rather than for the one we expect to go away.

## What we write things in

### The compiler should read it first

Every program is read twice: once by the machine that runs it, and once by the person who has to change it a year later. Plain JavaScript makes that person do the machine's job. Nothing in the file says what a value is, what a function needs, or what it hands back, so the only way to find out is to run it and watch. That is an acceptable way to write something small and a bad way to keep anything alive.

So everything we write is TypeScript, and a type is treated as a sentence the next reader gets for free. It is the one piece of documentation that cannot quietly go out of date, because the program stops compiling when it becomes a lie. The compiler reads the whole thing before anyone else does and refuses it at the only moment when refusal is cheap.

That is the general case, and it holds for most of what software does: waiting on a disk, a network or a person, where clarity matters and raw speed does not. We reach past it only when the machine itself is the limit.

### Rust where the machine is the limit

Some work is not waiting for anything. Nothing stands between the person and the result except how much the processor has to do and how much memory it has to hold while doing it. Rendering, printing, parsing large files, the hot path inside a long running service: in that work the language stops being a matter of taste.

Those parts are written in Rust. Not for fashion, and not because every program deserves it, but because it is the one choice that gives the speed of C without the family of mistakes that made C dangerous. Memory that was freed cannot be read back, and a race the author did not notice is usually a compile error rather than a report from a customer six months later.

The rule we hold ourselves to is narrow. Rust where it earns its weight, in the parts that are measured and found wanting, and the plainer language everywhere else. Choosing the harder language for work that does not need it is not rigour, it is decoration.

### Go where a program has to land on a stranger's machine

A small part of what we make has to run somewhere we do not control: a runner on a build machine, a helper beside a service. The useful question there is not how expressive the language is. It is what the person on the other end has to install before our program will start.

Go answers that better than anything else we use. One static binary, no runtime to put on the machine first, no version of anything to agree on. It copies across and runs. We use it for exactly that, and for nothing else.

### An interface is made out of someone else's time

A screen is where our decisions turn into somebody's afternoon. Every control that lies about what it will do, every dialog that appears for no reason, and every second of waiting is taken from a person who did not agree to spend it.

On the Linux desktop we build with Qt and QML, in the toolkit the desktop itself is made of. An application that uses the system's own controls, shortcuts and dialogs asks the user to learn nothing: it already behaves like everything else on the machine. On the web we use React, because the browser's model is one that millions of people already maintain and we have nothing better to propose, and we keep our own layer above it so the parts that are ours stay ours.

## What software is allowed to cost

### A program is a guest on the machine

The computer belongs to the person using it. Memory our software holds is memory their other work cannot have, and a processor busy with us is a processor not doing what they actually sat down to do. Treating the machine as ours to fill is the quiet rudeness most software has settled into.

So we put a number on it. An application from this organization runs under a hard cap of 500 MB of resident memory, aims at 200 MB or less, and is measured under real use rather than at a fresh idle boot. Graphics work is the only exception, and it states its own figure instead of being excused from having one.

When something goes over, it is fixed at the cause. We do not raise the cap, because the cap is not the problem, and a limit that moves whenever it is inconvenient was never a limit.

### Waiting is a cost nobody writes down

Nobody thanks software for being quick, which is exactly why it is the first thing to be given away. Each individual compromise is defensible, the whole is not, and it ends with a machine that is many times faster than the one before it, running software that feels slower.

We treat speed and size as part of whether the thing works at all, not as a later optimisation. A product that is correct and unusable has not been finished.

## Why we build our own tools

### A dependency is a promise somebody else is keeping

Everything a product stands on is a decision somebody else can change, abandon, rename or sell. That is not an argument for writing everything yourself, which is how small organizations drown. It is an argument for knowing exactly which promises hold you up and keeping the important ones in reach.

So the layer directly beneath our products is ours: the frontend framework, the bundler, the logger, the translations, the discipline that enforces the shape of the code. When something is wrong in that layer we fix it the same day instead of filing an issue and waiting. When it is good, it is published under MIT or the AGPL, so that being ours never means being a cage.

### The same shape every time

Every repository here has the same layout, the same tooling and the same rules, and a tool checks that rather than a person remembering it. File length, dead comments, import paths, where a thing is allowed to live: all of it is enforced, on every project, including the ones nobody is watching.

This is not tidiness for its own sake. It is what lets anyone open any repository in this organization and know where to look, and it is what makes the work survivable by people who were not there when it was written. A codebase that only its author can navigate is already half closed, whatever its licence says.

## How the work is made

### A machine can write a line, it cannot answer for it

We use AI the way we use a compiler, an editor or a search engine: as a tool held by a person who remains responsible for the result. It drafts, it suggests, it is often wrong, and none of that changes who is accountable. Nothing ships from here that the developer has not read, understood and is prepared to defend.

So the authorship never moves. Commits, releases and published work carry the name of the person who did them, never a model's, because the name on the work is a statement about who answers for it. A model cannot answer for anything. Writing its name there would be a lie about the one thing the signature exists to say.

### No AI image, anywhere

We do not use AI to make the things we hand over. No generated logos, no generated illustrations, no generated photographs, no generated marks or icons. You will not find an AI image anywhere in this organization, on this site, in a product, or in work delivered to a client, and you will not find one later either.

### A mark is a decision, not an average

A logo is a decision about who someone is, and a picture is a decision about what they show the world. A model cannot make either decision, because it has nobody to be accountable to; it averages what other people drew and returns something that resembles all of it and belongs to none of it.

So we draw it, slower, and we are answerable for every line. This is a craft, and the work is finished when it is right rather than when it is fast.
