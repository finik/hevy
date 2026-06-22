# Hevy Training Plan — Source of Truth

Living document for Dmitry's training program. Captures the design, the actual routines in Hevy, the adversarial review that shaped them, and the operational notes a future iteration needs. Update this file alongside any Hevy change.

- **Owner:** Dmitry (Hevy account)
- **First built:** 2026-06-20
- **Last updated:** 2026-06-21
- **Hevy MCP host:** MiniM1 (Claude Code, stdio transport, `chrisdoc/hevy-mcp`)

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
- **No hamstring curl machine** — hamstring work via RDL / Single-Leg RDL / banded curl

### Training frequency
- **3 sessions / week.** No fixed schedule. Home or BUR chosen ad hoc per day.
- Demonstrated adherence: ~3.0 sessions/wk sustained over 6+ months, ~12/month average for 2+ years.

---

## 2. Analysis driving the design (n=429 workouts since 2023-03-11)

### Volume per muscle — current intent (sets/wk, primary + 0.5×secondary)

| Muscle | Sets/wk target | Source movements |
|---|---|---|
| Chest | **10** | Bench D1 + Incline D2 + Fly carryover |
| Lats | **9** | Pulldown D1 (wide) + Pulldown D3 (close) + DB Row |
| Upper back | **9** | Seated Row D2 + DB Row D3 + Rear delt fly |
| Side delts | **12** (after adversarial review) | Lat raise D1 + D2 + D3 |
| Quads | **9** (after adversarial review) | Belt squat + Leg ext/press + BSS |
| Hamstrings | **9** (after adversarial review) | RDL + Leg curl + Nordic/banded |
| Glutes | **9** | RDL + Hip Thrust + BSS |
| Biceps | 6+ direct + pull carryover | Preacher/Cable curl D3 |
| Triceps | **9 effective** | Pushdown D2 + Overhead D3 + press carryover |
| Calves | 6, mixed heavy/high-rep | D1 + D2 |
| Abs | 6 | Knee Raise D1 + Cable Crunch D3 |

### Imbalances the program addresses

1. **Posterior chain** — no squat or conventional deadlift. Replaced with RDL + Hip Thrust + Leg Curl. Hip-dominant + knee-flexion both covered.
2. **No calves, no direct ab/core** — added to two days each.
3. **No vertical pull at home** until IronMaster cable tower returned. Now wide-grip + close-grip on separate days.
4. **No rear delt isolation** — Rear Delt Reverse Fly on Day 3.
5. **Bicep-heavy vs tricep direct work** — rebalanced toward triceps (9 effective vs 6 direct biceps).

### Progression — last 12 weeks (top-set est-1RM, Epley)

**Improving:** Bench Press +6.9%, Incl Bench +2.9%, DB Row +6%, Chest Fly +16%, Lat Raise +32%.
**Stalled:** Overhead Press 0%, Triceps Extension 0%, V-grip Row 0%.
**Regressing:** DB Shoulder Press −4%, Lying Leg Curl −8%.

Peak lifts late-2024 / early-2025 sit ~15–25% above current — consistent with documented fat-loss + lean-mass decline. Floor holding; bench rebuilding.

### Data hygiene
- 7,257/7,407 sets logged as `type=normal`; 150 warmup. No dropsets/failure/AMRAP markers historically.
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

User trains 3×/wk, picking one variant of each day per week. Home or BUR decided ad hoc by daily schedule.

### Progression scheme

**Double progression.**
1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Add 1 rep per set when possible each session.
3. When all sets hit the **top** of the range: next session **add 2.5 kg** (BB) / **5 lb** (DB), drop back to bottom of range.
4. Stop sets at **RIR 1–2**. Don't grind to failure on compounds.

### Deload protocol

Every **5–7 weeks** (tighter than the textbook 6–8 because of GLP-1 recovery tail — see §5 Norton critique), or when 2+ exercises stall for 2 consecutive sessions:

- **One light week.**
- Top-set weight × **0.6**.
- **2 sets** per exercise instead of 3.
- Same rep target, smooth bar speed.
- Resume normal loads next week.

---

## 4. The 12 routines

Each day = one table. Columns: **Slot · S×R (A / B) · Rest (A / B) · Home A · Home B · BUR A · BUR B**. Exercise + Hevy `exercise_template_id` shown inline. When A and B share the same prescription, the cell collapses. See §6 for the master template ID lookup.

### Day 1 — Press + Hinge + Vertical Pull

