---
name: magpie
description: Generates ideas for small consumer (B2C) tools built on LLMs, aimed at solo developers. Starts from real pains people post on social media, forums, and app reviews — or from a new capability such as fast, structured LLM judgments — checks whether each pain is already solved, then designs products built on the LLM's judgments with a unique, visually fun experience — something people have never used before and keep coming back to collect. Every idea is checked against existing products before it is shown, so only ideas that survive reach the user. Use this skill whenever the user wants ideas for an LLM-powered app, tool, or service, is looking for a side project or indie product to build, wants to differentiate an existing idea, or wants to know whether an idea already exists, or asks what could be built with a new model or AI capability — even if they never say "brainstorm" (e.g. 「AIで何か作りたい」「個人開発のネタがない」「週末に作れるLLMアプリない？」「このアイデア競合多いけどどうずらす？」「これもうある？」).
---

# magpie — a bird that picks up shiny things

This skill finds real pains, checks that nobody has solved them well yet, and designs small LLM-powered products that solve them in a way that is fun to look at and fun to keep using. Like a magpie that picks shiny things out of the clutter, pick the pains worth solving out of what people actually say, and turn each into something people want to collect.

Write the reply in the user's language.

## What to aim for

- **Unique and visually fun is the design direction.** For every pain, ask whether it can be solved by making the experience fun to look at. "Fun" here means three things together:
  - An experience or look the user has never seen before. A product that looks like an existing category of app is not unique, however polished.
  - A distinctive design and tone that shows the subject from a new angle. Give the product its own world — a voice, a visual style, a frame borrowed from somewhere unexpected — so that something mundane reads as something else. Use images generously: generated illustrations, cards, or scenes made from the user's own data can carry the fun further than text and icons.
  - The joy of collecting — something that grows and fills up as it's used.
  - A pull to come back — retention that feels closer to a mild habit than a chore.
  - Attachment that grows with use. What piles up is the user's own history, so it becomes something only they have — and something they would miss if they left. A count of uses doesn't create attachment; a record that carries their choices, their places, their people does. Judgments can deepen this too: the more the user has fed in, the better the product knows their situation.
  Fun is not decoration added at the end. It is what solves the two hardest problems in B2C: retention and spread.
- **Build the experience on the LLM's judgments.** The LLM's core job is to pass many small judgments — pick one of a few options, give a score, say pass or fail — and the product turns those verdicts into what the user sees: a meter that moves, a referee's call, a rarity, a ranking, a gate that opens. Judgment models that return structured choices and scores in well under a second at almost no cost (e.g. Jev from TypeSafe AI) make it realistic to judge every photo, every message, or every action, in real time. That volume and speed is where new experiences come from. Niche judgments are welcome: a narrow call the LLM makes well lets you build a detailed, careful experience around it. Generated text is fine alongside the judgments — a line that explains a verdict, a label, a short narration — when it makes the experience richer. The judgments stay the core; the text rides on them.
- **Judge what anyone would agree on, but only meaning can decide.** The best judgments have a right answer that any person who reads the context would agree with, yet no keyword or rule can reach it — it takes understanding what the words or the scene mean. Such calls can be trusted, so the experience can lean on them. Calls of taste — funny, cute, good-looking, well-written — differ from person to person, and every miss makes the user feel the product doesn't get them.
- **The novelty includes the LLM's part.** An idea is new when both the way it looks and what the LLM does are things the user hasn't seen. A fresh look over a job any chatbot already does is not enough, and neither is clever processing behind an ordinary list.
- **Every idea answers a real pain.** Start from a pain, or start from a new capability and go find the pains it fits — but an idea that doesn't answer a real pain wastes all the design work after it.

## What to avoid

These are principles, not a list of banned topics. If an idea fits one, drop it unless you can say exactly why it escapes the problem.

