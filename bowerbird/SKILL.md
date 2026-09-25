---
name: bowerbird
description: Turns an app idea into a product proposal (企画書) centered on its world and what the app is — the frame it borrows, its tone and vocabulary, what the user sees and feels, who opens it and when, and what builds up with use. Stops before technical design; the proposal is the brief that design and implementation work start from. Use this skill whenever the user has an app or service idea — from a one-line hunch to a detailed memo — and wants it written up, fleshed out, or made concrete enough to hand off, even if they never say "proposal" (e.g. 「このアイデアを企画書にして」「アプリの企画をまとめたい」「この案、世界観から詰めたい」「作る前にどんなアプリか整理したい」「このネタで企画書書いて」).
---

# bowerbird — a bird that builds a world to show

A bowerbird builds a bower and decorates it with things of one colour, arranged so that whoever sees it understands at once what it is. This skill does the same for an app idea: it builds the world the app lives in and shows what the app is, so clearly that a designer or engineer who has never heard the idea could picture it.

Write the proposal and the replies in the user's language.

## What this proposal is for

Detailed design and implementation are someone else's job. This proposal hands them **what to build and what it should feel like**, not how to build it. Its most important content is:

- **The world.** The frame the app borrows, the way it talks, what things are called inside it, what it looks like. The world is what makes the app one thing instead of a pile of features.
- **What the app is.** Who opens it, at what moment, what they do, what they see, and what they get. A reader should be able to replay a day of using it in their head.

Everything else — pain, scope, open questions — supports these two.

Leave out tech stack, architecture, data models, API choices, and screen-by-screen specs. When a decision like that matters to the experience ("it has to work offline because it's used on the mountain"), write it as an experience requirement and let design decide how.

## What makes a world hold together

- **One frame, derived from the idea.** Borrow the world from somewhere unexpected but fitting — an observatory, a train timetable, a museum label, a sumo ranking sheet — so the ordinary subject reads as something else. Derive it from what the user does, what piles up, and what they'd want to show someone; don't pick it from a fixed menu.
- **Everything follows from the frame.** Names, copy, visuals, the moment of reward, even what an error looks like should all come from the same world. If one element could be swapped into any other app, it isn't part of the world yet.
- **Concrete enough to picture.** "Warm and playful" says nothing. Write actual lines the app says, actual names for its things, and describe one image or screen in enough detail — what's in it, in what style, what colors — that two people would imagine roughly the same thing.
- **The world changes how it's used.** A cute theme over a to-do list is a skin. A world holds when it gives the user a reason to act differently — to collect, to come back, to show someone.

## How to work

### 1. Read the idea

The idea may arrive as one line, a memo, a pasted document, or earlier conversation. Pull out what's already decided: the pain, the user, what the app does, any look or tone. Note what's missing.

### 2. Ask only what shapes the world

Ask once, briefly, and only about things you can't reasonably decide yourself and that would change the world — typically who it's for, the moment it's used, and anything the user already feels strongly about ("it must not feel like a productivity app"). Offer a sensible default for each so the user can just say "go with that". If the idea is already clear enough, skip asking.

### 3. Offer world directions

Unless the user already has a world in mind, propose 2–3 contrasting directions before writing the full proposal. For each: the frame it borrows, one line the app would say, and one image or moment. Make them genuinely different — different frames, not three shades of the same one. Say which you'd pick and why, then let the user choose or mix.

This is the step where the user's taste matters most, so it's worth the extra round. If the user asked you to just write it, pick the strongest direction yourself and note the alternatives in one line at the end.

### 4. Write the proposal

Fill the template below. Write the world and the experience first and in the most detail; they carry the proposal. Keep the other sections short.

Save it as a Markdown file — `docs/proposals/<idea-name>.md` in the working directory unless the user names another place — and give a short summary in the reply: the one-liner, the world in a sentence, and the open questions that most need an answer.

### 5. Revise

Expect the user to push on the world. When they change one element, check what else has to follow — renaming the core thing usually changes copy, the reward moment, and the image too.

## Proposal template

```markdown
# [App name]

> [One line: what it is, in the app's own voice]

## In short
Two or three sentences: who it's for, what they do with it, and what they get — the version you'd say out loud.

## Why this app
- **The pain or wish**: who struggles with what, at what moment
- **What they do today**: the workaround, and why it isn't enough
- **Why this approach**: what the world and experience change about that

## The world
- **Frame**: what the app borrows its world from, and why that frame fits this subject
- **Vocabulary**: what the core things are called inside the app (e.g. entry → "specimen", history → "the collection")
- **Voice**: how it talks, with 3–5 actual lines (a greeting, a reward, an empty state, a mistake)
- **Look**: colors, textures, motifs, typography mood; describe one image or screen the user sees in detail
- **What it is not**: one or two apps or moods it must not be mistaken for

## Who and when
A short scene: a specific person, the moment they open the app, what's around them, why they reach for it now.

## The experience
- **Core loop**: open → do → see → get → come back, in one line each
- **Signature moment**: the one moment people will remember and describe to others
- **First time**: what happens in the first minute
- **A week in / a year in**: how it feels after repeated use

## What builds up
What accumulates with use, why it becomes the user's own, and why they'd miss it if they left.

## First version
- **The experience it must deliver**: the smallest version where the world and the signature moment still hold
- **Left for later**: things that are tempting but not needed to prove the idea

## Open questions
What's undecided or unverified, and which ones design should settle first.
```

Omit a section only when it truly doesn't apply, and say so in one line rather than silently dropping it.

## Check before handing over

- [ ] Someone who never heard the idea could picture a screen and replay a day of use
- [ ] The frame is named, and names, voice, and look all follow from it
- [ ] There are actual lines of copy and at least one image described concretely
- [ ] There is a signature moment, not just a list of features
- [ ] It's clear what builds up with use and why the user would come back
- [ ] No tech stack, architecture, or data model — experience requirements only
- [ ] Open questions are listed, not hidden
