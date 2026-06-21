# Hevy Training Plan — Source of Truth

Living document for Dmitry's training program. Captures the analysis behind the design, the actual routines in Hevy, and the operational notes a future iteration needs. Update this file alongside any Hevy change.

- **Owner:** Dmitry (Hevy account)
- **First built:** 2026-06-20
- **Last updated:** 2026-06-20
- **Hevy MCP host:** MiniM1 (Claude Code, stdio transport, `chrisdoc/hevy-mcp`)

---

## 1. Context

### Trainee
- **Phase:** Maintenance / muscle retention. Recently completed ~20 lb fat-loss phase on tirzepatide; now on maintenance dose (~4.2 mg/wk, 5-day cadence).
- **Primary goal:** Hypertrophy + preserve/build lean mass. DEXA history shows ~10.5 lb lean-mass decline during fat loss — this is the deficit to recover.
- **Out of scope for this plan:** Diet, macros, supplementation. Training only.
- **Known constraints:**
  - Bad knee. Avoid heavy axial squat loading and deep knee flexion. No conventional barbell deadlift (technique concern + knee load).
  - RPE is not logged historically (3/7407 sets) — program uses RIR cues + double progression, not RPE prescriptions.

### Equipment

**Home (enclosed garage):**
- Rogue wall-mounted rack (barbell work; assume pull-up bar mounted)
- Regular Olympic barbell + **Swiss bar (multi-grip)**
- Adjustable dumbbells **5–75 lb**
- IronMaster Super Bench
- IronMaster preacher curl attachment
- IronMaster cable tower
- IronMaster leg extension / leg curl attachments (custom Hevy templates: "Leg Extension (Home)", "Lying Leg Curl (Home)")
- Various cable handles (V, rope, rotating, single-arm)

**BUR (Burlingame office gym):**
- Power rack + barbell + plates
- Cable stack / functional trainer
- **Incline leg press** (custom: "Leg Press (Machine) (BUR)")
- Full dumbbell rack going past 75 lb
- **No hamstring curl machine** — hamstring work via RDL/Single-Leg RDL

### Training frequency
- **3 sessions / week.** No fixed schedule for Home vs BUR — chosen ad hoc per day's schedule.
- Demonstrated adherence: ~3.0 sessions/wk consistent over 6+ months, ~12/month average for 2+ years.

---

## 2. Analysis (as of 2026-06-19, n=429 workouts since 2023-03-11)

### Consistency & frequency
- 429 sessions over 170 weeks. Excellent adherence.
- Last 24 weeks: 2–3 sessions/wk, no extended gaps. Soft patch April 2026 (W17–W19, 5–10d gaps) — recovered fully.
- No structured deload pattern visible historically. Now scheduled at 6–8 week intervals (see §5).
- Avg session length last 60d: **94 min**. New design targets ~75–85 min.

### Current de-facto routine (last 60 days, 20 sessions)
Six unique days alternating between Home and BUR folders, equal exercise structure (Days 1/2/3 mirror across both). Approximate exercise list per day:
- **Day One:** Bench, leg curl, DB row, lat raise, hammer curl, tri pushdown
- **Day Two:** Incl bench, deadlift, lat pulldown¹, DB OHP, hammer curl, tri ext
- **Day Three:** Chest fly, Bulgarian split squat, V-grip row¹, OHP, bicep curl, tri ext

¹Cable-based items hadn't been performed at home recently — the IronMaster cable tower arrival fixes that.

### Weekly hard sets per muscle (last 8 weeks, primary + 0.5×secondary)

| Muscle | Sets/wk (old) | Sets/wk (new target) | Verdict |
|---|---|---|---|
| Chest | 7.9 | **10** | New plan: bench + incl + fly |
| Shoulders (side) | 8.8 (combined) | **6 direct + carryover** | Lat raise ×2 days |
| Biceps | 8.8 | 6+ direct + carryover | Reduced direct (was bicep-heavy) |
| Triceps | 7.6 | **9** effective | Pushdown + OH ext + press carryover |
| Quadriceps | 6.0 | 6 direct + carryover | Knee-friendly: BSS, leg ext, leg press |
| Lats | 5.5 | **9** | Pulldown ×2 + DB row |
| Upper back | 4.4 | **9** | Seated row + DB row + rear delt fly |
| Hamstrings | **1.8** ← gap | 6 | RDL + leg curl/single-leg RDL |
| Glutes | **1.2** ← gap | **9** | RDL + Hip Thrust + BSS |
| Calves | **0.5** ← gap | 6 | Day A + Day B |
| Abs | **0.8** ← gap | 6 | Knee Raise + Cable Crunch |