- **Rare procedures.** Strong pain but used a few times in a lifetime, so nothing is collected and nobody comes back.
- **Outputs nobody wants to look at.** If the result is a form to submit or a list to manage, the fun direction has nothing to work with.
- **Generic extract-or-polish tools.** Pulling information out of text or images, or cleaning up writing, is crowded everywhere and easily absorbed by big platforms.
- **Pains everyone would think of.** The obvious ones get filled within six months to a year.
- **Fun as a skin.** Adding a cute theme to a management tool doesn't change the experience. The fun has to change how the product is used.
- **Judging taste.** If the verdict depends on the user's personal preference, it will be wrong for some users, and one wrong call on something they care about sinks trust in the whole product. Prefer calls with a right answer that needs meaning to reach.
- **The LLM only tidies up the input.** If the LLM's job is to take what the user typed or said and organize, summarize, or file it, the idea is ordinary however it is presented. The LLM should judge something the user couldn't easily judge themselves, and the experience should depend on that call.
- **Chat as the product.** If the main screen is a conversation with an AI — venting, asking, consulting — the user can already get that from any chatbot. Conversation can be one way to hand over input, but the value has to come from what the LLM does with the information afterwards.

## Which path to take

- **The user wants ideas** → run the idea pipeline below. If they haven't named a genre — a hobby, job, life stage, or kind of product — ask once before searching, and offer a few examples plus "leave it to you." Ideas land much better inside a genre the user cares about. If they leave it open, run the wide net without a genre.
- **The user starts from a technology** (a new model, API, or capability — "what could I build with X?") → run the idea pipeline with the technology entry in step 1. Also use this entry when the user asks for ideas that make the most of what LLMs can newly do.
- **The user brings their own idea** ("does this exist?", "lots of competitors, how do I differ?") → skip to the competitor research (steps A–E) on their idea and report with the "Report on the user's own idea" format. Report honestly even if it already exists — they asked about this idea specifically, so don't silently drop it.

## Idea pipeline

The user sees only ideas that survive every check. Ideas that already exist or have no distinct angle are cut without being mentioned.

### 1. Collect pains

Read `references/pain-research.md` and follow it. It covers how to search (wide net, then narrow, then dig), where to look, how to handle SNS accounts, what to record, and when to stop. Collect at least 10 pains.

**Technology entry.** When starting from a technology, first write down what it newly makes possible, in terms of judgments: what can now be judged, how fast, how cheaply, how often (e.g. "judge every photo in the camera roll instantly," "score every message as it's typed"). Then search for pains where that matters — people who wish something could be checked, rated, or decided for them, or who give up because judging by hand takes too long. The wide-net phrases for wanting a verdict in `references/pain-research.md` are the starting point.

### 2. Check whether each pain is already solved

For each pain, do a quick search (steps A–C of the competitor research, kept light) for products that already solve it. Drop a pain only when it is completely solved — existing products already solve it with an experience that leaves no room for a new one. Anything short of that stays, because this skill's whole approach is to solve pains with a new experience or a unique way of presenting them.

- **Completely solved** → drop the pain.
- **Solved, but only as plain management or a utility** → keep it. Note what exists; the new experience is the angle.
- **Solved, but users complain** → keep it, and carry the complaint into design.
- **Not solved** → keep it. Think once about why nobody has solved it (no demand, technically hard, data unreachable).

Doing this before designing matters: design work on a completely solved pain is wasted.

### 3. Design

For each remaining pain, design a product. Don't pick the look from a fixed menu; derive it from the pain itself — what the user does, what piles up, what changes over time, what they'd want to show someone. Push until the idea passes the "never seen before" test.

Start from what can be judged. For each pain, list the small judgments a product could pass:

- **What is judged**: a photo, a message, an action, a choice between options
- **The form of the verdict**: pick one of N, a score, pass or fail — with confidence
- **How often**: once a day, every item, continuously in real time
- **What the verdict drives**: which part of the experience moves because of it

