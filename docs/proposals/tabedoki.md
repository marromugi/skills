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

# たべどき（仮）

<p class="sub">冷蔵庫を撮るだけで、<br>今夜食べる一品が決まる。</p>

<!--
「たべどき」は仮称。名前は デザイン・ブランディングの段階で決め直してよい。
元メモ：対象は一人暮らしの20代社会人／冷蔵庫の中身を撮るとAIが「今日中に食べるべきもの」を判定／使い切ると何かがもらえる／見た目は可愛く／課金は月300円くらい。
-->

---

<!-- _class: statement ch1 -->

<div class="ghost">01</div>
<p class="label">SCENE</p>

# 平日22時。冷蔵庫を開けると、<br>先週買った<strong>半分のキャベツ</strong>が<br>しなびかけている。

<!--
帰宅したのは21時半。疲れていて、何を作るか考える気力はない。
キャベツ、使いかけの豆腐、賞味期限がよくわからない卵。見なかったことにして扉を閉め、デリバリーを頼む。
このアプリが立ち会うのは、この「扉を閉める直前の数秒」。
-->

---

<!-- _class: split ch1 -->

<div class="panel">
<p class="label">TARGET</p>
<div class="big">みお</div>
<div class="meta">26歳・会社員・一人暮らし2年目</div>
</div>

## 自炊したい気持ちはある。<br>でも<strong>平日の夜</strong>は余力がない

- 週末にまとめ買い
- 平日は外食と惣菜
- 週末に傷んだ物を捨てる

<!--
ペルソナ補足：
- 料理は嫌いではない。簡単なものなら作れる。
- 食材を捨てるたびに「またやってしまった」と小さく落ち込む。
- 冷蔵庫管理アプリは入れたことがあるが、登録が面倒で3日でやめた。
- スマホで可愛いもの・集めるものは好き。
-->

---

<!-- _class: statement ch2 -->

<div class="ghost">02</div>
<p class="label">PROBLEM</p>

# 買った食材を、<br><strong>使い切れずに捨てている。</strong>

<p class="sub">そのたびに、自分の暮らしが少し嫌になる。</p>

<!--
問題はお金のロスだけではない。「ちゃんと暮らせていない」という小さな自己嫌悪が、捨てるたびに積み重なる。
-->

---

<!-- _class: turn ch2 -->

<div class="ghost">02</div>
<p class="label">INSIGHT</p>

# 忘れているんじゃない。<br><strong>見るのが気まずくて、<br>目をそらしている。</strong>

<!--
表向きの理由は「忘れていた」「期限を把握していなかった」。だから既存アプリは「一覧で管理」「期限を通知」で解決しようとする。
でも本当は、冷蔵庫の奥に何があるかは薄々わかっている。わかっているからこそ、しなびた野菜と向き合うのが気まずくて、見ないようにしている。
そこに期限リストや「あと2日です」という通知が来ても、気まずさが増えるだけで行動は変わらない。
必要なのは情報を増やすことではなく、「今日はこれだけ食べればいい」と一つに絞ってもらうこと、そしてできたときに気持ちよくなれること。
-->

---

<!-- _class: concept ch3 -->

<div class="ghost">03</div>
<p class="label">CORE CONCEPT</p>

# 冷蔵庫を開けるのが、<br><strong>ちょっと楽しみ</strong>になる。

<p class="sub">一人暮らしの20代が、撮るだけで今夜の一品を知り、<br>使い切るたびにほめられる。管理させない冷蔵庫の相棒。</p>

<!--
判断の軸：迷ったら「これで冷蔵庫を開けるのが楽しみになるか？ 気まずくなるか？」を問う。
- 期限リスト、廃棄量グラフ、急かす通知 → 気まずくなるので入れない。
- 今日の一品を一つだけ示す、使い切りをほめる、小さなごほうびが集まる → 楽しみになるので入れる。
-->

---

<!-- _class: ch4 -->

<p class="label">HOW IT WORKS</p>

## 撮るだけで、<strong>今夜の一品</strong>が決まる

<div class="steps">
<div class="step"><div class="num">01</div><div class="head">撮る</div><div class="body">扉を開けて一枚。<br>入力はしない</div></div>
<div class="step"><div class="num">02</div><div class="head">知る</div><div class="body">今日食べる物が<br>一つだけ出る</div></div>
<div class="step"><div class="num">03</div><div class="head">使い切る</div><div class="body">食べたら<br>ごほうびがもらえる</div></div>
</div>