### Imbalances flagged and addressed

1. **Posterior chain neglected** — barbell squat unperformed 473d, deadlift 12+ weeks. → New plan replaces with RDL + Hip Thrust + Leg Curl. No conventional deadlift due to knee/technique.
2. **No calves, no direct ab/core** → Added to two days each.
3. **No vertical pull at home** (Lat Pulldown was 100-session staple, last 68d ago) → IronMaster cable tower now solves at home. Lat Pulldown on Day A wide grip + Day C close grip.
4. **No rear delt isolation** → Rear Delt Reverse Fly on Day C.
5. **Bicep > tricep direct work imbalance** → Rebalanced.

### Progression — last 12 weeks (top-set est-1RM, Epley)

**Improving:** Bench Press +6.9%, Incl Bench +2.9%, DB Row +6%, Chest Fly +16%, Lat Raise +32% (small-number effect).
**Stalled:** Overhead Press 0%, Tri Ext 0%, V-grip Row 0%.
**Regressing:** DB Shoulder Press −4%, Lying Leg Curl −8%.

Peak lifts late-2024 / early-2025 sit ~15–25% above current — consistent with documented fat-loss + lean-mass decline. Floor holding; bench rebuilding. Good.

### Movements dropped (used 15+ times historically, gone now — mostly Elan leftovers)

- Lat Pulldown (Cable) Elan — 100 sessions, 68d ago
- Bent Over Row (Barbell) — 58 sessions, 72d ago
- Leg Press — 64 sessions, 72d ago
- Incline Bench Press (Dumbbell) — 46 sessions, 60d ago
- Triceps Extension (Cable) — 50 sessions, 212d ago
- Bicep Curl (Barbell) — 46 sessions, 527d ago
- **Squat (Barbell) — 31 sessions, 473d ago** (permanently retired)
- Preacher Curl (Barbell) — 34 sessions, 280d ago
- Deadlift (Dumbbell) — 31 sessions, 85d ago

### Data hygiene notes

- 7,257/7,407 sets logged as `type=normal`; only 150 warmup. No dropsets/failure/AMRAP markers.
- One outlier ignored: Dumbbell Row 2024-05-31, logged 2472 kg × 12 (decimal/unit typo).

---

## 3. Program design

### Architecture
**3 days × 2 variants × 2 locations = 12 routines.**

Each "Day N" is a hypertrophy target (push+hinge / OHP+quad / pull+posterior+arms). Variant A is the heavier-compound baseline; Variant B rotates the equipment/angles for variety while hitting the same muscle volume.

User trains 3×/wk, picking any single variant of Day 1, Day 2, Day 3 per week — Home or BUR is decided ad hoc based on schedule.

### Weekly volume per major muscle (achieved across either A or B variants)

| Muscle | Sets/wk | Source |
|---|---|---|
| Chest | 10 | Bench, Incl Bench, Fly |
| Lats | 9 | Lat Pulldown wide, Lat Pulldown close, DB Row |
| Upper back | 9 | Seated Row, DB Row, Rear Delt Fly |
| Side delts | 6 + carryover | Lat Raise Day 1 + Day 2 |
| Quads | 6 direct + DL/squat carryover | BSS or Cable Sq, Leg Ext/Press |
| Hamstrings | 6 | RDL + Leg Curl (or single-leg RDL) |
| Glutes | 9 | RDL + Hip Thrust + BSS |
| Biceps | 6+ direct + pull carryover | Preacher/Cable curl Day 3 |
| Triceps | 9 effective | Pushdown D2 + OH ext D3 + press carryover |
| Calves | 6 | Day 1 + Day 2 |
| Abs | 6 | Knee Raise D1 + Cable Crunch D3 |