| # | Slot | S×R (A / B) | Rest (A / B) | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|---|---|
| 1 | Horizontal press | 4×6–8 / 4×8–10 | 180 / 150 | Bench Press (BB) `79D0BB3A` | Swiss Bench Press `8b6558c7` | Bench Press (BB) `79D0BB3A` | Bench Press (DB) `D04AC939` |
| 2 | Hip hinge | 3×8–10 / 3×10–12 | 150 / 120 | Romanian Deadlift (BB) `2B4B7310` | Romanian Deadlift (DB) `72CFFAD5` | Romanian Deadlift (BB) `2B4B7310` | Romanian Deadlift (DB) `72CFFAD5` |
| 3 | Vertical pull (wide) | 3×8–10 / 3×10–12 | 120 / 120 | Lat Pulldown (Cable) `6A6C31A5` | Reverse Grip Lat Pulldown `046E25A2` | Lat Pulldown (Cable) (BUR) `36548ca5` | Reverse Grip Lat Pulldown `046E25A2` |
| 4 | Quad single-leg | 3×8–10/side / 3×10–12 | 120 / 120 | Bulgarian Split Squat `B5D3A742` | Belt Squat `e05d4883` | Bulgarian Split Squat `B5D3A742` | Split Squat (DB) `20C1A3CB` |
| 5 | Side delts | 4×12–15 | 75 / 60 | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` |
| 6 | Calves (heavy) | 3×6–10 | 90 | Standing Calf Raise (DB) `6DA40660` | Single Leg Standing Calf Raise (DB) `5DA40761` | Calf Press (Machine) `91237BDD` | Calf Press (Machine) `91237BDD` |
| 7 | Abs | 3×10–15 / 3×8–12 | 60 | Hanging Knee Raise `08590920` | Ab Wheel `99D5F10E` | Hanging Knee Raise `08590920` | Ab Wheel `99D5F10E` |

> **Notes:** Side delts raised to 4 sets per session in response to convergent Israetel/Norton critique. Calves shifted to a heavy 6–10 rep range (Norton).

### Day 2 — OHP + Quad + Horizontal Pull

| # | Slot | S×R (A / B) | Rest (A / B) | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|---|---|
| 1 | Vertical press | 4×6–8 / 4×8–10 | 180 / 150 | Overhead Press (BB) `7B8D84E8` | Shoulder Press (DB) `878CD1D0` | Overhead Press (BB) `7B8D84E8` | Arnold Press (DB) `A69FF221` |
| 2 | Horizontal pull | 3×10–12 | 120 | Seated Cable Row – V Grip `0393F233` | Seated Cable Row – Bar Wide `C3BCABB3` | Seated Cable Row – V Grip `0393F233` | Seated Cable Row – Bar Wide `C3BCABB3` |
| 3 | Incline press | 3×8–10 / 3×10–12 | 150 / 120 | Incline Bench Press (BB) `50DFDFAB` | Swiss Bar Incline `5f7bbdab` | Incline Bench Press (BB) `50DFDFAB` | Incline Bench Press (DB) `07B38369` |
| 4a | Quad compound | 4×10–12 | 120 | Leg Extension (Home) `d2db4633` | Belt Squat `e05d4883` | Leg Press (Machine) (BUR) `78581019` | Belt Squat `e05d4883` |
| 4b | Quad isolation | 2×12–15 (B only) | 60 | — | Leg Extension (Home) `d2db4633` | — | Leg Extension (Machine) `75A4F6C4` |
| 5 | Side delts | 4×12–15 | 75 / 60 | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` |
| 6 | Triceps (lengthened) | 3×10–12 | 75 | Overhead Triceps Extension (Cable) `B5EFBF9C` | Triceps Pushdown `93A552C6` | Overhead Triceps Extension (Cable) `B5EFBF9C` | Triceps Pushdown `93A552C6` |
| 7 | Calves (high-rep) | 3×12–15 | 90 | Standing Calf Raise `06745E58` | Single Leg Standing Calf Raise (DB) `5DA40761` | Calf Press (Machine) `91237BDD` | Calf Press (Machine) `91237BDD` |

> **Notes:** Quad slot expanded to compound + isolation (4 + 2 sets on B days) per Israetel/Norton — total quad direct sets rise from 6 to 9/wk. Day 2 triceps shifted to lengthened-position emphasis on A days (overhead) so the week is balanced with Day 3's pushdown/skullcrusher.

### Day 3 — Pull + Posterior + Arms

