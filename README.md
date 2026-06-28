# Hevy Training Plan

The current training program. Operational notes (Hevy account IDs, API, MCP) in [IMPLEMENTATION.md](./IMPLEMENTATION.md).

---

## 1. Context

**Trainee.** Adult male, 6+ yr training. Just finished ~20 lb fat-loss phase on tirzepatide; now on maintenance dose. DEXA shows ~10.5 lb lean mass to recover. Goal: hypertrophy + LBM reaccrual.

**Constraints.** Bad knee — no BB back squat. RPE not logged historically; program uses RIR cues.

**Frequency.** 3 sessions / week. Home or BUR (work gym) decided ad hoc per day.

**Equipment.**
- **Home (garage):** Rogue rack with pull-up bar, BB + Swiss bar, adjustable DBs 5–75 lb, IronMaster Super Bench + preacher attachment + cable tower + leg ext / leg curl attachments. Cable handles: V, rope, rotating, single-arm. **No trap bar.**
- **BUR (Burlingame office gym):** Power rack + BB + plates, **trap bar**, cable stack / functional trainer, incline leg press, landmine (for rows), full DB rack past 75 lb. **No hamstring curl machine, no leg extension machine, no calf press machine, no belt squat.**

---

## 2. Weekly hard sets per muscle

Primary + 0.5×secondary.

| Muscle | Sets/wk | Source |
|---|---|---|
| Chest | 10 | Bench D1 (4) + Incline D2 (3) + carryover |
| Lats | 9 | Pulldown wide D1 + Pulldown close D3 + DB Row D3 |
| Upper back | 9 | Seated Row D2 + DB Row D3 + Rear Delt Fly D3 |
| Side delts | 8 | Lat Raise DB D1 (4) + Lat Raise Cable D2 (4, lengthened bias) |
| Rear delts | 8 | Rear Delt Fly / Face Pull D2 (4) + D3 (4) |
| Quads | 7 | Split Squat / Belt Squat — D1 (3) + Leg Ext / Leg Press / Trap Bar — D2 (4) |
| Hamstrings | 9 | **Knee-flexion 6** (Leg Curl Home / Cable Curl BUR — D1 + D3) + **Hinge 3** (RDL D1) |
| Glutes | 9 | RDL + Single-Leg DB Hip Thrust / Cable Pull-Through + BSS |
| Biceps | 9 | Incline / Hammer Curl D1 (3 stretched) + Spider / Cable Curl D2 (3 mid) + Preacher / Cable D3 (3) |
| Triceps | 9 effective | Overhead D2A + Pushdown D2B + Pushdown D3A + Skullcrusher D3B + press carryover |
| Calves | 9 | Heavy 6–10 D1 (3) + High-rep 12–15 D2 (3) + D3 (3) |
| Abs | 6 | Knee Raise D1 (3) + Cable Crunch / Hanging Leg Raise D3 (3) |

> **Hamstring honesty:** the 9 total is **6 genuine knee-flexion** (the half that RDLs miss) + **3 hinge** (RDL). RDL is *not* double-counted as knee-flexion. Home does knee-flexion on the IronMaster leg-curl attachment (Lying Leg Curl — same attachment that does the leg extensions). BUR has no leg-curl machine, so both BUR knee-flexion slots are a **cable hamstring curl** (ankle strap on the stack); if no strap is available, fall back to lying DB / floor curls.

---

## 3. Program design

### Architecture
**3 days × 2 locations = 6 routines.** Train 3×/wk, one Day per session. Home or BUR decided ad hoc.

- **Day 1** — Press + Hinge + Vertical Pull
- **Day 2** — OHP + Quad + Horizontal Pull
- **Day 3** — Posterior + Pull + Arms (hamstrings opened first)

**Variants A and B live inside one routine as "choose one" superset pairs.** Each slot that has two valid options shows them as a bracketed pair in Hevy — **A (top) = heavier/compound** (lower reps, longer rest), **B (bottom) = variation** (Swiss bar / DB / cable, moderate reps). Pick one per slot; do not do both. Run a "pure A day" by always taking the top of each bracket, or mix for variety. Slots where A and B are the same movement are plain single exercises. The §4 tables below show the A and B options side by side — that's the content of each bracket.

