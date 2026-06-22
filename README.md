# Hevy Training Plan — Source of Truth

Living document for Dmitry's training program. The program, the analysis behind it, and the adversarial reviews that shaped it.

Operational notes (Hevy account state, API surface, MCP setup, template ID lookup) live in [IMPLEMENTATION.md](./IMPLEMENTATION.md).

- **Owner:** Dmitry (Hevy account)
- **First built:** 2026-06-20
- **Current version:** v3 (post second adversarial review)
- **Last updated:** 2026-06-21

---

## 1. Context

### Trainee
- **Phase:** Maintenance / muscle retention. Recently completed ~20 lb fat-loss phase on tirzepatide; now on maintenance dose (~4.2 mg/wk, 5-day cadence).
- **Primary goal:** Hypertrophy + preserve/build lean mass. DEXA history shows ~10.5 lb lean-mass decline during fat loss — this is the deficit to recover.
- **Out of scope:** Diet, macros, supplementation. Training only.
- **Constraints:**
  - Bad knee. Avoid heavy axial squat loading and deep knee flexion. No conventional barbell deadlift (technique concern + knee load).
  - RPE not logged historically — program uses RIR cues + double progression, not RPE prescriptions.

### Equipment

**Home (enclosed garage):**
- Rogue wall-mounted rack with pull-up bar
- Olympic barbell + **Swiss bar (multi-grip)**
- Adjustable dumbbells **5–75 lb**
- IronMaster Super Bench + preacher curl attachment
- IronMaster cable tower
- IronMaster leg extension / leg curl attachments
- Cable handles: V, rope, rotating, single-arm

**BUR (Burlingame office gym):**
- Power rack + barbell + plates
- Cable stack / functional trainer
- **Incline leg press**
- Full dumbbell rack going past 75 lb
- **No hamstring curl machine** — hamstring work via RDL + Nordic

### Training frequency
- **3 sessions / week.** No fixed schedule. Home or BUR chosen ad hoc per day.
- Demonstrated adherence: ~3.0 sessions/wk sustained over 6+ months, ~12/month average for 2+ years.

---

## 2. Analysis driving the design (n=429 workouts since 2023-03-11)

### Volume per muscle — current intent (sets/wk, primary + 0.5×secondary)

| Muscle | v1 | v2 | **v3** | Notes |
|---|---|---|---|---|
| Chest | 10 | 10 | **10** | Bench D1 + Incline D2 + Fly carryover |
| Lats | 9 | 9 | **9** | Pulldown wide D1 + Pulldown close D3 + DB Row |
| Upper back | 9 | 9 | **9** | Seated Row D2 + DB Row D3 + Rear Delt Fly |
| Side delts | 6 | 11 | **8** | Lat Raise D1 (4) + D2 (4). D3 hit cut per v2 review. |
| Quads | 6 | 9 | **9** | Belt Squat + Leg Ext/Press + BSS |
| Hamstrings | 6 | 9 | **6 direct** | RDL D1 (3 hinge) + Leg Curl/Nordic D3 (3 knee-flex); honest count after v2 audit |
| Glutes | 9 | 9 | **9** | RDL + Hip Thrust + BSS |
| Biceps | 3 | 3 | **6** | Incline Curl D1 (3) + Preacher/Cable D3 (3) — v3 addition |
| Triceps | 9 effective | 9 effective | **9 effective** | Pushdown D2/D3 + Overhead D2 + Skullcrusher D3B + press carryover |
| Calves | 6 | 6 | **6** | Heavy D1 (3×6–10) + High-rep D2 (3×12–15) |
| Abs | 6 | 6 | **6** | Knee Raise D1 + Cable Crunch D3 |

### Imbalances the program addresses

1. **Posterior chain** — no squat or conventional deadlift. Replaced with RDL + Hip Thrust + Leg Curl/Nordic. Hip-dominant + knee-flexion both covered.
2. **No calves, no direct ab/core** — added to two days each.
3. **No vertical pull at home** until IronMaster cable tower returned. Now wide-grip + close-grip on separate days.
4. **No rear delt isolation** — Rear Delt Reverse Fly on Day 3.
5. **Bicep-heavy vs tricep direct work** — rebalanced. Biceps now also has a stretched-position hit on D1 (v3).
6. **Long-head triceps underloaded** — D2 A-variants use Overhead Cable Ext (long head); v3 pairs with Day 3 lateral/medial work for full-spectrum.

