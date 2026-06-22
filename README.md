# Hevy Training Plan

The current training program. Operational notes (Hevy account IDs, API, MCP) in [IMPLEMENTATION.md](./IMPLEMENTATION.md).

---

## 1. Context

**Trainee.** Adult male, 6+ yr training. Just finished ~20 lb fat-loss phase on tirzepatide; now on maintenance dose. DEXA shows ~10.5 lb lean mass to recover. Goal: hypertrophy + LBM reaccrual.

**Constraints.** Bad knee — no BB back squat. Conventional BB deadlift is available at both locations but not currently used (RDL handles the hinge). RPE not logged historically; program uses RIR cues.

**Frequency.** 3 sessions / week. Home or BUR (work gym) decided ad hoc per day.

**Equipment.**
- **Home (garage):** Rogue rack with pull-up bar, BB + Swiss bar, adjustable DBs 5–75 lb, IronMaster Super Bench + preacher attachment + cable tower + leg ext / leg curl attachments. Cable handles: V, rope, rotating, single-arm.
- **BUR (Burlingame office gym):** Power rack + BB + plates, cable stack / functional trainer, incline leg press, landmine, full DB rack past 75 lb. **No hamstring curl machine. No belt squat.**

---

## 2. Weekly hard sets per muscle

Primary + 0.5×secondary.

| Muscle | Sets/wk | Source |
|---|---|---|
| Chest | 10 | Bench D1 (4) + Incline D2 (3) + carryover |
| Lats | 9 | Pulldown wide D1 + Pulldown close D3 + DB Row D3 |
| Upper back | 9 | Seated Row D2 + DB Row D3 + Rear Delt Fly D3 |
| Side delts | 8 | Lat Raise DB D1 (4) + Lat Raise Cable D2 (4, lengthened bias) |
| Rear delts | 4 | Rear Delt Fly / Face Pull D3 |
| Quads | 9 | Belt Squat / Landmine Squat / Leg Ext / Leg Press / BSS — D1 + D2 |
| Hamstrings | 9 | RDL D1 (3 hinge) + Leg Curl or SL RDL D1 (3) + Leg Curl or Nordic D3 (3) |
| Glutes | 9 | RDL + Hip Thrust + BSS |
| Biceps | 9 | Incline / Hammer Curl D1 (3 stretched) + Spider / Cable Curl D2 (3 mid) + Preacher / Cable D3 (3) |
| Triceps | 9 effective | Overhead D2A + Pushdown D2B + Pushdown D3A + Skullcrusher D3B + press carryover |
| Calves | 6 | Heavy 6–10 D1 (3) + High-rep 12–15 D2 (3) |
| Abs | 6 | Knee Raise D1 (3) + Cable Crunch / Hanging Leg Raise D3 (3) |

> At BUR, the D1 hamstring slot is Single-Leg RDL (hip-hinge bias) since BUR has no hamstring curl machine — total hams is still 9 sets but the location split is 6 hinge + 3 knee-flex (BUR) vs 3 hinge + 6 knee-flex (Home).

---

## 3. Program design

### Architecture
**3 days × 2 variants × 2 locations = 12 routines.** Train 3×/wk, one variant of each day per week. Home or BUR decided ad hoc.

- **Day 1** — Press + Hinge + Vertical Pull
- **Day 2** — OHP + Quad + Horizontal Pull
- **Day 3** — Posterior + Pull + Arms (hamstrings opened first)

Variant A: heavier compound baseline (lower reps, longer rest). Variant B: variety with Swiss bar / DBs / cables (moderate reps, shorter rest).

### Double progression
1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Add 1 rep per set when possible each session.
3. When all sets hit the **top**: next session **add 2.5 kg** (BB) / **5 lb** (DB), reset to bottom.
4. Stop at **RIR 1–2**. Don't grind to failure on compounds.

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
| 5 | Hamstrings | Lying Leg Curl (Home) — 3×10–12 · 90s | Standing Leg Curls — 3×10–12 · 90s | Single Leg RDL (DB) — 3×10–12 · 90s | Single Leg RDL (DB) — 3×10–12 · 90s |
| 6 | Side delts | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s |
| 7 | Biceps (stretched) | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s |
| 8 | Calves (heavy) | Standing Calf Raise (DB) — 3×6–10 · 90s | Single Leg Standing Calf Raise (DB) — 3×6–10/side · 90s | Calf Press (Machine) — 3×6–10 · 90s | Calf Press (Machine) — 3×6–10 · 90s |
| 9 | Abs | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s |