*(History note: this was 12 separate routines (Day N × A/B × location); the A/B variants were merged into choose-one pairs to cut it to 6. The old B routines are archived in Hevy.)*

### Double progression
1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Add 1 rep per set when possible each session.
3. When all sets hit the **top**: next session **add 5 lb** (or the smallest plate/microplate jump you have), reset to bottom.
4. Stop at **RIR 1–2**. Don't grind to failure on compounds.

### Rest periods — why each number

Rest scales with how heavy the set is and how much it taxes you systemically. Heavier, multi-joint, lower-rep work needs more recovery to preserve reps on the next set; small isolation work needs little.

| Rest | Applied to | Rationale |
|---|---|---|
| **150 s** | Heavy/moderate barbell compounds (bench, OHP, RDL, trap bar, incline, hip thrust, 4–8 rep openers) | Near-heavy loads tax ATP/CP stores and the CNS. Full-ish recovery keeps reps and bar speed up — under-resting here just bleeds reps off later sets. (Capped at 150s; 180s felt too long.) |
| **120 s** | Accessory compounds (pulldowns, rows, leg press, split/belt squat at ~10–12 reps) | Multi-joint but lighter/higher-rep — ~2 min restores enough to hit the target. |
| **90 s** | Larger isolations, leg curls, calves | Single-joint, smaller fatigue cost. |
| **60–75 s** | Small isolations (lateral raises, curls, pushdowns, rear delts, abs) | Tiny muscles, low systemic cost. Short rest keeps density and pump up without hurting the next set. |

**Evidence:** the old "short rest for hypertrophy" idea was overturned — Schoenfeld 2016 found ~3 min rest on compounds grew *more* muscle than 1 min, because total volume-load held up better. So: rest long enough on the big lifts to keep reps, rest short on isolation where fatigue is local. B variants use the shorter end of each tier (lighter loads, more density).

**These are starting points, not laws.** If you're fully recovered before the timer, go — RIR and bar speed matter more than the clock. To shorten a session, trim compound rest first, or superset antagonists (curl while resting from a triceps move) to cut total time without cutting per-muscle rest.

### Deload
Every 5–7 weeks, or when 2+ exercises stall for 2 consecutive sessions: one light week. Top-set weight × 0.6. 2 sets instead of 3. Same rep target. Smooth bar speed.

---

## 4. The 12 routines

