# Hevy Training Plan

The current training program. Operational notes (Hevy account IDs, API, MCP) in [IMPLEMENTATION.md](./IMPLEMENTATION.md).

---

## 1. Context

**Trainee.** Adult male, 6+ yr training. Just finished ~20 lb fat-loss phase on tirzepatide; now on maintenance dose. DEXA shows ~10.5 lb lean mass to recover. Goal: hypertrophy + LBM reaccrual.

**Constraints.** Bad knee — no BB back squat, no conventional BB deadlift. RPE not logged historically; program uses RIR cues.

**Frequency.** 3 sessions / week. Home or BUR (work gym) decided ad hoc per day.

**Equipment.**
- **Home (garage):** Rogue rack with pull-up bar, BB + Swiss bar, adjustable DBs 5–75 lb, IronMaster Super Bench + preacher attachment + cable tower + leg ext / leg curl attachments. Cable handles: V, rope, rotating, single-arm.
- **BUR (Burlingame office gym):** Power rack + BB + plates, cable stack / functional trainer, incline leg press, full DB rack past 75 lb. No hamstring curl machine.

---

## 2. Weekly hard sets per muscle

Primary + 0.5×secondary. Carryover noted where it materially adds.

| Muscle | Sets/wk | Source |
|---|---|---|
| Chest | 10 | Bench D1 (4) + Incline D2 (3) + Fly carryover from press work |
| Lats | 9 | Pulldown wide D1 + Pulldown close D3 + DB Row D3 |
| Upper back | 9 | Seated Row D2 + DB Row D3 + Rear Delt Fly D3 |
| Side delts | 8 | Lat Raise D1 (4) + D2 (4) |
| Rear delts | 4 | Rear Delt Fly / Face Pull D3 |
| Quads | 9 | Belt Squat / Leg Ext / Leg Press / BSS — split across D1 + D2 |
| Hamstrings | 6 direct | RDL D1 (3 hinge) + Lying Curl / Standing Curl / Nordic D3 (3 knee-flex) |
| Glutes | 9 | RDL + Hip Thrust + BSS |
| Biceps | 6 direct | Incline / Hammer Curl D1 (3) + Preacher / Cable D3 (3) + pull carryover |
| Triceps | 9 effective | Overhead D2A + Pushdown D2B + Pushdown D3A + Skullcrusher D3B + press carryover |
| Calves | 6 | Heavy 6–10 D1 (3) + High-rep 12–15 D2 (3) |
| Abs | 6 | Knee Raise D1 (3) + Cable Crunch / Hanging Leg Raise D3 (3) |

---

## 3. Program design

### Architecture
**3 days × 2 variants × 2 locations = 12 routines.** Train 3×/wk, one variant of each day per week. Home or BUR decided ad hoc.

- **Day 1** — Press + Hinge + Vertical Pull
- **Day 2** — OHP + Quad + Horizontal Pull
- **Day 3** — Pull + Posterior + Arms

Variant A: heavier compound baseline (lower reps, longer rest). Variant B: variety with Swiss bar / DBs / cables (moderate reps, shorter rest).

### Double progression
1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Add 1 rep per set when possible each session.
3. When all sets hit the **top**: next session **add 2.5 kg** (BB) / **5 lb** (DB), reset to bottom.
4. Stop at **RIR 1–2**. Don't grind to failure on compounds.

### Readiness gate
Morning, 10 seconds, before deciding the session — composite 1–10 score across sleep, soreness, appetite, mood, motivation.

- **≥ 5** → train as written.
- **3–4** → drop the top set on every compound. Keep weights.
- **< 3** → swap to Variant B if A was planned, or skip and walk.

### Nordic Hamstring Curl ramp-in
Five-week build-up. Don't skip; eccentric load is brutal.

- **Wk 1–2:** 2 sets × 3–5 reps, eccentric-only, 4-second descent. Drive concentric with hands on floor, or band wrapped around shoulders + rack.
- **Wk 3–4:** 2 sets × 5–8 reps, band-assisted full reps.
- **Wk 5+:** 3 sets × 5–8 reps, unassisted.

### Deload
Every 5–7 weeks, or when 2+ exercises stall for 2 consecutive sessions: one light week. Top-set weight × 0.6. 2 sets instead of 3. Same rep target. Smooth bar speed.

---

## 4. The 12 routines