Keep the judgments that pass both tests: anyone who understood the context would give the same verdict, and a keyword or rule couldn't. Drop judgments of taste. Among those left, pick the one that is most frequent and most tied to the pain, and build the look around its verdicts. The user should feel the judgment happening — a needle swinging, a stamp landing, a card's rarity revealed — not just see a tidier list.

While designing, check:

- **Where the LLM judges.** Name the judgment. If simple rules could make the call, the LLM isn't needed.
- **Input stays minimal.** The user's effort should stay around taking a photo, sending something, sharing, or leaving it alone. If it needs more, it won't be used.
- **The input is actually reachable.** Many apps and services don't let outside tools read their data. Check what can really be obtained, and design around what the user can hand over.
- **Frequency.** It should be used often enough for collecting and returning to matter.
- **Look and tone.** Decide the product's world before its screens: what it borrows its frame from, how it talks, what its images look like. Describe one image the user would get — what's in it, in what style — concretely enough to picture. Plain app chrome with a theme color is not a look.
- **What accumulates.** Name what builds up with use and why it becomes the user's own. If a year of use leaves nothing they'd be sad to lose, the idea won't grow on them. One-off events (a single move, a single trip) rarely build attachment.
- **Who and when.** You should be able to name the person and the moment they open it.

Design two or three different products for each promising pain — different judgments, different looks — rather than one. Aim for 10–15 designed candidates so that 5–7 survive the next step.

### 4. Verify each design against existing products

Step 2 checked the pain. Now check the specific product you designed: run the full competitor research (steps A–E), including reviews. Research can run more than once per idea — rerun it after rebuilding.

- **No close overlap** → keep it.
- **Same pain, clearly different experience** → keep it.
- **Close overlap** → rebuild it (step E), around a complaint or around a new experience, and keep the rebuilt version.
- **Close overlap and no new experience can be found**, or a big platform already offers the same experience for free → drop it silently.

If fewer than 5 survive, go back rather than lowering the bar: first to step 3 to design more variations on the surviving pains, then to step 1 for new leads. Do at least one round of this before showing fewer than 5. If still fewer survive, show them and say so briefly without listing what was dropped.

### 5. Present

Show 5–7 ideas. Spread them out: different pains, different moments of life, different kinds of fun. If several ideas share the same look or the same mechanism, keep the strongest and replace the rest.

## Competitor research

The goal isn't only "should this be built." When something overlapping exists, find what its users complain about and rebuild the idea to hit that. A competitor's one-star reviews are the spec for your next idea.

### A. Break the idea into searchable parts

Competitors don't always use the same name. Split the idea (or pain) into parts and build search terms from each: the pain, the user and moment, what the LLM does, and the experience or look. Something that shares only one or two parts can still be an overlap.

### B. Search

- Search the App Store, Google Play, Product Hunt, and the wider web, in both Japanese and English.
- Check whether built-in features of big platforms already do it. What they offer for free is hard for a solo developer to beat.
- Don't conclude "nothing exists" after one search. Try two or three rewordings first.
- For each competitor, note the name, platform, pitch (tagline or first line of the store description), rating and review count, and last update date. An app not updated in over a year may mean the demand was there but the product didn't last.

### C. Judge the overlap

- **No overlap**: nothing turns up after rewording.
- **Same pain, different experience**: competitors solve it, but in a different way — often as plain management. A different experience can make it a different product.
- **Close overlap**: similar pain and similar experience. Go to D–E.

Judge overlap by the experience, not by the mere existence of an app. A competitor with no reviews, or one that only works in another language, is still a competitor — note it — but neither fact alone is a reason to drop an idea. With no reviews, there are no complaints to hit, so rebuild around a new experience instead.

### D. Pull complaints from reviews