Each cell: exercise — sets×reps · rest. Hevy template IDs in [IMPLEMENTATION.md §2](./IMPLEMENTATION.md#2-exercise-template-id-lookup).

The **Est. time** row is moving time per variant — assumes ~40 s per working set, rest as programmed, plus a warm-up allowance for the heavy barbell openers. Phone/chatting adds to it.

### Day 1 — Press + Hinge + Vertical Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Horizontal press | Bench Press (BB) — 4×6–8 · 150s | Swiss Bench Press — 4×8–10 · 150s | Bench Press (BB) — 4×6–8 · 150s | Bench Press (DB) — 4×8–10 · 150s |
| 2 | Hip hinge | Romanian Deadlift (BB) — 3×8–10 · 150s | Romanian Deadlift (DB) — 3×10–12 · 120s | Romanian Deadlift (BB) — 3×8–10 · 150s | Romanian Deadlift (DB) — 3×10–12 · 120s |
| 3 | Vertical pull (wide) | Lat Pulldown (Cable) — 3×8–10 · 120s | Reverse Grip Lat Pulldown — 3×10–12 · 120s | Lat Pulldown (Cable) (BUR) — 3×8–10 · 120s | Reverse Grip Lat Pulldown — 3×10–12 · 120s |
| 4 | Quad single-leg | Bulgarian Split Squat — 3×8–10/side · 120s | Belt Squat — 3×10–12 · 120s | Bulgarian Split Squat — 3×8–10/side · 120s | Split Squat (DB) — 3×10–12 · 120s |
| 5 | Hamstrings (knee flexion) | Lying Leg Curl (Home) — 3×10–12 · 90s | Lying Leg Curl (Home) — 3×12–15 · 90s | Standing Leg Curl (Cable) — 3×10–12 · 90s | Standing Leg Curl (Cable) — 3×10–12 · 90s |
| 6 | Side delts | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s | Lateral Raise (DB) — 4×12–15 · 75s | Lateral Raise (DB) — 4×12–15 · 60s |
| 7 | Biceps (stretched) | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s | Incline Curl (DB) — 3×10–12 · 60s | Hammer Curl (DB) — 3×10–12 · 60s |
| 8 | Calves (heavy) | Standing Calf Raise (DB) — 3×6–10 · 90s | Single Leg Standing Calf Raise (DB) — 3×6–10/side · 90s | Single Leg Standing Calf Raise (DB) — 3×6–10/side · 90s | Single Leg Standing Calf Raise (DB) — 3×6–10/side · 90s |
| 9 | Abs | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s | Hanging Knee Raise — 3×10–15 · 60s | Ab Wheel — 3×8–12 · 60s |
| — | **Est. time** | **~76 min** | **~72 min** | **~76 min** | **~72 min** |

### Day 2 — OHP + Quad + Horizontal Pull

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Vertical press | Overhead Press (BB) — 4×6–8 · 150s | Shoulder Press (DB) — 4×8–10 · 150s | Overhead Press (BB) — 4×6–8 · 150s | Arnold Press (DB) — 4×8–10 · 150s |
| 2 | Horizontal pull | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s | Seated Cable Row — V Grip — 3×10–12 · 120s | Seated Cable Row — Bar Wide — 3×10–12 · 120s |
| 3 | Incline press | Incline Bench Press (BB) — 3×8–10 · 150s | Swiss Bar Incline — 3×10–12 · 120s | Incline Bench Press (BB) — 3×8–10 · 150s | Incline Bench Press (DB) — 3×10–12 · 120s |
| 4 | Quad | Belt Squat — 4×10–12 · 120s | Leg Extension (Home) — 4×12–15 · 90s | Leg Press (Machine) (BUR) — 4×10–12 · 120s | Trap Bar Deadlift — 4×8–10 · 150s |
| 5 | Side delts (lengthened) | Lateral Raise (Cable) — 4×12–15 · 75s | Lateral Raise (Cable) — 4×12–15 · 60s | Lateral Raise (Cable) — 4×12–15 · 75s | Lateral Raise (Cable) — 4×12–15 · 60s |
| 6 | Rear delts | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 7 | Biceps (mid-range) | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s |
| 8 | Triceps (lengthened on A) | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s |
| 9 | Calves (high-rep) | Standing Calf Raise (DB) — 3×12–15 · 90s | Single Leg Standing Calf Raise (DB) — 3×12–15/side · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s |
| — | **Est. time** | **~80 min** | **~75 min** | **~80 min** | **~80 min** |

### Day 3 — Posterior + Pull + Arms

| # | Slot | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|
| 1 | Hamstrings (priority) | Lying Leg Curl (Home) — 3×10–12 · 90s | Lying Leg Curl (Home) — 3×12–15 · 90s | Standing Leg Curl (Cable) — 3×10–12 · 90s | Standing Leg Curl (Cable) — 3×10–12 · 90s |
| 2 | Glute primary ⟮pick 1⟯ | Single Leg Hip Thrust (DB) — 3×10–12/side · 120s | Cable Pull-Through — 3×10–15 · 90s | Single Leg Hip Thrust (DB) — 3×10–12/side · 120s | Cable Pull-Through — 3×10–15 · 90s |
| 3 | Vertical pull (close) | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s | Lat Pulldown — Close Grip — 3×8–10 · 120s | Straight Arm Lat Pulldown (Cable) — 3×10–12 · 90s |
| 4 | Horizontal pull #2 | Dumbbell Row — 3×8–10 · 120s | Dumbbell Row — 3×10–12 · 90s | Dumbbell Row — 3×8–10 · 120s | Single Arm Cable Row — 3×10–12 · 90s |
| 5 | Rear delts | Rear Delt Reverse Fly (DB) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 6 | Biceps | Preacher Curl (DB) — 3×10–12 · 75s | Cross Body Hammer Curl — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Hammer Curl (Cable) — 3×10–12 · 75s |
| 7 | Triceps (lateral/medial on A) | Triceps Rope Pushdown — 3×10–12 · 75s | Skullcrusher (BB) — Swiss — 3×10–12 · 90s | Triceps Rope Pushdown (BUR) — 3×10–12 · 75s | Skullcrusher (BB) — 3×10–12 · 90s |
| 8 | Calves | Standing Calf Raise (DB) — 3×12–15 · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s |
| 9 | Abs | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s |
| — | **Est. time** | **~64 min** | **~60 min** | **~64 min** | **~60 min** |

---

## 5. Critique

Four reviewers (Mike Israetel, Layne Norton, Pavel Tsatsouline, Andy Galpin) were run as independent subagents, each refreshed on the persona's current published philosophy and asked to critique in their voice. The program was iterated until all four signed off, then re-confirmed after the equipment corrections (Nordic removed, trap bar added at BUR, quad slot simplified to 7 direct sets). Final verdicts verbatim.

**All four: APPROVE — no material changes needed.**

### Mike Israetel (Renaissance Periodization) — APPROVE
> Knee bars back squat, so leg press + trap-bar pull + belt squat carry the compound load, and 7 direct quad sets at meaningful loads on a 6+ yr trainee in a GLP-1 recovery phase is plenty — junk-volume territory starts well north of that. Cable hamstring curl is a fine Nordic replacement; you keep 6 knee-flexion sets at 2x frequency, which is what actually matters. Rear delts 8, hamstrings honest, calves 9 — all the earlier fixes held.

### Layne Norton (BioLayne) — APPROVE
> Quads at 7 direct is fine — single-leg work plus the trap-bar deadlift on BUR-B feeds the quads, so effective volume sits north of 7 and that's plenty to grow on. The Nordic-to-cable-curl swap is a non-issue: ankle-strap cable curls hit knee flexion honestly, 6 sets at 2x frequency, both locations. That's the fix I wanted, intact. Rear delts and calves still resolved.

### Pavel Tsatsouline (StrongFirst) — APPROVE
> The slots breathe now and a real bilateral pull anchors the day — that is strength training, not bodybuilding fidgeting. The trap-bar deadlift earns its keep: load the spine, drive the floor, grow the whole body. Quads at seven honest sets beat nine confused ones. You stopped chasing the machine and picked up the bar. Comrade, this is a block I would run.

### Andy Galpin (performance scientist) — APPROVE
> Quads at 7 direct sets/week with a trap-bar deadlift anchoring bilateral load is plenty for LBM preservation on a GLP-1 deficit — hypertrophy lives at intensity and proximity to failure, not set-count maximalism. Losing the Nordic costs you the long-length eccentric, but cable curls at 2x/week protect the hamstring tissue and the knee-flexion separation is what matters here; the eccentric was always a fatigue tax you don't need right now.

### Final validation (post-consolidation)

After the 12→6 consolidation and the hip-thrust removal, the panel was re-run to validate. **Consolidation:** all four confirm it's packaging-only — same exercises/sets/reps/rest, no effect on stimulus. **Glute swap:** 3 of 4 (Israetel, Norton, Tsatsouline) flagged that dropping the hip thrust deleted the only loaded peak-contraction bridge pattern; Galpin judged cable-only adequate for maintenance. Resolution: **Single-Leg DB Hip Thrust restored** as the Day 3 glute primary (choose-one with Cable Pull-Through) — a loadable bridge that isn't the awkward barbell version. All four now satisfied.

---

## 6. Open items (optional, non-blocking)

None of these block the program — the panel approved as-is. They're the dissents and upgrade paths to revisit if results stall.

1. **Readiness check** — Norton and Galpin both still want a 30-second morning gate (1–10 score, or sleep/soreness/motivation). Removed by your call as "autoregulation theater." Reconsider if recovery markers drift on the GLP-1.
2. **Quads at 7, not 9** — dropped when Day 2's split quad slot (4a/4b) was simplified to one slot. Defensible (single-leg D1 work counts heavy per-leg, and BUR's trap-bar adds a quad-dominant compound), but if quads lag, add a 2–3 set leg-extension finisher to Day 2 at Home (BUR has no leg-ext machine — would use leg-press or split squat instead).
3. **Side delts 8 → 12** — Israetel's earlier push; he approved at 8. Add a 3rd weekly hit if delts plateau.
4. **Horizontal rows vs vertical pulls** — Tsatsouline notes rows (~6 sets) run lean against vertical pulls (~9). Upper back is covered at 9 total, but converting one pulldown slot to a heavy row is a free rebalance if mid-back thickness lags. At BUR the landmine is the natural heavy-row tool.
5. **Zone 2** — Galpin's standing suggestion: two 20-min nasal-breathing walks on off days. Additive, doesn't touch the 3 lifting sessions.