<!--
機能の優先順位と、コンセプトへの効き方：
1. 撮影だけで食材を把握（手入力ゼロ）… 「管理させない」を守る土台。前回の写真との差分で「いつからあるか」を推定する。
2. 「今日中に食べるべき一品」の判定 … 一覧ではなく一つだけ出す。簡単な食べ方のヒントを一行添える程度。
3. 使い切りのごほうび … 次の写真でその食材が消えていたら（または自分で「食べた」を押したら）ごほうびが届く。
-->

---

<!-- _class: statement ch4 -->

<div class="ghost">04</div>
<p class="label">WHY THEY STAY</p>

# 使い切った食材が、<br><strong>ちゃんと暮らせた証</strong>として<br>たまっていく。

<!--
「何かがもらえる」の中身は、使い切った食材にちなんだ小さなコレクション（例：キャベツを使い切るとキャベツのシールが一枚増える、のような方向）。具体的な形はデザインに委ねる。
大事なのは、集まったものが「捨てなかった回数」の記録になり、自分をちょっと好きになれること。やめると、この記録が途切れるのが惜しい。
実物のごほうび（クーポン等）は第一版では扱わない。提携先が必要になり、コンセプトの軸が「お得」にずれるため。
-->

---

<!-- _class: ch5 -->

<p class="label">DIFFERENCE</p>

## ほかは「管理」させる。<br>これは<strong>今夜の一品</strong>だけ言う

<div class="vs">
<div class="them">
<div class="tag">OTHERS</div>
<div class="big">食材を登録して、<br>期限を一覧で見張る</div>
</div>
<div class="us">
<div class="tag">THIS</div>
<div class="big">撮るだけで、<br><strong>今夜食べる一品</strong>だけ<br>教えてくれる</div>
</div>
</div>

<!--
具体的な競合は付録の表を参照（パンダかご、AI冷蔵庫、Rezo、Pecco、パナソニックの冷蔵庫AIカメラなど）。
既存アプリもレシート撮影・食材撮影でAI登録ができるようになっており、「撮るとAIが認識する」こと自体は差別化にならない。
違いは出力の形：一覧と通知で見張らせるのではなく、一つに絞り、できたらほめる。
-->

---

<!-- _class: split ch5 -->

<div class="panel">
<p class="label">GUARDRAILS</p>
<div class="big">責めない。<br>増やさない。<br>一つだけ。</div>
</div>

<div class="dodont">
<div class="do">
<div class="head">DO</div>

- 撮るだけで完結
- 一度に一品だけ
- できたら必ずほめる

</div>
<div class="dont">
<div class="head">DON'T</div>

- 手入力をさせる
- 捨てた量を見せる
- 通知で急かす

</div>
</div>

<!--
各「DON'T」の理由は付録を参照。
-->

---

<!-- _class: ch5 -->

<p class="label">WORLD & TONE</p>

## 冷蔵庫に<strong>小さな味方</strong>がいる感じ

<div class="chips"><span>ゆるい</span><span>ほめ上手</span><span>手のひらサイズ</span></div>
<div class="chips"><span class="no">家計簿っぽさ</span><span class="no">エコの説教</span><span class="no">子ども向けすぎ</span></div>

<!--
メモの「見た目は可愛くしたい」を、方向性として言い換えるとこうなる。
可愛さの目的は「冷蔵庫を開ける気まずさを和らげること」。26歳の会社員が電車の中で開いても恥ずかしくない可愛さ。
具体的な色・キャラクター・レイアウトはデザインに委ねる。
-->

---

<!-- _class: statement ch6 -->

<div class="ghost">06</div>
<p class="label">FIRST VERSION</p>

# 撮った次の日も、<br><strong>また撮りたくなるか</strong>を確かめる。

<p class="sub">入れるのは「撮る・今日の一品・使い切りのごほうび」の3つだけ。</p>

<!--
第一版で入れないもの：レシピ検索、買い物リスト、家計・節約額の表示、家族共有、実物の特典。
-->

---

<!-- _class: ch6 -->

<p class="label">NEXT</p>

## まず確かめる<strong>3つ</strong>のこと

<ol class="big">
<li>写真だけの判定を信じてもらえるか</li>
<li>ごほうびで使い切りが続くか</li>
<li>月300円を払う理由はどこにあるか</li>
</ol>

<!--
1. 最大のリスク。写真からは賞味期限の文字が読めないことが多い。見た目と「前回の写真から何日あるか」で判定するが、外れたときに信頼を失わないか。手元の実物で1〜2週間の試用を数人に。
2. ごほうびが「最初の数回だけ嬉しい」で終わらないか。2週間後も撮影が続くかを見る。
3. 無料で核の体験（今日の一品）を渡したうえで、何に月300円を払いたいか。候補：撮影回数の上限解除、コレクションの拡張、過去の記録の振り返り。
-->

