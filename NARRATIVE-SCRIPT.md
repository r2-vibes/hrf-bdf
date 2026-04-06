# HRF Bitcoin Development Fund — Scrollytelling Narrative Script

> This is the story arc that drives the scroll experience. Each **SCENE** maps to a scroll step that transforms the visualization. The reader scrolls down; the data comes alive.

---

## SCENE 0 — THE SPARK
**Visual:** Black screen. A single orange dot fades in, placed over the UK on a dark world map.
**Text:**

> In June 2020, the Human Rights Foundation made a bet.
>
> One grant. One developer. One idea: a technique called CoinSwap that would help people defeat financial surveillance.
>
> His name was Chris Belcher.

**Data state:** 1 grant. 1 dot. 1 country. The map is almost entirely dark.

---

## SCENE 1 — FIRST WAVE
**Visual:** Two more dots appear (still UK-area + Argentina). A tiny bar chart begins forming at the bottom — 3 bars for categories: privacy, lightning, wallet.
**Text:**

> Two months later, Round 2. Three more grants: Zeus for Lightning node control, Fully Noded for mobile full-node access, and Openoms's JoinInbox for a graphical JoinMarket interface.
>
> The first $1 BTC grants to individual developers building tools people would actually use on their phones.

**Data state:** 4 grants across Rounds 1-2. 3 categories visible. Map: 2-3 locations.

---

## SCENE 2 — THE THESIS TAKES SHAPE
**Visual:** Dots multiply across the map — Nigeria, Argentina, US. The category bars grow. A timeline appears along the bottom, ticking through Rounds 3-6 (Dec 2020 → May 2021).
**Text:**

> Through 2021, a thesis emerged. This wasn't charity. It was infrastructure investment.
>
> Wallets for Nigeria. Lightning privacy for everyone. Bitcoin Core security. Arabic-language education. A mesh-networking protocol for people with no internet at all.
>
> Six rounds. Six categories. Developers on four continents.

**Data state:** ~20 grants. Categories: privacy, lightning, wallet, education, scaling, security. Map: ~8 countries + "Global."

---

## SCENE 3 — THE PIVOT
**Visual:** The education category bar suddenly surges — jumping from 2 grants to 5 in a single round. A new color appears in the category chart. The map shows cluster growth in Africa.
**Text:**

> Round 7 changed everything.
>
> Thirteen grants in one round — more than double any before it. Five were education: fellowships in Nigeria, Lightning development training, Bitcoin privacy workshops.
>
> HRF wasn't just funding code anymore. It was funding *people who would write the code next.*

**Data state:** 33 grants total. Education becomes the largest category. Nigeria cluster visible. First "hardware" and "design" grants appear.

---

## SCENE 4 — SCALE
**Visual:** The map fills rapidly. Dots cascade across Africa, Latin America, Asia. The cumulative grant counter ticks upward — 50, 75, 100. Timeline accelerates through Rounds 8-14 (2022-2023). Category chart becomes a stacked area, showing how the portfolio diversified.
**Text:**

> Then it scaled.
>
> 2022: mining grants, infrastructure builds, the first ecash project. 2023: nostr appears — a new protocol for censorship-resistant communication. Conferences in Africa, workshops in Latin America.
>
> By Round 14, the fund had backed over 100 projects across more than 30 countries.

**Data state:** ~130 grants. All major categories populated. Map shows global spread. Ecash (Round 9) and nostr (Round 11) highlighted as new entrants.

---

## SCENE 5 — THE NETWORK EFFECT
**Visual:** Lines begin connecting dots on the map — showing repeat grantees (BTCPay Server: 4 grants, Vinteum: 3, Summer of Bitcoin: 3). The visualization shifts to show a network graph: projects connected by shared categories and regions.
**Text:**

> Something unexpected happened. A network formed.
>
> BTCPay Server — the open-source payment processor — received four grants across multiple rounds. Summer of Bitcoin trained cohorts of developers who then received their own grants. Bitshala in India. Bitcoin Indonesia. Africa Bitcoin Conference.
>
> Grantees became mentors. Students became builders. The fund was compounding.