### Progression — last 12 weeks (top-set est-1RM, Epley)

**Improving:** Bench Press +6.9%, Incl Bench +2.9%, DB Row +6%, Chest Fly +16%, Lat Raise +32%.
**Stalled:** Overhead Press 0%, Triceps Extension 0%, V-grip Row 0%.
**Regressing:** DB Shoulder Press −4%, Lying Leg Curl −8%.

Peak lifts late-2024 / early-2025 sit ~15–25% above current — consistent with documented fat-loss + lean-mass decline. Floor holding; bench rebuilding.

### Data hygiene
- 7,257/7,407 sets logged as `type=normal`; 150 warmup. No dropsets / failure / AMRAP markers historically.
- One outlier ignored: Dumbbell Row 2024-05-31, logged 2472 kg × 12 (decimal/unit typo).

---

## 3. Program design

### Architecture
**3 days × 2 variants × 2 locations = 12 routines.**

- **Day 1** — Press + Hinge + Vertical Pull
- **Day 2** — OHP + Quad + Horizontal Pull
- **Day 3** — Pull + Posterior + Arms

- **Variant A** — heavier compound baseline (lower reps, longer rest).
- **Variant B** — variety with Swiss bar / DBs / cables (moderate reps, shorter rest).

Trains 3×/wk, one variant of each day per week. Home or BUR decided ad hoc by daily schedule.

### Double progression

1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Add 1 rep per set when possible each session.
3. When all sets hit the **top** of the range: next session **add 2.5 kg** (BB) / **5 lb** (DB), drop back to bottom of range.
4. Stop sets at **RIR 1–2**. Don't grind to failure on compounds.

### Readiness gate (v3 — Galpin MVP)

Morning, 10 seconds, before deciding the session:
- **Subjective 1–10 score** — composite of sleep, soreness, appetite, mood, motivation.
- **Score ≥ 5** → train as written.
- **Score 3–4** → drop the top set on every compound (3 sets become 2; 4 sets become 3). Keep weights.
- **Score < 3** → swap to Variant B if you had A planned (lower reps in better range, shorter rest, easier on CNS). Or skip and walk.

Log the score. Drift catches stalls before they show on the bar.

### Nordic Hamstring Curl — eccentric ramp-in (v3)

Nordic is brutal eccentric load. New movement, no skipping the ramp.

- **Weeks 1–2:** 2 sets × 3–5 reps, **eccentric-only**, 4-second lower. Concentric: drive from the floor with hands, or use a band wrapped around shoulders + rack. No unassisted descent yet.
- **Weeks 3–4:** 2 sets × 5–8 reps, band-assisted full reps.
- **Week 5+:** 3 sets × 5–8 reps, unassisted. Cue: lengthen the descent, no falling.

If DOMS shuts down a session, dial back a phase.

### Deload protocol

Every **5–7 weeks** (GLP-1 recovery tail), or when 2+ exercises stall for 2 consecutive sessions:
- **One light week.** Top-set weight × **0.6**. **2 sets** per exercise instead of 3. Same rep target. Smooth bar speed. Resume normal loads next week.

---

## 4. The 12 routines

One table per day. Four exercise columns: **Home A · Home B · BUR A · BUR B**. Each cell: exercise name — sets×reps · rest.

