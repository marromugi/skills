---
marp: true
lang: ja
paginate: true
size: 16:9
style: |
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700;900&display=swap');
  :root {
    --navy: #070A52;
    --red: #D21312;
    --red2: #ED2B2A;
    --coral: #F15A59;
    --white: #FFFFFF;
    --mist: rgba(7, 10, 82, 0.06);
    --line: rgba(7, 10, 82, 0.14);
    --sub: rgba(7, 10, 82, 0.62);
  }
  section {
    font-family: 'Noto Sans JP', sans-serif;
    font-size: 30px;
    line-height: 1.6;
    padding: 72px 96px;
    color: var(--navy);
    background: var(--white);
    justify-content: center;
  }
  section::after { color: var(--sub); font-size: 16px; }
  h1 { font-size: 52px; font-weight: 900; line-height: 1.35; margin: 0 0 0.5em; color: var(--navy); }
  h2 { font-size: 44px; font-weight: 900; line-height: 1.4; margin: 0 0 0.6em; color: var(--navy); }
  h1, h2 { text-wrap: balance; word-break: auto-phrase; }
  section strong, section h1 strong, section h2 strong { color: var(--red); font-weight: 900; }
  em { font-style: normal; color: var(--coral); font-weight: 700; }
  ul, ol { margin: 0; padding-left: 1.1em; }
  li { margin: 0.25em 0; }
  li::marker { color: var(--red2); }
  .label { display: inline-block; font-size: 18px; font-weight: 900; letter-spacing: 0.16em; color: var(--red); margin: 0 0 18px; padding-left: 44px; position: relative; }
  .label::before { content: ''; position: absolute; left: 0; top: 50%; width: 32px; height: 4px; background: var(--red); }
  .sub { font-size: 26px; color: var(--sub); }

  /* Title */
  section.lead { background: var(--navy); color: var(--white); }
  section.lead h1 { color: var(--white); font-size: 84px; margin: 0.1em 0 0.2em; }
  section.lead .sub { color: var(--coral); font-size: 32px; font-weight: 700; }
  section.lead .label { color: var(--coral); }
  section.lead .label::before { background: var(--coral); }

  /* One big statement */
  section.statement h1 { font-size: 60px; line-height: 1.45; }
  section.statement .sub { margin-top: 0.6em; }

  /* The core concept */
  section.concept { background: var(--navy); color: var(--white); }
  section.concept h1 { color: var(--white); font-size: 62px; line-height: 1.4; }
  section.concept strong, section.concept h1 strong { color: var(--coral); }
  section.concept .sub { color: rgba(255, 255, 255, 0.78); }
  section.concept .label { color: var(--coral); }
  section.concept .label::before { background: var(--coral); }

  /* Section divider */
  section.divider { background: var(--red); color: var(--white); }
  section.divider h1 { color: var(--white); font-size: 64px; }
  section.divider .label { color: var(--white); }
  section.divider .label::before { background: var(--white); }
  section.divider strong, section.divider h1 strong { color: var(--navy); }

  /* Steps */
  .steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 36px; margin-top: 12px; }
  .step { border-top: 6px solid var(--red); padding-top: 18px; }
  .step .num { font-size: 64px; font-weight: 900; color: var(--red); line-height: 1; }
  .step .head { font-size: 32px; font-weight: 900; margin: 12px 0 6px; }
  .step .body { font-size: 24px; color: var(--sub); line-height: 1.5; }

  /* Two columns: others vs this */
  .vs { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; margin-top: 8px; }
  .vs > div { border-radius: 20px; padding: 28px 36px; }
  .vs .them { background: var(--mist); color: var(--sub); }
  .vs .us { background: var(--navy); color: var(--white); }
  section .vs .us strong { color: var(--coral); }
  .vs .tag { font-size: 18px; font-weight: 900; letter-spacing: 0.12em; margin-bottom: 10px; }
  .vs .them .tag { color: var(--sub); }
  .vs .us .tag { color: var(--coral); }
  .vs .big { font-size: 34px; font-weight: 900; line-height: 1.45; }

  /* Do / don't */
  .dodont { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
  .dodont .head { font-size: 26px; font-weight: 900; margin-bottom: 10px; }
  .dodont .do .head { color: var(--navy); }
  .dodont .dont .head { color: var(--red); }
  .dodont li { font-size: 28px; }

  /* Keyword chips */
  .chips { display: flex; flex-wrap: wrap; gap: 16px; margin: 8px 0 28px; }
  .chips span { font-size: 30px; font-weight: 700; padding: 10px 28px; border-radius: 999px; border: 3px solid var(--navy); }
  .chips span.no { border-color: var(--coral); color: var(--coral); text-decoration: line-through; }

  /* Persona */
  .persona { display: grid; grid-template-columns: 300px 1fr; gap: 48px; align-items: center; }
  .persona .who { background: var(--navy); color: var(--white); border-radius: 24px; padding: 36px 28px; text-align: center; }
  .persona .who .name { font-size: 34px; font-weight: 900; }
  .persona .who .meta { font-size: 22px; color: var(--coral); font-weight: 700; margin-top: 6px; }

  /* Appendix: denser reference slides */
  section.appendix { font-size: 22px; display: block; padding-top: 64px; }
  section.appendix h2 { font-size: 32px; }
  table { font-size: 21px; border-collapse: collapse; width: 100%; }
  th { background: var(--navy); color: var(--white); font-weight: 700; }
  th, td { border: 1px solid var(--line); padding: 10px 16px; text-align: left; vertical-align: top; }
  tr:nth-child(even) td { background: var(--mist); }
---

<!-- _class: lead -->
<!-- _paginate: false -->

<p class="label">PRODUCT CONCEPT</p>

# [Product name]

<p class="sub">[Tagline — what it is, in one short line]</p>

---

<!-- _class: statement -->

<p class="label">SCENE</p>

# [A person, a place, a moment — one or two short lines that make the reader picture it]

<!--
Hook: open with the target user in the moment the need arises. Keep it a scene, not a description of a segment.
-->

---

<p class="label">TARGET</p>

## [Who this is for, as a message]

<div class="persona">
<div class="who">
<div class="name">[Name]</div>
<div class="meta">[Age · situation]</div>
</div>
<div>

- [Trait that matters to the idea]
- [Habit or routine]
- [What they do today]

</div>
</div>

---

<!-- _class: statement -->

<p class="label">PROBLEM</p>

# [The problem, as one line with the **key word** in red]

<p class="sub">[One supporting line]</p>

---

<!-- _class: statement -->

<p class="label">INSIGHT</p>

# [The insight — the truth about people — with the **turn** in red]

<!--
The surface behavior, what is really going on underneath, and why that matters. This slide is the "aha"; keep the reasoning here in notes.
-->

---

<!-- _class: concept -->

<p class="label">CORE CONCEPT</p>

# [The concept in one short sentence, with the **core value** highlighted]

<p class="sub">[One line: for whom · what they get · what's different]</p>

---

<p class="label">HOW IT WORKS</p>

## [The experience, as a message]

<div class="steps">
<div class="step"><div class="num">1</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
<div class="step"><div class="num">2</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
<div class="step"><div class="num">3</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
</div>

---

<!-- _class: statement -->

<p class="label">WHY THEY STAY</p>

# [What builds up with use, and why they'd miss it — one line]

---

<p class="label">DIFFERENCE</p>

## [How it differs, as a message]

<div class="vs">
<div class="them">
<div class="tag">OTHERS</div>
<div class="big">[What existing options give]</div>
</div>
<div class="us">
<div class="tag">THIS</div>
<div class="big">[What this gives, with the **difference** highlighted]</div>
</div>
</div>

<!--
Named alternatives are in the appendix table.
-->

---

<p class="label">GUARDRAILS</p>

## [The principle that decides what to build]

<div class="dodont">
<div class="do">
<div class="head">やる</div>

- [short]
- [short]
- [short]

</div>
<div class="dont">
<div class="head">やらない</div>

- [short]
- [short]
- [short]

</div>
</div>

---

<p class="label">WORLD & TONE</p>

## [The mood, as a message]

<div class="chips"><span>[keyword]</span><span>[keyword]</span><span>[keyword]</span></div>
<div class="chips"><span class="no">[not like]</span><span class="no">[not like]</span></div>

<p class="sub">Concrete visual design is left to design.</p>

---

<!-- _class: statement -->

<p class="label">FIRST VERSION</p>

# [The one thing the first version must prove]

<p class="sub">[What success looks like, in one line]</p>

---

<p class="label">NEXT</p>

## [What to verify first, as a message]

1. **[Riskiest assumption]**
2. **[Assumption]**
3. **[Open question]**

---

<!-- _class: divider -->
<!-- _paginate: false -->

<p class="label">APPENDIX</p>

# 補足資料

---

<!-- _class: appendix -->

## Alternatives in detail

| Alternative | What it does | What's different here |
| --- | --- | --- |
| [product or habit] | [...] | [...] |

---

<!-- _class: appendix -->

## Guardrails in detail

| Direction | Fits / betrays | Why |
| --- | --- | --- |
| [...] | [...] | [...] |

---

<!-- _class: appendix -->

## Scope, success signals, risks

| | |
| --- | --- |
| In the first version | [...] |
| Left for later | [...] |
| Success signals | [...] |
| Assumptions to verify | [...] |
| Open questions | [...] |

<!--
Other concept directions considered, in one line each, and why this one was chosen.
-->