**Data state:** Highlight repeat grantees (4+ grants: BTCPay; 3 grants: Vinteum, VLS, Summer of Bitcoin, Stratospher, OpenSats, Bitshala, Bitcoin Indonesia, Africa Bitcoin Conference).

---

## SCENE 6 — THE MAP TODAY
**Visual:** Full global view. All 297 grants visible. Countries pulse with intensity proportional to grant count. A ring chart shows the current category breakdown. The map slowly rotates or the camera pulls back to show the full picture.
**Text:**

> Today: 297 grants. 242 unique recipients. 23 rounds. Every continent except Antarctica.
>
> From Kenya to Brazil to India to Venezuela. From core protocol work to Lightning wallets to ecash privacy to education programs reaching thousands.
>
> The largest category? Education — 93 grants, nearly a third of the total. HRF bet that if you teach people to build, they'll build things you never imagined.

**Data state:** Full dataset. Hero stats: 297 grants, 242 recipients, 23 rounds, 55+ countries/regions.

---

## SCENE 7 — THE SHIFT
**Visual:** Animated stacked area chart showing category evolution over time. Early rounds: almost all privacy/lightning/wallet/core. Recent rounds: education dominates, with payments, community, and nostr growing. Two overlaid trend lines show the shift.
**Text:**

> Look at how the portfolio evolved.
>
> The early rounds were pure cypherpunk: privacy tools, Lightning infrastructure, Core contributions. Technical. Focused. Necessary.
>
> But over time, the fund followed the frontier. Education scaled. Payments — real tools people use to send and receive bitcoin — became a top category. Community organizations sprouted across the Global South. Nostr and ecash emerged as new vectors for freedom.
>
> The fund didn't just react to the ecosystem. It helped shape it.

**Data state:** Category evolution chart. Highlight the crossover point where education overtakes technical categories.

---

## SCENE 8 — WHAT'S NEXT
**Visual:** The map dims slightly. A few dots glow brighter — the most recent round (Round 23, April 2026). New categories and regions are highlighted. A subtle animation suggests growth continuing beyond the frame.
**Text:**

> Round 23. April 2026. Twenty-six new grants.
>
> Eight education projects. Five payment tools. Three wallets. Three research initiatives. Spanning Afghanistan to West Africa to Southeast Asia.
>
> The fund keeps moving — toward the places and people who need these tools most.

**Data state:** Round 23 highlighted. Latest grants spotlighted.

---

## SCENE 9 — CTA
**Visual:** Clean, minimal. The full map fades to a subtle background. Large text over it. Two buttons: "Explore the Data" (opens interactive explorer) and "Support the Fund" (links to HRF).
**Text:**

> Every grant is a bet on freedom.
>
> Explore the full dataset. See every project, every developer, every round.
>
> Or help write the next chapter.

**Buttons:**
- **[Explore the Data →]** scrolls to interactive explorer section
- **[Support the Fund →]** links to hrf.org/devfund (or equivalent)

---

## DESIGN NOTES

### Transitions
- Each scene transition should feel *inevitable* — the data morphs, it doesn't jump-cut
- Use D3's `transition()` with ~800ms easing (d3.easeCubicInOut)
- Dots on the map should appear with a slight scale-up + fade (not pop)
- Numbers should count up (odometer effect) when they change

### Typography
- Scene text: large, centered, max ~60 characters per line
- Use Inter or Space Grotesk for narrative text
- JetBrains Mono for data labels and stats only
- Text fades in as you scroll into each scene, fades out as you leave

### Mobile
- Scenes stack vertically (text above, viz below)
- Map reduces to a flat projection (no 3D)
- Reduce animation complexity for performance

### Color Palette
- Background: #0a0a0a (keep the darkness)
- Primary accent: #F7931A (BTC orange) — for data points, highlights, buttons
- Secondary: #00DD44 (slightly softer green) — for education/growth elements
- Text: #FFFFFF (headings), #BBBBBB (body), #666666 (muted)
- Category colors: a curated 12-color palette that works on dark backgrounds
