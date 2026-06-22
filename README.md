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
| Rear delts | 8 | Rear Delt Fly / Face Pull D2 (4) + D3 (4) |
| Quads | 9 | Belt Squat / Landmine Squat / Leg Ext / Leg Press / BSS — D1 + D2 |
| Hamstrings | 9 | **Knee-flexion 6** (Leg Curl / Nordic / Cable Curl — D1 + D3) + **Hinge 3** (RDL D1) |
| Glutes | 9 | RDL + Hip Thrust + BSS |
| Biceps | 9 | Incline / Hammer Curl D1 (3 stretched) + Spider / Cable Curl D2 (3 mid) + Preacher / Cable D3 (3) |
| Triceps | 9 effective | Overhead D2A + Pushdown D2B + Pushdown D3A + Skullcrusher D3B + press carryover |
| Calves | 9 | Heavy 6–10 D1 (3) + High-rep 12–15 D2 (3) + D3 (3) |
| Abs | 6 | Knee Raise D1 (3) + Cable Crunch / Hanging Leg Raise D3 (3) |

> **Hamstring honesty:** the 9 total is **6 genuine knee-flexion** (the half that RDLs miss) + **3 hinge** (RDL). RDL is *not* double-counted as knee-flexion. At BUR there's no leg-curl machine, so the D1 knee-flexion slot is a **cable hamstring curl** (ankle strap on the stack); if no strap is available, fall back to Single-Leg RDL and accept that week skews hinge. BUR's D3 knee-flexion is the Nordic.

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
| 5 | Hamstrings (knee flexion) | Lying Leg Curl (Home) — 3×10–12 · 90s | Standing Leg Curls — 3×10–12 · 90s | Hamstring Curl (Cable) — 3×10–12 · 90s | Hamstring Curl (Cable) — 3×10–12 · 90s |
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
| 6 | Rear delts | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull — 4×12–15 · 60s | Rear Delt Reverse Fly (Cable) — 4×12–15 · 60s | Face Pull (BUR) — 4×12–15 · 60s |
| 7 | Biceps (mid-range) | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s | Spider Curl (DB) — 3×10–12 · 75s | Bicep Curl (Cable) — 3×10–12 · 75s |
| 8 | Triceps (lengthened on A) | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s | Overhead Triceps Extension (Cable) — 3×10–12 · 75s | Triceps Pushdown — 3×10–12 · 75s |
| 9 | Calves (high-rep) | Standing Calf Raise — 3×12–15 · 90s | Single Leg Standing Calf Raise (DB) — 3×12–15/side · 90s | Calf Press (Machine) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s |

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
| 8 | Calves | Standing Calf Raise (DB) — 3×12–15 · 90s | Standing Calf Raise (DB) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s | Calf Press (Machine) — 3×12–15 · 90s |
| 9 | Abs | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s | Cable Crunch — 3×12–15 · 60s | Hanging Leg Raise — 3×10–15 · 60s |

---

## 5. Critique

Four reviewers (Mike Israetel, Layne Norton, Pavel Tsatsouline, Andy Galpin) were run as independent subagents, each refreshed on the persona's current published philosophy and asked to critique in their voice. The program was iterated across rounds until all four signed off. Final sign-off below; each verdict is verbatim.

**All four: APPROVE — no material changes needed.**

### Mike Israetel (Renaissance Periodization) — APPROVE
- **Rear delts:** Fixed. 4 to 8 sets across two weekly slots. Twice-a-week frequency, lands them squarely in the productive range for a stubborn, chronically underdone muscle.
- **Hamstring accounting:** Fixed, and honest. You stopped laundering the RDL hinge as knee-flexion. Six genuine knee-flexion plus three hinge is real coverage of both functions, and both locations now do actual curls.
- **Calves:** Fixed. 6 to 9 across three sessions with a heavy/high-rep split — exactly right for a tissue that lives on stimulus frequency.
- **Remaining:** None that blocks. Abs at 6 is light but defensible at maintenance; biceps at 9 is your call.

### Layne Norton (BioLayne) — APPROVE
- **Rear delts:** Resolved. 4 to 8 sets, now 2×/wk with a dedicated slot. A real working dose at a meaningful frequency. The weak link is fixed.
- **Hamstring accounting / BUR:** Resolved. The 9 is now honest — 6 true knee-flexion + 3 hinge — and both knee-flexion slots are genuine at both locations. You killed the RDL double-count and the BUR location-fragility.
- **Calves:** Resolved. 6 to 9 across 3×/wk. Right direction and frequency.
- **Remaining:** None that blocks. Still want autoregulation in writing, but you've made that call and it's defensible at this volume. Trap-bar's a nice optional, not a requirement.

### Pavel Tsatsouline (StrongFirst) — APPROVE
- **Rear-delt ratio:** Fixed. 8 rear : 9 arms is honest now. The posterior shoulder no longer pays in pennies while the arms feast. Eight quality sets across two days is enough frequency to grow them.
- **Remaining:** None that blocks. Rows at six against nine vertical is lean, but upper back credited at nine carries it. Quads at nine without a spine-loaded squat is fine for hypertrophy — leg press and BSS drive the tissue. "A block need not be perfect to be productive. This one will put on muscle. Make every rep own its weight."

### Andy Galpin (performance scientist) — APPROVE
- **Rear delts:** Yes. 4 to 8 sets across two days, true 2× frequency. Clears the dose-response floor and the asymmetry/posture concern for a forward-loaded history.
- **Hamstring separation / frequency:** Yes. The bucket is now honest — 6 knee-flexion at 2×/wk (D1+D3), hinge standing on its own. The 72-hr knee-flexion gap is closed.
- **Remaining:** None blocking. Still thinks a 30-second readiness gate is cheap insurance on a GLP-1 recovery phase, but that is your settled call and Zone 2 is optional under the 3-session constraint — neither is a physiological deal-breaker.

---

## 6. Open items (optional, non-blocking)

None of these block the program — the panel approved as-is. They're the dissents and upgrade paths to revisit if results stall.

1. **Readiness check** — Norton and Galpin both still want a 30-second morning gate (1–10 score, or sleep/soreness/motivation). Removed by your call as "autoregulation theater." Reconsider if recovery markers drift on the GLP-1.
2. **Side delts 8 → 12** — Israetel's earlier push; he approved at 8. Add a 3rd weekly hit if delts plateau.
3. **Horizontal rows vs vertical pulls** — Tsatsouline notes rows (~6 sets) run lean against vertical pulls (~9). Upper back is covered at 9 total, but converting one pulldown slot to a heavy row is a free rebalance if mid-back thickness lags.
4. **Deadlift / trap-bar** — available at both gyms, unprogrammed. Optional heavier-hinge stimulus; swap for D1A RDL if wanted.
5. **Zone 2** — Galpin's standing suggestion: two 20-min nasal-breathing walks on off days. Additive, doesn't touch the 3 lifting sessions.

**Not acted on, by design:**
- Tsatsouline: collapse variants / heavy strength singles / cut bicep volume — off-phase for hypertrophy + LBM reaccrual.
- Galpin: explicit protein targets / intra-session carbs — out of scope (training only).
