---
name: keystone
description: Writes a product proposal (企画書) for an app or service idea from a planner's point of view, as a story-driven concept deck (Marp Markdown slides, exported to HTML) built around its core concept — who it's for, the insight behind it, the value it promises, and how it differs from the alternatives — so that the people who design and build it later can make every decision by returning to that concept. Keeps the look and world abstract and leaves technical design out. Use this skill whenever the user has an app or service idea — from a one-line hunch to a detailed memo — and wants it written up as a proposal or pitch, wants to sharpen its concept, or wants something to hand off before design and implementation, even if they never say "proposal" (e.g. 「このアイデアを企画書にして」「アプリの企画をまとめたい」「コンセプトを固めたい」「作る前に何のアプリか整理したい」「このネタで企画書書いて」「企画のスライド作って」).
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

## Telling it as a story

A proposal deck that reads like a document has failed, even if every fact in it is right. The reader should be carried from one slide to the next, the way a good pitch unfolds: first they picture a person in a moment, then they feel the problem, then the insight turns it around, and only then does the concept land — as the answer to what they've just been shown.

The template follows that arc:

1. **Title** — the name and a tagline
2. **Scene** — one person, one place, one moment; the reader should be able to picture it
3. **Target** — who that person is
4. **Problem** — what goes wrong for them, in one line
5. **Insight** — the turn: what is really going on underneath
6. **Core concept** — the answer, on its own slide, in large type
7. **How it works** — three steps
8. **Why they stay** — what builds up with use
9. **Difference** — others give X, this gives Y
10. **Guardrails** — what we do / what we don't
11. **World and tone** — keywords only
12. **First version** — the one thing it must prove
13. **Next** — the three things to verify first
14. **Appendix** — the dense reference material (alternatives table, guardrails with reasons, scope, success signals, risks) for the people who design and build it

Read the slide titles alone, top to bottom: they should tell the story by themselves. If one of them doesn't follow from the one before, the order or the wording is off.

## Making each slide easy to read

- **One message per slide, and that's all the slide says.** The title is the message as a sentence ("疲れた夜は、考える気力が残っていない"), not a label ("インサイト"); the small label above it says which part of the story this is.
- **Very few words.** Statement slides (scene, problem, insight, concept, why they stay, first version) carry one or two lines and at most one supporting line. Other slides carry at most three short items, each a phrase of about 15 Japanese characters or less. When something doesn't fit, it doesn't belong on the slide: move it to the appendix or to presenter notes (`<!-- ... -->`), where the design team can still read it.
- **Highlight the key words.** Wrap the one phrase that matters most on each slide in `**...**` — or `<strong>...</strong>` inside the template's HTML blocks, where Markdown isn't parsed; the theme turns it red. One highlight per slide — if everything is highlighted, nothing is.
- **Break lines by hand.** On large-type slides, put `<br>` at natural phrase boundaries so no line ends mid-word and no line is left with one or two characters.
- **Use the layouts.** The theme has a class for each kind of slide — `lead`, `statement`, `concept`, `divider`, `appendix` — and blocks for steps, others-vs-this, do/don't, keyword chips, and a persona card. Use them as the template does rather than falling back to bullet lists; the variety is what keeps the deck from feeling like a document.
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

Copy `assets/slides-template.md` and fill it in, keeping its theme and its story order. Decide the concept slide first and with the most care; then write the slides before it so they lead up to it, and the slides after it so they visibly follow from it. If a slide says something the concept doesn't explain, either the slide is wrong or the concept is missing something — fix whichever it is.

Adjust the slide set to the idea: split a slide that's overcrowded rather than shrinking the text, and drop one that truly doesn't apply (mention that in the notes rather than dropping it silently). The main story is usually 12–14 light slides, plus a few appendix slides.

Save it as `docs/proposals/<idea-name>.md` in the working directory unless the user names another place. Then export HTML next to it so it can be opened in a browser:

```bash
npx -y @marp-team/marp-cli@latest docs/proposals/<idea-name>.md --html -o docs/proposals/<idea-name>.html < /dev/null
```

(`--html` lets the theme's layout blocks render. The `< /dev/null` matters: without it, the CLI can hang waiting for input.)

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
- [ ] Reading only the slide titles tells the story from scene to concept to next steps
- [ ] No main-story slide has more than three short items; dense material is in the appendix or notes
- [ ] World and tone stay at the level of direction; no concrete visual design or tech
- [ ] Risks and open questions are listed, not hidden
- [ ] The Markdown is saved and the HTML export was attempted
