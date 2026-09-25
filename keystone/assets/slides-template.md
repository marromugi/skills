---
marp: true
lang: ja
paginate: true
size: 16:9
header: "<span>01 場面</span><span>02 課題</span><span>03 コンセプト</span><span>04 体験</span><span>05 違い</span><span>06 次へ</span>"
style: |
  @import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700;900&display=swap');
  /*
    Layout system (1280 x 720)
    - Grid: side margin 80px, header band 0-96px, title line fixed at y=128px
    - Golden split: panels are 38.2% / 61.8% of the width
    - Rule of thirds: statement text sits on the lower third line (y=480)
    - Type scale x1.618: 18 / 29 / 47 / 76
  */
  :root {
    --navy: #070A52;
    --red: #D21312;
    --red2: #ED2B2A;
    --coral: #F15A59;
    --white: #FFFFFF;
    --mist: rgba(7, 10, 82, 0.05);
    --line: rgba(7, 10, 82, 0.14);
    --sub: rgba(7, 10, 82, 0.6);
    --fs-s: 18px;
    --fs-m: 29px;
    --fs-l: 47px;
    --fs-xl: 76px;
    --mx: 80px;
  }
  section {
    font-family: 'Noto Sans JP', sans-serif;
    font-feature-settings: 'palt';
    font-size: var(--fs-m);
    line-height: 1.7;
    letter-spacing: 0.02em;
    color: var(--navy);
    background: var(--white);
    padding: 128px var(--mx) 64px;
    display: flex !important;
    flex-direction: column !important;
    justify-content: flex-start !important;
    position: relative;
  }
  section::after { color: var(--sub); font-size: 14px; right: var(--mx); bottom: 28px; padding: 0; }
  h1, h2 { font-weight: 900; line-height: 1.4; letter-spacing: 0.01em; margin: 0; color: inherit; }
  h1 { font-size: var(--fs-xl); }
  h2 { font-size: var(--fs-l); margin-bottom: 48px; }
  p { margin: 0; }
  section strong, section h1 strong, section h2 strong { color: var(--red); font-weight: 900; }
  ul, ol { margin: 0; padding-left: 1.1em; }
  li { margin: 0 0 0.5em; }
  li::marker { color: var(--red2); font-weight: 900; }
  .sub { font-size: var(--fs-m); color: var(--sub); margin-top: 24px; line-height: 1.6; }
  .label { font-size: var(--fs-s); font-weight: 900; letter-spacing: 0.2em; color: var(--red); margin-bottom: 20px; }
  
  /* Progress header: chapters across the top; the current one is set by a chN class */
  header { top: 36px; left: var(--mx); right: var(--mx); padding: 0; font-size: 14px; letter-spacing: 0.12em; color: var(--sub); display: flex; gap: 0; }
  header span { flex: 1; border-top: 3px solid var(--line); padding-top: 8px; font-weight: 700; }
  section.ch1 header span:nth-child(1), section.ch2 header span:nth-child(2), section.ch3 header span:nth-child(3),
  section.ch4 header span:nth-child(4), section.ch5 header span:nth-child(5), section.ch6 header span:nth-child(6) { border-top-color: var(--red); color: var(--red); }
  section.ch2 header span:nth-child(1), section.ch3 header span:nth-child(-n+2), section.ch4 header span:nth-child(-n+3),
  section.ch5 header span:nth-child(-n+4), section.ch6 header span:nth-child(-n+5) { border-top-color: var(--navy); color: var(--navy); }
  
  /* Ghost chapter number, top right */
  .ghost { position: absolute; right: var(--mx); top: 72px; font-size: 220px; font-weight: 900; line-height: 1; color: var(--mist); letter-spacing: -0.02em; }
  
  /* Title: golden split, navy 61.8% | red 38.2%, title on the lower third */
  section.lead { justify-content: flex-end !important; background: linear-gradient(90deg, var(--navy) 61.8%, var(--red) 61.8%); color: var(--white); justify-content: flex-end; padding-bottom: 208px; }
  section.lead h1 { font-size: var(--fs-xl); max-width: 61.8%; }
  section.lead .label { color: var(--coral); }
  section.lead .sub { color: var(--coral); font-weight: 700; max-width: 58%; }
  
  /* Statement: one message on the lower third line */
  section.statement { justify-content: flex-end !important; justify-content: flex-end; padding-bottom: 208px; }
  section.statement h1 { font-size: var(--fs-l); font-size: 56px; }
  
  /* Turn: the insight, on red */
  section.turn { justify-content: flex-end !important; background: var(--red); color: var(--white); justify-content: flex-end; padding-bottom: 208px; }
  section.turn h1 { font-size: 56px; }
  section.turn strong, section.turn h1 strong { color: var(--navy); }
  section.turn .label, section.turn .sub { color: rgba(255, 255, 255, 0.85); }
  section.turn .ghost { color: rgba(255, 255, 255, 0.12); }
  section.turn header span { border-top-color: rgba(255, 255, 255, 0.35); color: rgba(255, 255, 255, 0.7); }
  section.turn.ch2 header span:nth-child(2) { border-top-color: var(--white); color: var(--white); }
  section.turn::after { color: rgba(255, 255, 255, 0.7); }
  
  /* Concept: navy, lower third */
  section.concept { justify-content: flex-end !important; background: var(--navy); color: var(--white); justify-content: flex-end; padding-bottom: 208px; }
  section.concept h1 { font-size: 60px; }
  section.concept strong, section.concept h1 strong { color: var(--coral); }
  section.concept .label { color: var(--coral); }
  section.concept .sub { color: rgba(255, 255, 255, 0.75); }
  section.concept .ghost { color: rgba(255, 255, 255, 0.07); }
  section.concept header span { border-top-color: rgba(255, 255, 255, 0.25); color: rgba(255, 255, 255, 0.55); }
  section.concept.ch3 header span:nth-child(-n+2) { border-top-color: rgba(255, 255, 255, 0.8); color: rgba(255, 255, 255, 0.8); }
  section.concept.ch3 header span:nth-child(3) { border-top-color: var(--coral); color: var(--coral); }
  section.concept::after { color: rgba(255, 255, 255, 0.55); }
  
  /* Split: golden split, navy panel 38.2% on the left, content 61.8% */
  section.split { background: linear-gradient(90deg, var(--navy) 38.2%, var(--white) 38.2%) 0 96px / 100% calc(100% - 96px) no-repeat, var(--white); padding: 128px var(--mx) 64px calc(38.2% + 64px); }
  section.split .panel { position: absolute; left: var(--mx); top: 144px; width: calc(38.2% - var(--mx) - 48px); color: var(--white); }
  section.split .panel .label { color: var(--coral); }
  section.split .panel .big { font-size: var(--fs-l); font-weight: 900; line-height: 1.35; }
  section.split .panel .meta { font-size: var(--fs-s); color: var(--coral); font-weight: 700; margin-top: 12px; letter-spacing: 0.08em; }
  section.split header { left: var(--mx); }
  section.split header span { border-top-color: rgba(7, 10, 82, 0.14); }
  section.split h2 { font-size: 40px; margin-bottom: 40px; }
  section.split { padding-top: 144px; }
  section.split li { font-size: 26px; }
  section.split .dodont { gap: 32px; }
  section.split .dodont li { font-size: 22px; }
  
  /* Steps */
  .steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 48px; }
  .step .num { font-size: var(--fs-xl); font-weight: 900; color: var(--red); line-height: 1; }
  .step .head { font-size: var(--fs-m); font-weight: 900; margin: 20px 0 8px; padding-top: 16px; border-top: 3px solid var(--navy); }
  .step .body { font-size: 22px; color: var(--sub); line-height: 1.6; }
  
  /* Others vs this: golden split 38.2 / 61.8 */
  .vs { display: grid; grid-template-columns: 38.2fr 61.8fr; gap: 32px; }
  .vs > div { border-radius: 16px; padding: 32px 40px; }
  .vs .them { background: var(--mist); color: var(--sub); }
  .vs .us { background: var(--navy); color: var(--white); }
  section .vs .us strong { color: var(--coral); }
  .vs .tag { font-size: var(--fs-s); font-weight: 900; letter-spacing: 0.2em; margin-bottom: 12px; }
  .vs .us .tag { color: var(--coral); }
  .vs .big { font-size: 32px; font-weight: 900; line-height: 1.5; }
  
  /* Do / don't */
  .dodont { display: grid; grid-template-columns: 1fr 1fr; gap: 40px; }
  .dodont .head { font-size: var(--fs-s); font-weight: 900; letter-spacing: 0.2em; margin-bottom: 16px; padding-bottom: 8px; border-bottom: 3px solid var(--navy); }
  .dodont .dont .head { color: var(--red); border-bottom-color: var(--red); }
  .dodont li { font-size: 26px; }
  
  /* Keyword chips */
  .chips { display: flex; flex-wrap: wrap; gap: 16px; margin-bottom: 24px; }
  .chips span { font-size: var(--fs-m); font-weight: 700; padding: 8px 28px; border-radius: 999px; border: 3px solid var(--navy); }
  .chips span.no { border-color: var(--coral); color: var(--coral); text-decoration: line-through; }
  
  /* Numbered list for NEXT */
  ol.big { list-style: none; padding: 0; counter-reset: n; }
  ol.big li { counter-increment: n; display: grid; grid-template-columns: 96px 1fr; align-items: baseline; font-size: 32px; font-weight: 900; padding: 16px 0; border-bottom: 1px solid var(--line); margin: 0; }
  ol.big li::before { content: '0' counter(n); color: var(--red); font-size: var(--fs-l); }
  
  /* Appendix divider and reference slides */
  section.divider { justify-content: flex-end !important; background: var(--navy); color: var(--white); justify-content: flex-end; padding-bottom: 208px; }
  section.divider .label { color: var(--coral); }
  section.appendix { font-size: 20px; padding-top: 80px; }
  section.appendix h2 { font-size: var(--fs-m); margin-bottom: 28px; }
  table { font-size: 19px; border-collapse: collapse; width: 100%; line-height: 1.6; }
  th { background: var(--navy); color: var(--white); font-weight: 700; }
  th, td { border: 1px solid var(--line); padding: 10px 16px; text-align: left; vertical-align: top; }
  tr:nth-child(even) td { background: var(--mist); }