| # | Slot | S×R (A / B) | Rest (A / B) | Home A | Home B | BUR A | BUR B |
|---|---|---|---|---|---|---|---|
| 1 | Vertical pull (close) | 3×8–10 / 3×10–12 | 120 / 90 | Lat Pulldown – Close Grip `4E5257DE` | Straight Arm Lat Pulldown (Cable) `D2387AB1` | Lat Pulldown – Close Grip `4E5257DE` | Straight Arm Lat Pulldown (Cable) `D2387AB1` |
| 2 | Glute primary | 3×8–12 / 3×10–12 | 150 / 120 | Hip Thrust (BB) `D57C2EC7` | Single Leg Hip Thrust (DB) `D1CD146F` | Hip Thrust (BB) `D57C2EC7` | Hip Thrust (Machine) `68CE0B9B` |
| 3 | Hamstrings (knee flexion) | 3×10–12 | 90 | Lying Leg Curl (Home) `322a9e07` | Standing Leg Curls `6120CAAB` | Nordic Hamstring Curl `3E81CD3D` | Nordic Hamstring Curl `3E81CD3D` |
| 4 | Horizontal pull #2 | 3×8–10 / 3×10–12 | 120 / 90 | Dumbbell Row `F1E57334` | Dumbbell Row `F1E57334` | Dumbbell Row `F1E57334` | Single Arm Cable Row `D0C4A899` |
| 5 | Rear delts | 4×12–15 | 60 | Rear Delt Reverse Fly (DB) `E5988A0A` | Face Pull `BE640BA0` | Rear Delt Reverse Fly (Cable) `C315DC2A` | Face Pull (BUR) `dcb574e5` |
| 6 | Side delts (3rd hit) | 3×12–15 | 60 | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` | Lateral Raise (DB) `422B08F1` |
| 7 | Biceps | 3×10–12 | 75 | Preacher Curl (DB) — IronMaster `FAB6EB2F` | Cross Body Hammer Curl `32C4D4A2` | Bicep Curl (Cable) `ADA8623C` | Hammer Curl (Cable) `36E8F14E` |
| 8 | Triceps | 3×10–12 | 90 | Overhead Triceps Extension (Cable) `B5EFBF9C` | Skullcrusher (BB) — Swiss `875F585F` | Overhead Triceps Extension (Cable) `B5EFBF9C` | Skullcrusher (BB) `875F585F` |
| 9 | Abs | 3×12–15 | 60 | Cable Crunch `23A48484` | Hanging Leg Raise `F8356514` | Cable Crunch `23A48484` | Hanging Leg Raise `F8356514` |

> **Notes:** BUR hamstring slot upgraded from Single-Leg RDL to Nordic Hamstring Curl (Norton/Israetel: dedicated knee-flexion needed, "or single-leg RDL" was an escape hatch). 3rd lat-raise hit added per Israetel volume target.

---

## 5. Adversarial review

Four persona reviewers were spawned in parallel to critique the program before commitment. Each refreshed on the persona's current published philosophy, then delivered specific feedback. Verbatim below, followed by a synthesis of convergent themes and the changes already merged into §4.

### 5.1 Mike Israetel (Renaissance Periodization)

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

### 5.2 Layne Norton (BioLayne)

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

### 5.3 Pavel Tsatsouline (StrongFirst)

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

### 5.4 Andy Galpin (performance scientist)

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

### 5.5 Synthesis — convergent themes & what we changed

| Theme | Israetel | Norton | Tsatsouline | Galpin | Action |
|---|---|---|---|---|---|
| Side delts undercooked (need 12+ sets/wk) | ✓ | ✓ | — | — | **Merged.** Lat raises → 4 sets D1, 4 sets D2, 3 sets D3 = 11 hard sets/wk. |
| Quad direct work too low (need 9+) | ✓ | ✓ | (separate critique) | ✓ | **Merged.** Day 2 quad slot split into compound (4×10–12) + isolation (2×12–15 on B days). |
| Hamstring stimulus poor, "or single-leg RDL" is an escape hatch | ✓ | ✓ | — | ✓ | **Merged.** BUR hamstring slot upgraded from Single-Leg RDL → Nordic Hamstring Curl. |
| Long-head triceps underloaded | ✓ | — | — | — | **Merged.** Day 2 triceps slot A-variants now Overhead Cable Extension; pushdown on B-variants. |
| Calves need heavy range too | — | ✓ | — | — | **Merged.** Day 1 calves now 3×6–10 heavy; Day 2 stays 3×12–15. |
| GLP-1 recovery tail → tighter deload | — | ✓ | — | (overlap: readiness) | **Merged.** Deload cadence narrowed to 5–7 weeks. |
| Autoregulation / readiness check | — | (RPE check) | — | ✓ | **Not merged.** Future addition — log morning 1–10 readiness, drop a set when red. Tracked as open item. |
| Add Zone 2 4th session | — | — | — | ✓ | **Not merged.** Trainee constraint = 3 sessions/wk; flagged for future consideration. |
| Collapse choice / fewer variants | — | — | ✓ | — | **Rejected.** A/B variants are deliberate adherence engineering for ad-hoc Home/BUR scheduling — Israetel, Norton, Galpin all endorsed this. |
| Heavy strength ramps (singles/doubles) before hypertrophy work | — | — | ✓ | — | **Rejected.** Phase goal is hypertrophy + LBM reaccrual, not max strength. Worth revisiting in a future strength block. |

**Net result:** 6 changes accepted (side delts +2 hits, quad isolation slot, BUR hams → Nordic, long-head triceps, heavy calf range, tighter deload). 2 open items tracked (readiness log, Zone 2). 2 rejections (collapse variants, heavy strength ramps) with explicit reasoning.

---

## 6. Master template ID reference

| Title | ID | Custom? |
|---|---|---|
| Belt Squat (= cable squat) | `e05d4883-21c8-4e27-abe2-d727abed2715` | yes |
| Bench Press (Barbell) | `79D0BB3A` | |
| Bench Press (Dumbbell) | `D04AC939` | |
| Bicep Curl (Cable) | `ADA8623C` | |
| Bicep Curl (Dumbbell) | `37FCC2BB` | |
| Bulgarian Split Squat | `B5D3A742` | |
| Cable Crunch | `23A48484` | |
| Calf Press (Machine) | `91237BDD` | |
| Chest Fly (Dumbbell) | `12017185` | |
| Cross Body Hammer Curl | `32C4D4A2` | |
| Dumbbell Row | `F1E57334` | |
| Face Pull | `BE640BA0` | |
| Face Pull (BUR) | `dcb574e5-54da-4d09-bb32-7a13e9940bea` | yes |
| Hammer Curl (Cable) | `36E8F14E` | |
| Hammer Curl (Dumbbell) | `7E3BC8B6` | |
| Hanging Knee Raise | `08590920` | |
| Hanging Leg Raise | `F8356514` | |
| Hip Thrust (Barbell) | `D57C2EC7` | |
| Hip Thrust (Machine) | `68CE0B9B` | |
| Incline Bench Press (Barbell) | `50DFDFAB` | |
| Incline Bench Press (Dumbbell) | `07B38369` | |
| Lat Pulldown (Cable) | `6A6C31A5` | |
| Lat Pulldown (Cable) (BUR) | `36548ca5-cd4d-4c26-9c8b-58540e6b2c97` | yes |
| Lat Pulldown – Close Grip (Cable) | `4E5257DE` | |
| Lateral Raise (Dumbbell) | `422B08F1` | |
| Leg Extension (Home) | `d2db4633-eda0-4a53-9eb3-4b604e7d9ad8` | yes |
| Leg Extension (Machine) | `75A4F6C4` | |
| Leg Press (Machine) (BUR) | `78581019-7446-44be-bda6-83feb96f5352` | yes |
| Lying Leg Curl (Home) | `322a9e07-47b6-4eca-af22-7786a2ad9e48` | yes |
| Nordic Hamstring Curl | `3E81CD3D` | |
| Overhead Press (Barbell) | `7B8D84E8` | |
| Overhead Triceps Extension (Cable) | `B5EFBF9C` | |
| Preacher Curl (Dumbbell) | `FAB6EB2F` | |
| Rear Delt Reverse Fly (Cable) | `C315DC2A` | |
| Rear Delt Reverse Fly (Dumbbell) | `E5988A0A` | |
| Reverse Grip Lat Pulldown (Cable) | `046E25A2` | |
| Romanian Deadlift (Barbell) | `2B4B7310` | |
| Romanian Deadlift (Dumbbell) | `72CFFAD5` | |
| Seated Cable Row – Bar Wide Grip | `C3BCABB3` | |
| Seated Cable Row – V Grip (Cable) | `0393F233` | |
| Shoulder Press (Dumbbell) | `878CD1D0` | |
| Arnold Press (Dumbbell) | `A69FF221` | |
| Single Arm Cable Row | `D0C4A899` | |
| Single Leg Hip Thrust (Dumbbell) | `D1CD146F` | |
| Single Leg Standing Calf Raise (Dumbbell) | `5DA40761` | |
| Skullcrusher (Barbell) | `875F585F` | |
| Split Squat (Dumbbell) | `20C1A3CB` | |
| Standing Calf Raise | `06745E58` | |
| Standing Calf Raise (Dumbbell) | `6DA40660` | |
| Standing Leg Curls | `6120CAAB` | |
| Straight Arm Lat Pulldown (Cable) | `D2387AB1` | |
| Swiss Bar Incline | `5f7bbdab-4cc9-4389-bfac-f32d30efac6d` | yes |
| Swiss Bench Press | `8b6558c7-d41b-4a26-afdb-6bb285f31df6` | yes |
| Triceps Pushdown | `93A552C6` | |
| Triceps Rope Pushdown | `94B7239B` | |
| Triceps Rope Pushdown (BUR) | `b1e50859-2ce0-4d97-9d17-3a25ac3677cb` | yes |

> Nordic Hamstring Curl ID `3E81CD3D` is a placeholder — confirm against the live `/v1/exercise_templates` lookup at execution time. If not found in the stock library, create as a custom template via `POST /v1/exercise_templates`.

---

## 7. Hevy account state — pending execution

### Folders (preserved, IDs unchanged)
- `Home` — `240862`
- `BUR` — `1975900`

### Routines

| Title | ID | Folder | Action |
|---|---|---|---|
| Day 1A (Home) | `e90cc7ec-e5a1-4f58-9af9-5e551dd76ea8` | Home | Rewrite in place |
| Day 2A (Home) | `caf5183d-0d7e-4687-b443-dc384e9fcd6e` | Home | Rewrite in place |
| Day 3A (Home) | `1488fcbc-fcad-4b4c-8e5a-8b11510391fd` | Home | Rewrite in place |
| Day 1A (BUR) | `7dfbbfe7-5b6b-477c-9e00-d1500c1e4e67` | BUR | Rewrite in place |
| Day 2A (BUR) | `57f9617a-b2cb-4b2c-8506-2d526b0e8713` | BUR | Rewrite in place |
| Day 3A (BUR) | `5b59e036-9271-4a62-b7dc-a7c2e4af9551` | BUR | Rewrite in place |
| Day 1B (Home) | _to be filled by execution_ | Home | Create |
| Day 2B (Home) | _to be filled by execution_ | Home | Create |
| Day 3B (Home) | _to be filled by execution_ | Home | Create |
| Day 1B (BUR) | _to be filled by execution_ | BUR | Create |
| Day 2B (BUR) | _to be filled by execution_ | BUR | Create |
| Day 3B (BUR) | _to be filled by execution_ | BUR | Create |

### Stale routines to archive (rename to `[ARCHIVE]` prefix; user deletes in app)

| Title | ID | Action |
|---|---|---|
| Full Body 1 | `e92037d2-b707-49cc-8c5b-4250fc0f1b3d` | Rename `[ARCHIVE] Full Body 1`, delete in app |
| Full Body 2 | `ac9a87f6-7f53-4411-955c-4647a7c7e46b` | Rename `[ARCHIVE] Full Body 2`, delete in app |
| Full Body 3 | `ec055913-9697-4495-a05d-c6270c8c4ad4` | Rename `[ARCHIVE] Full Body 3`, delete in app |
| Body weight | `80bf3897-8953-4e01-b96c-948f7a8f4055` | Rename `[ARCHIVE] Body weight`, delete in app |

### Custom exercise templates to delete manually
Hevy public API does **not** support `DELETE` on exercise templates. Delete these in the app: Profile → Exercises → swipe/delete.

- `Face Pull (ELAN)` — `4da56071-81b4-45b8-aea4-0452ffc2b154`
- `Lat Pulldown (Cable) (ELAN)` — `a1c560db-a282-43f1-881e-41271c873d2b`
- `Seated Cable Row - Elan` — `b672c418-efc2-4af1-8e3c-992fa2b2d6e8`
- `Triceps Extension (Cable) (ELAN)` — `86947ea3-34d3-4167-a083-06ecf463581c`
- `Triceps Rope Pushdown (ELAN)` — `b4841559-c2fb-4583-973d-ffd8a47522f7`

No active routine references these after the rewrite — they're inert until you delete.

---

## 8. Operational notes (for future iterations)

### Hevy API surface (what works, what doesn't)
Base URL: `https://api.hevyapp.com`. Auth header: `api-key: <HEVY_API_KEY>`.

