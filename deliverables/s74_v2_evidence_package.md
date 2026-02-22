# s74 v2 Evidence Package (Immutable)

Task: `s74UTfZQx7XR6vdV_0IJs`  
Prepared by: Scout (`VzKdJ89cpXOcS7EiC_n99`)  
UTC: 2026-02-22T10:00:00Z

This package is implementation-ready evidence for adversary re-entry.

---

## A) Final ASO Copy Variants

### Variant A — Safety + Daily Novelty
- **Title (<=30):** Pet Parade Hop for Kids
- **Short description (<=80):** One-tap pet runner with daily themes, kid-safe ads, no chat.
- **Long description:**

Welcome to Pet Parade Hop — a colorful one-tap runner made for kids and families.

WHAT KIDS DO
- Tap to hop lanes and guide cute pets through parade routes
- Collect stars and costume tokens in quick 60-second rounds
- Unlock fun outfits, trails, and themed parade days

WHY FAMILIES LIKE IT
- Easy controls for young players
- No chat, no open text, no public profiles
- Gentle difficulty and low-pressure progression

KID-SAFE DESIGN
- Family-safe ad setup with strict caps
- Rewarded ads are optional and never required to progress
- External links are protected by a parental gate
- Data minimization for child-directed use

FRESH EVERY DAY
- Daily Parade Theme (Rainbow Day, Dino Day, Space Day)
- Sticker Passport stamps and weekly costume surprises

Play, collect, and parade again!

### Variant B — Collect & Customize
- **Title:** Pet Parade Hop: Cute Runner
- **Short description:** Tap, collect, and dress up pets in a safe kids runner game.
- **Long description:**

Pet Parade Hop is a kid-friendly runner where every short round brings new costume rewards.

HOP + COLLECT LOOP
- One-tap lane hopping
- Avoid playful obstacles
- Gather stars and costume tokens

CUSTOMIZATION FUN
- Unlock pet costumes and themed trails
- Build your Sticker Passport day by day
- Discover weekend surprise cosmetics

FAMILY-SAFE FEATURES
- No chat or open user-generated text
- Optional rewarded ads with strict daily cap
- Parent-protected external navigation
- Built with child privacy in mind

Perfect for quick, repeatable play sessions.

### Variant C — Quick Sessions / Parent Trust
- **Title:** Pet Parade Hop Kids Game
- **Short description:** Fast 60-second runs, safe design, daily kid-friendly rewards.
- **Long description:**

Looking for a simple game kids can enjoy in short sessions? Pet Parade Hop delivers fast fun with family-safe guardrails.

FAST FUN
- 60-second rounds
- One-tap controls
- Instant replay

REWARD CADENCE
- Every run: stars + tokens
- Every 3 runs: chest reward
- Daily themes + streak stamps

TRUST & SAFETY
- No chat, no public social feed
- No required ad watching for progression
- Kid-appropriate ad controls and frequency caps
- Parent gate for outbound links

Parade with adorable pets and collect new looks every day.

---

## B) Screenshot Shot List (Families-safe constraints)

### Global constraints (must pass)
1. No pressure language or loss-aversion urgency.
2. No open chat/community claims or visuals.
3. No deceptive/fake UI controls.
4. Readable text, high contrast, child-appropriate.
5. Only shipped features shown.
6. No third-party ad creatives in screenshots.
7. At least one parent-safety screenshot included.

### Shot list (8)
1. **Core gameplay clarity**
   - Visual: lane hopping + stars + obstacles
   - Overlay: “One-Tap Pet Parade Fun”
2. **60-second sessions**
   - Visual: in-run timer visible
   - Overlay: “Quick 60-Second Rounds”
3. **Costume unlock**
   - Visual: reward reveal with costume
   - Overlay: “Unlock Cute Costumes”
4. **Daily theme**
   - Visual: themed route (Dino/Space)
   - Overlay: “New Theme Every Day”
5. **Sticker Passport**
   - Visual: stamp board progression
   - Overlay: “Collect Daily Stamps”
6. **Replay loop**
   - Visual: end-run card with Play Again
   - Overlay: “Tap to Replay Instantly”
7. **Parent safety card**
   - Visual: settings + parent gate controls
   - Overlay: “No Chat • Parent Gate • Kid-Safe Ads”
8. **Friendly challenge mode**
   - Visual: challenge card, no usernames/chat
   - Overlay: “Friendly Challenges, No Public Chat”

---

## C) Experiment Tracker Template + Measurable Plan

### Tracker schema (implementation fields)
- Exp_ID
- Week
- Owner
- Hypothesis
- Surface
- Variant_A
- Variant_B
- Segment
- Start_UTC
- End_UTC
- Primary_KPI
- Guardrail_KPIs
- Min_Sample
- Success_Threshold
- Fail_Threshold
- COPPA_Families_Risk
- Kill_Switch_Trigger
- Rollback_Action
- Status
- Decision
- Evidence_URL

CSV template file: `deliverables/s74_experiment_tracker_template.csv`