---

<!-- _class: lead -->
<!-- _header: "" -->
<!-- _paginate: false -->

<p class="label">PRODUCT CONCEPT</p>

# [Product name]

<p class="sub">[Tagline, one short line —<br>break it by hand if it runs long]</p>

---

<!-- _class: statement ch1 -->

<div class="ghost">01</div>
<p class="label">SCENE</p>

# [A person, a place, a moment.<br>Two or three short lines,<br>with the <strong>detail that makes it vivid</strong> in red.]

<!--
Hook: the target user in the moment the need arises — a scene, not a segment description.
-->

---

<!-- _class: split ch1 -->

<div class="panel">
<p class="label">TARGET</p>
<div class="big">[Name]</div>
<div class="meta">[Age ・ situation]</div>
</div>

## [Who this is for,<br>with the <strong>key moment</strong>]

- [Trait or routine, ≤ 15 chars]
- [Habit, ≤ 15 chars]
- [What they do today, ≤ 15 chars]

---

<!-- _class: statement ch2 -->

<div class="ghost">02</div>
<p class="label">PROBLEM</p>

# [The problem in one line,<br>with the <strong>key words</strong> in red.]

<p class="sub">[One supporting line]</p>

---

<!-- _class: turn ch2 -->

<div class="ghost">02</div>
<p class="label">INSIGHT</p>