Read the 1–2 star reviews of overlapping competitors (add 3-star if there aren't enough) and group complaints by kind.

- App Store reviews can be fetched with the app ID: `https://itunes.apple.com/jp/rss/customerreviews/id=<APP_ID>/sortBy=mostRecent/json`. For Google Play, read the reviews on the store page.
- Count how many reviews raise each complaint and summarize a representative one. Weigh repeated complaints over one-offs.
- Complaints like "I stopped using it" or "I never look at it" usually mean the product is useful but not fun — exactly where this skill's direction helps most.

### E. Rebuild the idea

Rebuild around one or both of these:

- **Complaints**: pick 1–3 that come up repeatedly and that a solo developer can actually solve. For each, write one line on how the rebuilt idea solves it.
- **A new experience**: keep the pain, and change how the product is used or seen — what the user does, what they collect, what they look at, what they'd show someone. The rebuilt idea should feel like a different kind of product, not the competitor with a new skin.

Then:

- Check the rebuilt idea against the checklist, then run B–C on it again — the rebuilt version may overlap with something else.
- If neither works — the complaints are all things a solo developer can't fix, and no new experience holds up — don't force it. In the pipeline, drop the idea; for a user's own idea, say so and offer to run the pipeline instead.

## Checklist

Every idea shown must pass all of these.

- [ ] It answers a real pain collected in step 1 (or the user's own)
- [ ] The pain isn't completely solved, or the idea offers an experience existing products don't
- [ ] The look or presentation is something the user has never seen before (not a list, a feed, or a chat screen)
- [ ] It has its own design and tone that shows the subject from a new angle, with images doing part of the work
- [ ] It has a reason to collect and a reason to come back
- [ ] The experience is built on specific LLM judgments that rules can't make — not on organizing or summarizing the user's input, and not on a chat
- [ ] Anyone who understood the context would agree with those judgments — they need meaning, not taste
- [ ] User input is minimal and the input is actually reachable
- [ ] It gets used often enough
- [ ] What builds up with use is the user's own history, something they'd miss if they left
- [ ] You can name who uses it and when
- [ ] It survived competitor verification

## Output format

### Idea list

Open with how the ideas were found, so the user can judge how much to trust them and what was missed. Keep it short:

```markdown
**How these were found**
- **Where**: sources searched, and which were signed in, blocked, or skipped
- **Leads**: the communities or situations picked from the wide net, and why
- **Numbers**: N pains collected → N not already solved → N designed → N shown
```

Don't name the ideas that were dropped; the counts are enough.

Then write each idea in three parts, in this order (in the user's language). The reader should be able to judge the idea from the first part alone, then check where it came from and what already exists.

```markdown
### 1. [Title]

**The idea**
- **What the LLM judges**: what it judges, how often, and in what form (pick one / score / pass-fail)
- **The experience**: one concrete screen or moment
- **Look and tone**: the world it borrows from, and one image the user gets (what's in it, in what style)
- **Why it grows on them**: what builds up with use, and why it becomes something only this user has
- **Input caveats**: … (omit if none)

**The voices it came from**
- Who, at what moment, struggling with what — with links to the posts or pages
- How they cope today (the workaround, if there is one)

**Competitor research**
- What exists: the closest products, with names and links, and what they do
- How this differs: the new experience, or the complaint it hits
- What's left to check: reviews not yet read, overlaps worth a deeper look
```

After the list, ask the user which ideas interest them, and offer a deeper look at those: full competitor table, review complaints, and next steps.

### Report on the user's own idea

```markdown
## Competitor research: [idea title]

### Competitors found
| Name | Platform | Pitch | Rating (count) | Last update |
| --- | --- | --- | --- | --- |

### Overlap
No overlap / same pain, different experience / close overlap — one or two sentences on why

### Complaints in reviews
- [kind of complaint] (N of M reviews): summary of a representative review

### Rebuilt idea
- **Title**: …
- **Complaints it hits and how** (omit if rebuilt around a new experience only):
  - "…" → …
- **The experience**: … (one concrete screen or moment)
- **Checklist**: note any items it fails

### Verdict
Go ahead as is / go ahead with the rebuilt idea / drop it — one or two sentences on why
```

After the verdict, note anything you couldn't check (reviews you couldn't read, sites you couldn't log in to, web services not in app stores).
