---
name: keystone
description: Writes a product proposal (企画書) for an app or service idea from a planner's point of view, as a concept presentation deck (Marp Markdown slides, exported to HTML) built around its core concept — who it's for, the insight behind it, the value it promises, and how it differs from the alternatives — so that the people who design and build it later can make every decision by returning to that concept. Keeps the look and world abstract and leaves technical design out. Use this skill whenever the user has an app or service idea — from a one-line hunch to a detailed memo — and wants it written up as a proposal or pitch, wants to sharpen its concept, or wants something to hand off before design and implementation, even if they never say "proposal" (e.g. 「このアイデアを企画書にして」「アプリの企画をまとめたい」「コンセプトを固めたい」「作る前に何のアプリか整理したい」「このネタで企画書書いて」「企画のスライド作って」).
---

# keystone — the stone that holds the arch together

The keystone sits at the top of an arch; take it out and everything else falls. A product's core concept plays the same role. This skill writes a proposal from a planner's point of view: it finds the core concept of an idea, states it sharply, and shows how everything else in the product hangs from it — as a short concept deck someone can read in a few minutes.

Write the deck and the replies in the user's language.

## What this proposal is for

Design and implementation are someone else's job, and the look is still undecided. The proposal gives them **what the product is, for whom, and why it should exist**, clearly enough that when they face a choice the proposal doesn't cover, they can answer it by going back to the concept.

So the core concept gets the most weight. Everything else — the target, the problem, the experience, the alternatives, the scope — is there to explain and support it.

Keep these out: tech stack, architecture, data models, screen specs, concrete visual design (colors, fonts, layouts, character designs), and detailed pricing tables. The world and tone appear only as a direction — a few keywords and what the product must not feel like — because deciding them is design's job. When a constraint matters to the concept ("used one-handed on a crowded train"), write it as a requirement on the experience.

## What makes a strong core concept

- **One short sentence carries it.** Short enough to fit on a slide in large type — in Japanese, roughly 40 characters or less. Put the unpacking (for whom, what they get, what's different) in one supporting line underneath. If the concept needs a paragraph, it isn't decided yet.
- **It rests on an insight.** Behind every good concept there's a truth about people that others have missed or underrated — why they really struggle, or what they actually want as opposed to what they say. Name it. A concept without an insight is just a feature description.
- **It promises value, not features.** "Photos are auto-tagged" is a feature; "you never lose a memory because you forgot where you put it" is value. Features come later, as the means.
- **It can say no.** A useful concept rules things out. If every plausible feature fits it, it's too vague to guide anyone. Write down what fits and what would betray it.
- **It is different in a way that matters to the user.** Not "uses AI" or "is prettier" — a difference the target user would notice and care about compared with what they use today.

## Making the deck easy to read

The deck is read, not presented, so each slide has to make its point on its own.

- **One message per slide.** The slide title is that message as a sentence ("疲れた夜は、考える気力が残っていない"), not a label ("インサイト"). The small label above it says which part of the proposal this is.
- **Few words on the slide.** At most about five short lines. Phrases over sentences. If it doesn't fit, split the slide or move the reasoning into presenter notes (`<!-- ... -->`), which the design team can still read.
- **Tables for comparisons.** Alternatives, today's workarounds, in/out of scope — anything with two or more axes reads better as a table than as nested bullets.
- **Concrete people and moments.** "A 26-year-old office worker opening the fridge at 10pm" beats "busy young professionals".

## How to work

### 1. Read the idea

The idea may arrive as one line, a memo, a pasted document, or earlier conversation. Pull out what's already decided: the target, the pain, what the product does, any preferences. Note what's missing.

### 2. Sharpen the concept

This is the heart of the work. From the same idea, several different concepts are usually possible — the same app can be about saving time, about feeling proud, or about connecting with someone — and each leads to a different product.

Unless the user already has a clear concept, propose 2–3 candidate concepts that differ in the value they promise, not just in wording. For each: the one-sentence concept, the insight it rests on, and one line on how the product would differ as a result. Say which you'd pick and why, then let the user choose or mix.

Ask at the same time only what you can't reasonably decide yourself and that would change the concept — usually who it's for and the moment it's used. Offer a default for each so the user can just say "go with that".

If the user asked you to just write it, pick the strongest concept yourself and put the alternatives in the presenter notes of the last slide.

### 3. Look at the alternatives

Before writing, work out what the target user uses today instead: competing apps, built-in features of platforms they already use, and plain habits (a notes app, a group chat, doing nothing). If you can search the web, do a few quick searches to find real competing products and name them; otherwise work from what you know and say so in the notes. The point is not a market report — it's to make sure the stated difference is real and matters to the target user.

### 4. Write the deck

Copy `assets/slides-template.md` and fill it in. It holds the Marp setup, a simple theme, and one slide per part of the proposal: title, core concept, insight, target and persona, problem, experience, concept guardrails (fits / betrays), alternatives, world and tone, first version and success, risks and open questions. Write the core concept slide first and with the most care; then make every other slide visibly follow from it. If a slide says something the concept doesn't explain, either the slide is wrong or the concept is missing something — fix whichever it is.

Adjust the slide set to the idea: split a slide that's overcrowded, and drop one that truly doesn't apply (mention that in the notes rather than dropping it silently). Keep the whole deck around 10–14 slides.

Save it as `docs/proposals/<idea-name>.md` in the working directory unless the user names another place. Then export HTML next to it so it can be opened in a browser:

```bash
npx -y @marp-team/marp-cli@latest docs/proposals/<idea-name>.md -o docs/proposals/<idea-name>.html < /dev/null
```

(The `< /dev/null` matters: without it, the CLI can hang waiting for input.)

If the export fails (no Node, no network), keep the Markdown and tell the user how to render it (the Marp CLI command above, or the Marp extension for VS Code).

In the reply, give a short summary: the concept sentence, the insight, and the open questions that most need an answer, plus the paths to the two files.

### 5. Revise

When the user changes the concept, revisit every slide; a new concept usually changes the target moment, the experience, the guardrails, and the scope too.

## Check before handing over

- [ ] The concept fits in one short sentence on its slide, with a supporting line that names whom it's for, what they get, and what's different
- [ ] There's an insight, and it's something about people — not a feature or a technology
- [ ] The target is a specific persona in a specific moment
- [ ] The alternatives are named, and the difference is one the target user would care about
- [ ] The guardrails rule things out; the "betrays" list is real
- [ ] Every slide title is a message, and no slide is crowded
- [ ] World and tone stay at the level of direction; no concrete visual design or tech
- [ ] Risks and open questions are listed, not hidden
- [ ] The Markdown is saved and the HTML export was attempted