| Endpoint | Methods supported |
|---|---|
| `/v1/workouts` | GET, POST |
| `/v1/workouts/{id}` | GET, PUT |
| `/v1/workouts/count` | GET |
| `/v1/routines` | GET, POST |
| `/v1/routines/{id}` | GET, PUT |
| `/v1/routine_folders` | GET, POST |
| `/v1/exercise_templates` | GET, POST |
| `/v1/exercise_templates/{id}` | GET only |

**No DELETE anywhere in the public API.** Renames are the workaround for "delete." Trust `Allow:` response headers, not the CORS preflight — preflight advertises DELETE but endpoints 404.

Default `pageSize` is 10 for paginated endpoints. 429 workouts = 43 pages = 43 round-trips.

### MCP setup
- Server: `chrisdoc/hevy-mcp` (npm `hevy-mcp`, stdio transport)
- Requires Node ≥26 (installed v26.3.1 via nvm 2026-06-20).
- Requires Hevy **Pro** subscription + API key from hevy.com/settings?developer.
- Registered at user scope: `claude mcp add-json -s user hevy '{"type":"stdio","command":"npx","args":["-y","hevy-mcp"]}'`.
- **Env strategy:** No env block in MCP config. Subprocess inherits `HEVY_API_KEY` from the Claude Code parent process at launch. **`HEVY_API_KEY` must be exported in the shell before Claude Code launches** for the MCP to connect. If `claude mcp list` shows hevy ✘ Failed to connect, the env isn't being inherited — export the key and relaunch Claude Code.
- MCP changes do not take effect mid-session; Claude Code must restart to pick up newly-registered servers.