### Progression scheme (encoded in routine notes)

**Double progression.**
1. Start at the **bottom** of the rep range with a weight finishable at all sets at RIR 2.
2. Each session, add 1 rep per set when possible.
3. When all sets hit the **top** of the range: next session **add 2.5 kg** (BB) / **5 lb** (DB), drop back to bottom of range.
4. Stop sets at **RIR 1–2**. Don't grind to failure on compounds.

### Deload protocol (in routine notes)

Every **6–8 weeks**, or when 2+ exercises stall for 2 consecutive sessions: **one light week.**
- Top-set weight × **0.6**
- **2 sets** per exercise instead of 3
- Same rep target, smooth bar speed
- Resume normal loads next week.

---

## 4. The 12 routines

Templates referenced by Hevy `exercise_template_id`. Sets×Reps target shown as "S×R-R". Rest in seconds.

### Day 1 — Press + Hinge + Vertical Pull

#### Day 1A (heavy compound)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Horizontal press | Bench Press (BB) | `79D0BB3A` | Bench Press (BB) | `79D0BB3A` | 4×6–8 | 180 |
| 2 | Hip hinge | Romanian Deadlift (BB) | `2B4B7310` | Romanian Deadlift (BB) | `2B4B7310` | 3×8–10 | 150 |
| 3 | Vertical pull (wide) | Lat Pulldown (Cable) | `6A6C31A5` | Lat Pulldown (Cable) (BUR) | `36548ca5-cd4d-4c26-9c8b-58540e6b2c97` | 3×8–10 | 120 |
| 4 | Quad single-leg | Bulgarian Split Squat | `B5D3A742` | Bulgarian Split Squat | `B5D3A742` | 3×8–10/side | 120 |
| 5 | Side delts | Lateral Raise (DB) | `422B08F1` | Lateral Raise (DB) | `422B08F1` | 3×12–15 | 75 |
| 6 | Calves | Standing Calf Raise | `06745E58` | Standing Calf Raise | `06745E58` | 3×12–15 | 90 |
| 7 | Abs | Hanging Knee Raise | `08590920` | Hanging Knee Raise | `08590920` | 3×10–15 | 60 |

#### Day 1B (Swiss bar / DB / cable variety)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Horizontal press | Swiss Bench Press | `8b6558c7-d41b-4a26-afdb-6bb285f31df6` | Bench Press (DB) (use heavy DBs) | use stock `Bench Press (Dumbbell)` lookup | 4×8–10 | 150 |
| 2 | Hip hinge | Romanian Deadlift (DB) | `72CFFAD5` | Romanian Deadlift (DB) | `72CFFAD5` | 3×10–12 | 120 |
| 3 | Vertical pull (reverse) | Reverse Grip Lat Pulldown (Cable) | `046E25A2` | Reverse Grip Lat Pulldown (Cable) | `046E25A2` | 3×10–12 | 120 |
| 4 | Quad (cable squat) | Belt Squat | `e05d4883-21c8-4e27-abe2-d727abed2715` | Split Squat (DB) | `20C1A3CB` | 3×10–12 | 120 |
| 5 | Side delts | Lateral Raise (DB) cable variant | `422B08F1` | Lateral Raise (DB) cable variant | `422B08F1` | 3×12–15 | 60 |
| 6 | Calves | Standing Calf Raise (Dumbbell) | `6DA40660` | Standing Calf Raise (Dumbbell) | `6DA40660` | 3×12–15 | 90 |
| 7 | Abs | Ab Wheel | `99D5F10E` | Ab Wheel | `99D5F10E` | 3×8–12 | 60 |

### Day 2 — OHP + Quad + Horizontal Pull