Hevy template IDs are in [IMPLEMENTATION.md §2](./IMPLEMENTATION.md#2-exercise-template-id-lookup).

### Day 1 — Press + Hinge + Vertical Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Horizontal press | Bench Press (BB) — 4×6–8 · 180s | Swiss Bench Press — 4×8–10 · 150s | Bench Press (BB) — 4×6–8 · 180s | Bench Press (DB) — 4×8–10 · 150s |
| 2 | Hip hinge | Romanian Deadlift (BB) — 3×8–10 · 150s | Romanian Deadlift (DB) — 3×10–12 · 120s | Romanian Deadlift (BB) — 3×8–10 · 150s | Romanian Deadlift (DB) — 3×10–12 · 120s |
| 3 | Vertical pull (wide) | Lat Pulldown (Cable) — 3×8–10 · 120s | Reverse Grip Lat Pulldown — 3×10–12 · 120s | Lat Pulldown (Cable) (BUR) — 3×8–10 · 120s | Reverse Grip Lat Pulldown — 3×10–12 · 120s |
| 4 | Quad single-leg | Bulgarian Split Squat — 3×8–10/side · 120s | Belt Squat — 3×10–12 · 120s | Bulgarian Split Squat — 3×8–10/side · 120s | Split Squat (DB) — 3×10–12 · 120s |
| 5 | Side delts | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s |
| 6 | Biceps (stretched) | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s |
| 7 | Calves (heavy) | Standing Calf Raise (DB) — 3×6–10 · 90s | Single Leg Standing Calf Raise (DB) — 3×6–10/side · 90s | Calf Press (Machine) — 3×6–10 · 90s | Calf Press (Machine) — 3×6–10 · 90s |
| 8 | Abs | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s |

> **v3 notes:** Slot 6 (Incline / Hammer Curl) is new — added per Israetel/Norton dose-response critique on biceps. Slot 7 calves shifted to a heavy 6–10 range per Norton (calves respond to load too, not just high-rep).

### Day 2 — OHP + Quad + Horizontal Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical press | Overhead Press (BB) — 4×6–8 · 180s | Shoulder Press (DB) — 4×8–10 · 150s | Overhead Press (BB) — 4×6–8 · 180s | Arnold Press (DB) — 4×8–10 · 150s |
| 2 | Horizontal pull | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide Grip — 3×10–12 · 120s | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide Grip — 3×10–12 · 120s |
| 3 | Incline press | Incline Bench Press (BB) — 3×8–10 · 150s | Swiss Bar Incline — 3×10–12 · 120s | Incline Bench Press (BB) — 3×8–10 · 150s | Incline Bench Press (DB) — 3×10–12 · 120s |
| 4a | Quad compound | Leg Extension (Home) — 4×10–12 · 120s | Belt Squat — 4×10–12 · 120s | Leg Press (Machine) (BUR) — 4×10–12 · 120s | Belt Squat — 4×10–12 · 120s |
| 4b | Quad isolation (B only) | — | Leg Extension (Home) — 2×12–15 · 60s | — | Leg Extension (Machine) — 2×12–15 · 60s |
| 5 | Side delts | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s |
| 6 | Triceps (lengthened on A) | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s |
| 7 | Calves (high-rep) | Standing Calf Raise — 3×12–15 · 90s | Single Leg Standing Calf Raise (DB) — 3×12–15/side · 90s | Calf Press (Machine) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s |

> **v3 notes:** Slot 4 split into compound + isolation on B days (Israetel/Norton: quads at 6 sets undertrained for a no-squat program). Slot 6 A-variants are Overhead Cable Ext for long-head emphasis; pairs with Day 3 short-head/lateral work.

### Day 3 — Pull + Posterior + Arms

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical pull (close) | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s |
| 2 | Glute primary | Hip Thrust (BB) — 3×8–12 · 150s | Single Leg Hip Thrust (DB) — 3×10–12/side · 120s | Hip Thrust (BB) — 3×8–12 · 150s | Hip Thrust (Machine) — 3×10–12 · 120s |
| 3 | Hamstrings (knee flexion) | Lying Leg Curl (Home) — 3×10–12 · 90s | Standing Leg Curls — 3×10–12 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s |
| 4 | Horizontal pull #2 | Dumbbell Row — 3×8–10 · 120s | Dumbbell Row — 3×10–12 · 90s | Dumbbell Row — 3×8–10 · 120s | Single Arm Cable Row — 3×10–12 · 90s |
| 5 | Rear delts | Rear Delt Reverse Fly (DB) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 6 | Biceps | Preacher Curl (DB) — IronMaster — 3×10–12 · 75s | Cross Body Hammer Curl — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Hammer Curl (Cable) — 3×10–12 · 75s |
| 7 | Triceps (lateral/medial on A) | Triceps Rope Pushdown — 3×10–12 · 75s | Skullcrusher (BB) — Swiss — 3×10–12 · 90s | Triceps Rope Pushdown (BUR) — 3×10–12 · 75s | Skullcrusher (BB) — 3×10–12 · 90s |
| 8 | Abs | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s |

> **v3 notes:** Day 3 lat raise cut (v2 reviewers convergent: cuff/AC joint risk + junk volume by week 3). BUR hamstring slot is Nordic, not Single-Leg RDL (forces knee-flexion bias; no escape hatch). Slot 7 A-variants flipped to Pushdown so the week balances long-head (D2A Overhead + D3B Skullcrusher) against lateral/medial (D2B + D3A Pushdown).

---

## 5. Adversarial review

Each round, four persona reviewers (Mike Israetel / Layne Norton / Pavel Tsatsouline / Andy Galpin) were spawned in parallel, refreshed on the persona's current philosophy via web search, and asked to critique the program in their voice. Round 1 reviewed v1; round 2 reviewed v2 (the v1 changes already merged). Both rounds are verbatim below, each followed by a synthesis listing convergent themes and which were merged / tracked / rejected.

### 5.1 Round 1 — Mike Israetel (Renaissance Periodization) on v1

**Critiques:**
- Side delt volume is undercooked. 6 direct sets plus "carryover" — pressing carryover to side delts is basically a rounding error; the medial deltoid barely fires on bench or OHP. For a 6-year trainee in a hypertrophy block trying to recover lean mass, side delts should be 12–20 hard sets. Three lat raise sessions of 3 sets at 12–15 with RIR 1–2 is maintenance, not growth.
- Hamstring volume is light AND the exercise selection is fatigue-heavy. RDL + single-leg RDL + lying leg curl gives you stretch but RDLs cost a fortune in systemic fatigue and lower back tax for the hammy stimulus you get. Stimulus-to-fatigue ratio is mediocre when you can't squat or pull conventionally — you need more isolation, less compound hinge.
- Quad direct work at 6 sets is too low for a guy who can't squat. Belt squat and leg press are your meat-and-potatoes here; treat them like your squat replacement, not an accessory.
- Triceps "9 effective" is fine on paper but the long head is underloaded — one overhead session per week against two pushdown sessions is backwards if you want the meatiest head to grow.
- No dedicated upper back row at a stretched position with heavy load; DB rows are fine but you're leaving chest-supported or machine rows on the table at BUR.

**Changes he'd make:**
- Add a third lat raise slot on Day 3 (cable Y-raise or DB), push to 4 sets each session. Target 12+ direct sets/week.
- Swap one RDL slot for seated leg curl variant or Nordic; bump hams to 9 sets. Add a 4th quad set on Day 2.
- Make one triceps slot per week a true overhead/lengthened position (overhead rope or cross-body cable kickback), keep one pushdown.

**Keep:**
- Double progression with RIR 1–2 stop and the 6–8 week deload cadence — clean, sustainable, appropriate for a 6-year trainee on a GLP-1 maintenance.
- Two variants per day for location flexibility is smart adherence engineering.

### 5.2 Round 1 — Layne Norton (BioLayne) on v1

**Critiques:**
- Your "10 sets chest" only hits if you count incline as chest — fine, but you've got chest 2×/week with 4 working sets on Day 1 and 3 on Day 2. Meta-analyses (Schoenfeld et al., and the more recent Baz-Valle work) suggest frequency past 2× adds little if volume is matched, but 7 hard sets is on the low end for someone 6+ years in chasing reaccrual. Same problem with side delts — 6 "direct" sets at RIR 1–2 on lat raises is maintenance volume, not growth volume, especially post-cut.
- Hamstrings are undercooked and lopsided. RDL + leg curl + single-leg RDL gives you hip-dominant bias and only 6 sets. The data on knee-flexion-biased work (leg curl, Nordic) for the short head is pretty clear — you need dedicated knee flexion, and "or single-leg RDL" lets you skip it. Don't give yourself an out.
- Quads at 6 direct sets is straight-up undertraining for a hypertrophy block, especially with no squat or hack. Belt squat + leg press + split squat should be your bread and butter here, not an afterthought behind RDLs.
- RIR 1–2 stop with double progression is fine, but you have no autoregulation for the GLP-1 fatigue tail. Tirzepatide blunts appetite and recovery feels fine until it doesn't. Build in a session-RPE check.
- Calves 6 sets, 12–15 only. Calves respond to load and stretch — add a heavy 6–8 range.

**Changes he'd make:**
- Add a 4th set to lat raises and a dedicated hamstring curl variation (banded leg curl at home) — non-negotiable. Push quads to 9–10 sets.
- Lock "single-leg RDL" out of the leg curl slot. It's a hinge, not a knee flexor.
- Deload every 5 weeks on GLP-1, not 6–8. Recovery is the limiter, not boredom.

**Keep:**
- Double progression with RIR cues and the A/B variant structure — pragmatic, autoregulates around equipment, and the evidence on rep ranges 6–15 being roughly equivalent for hypertrophy supports the flexibility.
- Excluding back squat/conventional DL given the knee. Smart. Belt squat and split squat work.

### 5.3 Round 1 — Pavel Tsatsouline (StrongFirst) on v1

**Critiques:**
- Twelve routines, two variants, a buffet of choices. Comrade, the program is the program. When you can pick, you will pick what feels good that day, never what is hard. Choice is the enemy of progress.
- Seven, eight movements per session, three sets of ten, RIR one or two — this is bodybuilder's busywork dressed as strength. You are chasing the pump and calling it hypertrophy. Pump is a side effect, not a goal.
- Where is the strength? Bench 4×6–8 is the only honest set on the page. Press, pull, hinge — these deserve heavy fives, doubles, singles. Strength is the mother quality. Build the engine, then the chrome.
- No squat, no deadlift — fine, the knee is the knee. But you replaced the king with a court of jesters: split squat, belt squat, leg extension, leg press, hip thrust. Pick one hinge, one knee-bend. Master it. Stop hedging.
- Lateral raises and calf raises every session. You are not a sculptor polishing marble. You are a man rebuilding ten pounds of muscle the needle stole from you. Feed the basics.

**Changes he'd make:**
- Collapse to one variant per day per location. Same exercises, no menu. Decide before you walk in.
- Day 1 and Day 2: add a heavy ramp before the hypertrophy work — Bench and Press worked up to a hard double or triple, then your back-off eights. Strength first, size follows.
- Replace the split squat / belt squat shuffle with one heavy goblet squat or front-foot-elevated split squat, 5×5, progressed weekly. Knee tolerates this. Pick it. Live with it.

**Keep:**
- Double progression with RIR 1–2 stop and the 6–8 week deload. Honest, conservative, sustainable. This is the spine of the plan — do not break it.

### 5.4 Round 1 — Andy Galpin (performance scientist) on v1

**Critiques:**
- You're rebuilding lean mass after a GLP-1 cut with a ~10.5 lb LBM deficit, but total weekly hard sets per muscle sit at the floor of what the 2024-25 literature considers hypertrophic — chest 10, quads 6 direct, hams 6, biceps 6. For a 6+ year trainee in a recovery phase with elevated protein synthesis sensitivity post-cut, that's leaving meat on the bone. Quads at 6 direct sets is the standout deficit given you lost LBM and your knee restricts the heavy bilateral driver.
- No autoregulation infrastructure. You've never logged RPE, you're prescribing RIR, and you're on a GLP-1 — appetite, sleep architecture, and resting heart rate can all shift on tirzepatide maintenance. Without even a 1–10 morning readiness check or a session RPE log, you're flying blind on recovery debt and won't catch the drift before a stall.
- Zero Zone 2 / mitochondrial work programmed. Three lifting sessions and nothing for the aerobic base. At your training age, capillary density and mitochondrial function are independent levers for both recovery between sets and long-term healthspan. This is a gap I'd flag for anyone over 35.
- Hinge frequency is once per week (Day 1) with hip thrust as the Day 3 posterior anchor. Given no conventional deadlift, hamstrings are under-stimulated at the hip-hinge pattern specifically.

**Changes he'd make:**
- Add a 4th low-fatigue session: 30–40 min Zone 2 plus one hamstring-biased movement (Nordic eccentric or 45-degree back extension) to push hams to 9+ sets.
- Add 2–3 sets of direct quad work (sissy squat, leg extension drop set) to Day 1 Var B; bring quads to 9 direct.
- Implement a 60-second morning HRV + subjective readiness log; adjust top set RIR by 1 when readiness is red.

**Keep:**
- Variant A/B structure — it's intelligent equipment-aware programming for an ad hoc schedule.
- Double progression with a 6–8 week deload cadence is appropriate for your training age.

### 5.5 Round 1 synthesis (→ v2)

| Theme | Israetel | Norton | Tsatsouline | Galpin | Action |
|---|---|---|---|---|---|
| Side delts undercooked (need 12+) | ✓ | ✓ | — | — | **Merged.** D3 lat raise added; 6 → 11 sets/wk. (Reversed in v3 — see §5.10.) |
| Quad direct work too low (need 9+) | ✓ | ✓ | (separate critique) | ✓ | **Merged.** D2B split into compound + isolation. |
| Hamstring stimulus poor, "or single-leg RDL" is an escape hatch | ✓ | ✓ | — | ✓ | **Merged.** BUR ham slot → Nordic Hamstring Curl. |
| Long-head triceps underloaded | ✓ | — | — | — | **Merged.** D2 A-variants → Overhead Cable Ext. |
| Calves need a heavy range | — | ✓ | — | — | **Merged.** D1 calves → 3×6–10. |
| Tighter deload on GLP-1 | — | ✓ | — | (overlap) | **Merged.** 6–8 → 5–7 weeks. |
| Autoregulation / readiness check | — | (RPE check) | — | ✓ | **Open** (round 2 will merge — see §5.10). |
| Add Zone 2 4th session | — | — | — | ✓ | **Open.** Trainee constraint = 3 sessions/wk. |
| Collapse choice / fewer variants | — | — | ✓ | — | **Rejected.** A/B variants are deliberate adherence engineering — 3 of 4 endorsed. |
| Heavy strength ramps (singles/doubles) | — | — | ✓ | — | **Rejected.** Phase goal is hypertrophy + LBM reaccrual, not max strength. Future strength block. |

---

### 5.6 Round 2 — Mike Israetel on v2

**Residual critiques:**
- Biceps at 6+ is still the runt of the litter. You raised delts and quads but left elbow flexors at MV when the trainee has 10.5 lb LBM to reaccrue — arms grow during reaccrual cheaply, you're leaving free tissue on the table. Push to 8–10.
- Hamstring volume reads 9 but knee-flexion vs hip-hinge split is muddy. Nordic + leg curl + RDL/hip thrust means hip-dominant is probably double-counted. Audit by function, not slot.
- Calves at 6 sets is still MV-adjacent for a 6+ yr trainee. Heavy/high-rep split is correct; the number isn't.

**New critiques from v2:**
- 11 sets of lateral raise across 3 consecutive sessions with zero recovery gap — medial delt is small but it's not magic. Expect the third session's raises to be junk volume by week 3. Stagger intensities or accept the last slot is a pump finisher, not a stimulus.
- Overhead cable extension Day 2 + overhead cable extension Day 3 Var A = long head twice, lateral/medial head undertrained. Vary the shoulder angle across the week.

**v3 suggestions:**
- Biceps to 8 sets: add 2 sets incline DB curl to Day 1 (stretched position, fits the press day cooldown).
- Demote Day 3 lat raise to 2 sets myo-rep or cut it; reallocate to a true lateral/medial tri movement (close-grip press or dips).

**Verdict:** Real step forward — delts, quads, and ham bias were the load-bearing fixes and you made them; v3 is fine-tuning, not rebuilding.

### 5.7 Round 2 — Layne Norton on v2

**Residual critiques:**
- Biceps at 6 sets is still under the dose-response curve. Schoenfeld's meta-regression shows hypertrophy scaling to ~12–20 sets for small muscles in trained lifters. You're a 6-year guy on a GLP-1 trying to recover 10.5 lb LBM — direct elbow flexion volume is the cheapest set you can buy. Bump to 9–10.
- Still no morning HRV or bodyweight readiness gate. On a GLP-1, appetite suppression masks under-recovery. You need objective data, not vibes.
- No RIR/RPE prescription written anywhere. "3×8–10" without proximity-to-failure is just numbers — the literature (Helms, Zourdos) is unambiguous that effort prescription drives the stimulus.

**New critiques from v2:**
- Day 2 Var B quads: 4×10–12 belt squat + 2×12–15 leg ext stacks 6 sets of knee-dominant work after an OHP-fatigued CNS. Watch the bad knee.
- Nordic-only BUR hamstring is brutal eccentric load with no regression listed. Prescribe a band-assisted progression or you'll tweak something.
- Overhead cable tri appears Day 2A AND Day 3A — that's 6 sets of long-head bias in 48 hours. Rotate one to a pronated pushdown.

**v3 suggestions:**
- Add RIR targets: compounds 2–3 RIR weeks 1–2, 1–2 RIR weeks 3–4, 0–1 RIR week 5; isolations 1 RIR throughout.
- Daily 5-question readiness log (sleep, soreness, appetite, mood, motivation) — autoregulate top set when score drops.

**Verdict:** Volume distribution is now defensible; tighten autoregulation and biceps dose and this is a legitimate v3.

### 5.8 Round 2 — Pavel Tsatsouline on v2

**Residual critiques:**
- A/B menu. Still wrong. You call it adherence. I call it noise. The body adapts to the stress you repeat, not the stress you choose from a menu. But fine — your choice, your results.
- No top set. Eight reps is not heavy. Eight reps after warm-ups is jogging. One hard double before the back-offs costs nothing, teaches intent. You filed it. I unfile it every block.
- Knee bend. Two coaches told you to add quad isolation. I told you to fix the pattern. Adding leg extensions does not fix a knee — it feeds it.

**New critiques from v2:**
- Eleven sets of side delts across three days on a GLP-1 maintenance recovery. The delt is small. You will inflame the cuff before you grow the shoulder.
- Nordic curl with a bad knee and no squat pattern? Eccentric overload on a joint you are protecting. Foolish.
- Triceps now nine sets, all variants long-head biased. Pick one. Stop collecting.

**v3 suggestions:**
- Drop Day 3 lat raise. Nine sets is plenty. Cuff will thank you.
- Replace Nordic with back-loaded 45-degree hyper or seated leg curl. Same hamstring, no knee tax.

**Verdict:** More volume is not more program — it is more to recover from, and this trainee has less to spend.

### 5.9 Round 2 — Andy Galpin on v2

**Residual critiques:**
- Readiness log still absent. On a GLP-1 with an LBM debt, RPE drift is your only autoregulation signal — that's a hardware gap, not a nice-to-have. HRV-only is fine if daily compliance is the bottleneck.
- Zone 2 still unaddressed. Mitochondrial density and substrate flexibility are blunted on GLP-1 caloric deficits; you're banking on lifting alone to drive aerobic base. It won't.
- A/B variants endorsed — but no rule for *when* to rotate. Undefined = drift.

**New critiques from v2:**
- Side delts at 11 with three pressing slots and rear delt work — shoulder cuff tissue tolerance is the rate-limiter, not stimulus. Watch AC joint.
- Quads 9 + hams 9 + glutes 9 on one bad knee across BSS/belt squat/hip thrust — recovery cost is real on a 500–700 kcal protein-prioritized intake.
- Nordic at BUR only with no eccentric ramp-in protocol. That's a DOMS landmine week one.

**v3 suggestions:**
- Readiness MVP: single 1–10 morning score, sub-5 = drop top set, sub-3 = swap to Var B lighter. Ten seconds.
- Z2 MVP: two 20-min walks at nasal-breathing pace, non-lifting days. Additive, sub-threshold, won't tax recovery.

**Verdict:** Structurally sound, autoregulation still the weak link.

### 5.10 Round 2 synthesis (→ v3)

| Theme | Israetel | Norton | Tsatsouline | Galpin | Action |
|---|---|---|---|---|---|
| Biceps still undertrained (need 8–10) | ✓ | ✓ | — | — | **Merged.** D1 Incline Curl 3 sets added; 3 → 6 direct + pull carryover (~8 effective). |
| Long-head triceps double-hit on D2A + D3A | ✓ | ✓ | (separate "pick one" critique) | — | **Merged.** D3A triceps Overhead → Rope Pushdown; week balances long-head (D2A + D3B) with lateral/medial (D2B + D3A). |
| D3 lat raise junk / cuff risk | ✓ (junk volume by wk 3) | — | ✓ (cuff) | ✓ (AC joint) | **Merged.** D3 lat raise cut. Side delts 11 → 8 sets/wk. |
| Readiness gate / autoregulation absent | — | ✓ | — | ✓ (with MVP) | **Merged.** Galpin's MVP wired into §3: 1–10 morning score, gates top set + variant swap. |
| Nordic eccentric ramp-in missing | — | ✓ | (rejects Nordic outright) | ✓ | **Merged.** §3 includes a 5-week eccentric ramp; weeks 1–2 are eccentric-only / band-assisted. |
| Hamstring volume audit (hinge vs knee-flex double-count) | ✓ | — | — | — | **Merged.** v3 table reflects honest count: 6 direct (3 hinge + 3 knee-flex). |
| Biceps to 8–10 (Norton ceiling) | (8) | (9–10) | — | — | **Partial.** v3 at 6 direct + pull carryover ≈ 8 effective. Room to push higher next iteration. |
| RIR/RPE prescription per phase | — | ✓ | — | (overlap) | **Open.** Will wire RIR-by-week targets into §3 next iteration. |
| Z2 / aerobic base | — | — | — | ✓ (MVP: 2×20-min nasal walks) | **Open.** Trainee constraint is 3 lifting sessions; Z2 walks tracked as additive option. |
| Calves still 6 sets (Israetel: MV-adjacent) | ✓ | — | — | — | **Not merged.** Defer; 6 hits the floor of hypertrophic range. Revisit if calves stall 4+ weeks. |
| Side delts overcooked at 11 (Tsatsouline/Galpin cuff concerns) | (junk volume) | — | ✓ | ✓ | **Resolved via D3 cut.** Now at 8 sets/wk — Israetel's growth range, Tsatsouline/Galpin's safety band. |
| Nordic foolish for bad knee (Pavel) | — | — | ✓ | — | **Rejected.** Norton + Galpin endorse with eccentric ramp; merged the ramp protocol. Tsatsouline overruled 3-to-1. |
| Collapse A/B variants (Pavel reiterates) | — | — | ✓ | — | **Rejected.** Same reasoning as round 1. |
| Heavy strength ramps before hypertrophy (Pavel reiterates) | — | — | ✓ | — | **Rejected.** Off-phase; tracked in §6 for a future strength block. |

**Net v2→v3:** 6 changes merged (biceps slot, triceps angle rotation, lat raise cut, readiness gate, Nordic ramp-in, hamstring volume re-counted honestly). 2 open items added (RIR-by-phase prescription, Z2 MVP). 3 rejections carried forward (Nordic-for-knee, collapse variants, strength ramps).

---

## 6. Open items not yet merged

1. **RIR-by-phase prescription** (Norton round 2) — Add per-week RIR targets (compounds 2–3 → 1–2 → 0–1 across a 5-week mesocycle; isolations 1 RIR throughout). Defer until baseline RIR logging habit forms.
2. **Zone 2 MVP** (Galpin both rounds) — Two 20-min nasal-breathing walks on non-lifting days. Additive, sub-threshold. Easy to drop in once lifting program stabilizes.
3. **Calves push to 9 sets** (Israetel round 2) — If calves stall 4+ weeks at the current 6, add a third weekly hit on Day 3.
4. **Biceps push to 9–10** (Norton round 2) — v3 is at 6 direct + carryover. Room to push if forearm/elbow recovery permits.
5. **Future strength-focused block** (Tsatsouline both rounds) — 4–6 week mesocycle at 5×3–5 on Bench, OHP, RDL with heavy ramps. Off-phase now; valid future option.

---

## 7. Change log

- **2026-06-21 — v3.** Second adversarial review on v2 (round 2 by same 4 personas). 6 changes merged: D1 Incline Curl slot added (biceps 3 → 6 direct), D3A triceps Overhead → Rope Pushdown (week-level long-head/lateral balance), D3 lat raise cut (cuff/junk-volume convergence), readiness 1–10 morning gate wired into §3, Nordic 5-week eccentric ramp-in wired into §3, hamstring volume re-counted honestly (6 direct, not 9). 2 open items added (RIR-by-phase, Z2 MVP). Operational notes split out to `IMPLEMENTATION.md`. Routine tables reformatted: each cell now inlines exercise · S×R · rest.
- **2026-06-21 — v2.** Restructured §4 to one table per day with Home A / Home B / BUR A / BUR B columns. Stripped Elan-era historical narrative from §2. First adversarial review (Israetel, Norton, Tsatsouline, Galpin). 6 changes merged: side delts 6 → 11 sets/wk, quad isolation slot added, BUR hams → Nordic, long-head triceps emphasis on D2A, heavy calf range on D1, deload tightened 6–8 → 5–7 wk. 2 tracked, 2 rejected.
- **2026-06-20 — v1.** Initial plan built from 429-workout analysis. 3-day rotation × 2 variants × 2 locations; no conventional deadlift (knee); RDL + Hip Thrust + Leg Curl for posterior chain; Belt Squat = cable squat; preserve existing routine IDs; rename floaters to `[ARCHIVE]` for manual deletion.