### Key-handling rules
- Do not commit `HEVY_API_KEY` to any chezmoi-tracked dotfile.
- Do not embed in the MCP `env:` config block (file persistence, hard to rotate).
- Preferred: export in current shell when needed; rotate periodically via Hevy settings.

### How to use this file in future sessions
1. Read this `README.md` first — design decisions and current Hevy state.
2. Updating routines: IDs in §7 are stable. Use `PUT /v1/routines/{id}` with `{"routine": {...}}` body.
3. Creating templates: `POST /v1/exercise_templates` with `{"exercise": {"title": ..., "muscle_group": ..., "exercise_type": ..., "equipment_category": ...}}`. Allowed enums returned in the 400 Zod error if you POST `{}`.
4. Set type values: `normal`, `warmup`, `failure`, `dropset`. Working sets are `normal`.
5. After any routine change, update §4 (routines) and §7 (state).
6. Pull fresh workout history: paginate `/v1/workouts?page=N&pageSize=10` until `page == page_count`.

### Open Brain (cross-reference)
After execution, capture three notes:
- Routine design + reasoning (including persona feedback synthesis)
- Key analysis findings (volume targets, imbalances, lean-mass context)
- Hevy MCP wired into Claude Code on MiniM1

---

## 9. Open items not yet merged into the program