#### Day 2A (BB OHP focus)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Vertical press | Overhead Press (BB) | `7B8D84E8` | Overhead Press (BB) | `7B8D84E8` | 4×6–8 | 180 |
| 2 | Horizontal pull | Seated Cable Row – V Grip | `0393F233` | Seated Cable Row – V Grip | `0393F233` | 3×10–12 | 120 |
| 3 | Incline press | Incline Bench Press (BB) | `50DFDFAB` | Incline Bench Press (BB) | `50DFDFAB` | 3×8–10 | 150 |
| 4 | Quad (knee-safe) | Leg Extension (Home) | `d2db4633-eda0-4a53-9eb3-4b604e7d9ad8` | Leg Press (Machine) (BUR) | `78581019-7446-44be-bda6-83feb96f5352` | 3×10–12 | 120 |
| 5 | Side delts | Lateral Raise (DB) | `422B08F1` | Lateral Raise (DB) | `422B08F1` | 3×12–15 | 75 |
| 6 | Triceps | Triceps Rope Pushdown | `94B7239B` | Triceps Rope Pushdown (BUR) | `b1e50859-2ce0-4d97-9d17-3a25ac3677cb` | 3×10–12 | 75 |
| 7 | Calves | Standing Calf Raise (DB) | `6DA40660` | Calf Press (Machine) | `91237BDD` | 3×12–15 | 90 |

#### Day 2B (DB shoulder / cable variety)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Vertical press | Shoulder Press (DB) | `878CD1D0` | Arnold Press (DB) | `A69FF221` | 4×8–10 | 150 |
| 2 | Horizontal pull | Seated Cable Row – Bar Wide Grip | `C3BCABB3` | Seated Cable Row – Bar Wide Grip | `C3BCABB3` | 3×10–12 | 120 |
| 3 | Incline press | Swiss Bar Incline | `5f7bbdab-4cc9-4389-bfac-f32d30efac6d` | Incline Bench Press (DB) | `07B38369` | 3×10–12 | 120 |
| 4 | Quad (cable squat) | Belt Squat | `e05d4883-21c8-4e27-abe2-d727abed2715` | Belt Squat | `e05d4883-21c8-4e27-abe2-d727abed2715` | 3×10–12 | 120 |
| 5 | Side delts | Lateral Raise (DB) | `422B08F1` | Lateral Raise (DB) | `422B08F1` | 3×12–15 | 60 |
| 6 | Triceps | Triceps Pushdown | `93A552C6` | Triceps Pushdown | `93A552C6` | 3×10–12 | 75 |
| 7 | Calves | Single Leg Standing Calf Raise (DB) | `5DA40761` | Single Leg Standing Calf Raise (DB) | `5DA40761` | 3×12–15 | 90 |

### Day 3 — Pull + Posterior + Arms

#### Day 3A (heavier, IronMaster preacher)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Vertical pull (close) | Lat Pulldown – Close Grip | `4E5257DE` | Lat Pulldown – Close Grip | `4E5257DE` | 3×8–10 | 120 |
| 2 | Glute primary | Hip Thrust (BB) | `D57C2EC7` | Hip Thrust (BB) | `D57C2EC7` | 3×8–12 | 150 |
| 3 | Hamstrings | Lying Leg Curl (Home) | `322a9e07-47b6-4eca-af22-7786a2ad9e48` | Single Leg Romanian Deadlift (DB) | `937292AB` | 3×10–12 | 90 |
| 4 | Horizontal pull #2 | Dumbbell Row | `F1E57334` | Dumbbell Row | `F1E57334` | 3×8–10 | 120 |
| 5 | Rear delts | Rear Delt Reverse Fly (DB) | `E5988A0A` | Rear Delt Reverse Fly (Cable) | `C315DC2A` | 3×12–15 | 60 |
| 6 | Biceps | Preacher Curl (DB) — IronMaster | `FAB6EB2F` | Bicep Curl (Cable) | `ADA8623C` | 3×10–12 | 75 |
| 7 | Triceps | Overhead Triceps Extension (Cable) | `B5EFBF9C` | Overhead Triceps Extension (Cable) | `B5EFBF9C` | 3×10–12 | 75 |
| 8 | Abs | Cable Crunch | `23A48484` | Cable Crunch | `23A48484` | 3×12–15 | 60 |

#### Day 3B (cable variety + skullcrusher)