### Day 2 — OHP + Quad + Horizontal Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical press | Overhead Press (BB) — 4×6–8 · 180s | Shoulder Press (DB) — 4×8–10 · 150s | Overhead Press (BB) — 4×6–8 · 180s | Arnold Press (DB) — 4×8–10 · 150s |
| 2 | Horizontal pull | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s |
| 3 | Incline press | Incline Bench Press (BB) — 3×8–10 · 150s | Swiss Bar Incline — 3×10–12 · 120s | Incline Bench Press (BB) — 3×8–10 · 150s | Incline Bench Press (DB) — 3×10–12 · 120s |
| 4a | Quad compound | Leg Extension (Home) — 4×10–12 · 120s | Belt Squat — 4×10–12 · 120s | Leg Press (Machine) (BUR) — 4×10–12 · 120s | Landmine Squat — 4×10–12 · 120s |
| 4b | Quad isolation (B only) | — | Leg Extension (Home) — 2×12–15 · 60s | — | Leg Extension (Machine) — 2×12–15 · 60s |
| 5 | Side delts (lengthened) | Lateral Raise (Cable) — 4×12–15 · 75s | Lateral Raise (Cable) — 4×12–15 · 60s | Lateral Raise (Cable) — 4×12–15 · 75s | Lateral Raise (Cable) — 4×12–15 · 60s |
| 6 | Biceps (mid-range) | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s |
| 7 | Triceps (lengthened on A) | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s |
| 8 | Calves (high-rep) | Standing Calf Raise — 3×12–15 · 90s | Single Leg Standing Calf Raise (DB) — 3×12–15/side · 90s | Calf Press (Machine) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s |

### Day 3 — Posterior + Pull + Arms

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Hamstrings (priority) | Lying Leg Curl (Home) — 3×10–12 · 90s | Standing Leg Curls — 3×10–12 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s | Nordic Hamstring Curl — see ramp-in §3 · 90s |
| 2 | Glute primary | Hip Thrust (BB) — 3×8–12 · 150s | Single Leg Hip Thrust (DB) — 3×10–12/side · 120s | Hip Thrust (BB) — 3×8–12 · 150s | Hip Thrust (Machine) — 3×10–12 · 120s |
| 3 | Vertical pull (close) | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s |
| 4 | Horizontal pull #2 | Dumbbell Row — 3×8–10 · 120s | Dumbbell Row — 3×10–12 · 90s | Dumbbell Row — 3×8–10 · 120s | Single Arm Cable Row — 3×10–12 · 90s |
| 5 | Rear delts | Rear Delt Reverse Fly (DB) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 6 | Biceps | Preacher Curl (DB) — 3×10–12 · 75s | Cross Body Hammer Curl — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Hammer Curl (Cable) — 3×10–12 · 75s |
| 7 | Triceps (lateral/medial on A) | Triceps Rope Pushdown — 3×10–12 · 75s | Skullcrusher (BB) — Swiss — 3×10–12 · 90s | Triceps Rope Pushdown (BUR) — 3×10–12 · 75s | Skullcrusher (BB) — 3×10–12 · 90s |
| 8 | Abs | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s |

---

## 5. Critique

Four reviewers (Mike Israetel, Layne Norton, Pavel Tsatsouline, Andy Galpin) spawned in parallel; each refreshed on the persona's current published philosophy before delivering feedback in their voice. Verbatim below.

### Mike Israetel (Renaissance Periodization)

**Critiques:**
- Side delt volume is undercooked for an advanced lifter recovering LBM — 8 sets across two flavors is maintenance-tier when delts are notoriously volume-hungry and recover fast. You've got the frequency right but the magnitude wrong; this is the muscle that visibly sells the "I got my size back" look.
- Rear delts at 4 sets is borderline insulting after 6+ years of training. One 4-set slot on D3 isn't going to move the needle, especially with zero direct rear delt work on D1 or D2 where horizontal pulls are doing most of the heavy lifting incidentally.
- Hamstring volume is technically 9 but the knee-flexion bias is heavy (6 sets) versus 3 hinge sets. For an advanced lifter without BB squat, hinge-pattern hams should be the anchor, not the accessory — RDL/DB RDL deserves more love.

**Changes:**
- Add 2 sets of rear delts to D1 and D2 (cable reverse fly or face pull, 12–15). Push side delts to 12 weekly sets by adding a third lat raise slot.
- Bump RDL on D1A to 4×8–10; consider a second hinge slot on D3B replacing straight-arm pulldown.

**Verdict:** Yes, defensible — solid skeleton, just underdosed on delts and slightly miscalibrated on ham pattern split.

### Layne Norton (BioLayne)