# [The surface belief, turned.<br><strong>What is really going on.</strong>]

<!--
The reasoning behind the insight: what people say or do, what is going on underneath, and why it matters.
-->

---

<!-- _class: concept ch3 -->

<div class="ghost">03</div>
<p class="label">CORE CONCEPT</p>

# [The concept in one short sentence,<br>with the <strong>core value</strong> highlighted.]

<p class="sub">[One line: for whom · what they get · what's different]</p>

---

<!-- _class: ch4 -->

<p class="label">HOW IT WORKS</p>

## [The experience as a message, with the <strong>payoff</strong>]

<div class="steps">
<div class="step"><div class="num">01</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
<div class="step"><div class="num">02</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
<div class="step"><div class="num">03</div><div class="head">[Verb]</div><div class="body">[One short line]</div></div>
</div>

<!--
Main functions in priority order, each with one line on how it serves the concept.
-->

---

<!-- _class: statement ch4 -->

<div class="ghost">04</div>
<p class="label">WHY THEY STAY</p>

# [What builds up with use,<br><strong>and why they'd miss it.</strong>]

---

<!-- _class: ch5 -->

<p class="label">DIFFERENCE</p>

## [Others give X.<br>This gives <strong>Y</strong>]

<div class="vs">
<div class="them">
<div class="tag">OTHERS</div>
<div class="big">[What existing options give,<br>two short lines]</div>
</div>
<div class="us">
<div class="tag">THIS</div>
<div class="big">[What this gives, with the<br><strong>difference</strong> highlighted]</div>
</div>
</div>

<!--
Named alternatives are in the appendix table.
-->

---

<!-- _class: split ch5 -->

<div class="panel">
<p class="label">GUARDRAILS</p>
<div class="big">[The principle<br>to return to,<br>in three lines]</div>
</div>

<div class="dodont">
<div class="do">
<div class="head">[DO]</div>

- [≤ 12 chars]
- [≤ 12 chars]
- [≤ 12 chars]

</div>
<div class="dont">
<div class="head">[DON'T]</div>

- [≤ 12 chars]
- [≤ 12 chars]
- [≤ 12 chars]

</div>
</div>

<!--
The reason for each "don't" is in the appendix.
-->

---

<!-- _class: ch5 -->

<p class="label">WORLD & TONE</p>

## [The mood, with the <strong>key word</strong>]

<div class="chips"><span>[keyword]</span><span>[keyword]</span><span>[keyword]</span></div>
<div class="chips"><span class="no">[not like]</span><span class="no">[not like]</span><span class="no">[not like]</span></div>

<!--
Concrete visual design is left to design.
-->

---

<!-- _class: statement ch6 -->

<div class="ghost">06</div>
<p class="label">FIRST VERSION</p>

# [The one thing the first version<br>must prove, with the <strong>moment</strong>.]

<p class="sub">[What is in the first version, one line]</p>

---

<!-- _class: ch6 -->

<p class="label">NEXT</p>

## [What to verify first, with the <strong>count</strong>]

<ol class="big">
<li>[Riskiest assumption]</li>
<li>[Assumption]</li>
<li>[Open question]</li>
</ol>

---

<!-- _class: divider -->
<!-- _header: "" -->
<!-- _paginate: false -->

<p class="label">APPENDIX</p>

# [Appendix]

---

<!-- _class: appendix -->
<!-- _header: "" -->

## [Alternatives in detail]

| [Alternative] | [What it does] | [What's different here] |
| --- | --- | --- |
| [product or habit] | [...] | [...] |

---

<!-- _class: appendix -->
<!-- _header: "" -->

## [Guardrails in detail]

| [Direction] | [Do / don't] | [Why] |
| --- | --- | --- |
| [...] | [...] | [...] |

---

<!-- _class: appendix -->
<!-- _header: "" -->

## [Scope, success, risks]

| | |
| --- | --- |
| [In the first version] | [...] |
| [Left for later] | [...] |
| [Success signals] | [...] |
| [Assumptions to verify] | [...] |
| [Open questions] | [...] |

<!--
Other concept directions considered, one line each, and why this one was chosen.
-->