**Not acted on, by design:**
- Tsatsouline: collapse variants / heavy strength singles / cut bicep volume — off-phase for hypertrophy + LBM reaccrual.
- Galpin: explicit protein targets / intra-session carbs — out of scope (training only).

---

## 7. Travel / hotel program

**Real hypertrophy-retention training, not bare maintenance** — the trainee trains 3×/week even while traveling. **One full-body routine, done 3×/week**, repeatable. Full-body 3× = ~9 sets/muscle/week, matching the home targets. The lead bench gets an **AMRAP** final set. Train **0–2 RIR** — light hotel loads mean training close to failure.

**One routine, equipment-agnostic.** Six slots are fixed dumbbell movements (always do them). The other slots are **"choose one" superset pairs** — a DB option and a cable option grouped together; do whichever the hotel gym supports, not both. (Hevy has no native "exercise alternative," so the superset bracket is repurposed as the either/or cue — see the feature request we filed.)

Hevy routine: **Hotel (Travel)** (`88260512-…`), Travel folder. IDs in [IMPLEMENTATION.md §1](./IMPLEMENTATION.md#1-hevy-account-state).

| Slot | DB option (dumbbells only) | Cable option (functional trainer) | Sets × Reps |
|---|---|---|---|
| 1 — Chest | **DB Bench Press** (+ AMRAP last set) | *(same)* | 3 × 6–10 |
| 2 — Back ⟮pick 1⟯ | One-Arm DB Row | Cable Row | 3 × 8–12 |
| 3 — Hinge ⟮pick 1⟯ | DB Romanian Deadlift *(tempo)* | Cable Pull-Through *(tempo)* | 3 × 12–20 |
| 4 — Quad | **DB Box Step-up** *(tempo)* | *(same)* | 3 × 12–20 / side |
| 5 — Shoulders | **DB Overhead Press** | *(same)* | 3 × 8–12 |
| 6 — Side delts ⟮pick 1⟯ | DB Lateral Raise | Cable Lateral Raise | 3 × 12–20 |
| 7 — Rear delts ⟮pick 1⟯ | Chest-Supported Reverse Fly | Cable Face Pull | 3 × 12–20 |
| 8 — Biceps ⟮pick 1⟯ | DB Incline Curl | Cable Curl | 3 × 10–15 |
| 9 — Triceps ⟮pick 1⟯ | DB Skullcrusher | Cable Pushdown | 3 × 10–15 |
| 10 — Calves | **DB Standing Calf Raise** | *(same)* | 3 × 12–20 |

You perform **10 movements** per session (~65 min): the 4 fixed singles + one from each of the 6 pairs. In Hevy that's 16 exercise rows (4 singles + 6 superset pairs).

**Light-DB protocol — the travel variable.** Hotel DBs cap ~50 lb on the low end, which under-loads the hinge, legs, and pressing for a strong lifter. Convert the load ceiling into tension and failure proximity:
- **3-second lowering** on every rep.
- **1–2 s pause in the stretched position** on presses, rows, the hinge, and the step-up.
- **Last set of each movement:** add 1.5-reps, partials at the hard point, or go to true failure.
- **Hinge + step-up specifically:** run 12–20 reps with the slow eccentric + stretched pause — that's where the light bells bite least, so tension technique matters most.
- When heavier DBs are available, just load up and work the lower rep end normally.

**Single-leg / knee note.** Box Step-up to a controlled, pain-free height. Knee good → progress to Bulgarian split squat / reverse lunge to controlled depth. Knee cranky → lower the box / reduce ROM.

**Panel.** Settled over multiple rounds — all four (Israetel, Norton, Tsatsouline, Galpin) APPROVE. The minimalist first draft was rebuilt fuller once the trainee confirmed adherence/time is not a travel constraint. Final consensus: full-body 3-set volume balanced front-to-back, a **vertical pull in both setups** (DB Pullover / Lat Pulldown — the gap Norton caught), and an explicit **tempo/pause/failure protocol** to beat the light-DB ceiling (Tsatsouline + Galpin).