---

<!-- _class: divider -->
<!-- _header: "" -->
<!-- _paginate: false -->

<p class="label">APPENDIX</p>

# 付録

---

<!-- _class: appendix -->
<!-- _header: "" -->

## 代替手段の詳細

| 代替手段 | していること | ここでの違い |
| --- | --- | --- |
| パンダかご | レシート撮影で在庫と期限を自動追跡 | 在庫の把握はさせず、今日の一品だけを示す |
| AI冷蔵庫（fridge ai） | レシート撮影で登録、期限通知、AIレシピ提案 | 通知で追わない。できたらほめる |
| Rezo | 食材撮影でAIが名前・期限候補を提案して登録 | 登録という作業自体をなくす |
| Pecco | 手入力で食材・期限管理、手持ち食材でレシピ検索 | レシピ探しではなく「何を食べるか」を一つに決める |
| パナソニック 冷蔵庫AIカメラ | 対応冷蔵庫の野菜室を自動撮影・認識 | 専用家電が不要。一人暮らしの小型冷蔵庫で使える |
| 何もしない／デリバリー | 見なかったことにして、週末に捨てる | 扉を閉める前の数秒に、気まずくない選択肢を出す |

<!--
2026年9月時点のWeb検索で確認した主なアプリ。機能は各社の紹介ページ・記事に基づく概要で、詳細は未検証。
-->

---

<!-- _class: appendix -->
<!-- _header: "" -->

## ガードレールの詳細

| 方向 | する／しない | 理由 |
| --- | --- | --- |
| 入力 | 撮影だけで完結させる。手入力は必須にしない | 登録の手間が、既存アプリが続かない最大の理由 |
| 提示 | 一度に一品だけ示す。一覧を主役にしない | 情報が増えるほど気まずさが増え、目をそらす |
| 評価 | 使い切りをほめる。捨てた量・金額は見せない | 罪悪感は行動ではなく「開かない」を生む |
| 通知 | 急かす通知は送らない。送るなら誘い | 「あと2日です」は冷蔵庫を開ける前の気まずさを増やす |
| 課金 | 「今日の一品」は無料でも必ず使える | 核の体験に鍵をかけると、コンセプトごと届かない |
| 見た目 | 可愛く、でも大人が使えるトーン | 対象は20代社会人。子ども向けに寄ると離れる |

---

<!-- _class: appendix -->
<!-- _header: "" -->

## 範囲・成功の目安・リスク

| | |
| --- | --- |
| 第一版 | 冷蔵庫の撮影／今日食べるべき一品の判定（一品のみ）／使い切りのごほうびとコレクション |
| 後回し | レシピ検索、買い物リスト、節約額の表示、家族・同居人との共有、実物の特典や提携 |
| 成功の目安 | 撮影が週3回以上、2週間後も続いている／示した一品を実際に食べた割合が高い／「捨てる量が減った」と本人が感じる |
| 前提 | 写真だけで「今日食べるべき」を納得感ある精度で判定できる／ごほうびが使い切り行動を後押しする |
| 課金の方向 | 月300円前後のサブスクを想定。何に払ってもらうかは未確定（候補：回数上限の解除、コレクション拡張、記録の振り返り） |
| リスク | 判定が外れて傷んだ物を勧める（食の安全に関わるため「最終判断は自分で」の伝え方が要る）／冷蔵庫の写真を撮られることへの抵抗感 |
| 未決事項 | 冷凍庫・調味料を対象に含めるか／「使い切った」を写真差分で判定するか自己申告にするか／名前 |

<!--
検討した他のコンセプトの方向（今回は採用せず）：
- 「考えなくていい夜ごはん」：今日の献立を決める負担を減らす方向。価値は時短・判断疲れの軽減。レシピアプリとの差が小さく、メモの「ごほうび」「可愛さ」が活きにくいので見送り。
- 「捨てない自分を育てる」：使い切り記録で自己効力感を育てる方向。ゲーム性が強くなり、撮影という日常動作から離れやすい。要素は「WHY THEY STAY」に取り込んだ。
- 採用：「冷蔵庫を開けるのが、ちょっと楽しみになる」。インサイト（気まずくて目をそらす）に正面から応え、メモの4要素（撮影・判定・ごほうび・可愛さ）がすべてこの一文から説明できるため。
-->