Each cell: exercise — sets×reps · rest. Hevy template IDs in [IMPLEMENTATION.md §2](./IMPLEMENTATION.md#2-exercise-template-id-lookup).

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

### Day 2 — OHP + Quad + Horizontal Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical press | Overhead Press (BB) — 4×6–8 · 180s | Shoulder Press (DB) — 4×8–10 · 150s | Overhead Press (BB) — 4×6–8 · 180s | Arnold Press (DB) — 4×8–10 · 150s |
| 2 | Horizontal pull | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s |
| 3 | Incline press | Incline Bench Press (BB) — 3×8–10 · 150s | Swiss Bar Incline — 3×10–12 · 120s | Incline Bench Press (BB) — 3×8–10 · 150s | Incline Bench Press (DB) — 3×10–12 · 120s |
| 4a | Quad compound | Leg Extension (Home) — 4×10–12 · 120s | Belt Squat — 4×10–12 · 120s | Leg Press (Machine) (BUR) — 4×10–12 · 120s | Belt Squat — 4×10–12 · 120s |
| 4b | Quad isolation (B only) | — | Leg Extension (Home) — 2×12–15 · 60s | — | Leg Extension (Machine) — 2×12–15 · 60s |
| 5 | Side delts | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s |
| 6 | Triceps (lengthened on A) | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s |
| 7 | Calves (high-rep) | Standing Calf Raise — 3×12–15 · 90s | Single Leg Standing Calf Raise (DB) — 3×12–15/side · 90s | Calf Press (Machine) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s |

### Day 3 — Pull + Posterior + Arms

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical pull (close) | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s |
| 2 | Glute primary | Hip Thrust (BB) — 3×8–12 · 150s | Single Leg Hip Thrust (DB) — 3×10–12/side · 120s | Hip Thrust (BB) — 3×8–12 · 150s | Hip Thrust (Machine) — 3×10–12 · 120s |
| 3 | Hamstrings (knee flexion) | Lying Leg Curl (Home) — 3×10–12 · 90s | Standing Leg Curls — 3×10–12 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s |
| 4 | Horizontal pull #2 | Dumbbell Row — 3×8–10 · 120s | Dumbbell Row — 3×10–12 · 90s | Dumbbell Row — 3×8–10 · 120s | Single Arm Cable Row — 3×10–12 · 90s |
| 5 | Rear delts | Rear Delt Reverse Fly (DB) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 6 | Biceps | Preacher Curl (DB) — 3×10–12 · 75s | Cross Body Hammer Curl — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Hammer Curl (Cable) — 3×10–12 · 75s |
| 7 | Triceps (lateral/medial on A) | Triceps Rope Pushdown — 3×10–12 · 75s | Skullcrusher (BB) — Swiss — 3×10–12 · 90s | Triceps Rope Pushdown (BUR) — 3×10–12 · 75s | Skullcrusher (BB) — 3×10–12 · 90s |
| 8 | Abs | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s |

---

## 5. Critique

Four persona reviewers (Mike Israetel, Layne Norton, Pavel Tsatsouline, Andy Galpin) were spawned in parallel to critique the program. Each refreshed on the persona's current published philosophy before delivering feedback in their voice. Verbatim below.

### Mike Israetel (Renaissance Periodization)

**Critiques:**
- Side delt volume is undercooked for a 6+ year trainee in a recovery phase. 8 sets across two pressing days will not drive hypertrophy in someone with that much training age. Cable lateral work beats DBs at the stretched position anyway, and you have stacks at both locations.
- Hamstring volume is the weakest link. 3 hinge sets plus 3 knee-flexion sets is maintenance, not growth. RDLs are hip-dominant; you need more knee-flexion work, especially since LBM recovery is the goal. The 5-week Nordic ramp is too slow and Nordics alone are a brutal stimulus-to-fatigue ratio for a knee-compromised lifter.
- Direct biceps at 6 sets is light for a guy trying to reclaim 10.5 lb of LBM. Arms regrow fast on the way back up. Exploit it.
- Calves at 6 sets, half of which are "heavy 6–10," is suboptimal. Calves want frequency and stretch-biased reps in the 8–20 range, not low-rep heavy work.
- Readiness gate is fine but the deload trigger at 5–7 weeks is too rigid on a GLP-1; recovery is impaired, fatigue accumulates faster than you think.

**Changes:**
- Add 3–4 sets cable laterals to Day 3, push side delts to 12.
- Swap Day 1 BSS/split squat for a second knee-flexion exercise (seated or lying curl); bring hams to 9 direct.
- Add a second biceps movement on Day 2; arms to 9–10.

**Verdict:** Defensible skeleton, undervolumed in the exact muscles you need to regrow.

### Layne Norton (BioLayne)

**Critiques:**
- Side delt volume is fine but you're doing the same lat raise 4 sessions/wk with zero variation in angle or implement. Lateral raises respond to lengthened-position bias (Ottinger et al. 2023 EMG, plus Maeo's recent lengthened-vs-shortened work) — at least one slot should be a cable lateral with the working arm behind the torso or a leaning DB raise.
- Hamstring volume is undercooked given the no-conventional-DL constraint. 3 hinge + 3 knee-flex sets is maintenance, not recovery. Schoenfeld/Grgic dose-response data point to 10+ direct sets/wk for hypertrophy in trained lifters. You're literally rebuilding LBM — push it.
- Nordic ramp is reasonable but eccentric-only Nordics are brutally fatiguing and you've buried them on Day 3 after hip thrusts. Order matters for a knee-compromised lifter; one ugly rep and you're out for a week.
- "Readiness gate" with a 1–10 subjective score has weak validity (Saw et al. 2016 meta — subjective measures track training load, but the cutoffs you've drawn are arbitrary). Fine as a heuristic, don't pretend it's auto-regulation.
- Direct biceps at 6 sets is low for someone trying to recomp on a GLP-1 with blunted appetite/anabolic drive.

**Changes:**
- Swap one DB lateral/wk for a lengthened-bias cable variant; add a 4th knee-flex set and a 4th hinge set.
- Move Nordics to the top of Day 3 before hip thrust.
- Bump direct biceps to 9 sets; rotate supinated/neutral/pronated.

**Verdict:** Defensible skeleton, but underdosed where it matters most for a lean-mass rebuild.

### Pavel Tsatsouline (StrongFirst)

**Critiques:**
- Too many tools, not enough mastery. Twelve routines for three sessions a week is variety worship. The body adapts to the stimulus you repeat, not the stimulus you rotate. Pick the lift, own the lift.
- RIR 1–2 on every set is a tax you pay in nervous system currency. On GLP-1, appetite suppressed, recovery already taxed — proximity to failure must be earned, not defaulted.
- Side delts at 8 weekly sets while biceps get 6 direct is cosmetic accounting. The lat pulldown is not a bicep builder for a six-year trainee — he is strong enough that the back takes the work. Pay the arms directly or accept the deficit.
- The "morning 1–10 gate" is autoregulation theater. A man with six years under the bar reads the first warm-up set honestly. Trust the bar, not the questionnaire.
- Hip thrust 3×8–12 and RDL 3×8–10 is thin posterior chain insurance when the conventional deadlift is off the table. The hamstring is the bridge between the knee you cannot load and the hip you can.

**Changes:**
- Anchor each session with one lift held for 6–8 weeks. Progress the load, not the menu.
- Add a second hamstring slot on Day 1 or Day 3. Six direct sets is the floor, not the program.
- Replace one lateral raise block with weighted carries or heavy KB swings. LBM is built by tension under load, not feathered isolation.

**Verdict:** Defensible as a hypertrophy block — competent, conservative, over-engineered; it will grow him in spite of itself, not because of itself.

### Andy Galpin (performance scientist)

**Critiques:**
- Direct hamstring volume (6) is light for a knee-compromised lifter recovering LBM; with no BB squat/DL, posterior chain is your main quad-sparing driver and deserves more love.
- Bicep direct volume (6) lags triceps and back pulling work; for hypertrophy recovery in a 6+ yr trainee, 10–12 sets/wk is closer to the meta-analytic sweet spot.
- Lat raises 4×12–15 twice weekly is fine, but rear delts only hit hard on Day 3 — shoulder health and the visual delt cap want more posterior deltoid frequency.
- Readiness gate is a nice idea but a 1–10 subjective scale without HRV or grip dynamometry is noisy; you'll auto-regulate based on mood as much as recovery.
- GLP-1 context underweighted: appetite suppression plus a 10.5 lb LBM rebuild demands explicit protein targets (1.6–2.2 g/kg) and intra-session carb consideration, not just programming.

**Changes:**
- Add a second hamstring slot Day 1 (swap BSS for a Romanian/single-leg RDL variant some weeks) to push direct hams to 9–10 sets.
- Move one lat raise slot to a rear delt/face pull, and add a biceps set on Day 2 (incline or cable curl) to balance arms.
- Replace subjective readiness with a 3-metric gate: sleep hours, resting HR delta, bar speed on first warm-up set.

**Verdict:** Yes — structurally sound, constraint-aware, and defensible; it just needs minor volume rebalancing and a less hand-wavy autoregulation signal.

---

## 6. Open items to resolve

Convergent themes from §5, ranked by how broadly the panel agreed. Action when you next revise the program.

1. **Hamstrings 6 → 9–10 direct sets/wk** — all four flagged it. Add a second knee-flex slot to Day 1 (e.g. swap one BSS for a curl variant), or add a 4th set to the existing D3 ham slot.
2. **Biceps 6 → 9–10 direct sets/wk** — Israetel, Norton, Galpin. Add a 3-set bicep movement to Day 2 (incline or cable curl).
3. **Side delts — vary the angle/implement** — Norton, Israetel. Replace one DB lat raise slot with a cable lateral in lengthened position (working arm behind torso) or a leaning DB raise. Israetel also wants total volume pushed to 12 sets; Norton thinks 8 is fine if the angle varies.
4. **Move Nordic to start of Day 3** — Norton. Brutal eccentric stimulus shouldn't come after hip thrusts.
5. **Readiness gate — replace with objective signal or accept it's a heuristic** — Norton, Galpin (Tsatsouline rejects the gate entirely). Galpin's 3-metric replacement: sleep hours + resting HR delta + bar speed on first warm-up set.
6. **Calves — drop the heavy 6–10 range, shift all to 8–20 stretch-biased** — Israetel only. Lower priority unless calves stall.
7. **Rear delt frequency** — Galpin. Currently only D3. Consider trading one D2 lateral raise for a rear-delt slot.

**Not acted on, by design:**
- Tsatsouline's "collapse to one variant" / "anchor one lift 6–8 weeks" / "heavy KB swings instead of laterals" — off-phase for hypertrophy + LBM reaccrual; valid for a future strength block.
- Galpin's "explicit protein targets / intra-session carbs" — out of scope (training only).