| # | Slot | Exercise (Home) | ID (Home) | Exercise (BUR) | ID (BUR) | S×R | Rest |
|---|---|---|---|---|---|---|---|
| 1 | Vertical pull (stretch) | Straight Arm Lat Pulldown (Cable) | `D2387AB1` | Straight Arm Lat Pulldown (Cable) | `D2387AB1` | 3×10–12 | 90 |
| 2 | Glute primary | Single Leg Hip Thrust (DB) | `D1CD146F` | Hip Thrust (Machine) | `68CE0B9B` | 3×10–12/side | 120 |
| 3 | Hamstrings | Standing Leg Curls | `6120CAAB` | Single Leg Romanian Deadlift (DB) | `937292AB` | 3×10–12 | 90 |
| 4 | Horizontal pull #2 | Dumbbell Row | `F1E57334` | Single Arm Cable Row | `D0C4A899` | 3×10–12 | 90 |
| 5 | Rear delts | Face Pull | `BE640BA0` | Face Pull (BUR) | `dcb574e5-54da-4d09-bb32-7a13e9940bea` | 3×12–15 | 60 |
| 6 | Biceps | Cross Body Hammer Curl | `32C4D4A2` | Hammer Curl (Cable) | `36E8F14E` | 3×10–12 | 75 |
| 7 | Triceps | Skullcrusher (BB) — Swiss bar | `875F585F` | Skullcrusher (BB) | `875F585F` | 3×10–12 | 90 |
| 8 | Abs | Hanging Leg Raise | `F8356514` | Hanging Leg Raise | `F8356514` | 3×10–15 | 60 |

### Master template ID reference (quick lookup)

| Title | ID | Custom? |
|---|---|---|
| Belt Squat (= cable squat) | `e05d4883-21c8-4e27-abe2-d727abed2715` | yes |
| Bench Press (Barbell) | `79D0BB3A` | |
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
| Single Arm Lat Pulldown | `2EE45F81` | |
| Single Leg Hip Thrust (Dumbbell) | `D1CD146F` | |
| Single Leg Romanian Deadlift (Dumbbell) | `937292AB` | |
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

---

## 5. Hevy account state — what we changed and what we left

### Folders (preserved, IDs unchanged)
- `Home` — `240862`
- `BUR` — `1975900`

### Routines

| Title | ID | Folder | Action |
|---|---|---|---|
| Day 1A (Home) | `e90cc7ec-e5a1-4f58-9af9-5e551dd76ea8` | Home | Renamed from "Day One (Home)" + rewritten |
| Day 2A (Home) | `caf5183d-0d7e-4687-b443-dc384e9fcd6e` | Home | Renamed from "Day Two (Home)" + rewritten |
| Day 3A (Home) | `1488fcbc-fcad-4b4c-8e5a-8b11510391fd` | Home | Renamed from "Day Three (Home)" + rewritten |
| Day 1A (BUR) | `7dfbbfe7-5b6b-477c-9e00-d1500c1e4e67` | BUR | Renamed from "Day One (BUR)" + rewritten |
| Day 2A (BUR) | `57f9617a-b2cb-4b2c-8506-2d526b0e8713` | BUR | Renamed from "Day Two (BUR)" + rewritten |
| Day 3A (BUR) | `5b59e036-9271-4a62-b7dc-a7c2e4af9551` | BUR | Renamed from "Day Three (BUR)" + rewritten |
| Day 1B (Home) | _to be filled by execution_ | Home | Created |
| Day 2B (Home) | _to be filled_ | Home | Created |
| Day 3B (Home) | _to be filled_ | Home | Created |
| Day 1B (BUR) | _to be filled_ | BUR | Created |
| Day 2B (BUR) | _to be filled_ | BUR | Created |
| Day 3B (BUR) | _to be filled_ | BUR | Created |
| [ARCHIVE] Full Body 1 | `e92037d2-b707-49cc-8c5b-4250fc0f1b3d` | (no folder) | Renamed; user to delete in app |
| [ARCHIVE] Full Body 2 | `ac9a87f6-7f53-4411-955c-4647a7c7e46b` | (no folder) | Renamed; user to delete in app |
| [ARCHIVE] Full Body 3 | `ec055913-9697-4495-a05d-c6270c8c4ad4` | (no folder) | Renamed; user to delete in app |
| [ARCHIVE] Body weight | `80bf3897-8953-4e01-b96c-948f7a8f4055` | (no folder) | Renamed; user to delete in app |