1. **Morning readiness log (1–10 + HRV optional)** — Galpin/Norton flagged. Drop one set when red. Not yet wired; revisit after 4 weeks on the new program.
2. **Zone 2 4th session (30–40 min)** — Galpin flagged. Trainee constraint is 3 lifting sessions; consider adding a non-lifting Z2 day if recovery permits.
3. **Heavy strength block** — Tsatsouline's heavy-singles ramp argument is sound but off-phase. Revisit in a future strength-focused mesocycle (4–6 weeks at 5×3–5 on Bench, OHP, RDL).

---

## 10. Change log

- **2026-06-21** — Restructured §4 to one table per day with Home A / Home B / BUR A / BUR B columns. Stripped Elan-era historical narrative from §2. Ran adversarial review against Israetel, Norton, Tsatsouline, Galpin in §5; merged 6 changes (side delts +2 hits, quad isolation slot, BUR hams → Nordic, long-head triceps, heavy calf range, tighter deload), tracked 2 open items (readiness log, Zone 2), rejected 2 with reasoning (collapse variants, strength ramps).
- **2026-06-20** — Initial plan built from 429-workout analysis. Decisions: 3-day rotation × 2 variants × 2 locations; no conventional deadlift (knee); RDL + Hip Thrust + Leg Curl for posterior chain; Belt Squat = cable squat; preserve existing routine IDs; rename floaters to `[ARCHIVE]` for manual deletion.
