---
name: keystone
description: Writes a product proposal (企画書) for an app or service idea from a planner's point of view, built around its core concept — who it's for, what value it promises, the insight behind it, and why it's different — so that the people who design and build it later can make every decision by returning to that concept. Keeps the look and world abstract and leaves technical design out. Use this skill whenever the user has an app or service idea — from a one-line hunch to a detailed memo — and wants it written up as a proposal, wants to sharpen its concept, or wants something to hand off before design and implementation, even if they never say "proposal" (e.g. 「このアイデアを企画書にして」「アプリの企画をまとめたい」「コンセプトを固めたい」「作る前に何のアプリか整理したい」「このネタで企画書書いて」).
---

# keystone — the stone that holds the arch together

The keystone sits at the top of an arch; take it out and everything else falls. A product's core concept plays the same role. This skill writes a proposal from a planner's point of view: it finds the core concept of an idea, states it sharply, and shows how everything else in the product hangs from it.

Write the proposal and the replies in the user's language.

## What this proposal is for

Design and implementation are someone else's job, and the look is still undecided. The proposal gives them **what the product is and why it should exist**, clearly enough that when they face a choice the proposal doesn't cover, they can answer it by going back to the concept.

So the core concept gets the most weight. Everything else — the user, the pain, the experience, the scope — is there to explain and support it.

Keep these out: tech stack, architecture, data models, screen specs, concrete visual design (colors, fonts, layouts, illustrations). The world and tone appear only as a direction — a few keywords and what the product must not feel like — because deciding them is design's job. When a constraint matters to the concept ("used one-handed on a crowded train"), write it as a requirement on the experience and let design decide how to meet it.

## What makes a strong core concept

- **One sentence carries it.** For whom, in what situation, what they get, and what makes it different. If it takes a paragraph, the concept isn't decided yet.
- **It rests on an insight.** Behind every good concept there's a truth about people that others have missed or underrated — why they really struggle, or what they actually want as opposed to what they say. Name it. A concept without an insight is just a feature description.
- **It promises value, not features.** "Photos are auto-tagged" is a feature; "you never lose a memory because you forgot where you put it" is value. Features belong later, as the means.
- **It can say no.** A useful concept rules things out. If every plausible feature fits it, it's too vague to guide anyone. Write down what the concept includes and what it excludes.
- **It is different in a way that matters to the user.** Not "uses AI" or "is prettier" — a difference the target user would notice and care about compared with what they do today.

## How to work

### 1. Read the idea

The idea may arrive as one line, a memo, a pasted document, or earlier conversation. Pull out what's already decided: the user, the pain, what the product does, any preferences. Note what's missing.

### 2. Sharpen the concept

This is the heart of the work. From the same idea, several different concepts are usually possible — the same app can be about saving time, about feeling proud, or about connecting with someone — and each leads to a different product.

Unless the user already has a clear concept, propose 2–3 candidate concepts that differ in the value they promise, not just in wording. For each: the one-sentence concept, the insight it rests on, and one line on how the product would differ as a result. Say which you'd pick and why, then let the user choose or mix.

Ask at the same time only what you can't reasonably decide yourself and that would change the concept — usually who it's for and the moment it's used. Offer a default for each so the user can just say "go with that".

If the user asked you to just write it, pick the strongest concept yourself and note the alternatives in one line at the end of the proposal.

### 3. Write the proposal

Fill the template below. Write the core concept section first and with the most care; then write every other section so it visibly follows from the concept. If a section says something the concept doesn't explain, either the section is wrong or the concept is missing something — fix whichever it is.

Save it as a Markdown file — `docs/proposals/<idea-name>.md` in the working directory unless the user names another place — and give a short summary in the reply: the concept sentence, the insight, and the open questions that most need an answer.

### 4. Revise

When the user changes the concept, revisit every section; a new concept usually changes the target moment, the core experience, and the scope too.

## Proposal template

```markdown
# [Product name (working title)]

## Core concept
- **Concept**: one sentence — for whom, in what situation, what they get, what makes it different
- **Insight**: the truth about people this concept rests on
- **Core value**: the one thing the user must feel for the product to have succeeded
- **Fits the concept / doesn't**: 3–5 examples each of directions that follow from the concept and ones that would betray it

## Background
- **Who**: the target user, specific enough to picture one person
- **The moment**: when and where the need arises
- **The problem or wish**: what they struggle with or want
- **Today**: how they cope now, and why it isn't enough

## What the product offers
- **Core experience**: what the user does and gets, in a few lines — the experience that delivers the core value
- **Main functions**: each with one line on how it serves the concept, in priority order
- **Why they come back**: what makes it part of their routine, if it's meant to be used repeatedly

## Why this, why now
- **Alternatives**: the existing products or habits it competes with
- **Difference**: what the user would notice and care about
- **Why now** (omit if not relevant): what has changed that makes it possible or needed

## World and tone (direction only)
- **Keywords**: three to five words for the mood
- **Not like**: products or moods it must not be mistaken for
- Concrete visual design is left to design.

## First version
- **Must prove**: the smallest version in which the core value can be felt
- **Left for later**: tempting things that aren't needed to prove the concept

## Success
- **What success looks like**: the state of users when the concept is working
- **Signals**: a few things you could observe or measure to tell

## Risks and open questions
- **Assumptions to verify**: the beliefs the concept depends on, riskiest first
- **Open questions**: what's undecided, and which ones design should settle first
```

Omit a section only when it truly doesn't apply, and say so in one line rather than silently dropping it.

## Check before handing over

- [ ] The concept fits in one sentence and names whom it's for, what they get, and what's different
- [ ] There's an insight, and it's something about people — not a feature or a technology
- [ ] The concept rules things out; the "doesn't fit" list is real
- [ ] Every function and the first-version scope can be traced back to the concept
- [ ] World and tone stay at the level of direction; no concrete visual design
- [ ] No tech stack, architecture, or data model
- [ ] Assumptions and open questions are listed, not hidden