### Custom exercise templates left for manual cleanup
Hevy public API does **not** support `DELETE` on exercise templates. Delete these in the Hevy app: Profile → Exercises → swipe/delete:

- `Face Pull (ELAN)` — `4da56071-81b4-45b8-aea4-0452ffc2b154`
- `Lat Pulldown (Cable) (ELAN)` — `a1c560db-a282-43f1-881e-41271c873d2b`
- `Seated Cable Row - Elan` — `b672c418-efc2-4af1-8e3c-992fa2b2d6e8`
- `Triceps Extension (Cable) (ELAN)` — `86947ea3-34d3-4167-a083-06ecf463581c`
- `Triceps Rope Pushdown (ELAN)` — `b4841559-c2fb-4583-973d-ffd8a47522f7`

No active routine references these after the rewrite — they're inert until you delete.

---

## 6. Operational notes (for future iterations)

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

**No DELETE anywhere in the public API.** Renames are the workaround for "delete." `Allow:` headers responded by the server are the source of truth — don't trust the CORS preflight (it allows DELETE in CORS but the endpoints 404).

Default `pageSize` is 10 for paginated endpoints; max likely 10 (untested above). 429 workouts = 43 pages = 43 round-trips.

### MCP setup
- Server: `chrisdoc/hevy-mcp` (npm `hevy-mcp`, stdio transport)
- Requires Node ≥26 (installed v26.3.1 via nvm 2026-06-20).
- Requires Hevy **Pro** subscription + API key from hevy.com/settings?developer.
- Registered at user scope: `claude mcp add-json -s user hevy '{"type":"stdio","command":"npx","args":["-y","hevy-mcp"]}'`.
- **Env strategy:** No env block in MCP config. The subprocess inherits `HEVY_API_KEY` from the Claude Code parent process at launch. **This means** `HEVY_API_KEY` **must be exported in the shell before Claude Code launches** for the MCP to connect. If `claude mcp list` shows hevy ✘ Failed to connect, the env isn't being inherited — export the key and relaunch Claude Code.
- MCP changes do not take effect mid-session; Claude Code must restart to pick up newly-registered servers.

### Key-handling rules
- Do not commit `HEVY_API_KEY` to any chezmoi-tracked dotfile.
- Do not embed in the MCP `env:` config block (file persistence, hard to rotate).
- Preferred: export in current shell when needed; rotate periodically via Hevy settings.

### How to use this file in future sessions
1. Read this `README.md` first — it captures all design decisions and the current Hevy state.
2. If updating routines: the IDs above are stable. Use `PUT /v1/routines/{id}` with `{"routine": {...}}` body.
3. If creating new templates: `POST /v1/exercise_templates` with `{"exercise": {"title": ..., "muscle_group": ..., "exercise_type": ..., "equipment_category": ...}}`. Allowed enums are returned in the 400 Zod error if you POST `{}`.
4. Set type valid values: `normal`, `warmup`, `failure`, `dropset`. All working sets are `normal`.
5. After any routine change here or in Hevy, update §4 (routines) and §5 (state).
6. To pull current workout history fresh for re-analysis: paginate `/v1/workouts?page=N&pageSize=10` until `page == page_count`.

### Open Brain — captured findings (cross-reference)
After this plan was finalized, the following notes were captured to Open Brain as standalone references:
- Routine design + reasoning
- Key analysis findings (imbalances, stalls, lean-mass context)
- Hevy MCP wired into Claude Code on MiniM1

---

## 7. Change log

- **2026-06-20** — Initial plan built from 429-workout analysis. Decisions: 3-day rotation × 2 variants × 2 locations; no conventional deadlift (knee); RDL + Hip Thrust + Leg Curl for posterior chain; Belt Squat = cable squat; preserve existing routine IDs; rename floaters to `[ARCHIVE]` for manual deletion.