### Execution plan (owners, timeline, thresholds)
| Exp_ID | Owner | Timeline (UTC window) | Primary KPI | Success threshold | Fail threshold |
|---|---|---|---|---|---|
| W1-E01 Icon A/B | Growth PM | 2026-02-23 → 2026-02-25 | Store CVR | +8% CVR vs baseline | -5% CVR vs baseline |
| W1-E02 Screenshot order | ASO Lead | 2026-02-23 → 2026-02-25 | Store CVR | +6% CVR | -4% CVR |
| W1-E03 Onboarding length | Game PM | 2026-02-24 → 2026-02-27 | Tutorial complete rate | >=90% | <85% |
| W2-E04 Chest cadence | Economy Designer | 2026-02-27 → 2026-03-02 | D1 retention | +2pp | -2pp |
| W2-E05 Rewarded cap 2 vs 3/day | Monetization Lead | 2026-02-27 → 2026-03-02 | ARPDAU | +3% with policy compliance | Any cap breach or D1 -1pp |
| W2-E06 End-run CTA copy | UX Writer | 2026-02-28 → 2026-03-02 | Replay rate | +5% | -3% |
| W3-E07 Theme naming | Content Lead | 2026-03-03 → 2026-03-06 | D3 return rate | +2pp | sentiment -10% |
| W3-E08 Challenge timing | Systems PM | 2026-03-03 → 2026-03-06 | Session frequency | +4% | negative sentiment +15% |
| W3-E09 Stamp threshold | Economy Designer | 2026-03-04 → 2026-03-07 | D7 retention | +1.5pp | session inflation >25% |
| W4-E10 EN vs EN+ES+PT | Localization Lead | 2026-03-08 → 2026-03-12 | New-user conversion | +5% | translation QA <95% |
| W4-E11 Creative refresh cadence | UA Lead | 2026-03-10 → 2026-03-14 | CTR | +7% | CVR -10% |
| W4-E12 Soft UA pilot | UA Lead + Compliance | 2026-03-10 → 2026-03-14 | CPI quality | +10% quality installs | Any Families policy warning |

Global guardrails for all experiments:
- Crash-free users >= 99.3%
- Policy warning tolerance = 0
- Ad cap compliance = 100%

---

## D) COPPA/Families Compliance Matrix + Rollback Triggers

### Asset-level matrix
| Asset | Risk focus | Control | Rollback trigger | Rollback action |
|---|---|---|---|---|
| ASO title/short/long copy | Misleading claims, child-targeting language misuse | Compliance review before publish | Any claim mismatch vs shipped features | Revert to previous approved listing copy |
| Screenshot set | Unsafe social/pressure/deceptive UI | Families-safe checklist gate | Screenshot fails any of 7 global constraints | Remove violating image + republish previous set |
| Store experiment metadata | Segment misuse | Restrict to approved audience configs | Misconfigured audience targeting | Pause experiment + restore baseline config |

### Experiment-level matrix
| Exp_ID | COPPA/Families risk | Specific risk | Kill switch trigger | Rollback condition |
|---|---|---|---|---|
| W1-E01 | Low | Misleading icon | Complaint spike >0.5% reviews/day | Restore baseline icon immediately |
| W1-E02 | Low | Unshipped feature claim | Any mismatch report from QA/compliance | Revert screenshot ordering set |
| W1-E03 | Medium | Reduced child clarity | Tutorial completion <85% | Reinstate guided onboarding |
| W2-E04 | Medium | Pressure loop | Negative reviews +20% | Return to prior chest cadence |
| W2-E05 | High | Ad pressure/non-compliant caps | Any cap breach OR D1 drop >1pp OR policy alert | Force cap=2/day and disable variant B |
| W2-E06 | Low | Manipulative CTA language | Policy/QA flag on CTA text | Revert to approved neutral CTA copy |
| W3-E07 | Low | Theme language appropriateness | Any exclusionary/fear wording flagged | Remove/rename theme set |
| W3-E08 | Medium | Social pressure | Sentiment drop +15% | Disable default challenge prompt |
| W3-E09 | Medium | Streak compulsion | Session inflation >25% + sentiment decline | Revert to 5-of-7 threshold |
| W4-E10 | Low | Translation policy mismatch | QA score <95% or policy term error | Roll back affected locale |
| W4-E11 | Low | Creative mismatch | CVR drop >10% over 48h | Revert prior creative pack |
| W4-E12 | High | Placement/policy non-compliance | Any Families warning/disapproval | Pause UA pilot instantly |

### Global kill-switch protocol
1. Trigger detected (dashboard/compliance alert).
2. Owner ACK within 30 minutes.
3. Disable variant via remote config.
4. Revert to last compliant baseline.
5. Log incident in experiment tracker with UTC + evidence URL.
6. Compliance sign-off required before re-enable.

---

## Evidence index
- This package is the canonical v2 evidence payload for adversary review.
- Tracker CSV companion in same commit/repo path.
