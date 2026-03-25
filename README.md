# Who's Smarter? — Social Competitive Cognitive Game Prototype

A mobile-first async cognitive competition prototype exploring social mechanics as a retention driver in the mid-core social game space.

🕹️ **[Play the prototype →](https://ds30mins.github.io/whos-smarter-prototype/)**

---

## 🎯 Product Vision

Who's Smarter? started as a **market research project** before becoming a prototype.

The mobile gaming market reached $103B in 2025, but the growth story has shifted: downloads fell 7.2% while IAP revenue still grew — meaning the competitive advantage now belongs to games that retain existing players, not acquire new ones. The data points to one consistent driver: **social competition**. Mid-core social games achieve 11.45% D30 retention against a hybrid-casual baseline of 5.86% — nearly double. Players in social networks within games are 50% more likely to keep playing than solo players.

The specific category this prototype targets — **async social competition built around cognitive mini-games** — sits in an underserved position. The closest reference points are Duolingo (async 1v1, league system, weekly seasons), Words With Friends 2 (friend challenges, async format), and Trivia Crack 2 (cognitive + competitive, leagues). What none of them offer is a **skill-fair competitive format with no pay-to-win ceiling** — which is the explicit gap this concept addresses, and a direct lesson drawn from Elevate's 2025 league launch, which drove +40% DAU initially but faced backlash for pay-to-win perception.

This is not a brain training app. The framing is entertainment-first: *a social arena where intellectual performance is a currency for status — cognitive benefit is the side-effect, not the pitch.* That distinction matters both for positioning and for regulatory reasons (Lumosity was fined $50M in 2016 for medical claims).

This prototype is a playable hypothesis for what that product could feel like — built to validate the core loop before any further investment.

---

> 📸 *Screenshots — challenge flow and league standings*
>
> *Challenge screenshot*
>
> <img width="418" height="932" alt="Screenshot 2026-03-25 140325" src="https://github.com/user-attachments/assets/37d971b7-1f01-4727-b235-4a61e495cebc" />
> <img width="424" height="932" alt="Screenshot 2026-03-25 140438" src="https://github.com/user-attachments/assets/15b85d6c-c2fa-443b-9aa7-8743ab00bca3" />

> *League standings screenshot*
> 
> <img width="419" height="935" alt="Screenshot 2026-03-25 140529" src="https://github.com/user-attachments/assets/d54ad1a1-26b0-46fa-a7ce-fa3069cc45cb" />
> <img width="419" height="932" alt="Screenshot 2026-03-25 140547" src="https://github.com/user-attachments/assets/36202667-0fe3-40d8-851b-e45dd96d822d" />


---

## ✨ Core Features

### Async 1v1 Challenge Flow
Players accept or send friend challenges, then complete a 3-game sprint (Pattern Logic → Speed Tap → Memory Recall) at their own convenience. No scheduling required. The async model is a deliberate design decision — the 35–44 target player plays in short interstitial sessions, and real-time multiplayer creates scheduling friction that drives churn. Duolingo's Friends Clash validates this model at scale.

### 3-Game Sprint Format
Each challenge consists of three distinct cognitive mini-games targeting different ability types:
- **Pattern Logic** — spatial and sequential reasoning
- **Speed Tap** — processing speed and reaction time
- **Memory Recall** — short-term retention

Each game contributes to a combined score, reducing the impact of any single category on the outcome and making results feel fairer to a broad skill range.

### League System (Bronze → Silver → Gold → Diamond)
Players are placed in 30-person divisions. League Points are earned purely through gameplay performance — they **cannot be purchased**. This protects competitive integrity and prevents pay-to-win perception. Promotion and demotion thresholds create loss aversion mechanics that drive end-of-week session spikes (a testable hypothesis — see A/B Tests below).

### Dual-Currency Economy
- **League Points (soft currency):** Earned only through play. Drive rank movement. Cannot be bought.
- **Gems (hard currency):** Earned slowly through play or purchased via IAP. Used exclusively for cosmetics (avatar accessories, division banners) and convenience features (streak shields, extra daily sprints).

The separation ensures players at every spend level compete fairly, while higher spenders earn visible status — not rankings.

### Mobile-First UX
- Max-width 480px shell with dark UI optimised for low-light, commute-friendly sessions.
- Screen-to-screen navigation built for one-handed use with large tap targets throughout.
- Fade-in transitions and responsive micro-interactions on all interactive elements.

---

## 🧠 Design Decisions & Trade-offs

| Decision | Rationale |
|---|---|
| Async over real-time multiplayer | Removes scheduling friction for interstitial players; validated by Duolingo Friends Clash model |
| 30-person leagues over global leaderboards | Global boards feel unattainable and anonymous; small divisions make promotion feel achievable and demotion feel threatening |
| Cognitive framing over brain training framing | Brain training apps position cognitive challenge as a health outcome — users churn when they stop feeling they're improving. Entertainment framing sustains play without that ceiling. Also avoids FTC compliance risk (Lumosity fined $50M in 2016 for medical claims) |
| Soft currency for league points only | Protects competitive integrity; prevents pay-to-win perception that damaged Elevate's league launch |
| 3-game sprint format | Multi-category scoring reduces single-skill dominance, makes results feel fairer and broadens the viable player demographic |

---

## 📊 KPIs This Prototype Is Designed to Measure

If taken to soft launch, the primary hypothesis is: **social competition features drive retention above the hybrid-casual baseline.** Every metric below traces back to that hypothesis.

| KPI | Target | Benchmark / Rationale |
|---|---|---|
| D1 Retention | 40%+ | Hybrid-casual competitive baseline (GameAnalytics 2024) |
| D7 Retention | 16%+ | Hybrid-casual competitive baseline; social feature activation proxy |
| D30 Retention | 11%+ | Mid-core social target; nearly 2× hybrid-casual baseline of 5.86% |
| Daily Sprints / User | 3.5+ | Driven by rank-change push notifications |
| Challenge Accept Rate | 40%+ | Proxy for social layer engagement depth |
| K-Factor | 0.2 | Organic social referral target |
| ARPDAU | $0.60+ | Above hybrid-casual benchmark; *note: direct ARPDAU comps for this specific category are a known data gap* |

---

## 🧪 A/B Tests I Would Run First

Three highest-priority experiments for soft launch, each designed to validate a specific product decision before scaling UA spend:

**Test 1 — Does league demotion threat drive end-of-week sessions?**
Show a demotion warning notification to 50% of at-risk players (bottom 20% of division) on Sunday. Measure session frequency Sunday vs. Monday per segment. Hypothesis: demotion-zone players open the app 2× more on Sunday.

**Test 2 — Does async 1v1 challenge increase D7 retention vs. league-only?**
Split: 50% see a friend challenge CTA after onboarding; 50% see only the league CTA. Primary metric: D7 retention by variant + challenge send rate. Hypothesis: players who send or receive a direct challenge retain at D7 at 5%+ higher rate.

**Test 3 — Which onboarding framing drives higher D1 completion?**
A: *"Find your rank"* copy vs. B: *"Test your brain"* copy. All else identical. Primary metrics: onboarding completion rate + time to first league placement. Hypothesis: rank/competition framing outperforms brain training framing for the 35–44 segment.

---

## 🗺️ Now / Next / Later Roadmap

| NOW (Month 1–2) | NEXT (Month 3–4) | LATER (Month 5–6) |
|---|---|---|
| Core mini-game engine (3 types) | Friend challenge (async 1v1) | Clan / team challenges |
| 30-person leagues + MMR | Weekly season-end alerts | Avatar + customisation |
| Basic FTUE + onboarding | Brain report screen | Pro subscription tier |
| Soft launch (20 friends) | Daily streak system | AI difficulty personalisation |
| D1/D7 retention measurement | A/B test: demotion alert | National / regional leaderboards |
| A/B test: onboarding framing | Monetisation: ad integration | Broader soft launch scale-up |

---

## 🛠️ Technical Stack

| Layer | Choice | Note |
|---|---|---|
| Core | Vanilla HTML/CSS/JS (no build step) | Single `.html` file for maximum portability and shareability |
| Styling | Custom CSS with CSS variables | Dark UI with a consistent design token system |
| Fonts | Google Fonts — Plus Jakarta Sans | Clean, modern type that works across cognitive game screens |
| Deployment | GitHub Pages | Zero-config, shareable link |
| AI-assisted development | Claude (Anthropic) + Gemini (Google) | Used for code generation, iteration, and debugging during prototyping |

---

## 🎮 Other Projects

- [Mercantail — Pet Merge & Economy Prototype - Play the prototype](https://ds30mins.github.io/mercantail-pet-merge-prototype/) · [repo](https://github.com/ds30mins/mercantail-pet-merge-prototype)

---

📄 *A full product brief — including market research, competitor analysis, player segmentation, and full KPI framework — is available upon request.*

*Built as a personal project to explore social retention mechanics and async competition design in mobile gaming.*