**Critiques:**
- Rear delts at 4 sets is under-dosed relative to your side delts (8) and upper back (9). Meta-analytic data (Schoenfeld/Baz-Valle) puts the hypertrophy dose-response curve well above 4 weekly sets for a 6+ yr trainee in a maintenance/recomp context. They're a small muscle that recovers fast — feed them.
- No autoregulation. You're on a GLP-1, recovering ~10.5 lb LBM, training 3×/wk with no readiness check. RIR 1–2 is fine on paper, but appetite suppression plus sub-maintenance fueling history means session-to-session readiness will swing. A 1-question 1–10 readiness or velocity-loss heuristic costs nothing and protects the LBM you're trying to regain (Helms, Zourdos work on RPE/RIR fidelity).
- Calves at 6 sets is light for a stubborn, high-MHC-I muscle in a 6-yr lifter. Literature (Ottinger 2023) supports 8–12+ for advanced.

**Changes:**
- Add 2 sets rear delts on D2 (face pull or reverse pec deck); add 1 calf set per session (calves to 9).
- Insert a 1–10 readiness check; if ≤5, drop top set or shift to RIR 3.

**Verdict:** Yes, defensible. Structurally sound, fixes are dose tweaks not redesign.

### Pavel Tsatsouline (StrongFirst)

**Critiques:**
- Nine working sets for biceps and triceps next to one direct row variant for rear delts is vanity, not balance. Your posterior shoulder will be the weakest link, and weak links break first. Fix the ratio before you chase the pump.
- Side delts get cable and dumbbell raises but no overhead press variant that loads them hard outside Day 2. One pressing slot owning the deltoid for the week is thin. Hypertrophy still answers to load on the biggest movement, not just to volume on the smallest.
- Nordic ramp on Day 3 with hamstrings already worked Day 1 via RDL is generous. Eccentrics tax the tissue for days. Watch the overlap or you will blunt both.

**Changes:**
- Cut two sets from biceps. Add two sets of face pulls or reverse fly. Earn the symmetry.
- Day 2: add a hard set or two of high-incline or seated DB press above the lateral raises. Press first, isolate after.

**Verdict:** Solid bones, lazy shoulders, vain arms. Tighten it, and it will grow you back.

### Andy Galpin (performance scientist)

**Critiques:**
- Side delt volume looks like 8 hard sets, but you're double-counting overlap from pressing. Real direct mid-delt stimulus is fine; the bigger issue is rear delts at 4 sets — under-dosed for someone with 6+ years training and a presumed forward-loaded upper-body history. Asymmetry risk, posture cost.
- Hamstring "9 sets" conflates hinge and knee-flexion as if interchangeable. They aren't — biarticular function means you want both, but counting them into one bucket masks that knee-flexion is concentrated D1+D3 with a 72-hr gap and hinge sits alone on D1. For LBM recovery on a GLP-1 (blunted appetite, lower protein turnover headroom), I'd want cleaner separation and frequency.
- Dropping the readiness check on Tsatsouline's authority is a rhetorical move, not a physiological one. On a GLP-1 in a recovery phase, HRV/sleep/sRPE gating is cheap insurance against junk volume.

**Changes:**
- Add 2 sets rear delt to Day 2 (face pull or reverse pec deck analog); pull 1 set from side delts if fatigue budget tight.
- Reinstate a 30-second morning check (sleep, soreness, motivation 1–5); auto-cut top set or drop a back-off if two of three flag.

**Verdict:** Defensible — structure, progression, and exercise selection fit the constraints; the volume distribution and removed autoregulation are the soft spots, not deal-breakers.

---

## 6. Open items to resolve

1. **Rear delts 4 → 6–7 sets** — all four reviewers converged. Highest priority. Add a 2–3 set face pull / reverse fly slot to Day 2 (between Lat Raise and Spider Curl).
2. **Calves 6 → 9 sets** — Norton (persistent across rounds). Add a third weekly hit, e.g. on Day 3.
3. **Side delts 8 → 12 sets** — Israetel only; Galpin satisfied at 8. Push if delts plateau.
4. **Readiness check** — Norton and Galpin re-pitched it (1-question 1–10, or 3-metric sleep/soreness/motivation). Removed in this revision per the no-theater argument; reconsider if recovery markers drift.
5. **Hinge/knee-flex hamstring split** — Israetel and Galpin both want cleaner separation. At BUR especially, the D1 ham slot is Single-Leg RDL (hinge) since there's no curl machine. Options: cable hamstring curl with ankle strap, stability ball curl, or add a second Home-only D1 ham curl set.
6. **Deadlift option** — available at both locations, not currently programmed. Consider swapping D1A RDL for conventional or trap-bar deadlift if a heavier hinge stimulus is wanted.

**Not acted on, by design:**
- Tsatsouline: collapse variants / heavy strength singles / cut bicep volume — off-phase for hypertrophy + LBM reaccrual.
- Galpin: explicit protein targets / intra-session carbs — out of scope (training only).
