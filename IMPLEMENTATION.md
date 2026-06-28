# Hevy Implementation Notes

Operational reference for working with the Hevy account, the API, the MCP integration, and account-state cleanup. The training program itself lives in [README.md](./README.md) — this file exists only so that file can stay about the program.

- **Last updated:** 2026-06-21

---

## 1. Hevy account state

### Folders
| Title | ID |
|---|---|
| Home | `240862` |
| BUR | `1975900` |
| Travel | `3124163` |

### Travel routines
| Title | ID | Folder | Notes |
|---|---|---|---|
| Hotel (Travel) | `88260512-0cb4-4153-960a-a97ecabc43fe` | Travel | Combined single routine; 6 "choose-one" superset pairs (DB or cable) + 4 fixed DB singles |
| [ARCHIVE] Hotel 2 (merged) | `98c592d6-9cc0-4594-a3c4-52fa52e56ae1` | Travel | Merged into Hotel (Travel); delete in app |

### Routines

| Title | ID | Folder | Status |
|---|---|---|---|
| Day 1A (Home) | `e90cc7ec-e5a1-4f58-9af9-5e551dd76ea8` | Home | Rewritten in place ✓ |
| Day 2A (Home) | `caf5183d-0d7e-4687-b443-dc384e9fcd6e` | Home | Rewritten in place ✓ |
| Day 3A (Home) | `1488fcbc-fcad-4b4c-8e5a-8b11510391fd` | Home | Rewritten in place ✓ |
| Day 1A (BUR) | `7dfbbfe7-5b6b-477c-9e00-d1500c1e4e67` | BUR | Rewritten in place ✓ |
| Day 2A (BUR) | `57f9617a-b2cb-4b2c-8506-2d526b0e8713` | BUR | Rewritten in place ✓ |
| Day 3A (BUR) | `5b59e036-9271-4a62-b7dc-a7c2e4af9551` | BUR | Rewritten in place ✓ |
| Day 1B (Home) | `3a9e4154-ba85-44df-a297-371a373b58b1` | Home | Created |
| Day 2B (Home) | `5484feba-81bf-45e2-92b9-69fd33aadaa6` | Home | Created |
| Day 3B (Home) | `c78697f9-d862-4943-9382-19c296ae1726` | Home | Created |
| Day 1B (BUR) | `6828bec5-c90b-49f9-8d04-93a4a626a5bd` | BUR | Created |
| Day 2B (BUR) | `96e333e3-0411-4023-8358-d0d6c5a84c80` | BUR | Created |
| Day 3B (BUR) | `1aa1500a-23d8-44cc-9893-717d8d28cabf` | BUR | Created |

### Stale routines — archived ✓ (delete in app)
Hevy's API doesn't support routine `DELETE`. These were renamed with the `[ARCHIVE]` prefix via `PUT`. **You delete them in the app** (long-press → delete).

| Title | ID |
|---|---|
| [ARCHIVE] Full Body 1 | `e92037d2-b707-49cc-8c5b-4250fc0f1b3d` |
| [ARCHIVE] Full Body 2 | `ac9a87f6-7f53-4411-955c-4647a7c7e46b` |
| [ARCHIVE] Full Body 3 | `ec055913-9697-4495-a05d-c6270c8c4ad4` |

> **Body weight** (`80bf3897-…`) is kept by the trainee's choice — not archived.

### Custom exercise templates to delete manually
`DELETE /v1/exercise_templates/{id}` does not exist. Delete these in-app (Profile → Exercises → swipe/delete). No active routine references them after the rewrite.

| Title | ID |
|---|---|
| Face Pull (ELAN) | `4da56071-81b4-45b8-aea4-0452ffc2b154` |
| Lat Pulldown (Cable) (ELAN) | `a1c560db-a282-43f1-881e-41271c873d2b` |
| Seated Cable Row - Elan | `b672c418-efc2-4af1-8e3c-992fa2b2d6e8` |
| Triceps Extension (Cable) (ELAN) | `86947ea3-34d3-4167-a083-06ecf463581c` |
| Triceps Rope Pushdown (ELAN) | `b4841559-c2fb-4583-973d-ffd8a47522f7` |

---

## 2. Exercise template ID lookup

Used by the routine tables in `README.md` §4. If a template isn't found at execution time, create it via `POST /v1/exercise_templates` (see §3 for the schema) and record the new ID here.

| Title | ID | Custom? |
|---|---|---|
| Belt Squat (= cable squat) | `e05d4883-21c8-4e27-abe2-d727abed2715` | yes |
| Bench Press (Barbell) | `79D0BB3A` | |
| Bench Press (Dumbbell) | `3601968B` | (was wrongly `D04AC939` = Squat (Barbell)) |
| Bicep Curl (Cable) | `ADA8623C` | |
| Bicep Curl (Dumbbell) | `37FCC2BB` | |
| Bulgarian Split Squat | `B5D3A742` | |
| Cable Crunch | `23A48484` | |
| Chest Fly (Dumbbell) | `12017185` | |
| Cross Body Hammer Curl | `32C4D4A2` | |
| Crunch (Weighted) | `D928C232` | travel abs |
| Dumbbell Row | `F1E57334` | one-arm row (travel) |
| Dumbbell Step Up | `BF6ECE89` | travel single-leg |
| Face Pull | `BE640BA0` | |
| Farmers Walk | `50C613D0` | (dropped from v5 travel) |
| Pullover (Dumbbell) | `67280085` | travel vertical pull (Setup 1) |
| Seated Incline Curl (Dumbbell) | `8BAB2735` | = Incline Curl |
| Skullcrusher (Dumbbell) | `68F8A292` | travel triceps |
| Face Pull (BUR) | `dcb574e5-54da-4d09-bb32-7a13e9940bea` | yes |
| Glute Kickback (Cable) | `ACB2751D` | stock "Standing Cable Glute Kickbacks" |
| Cable Pull-Through | `8C331CD8` | stock "Cable Pull Through" |
| Hammer Curl (Cable) | `36E8F14E` | |
| Hammer Curl (Dumbbell) | `7E3BC8B6` | |
| Standing Leg Curl (Cable) — BUR hams | `6120CAAB` | stock "Standing Leg Curls"; done with cable + ankle strap |
| Hanging Knee Raise | `08590920` | |
| Hanging Leg Raise | `F8356514` | |
| Incline Bench Press (Barbell) | `50DFDFAB` | |
| Incline Bench Press (Dumbbell) | `07B38369` | |
| Incline Curl (Dumbbell) | `8BAB2735` | stock "Seated Incline Curl (Dumbbell)" |
| Lat Pulldown (Cable) | `6A6C31A5` | |
| Lat Pulldown (Cable) (BUR) | `36548ca5-cd4d-4c26-9c8b-58540e6b2c97` | yes |
| Lat Pulldown – Close Grip (Cable) | `4E5257DE` | |
| Lateral Raise (Cable) | `BE289E45` | |
| Lateral Raise (Dumbbell) | `422B08F1` | |
| Leg Extension (Home) | `d2db4633-eda0-4a53-9eb3-4b604e7d9ad8` | yes |
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
| Single Leg Romanian Deadlift (Dumbbell) | `937292AB` | |
| Single Leg Standing Calf Raise (Dumbbell) | `5DA40761` | |
| Skullcrusher (Barbell) | `875F585F` | |
| Spider Curl (Dumbbell) | `90427D4A` | |
| Split Squat (Dumbbell) | `20C1A3CB` | |
| Standing Calf Raise | `06745E58` | |
| Standing Calf Raise (Dumbbell) | `6DA40660` | |
| Straight Arm Lat Pulldown (Cable) | `D2387AB1` | |
| Swiss Bar Incline | `5f7bbdab-4cc9-4389-bfac-f32d30efac6d` | yes |
| Swiss Bench Press | `8b6558c7-d41b-4a26-afdb-6bb285f31df6` | yes |
| Trap Bar Deadlift | `B923B230` | stock "Deadlift (Trap bar)"; BUR only |
| Triceps Pushdown | `93A552C6` | |
| Triceps Rope Pushdown | `94B7239B` | |
| Triceps Rope Pushdown (BUR) | `b1e50859-2ce0-4d97-9d17-3a25ac3677cb` | yes |

> **No custom exercises need to be created.** Every movement maps to a stock Hevy template or one of the trainee's existing customs (marked "yes"). IDs above were resolved against the cached full template list (452 templates pulled 2026-06-20). Re-verify against the live `/v1/exercise_templates` at execution in case the library changed.

---

## 3. Hevy API

Base URL: `https://api.hevyapp.com`.
Auth header: `api-key: <HEVY_API_KEY>`.

### Endpoint surface

| Endpoint | Methods |
|---|---|
| `/v1/workouts` | GET, POST |
| `/v1/workouts/{id}` | GET, PUT |
| `/v1/workouts/count` | GET |
| `/v1/routines` | GET, POST |
| `/v1/routines/{id}` | GET, PUT |
| `/v1/routine_folders` | GET, POST |
| `/v1/exercise_templates` | GET, POST |
| `/v1/exercise_templates/{id}` | GET only |

**No DELETE anywhere in the public API.** Workarounds:
- Routines → rename with `[ARCHIVE]` prefix, then delete in-app.
- Exercise templates → no rename trick (won't free the slot from routines that reference them); delete in-app.

Trust the `Allow:` response header, not the CORS preflight. Preflight advertises `DELETE` but every endpoint 404s on it.

### Pagination
- Default `pageSize = 10`.
- 429 workouts = 43 pages = 43 round-trips for a full backfill.
- Loop: `for p in 1..page_count: GET /v1/workouts?page=$p&pageSize=10`.

### Routine update payload
```
PUT /v1/routines/{id}
{
  "routine": {
    "title": "Day 1A (Home)",
    "folder_id": 240862,
    "notes": "...",
    "exercises": [
      {
        "exercise_template_id": "79D0BB3A",
        "sets": [
          { "type": "normal", "weight_kg": null, "reps": null, "rest_seconds": 180 },
          ...
        ]
      },
      ...
    ]
  }
}
```

### Exercise template create payload
```
POST /v1/exercise_templates
{
  "exercise": {
    "title": "Incline Curl (Dumbbell)",
    "muscle_group": "biceps",
    "exercise_type": "weight_reps",
    "equipment_category": "dumbbell"
  }
}
```

Allowed enums (`muscle_group`, `exercise_type`, `equipment_category`) are returned in the 400 Zod error if you POST `{}`.

### Set types
Valid `type` values: `normal`, `warmup`, `failure`, `dropset`. All working sets use `normal`.

---

## 4. MCP setup (chrisdoc/hevy-mcp on MiniM1)

- npm: `hevy-mcp`
- Transport: stdio
- Node requirement: **≥ 26** (installed v26.3.1 via nvm on 2026-06-20)
- Hevy requirement: **Pro** subscription + API key from hevy.com/settings?developer

### Registration
```
claude mcp add-json -s user hevy '{"type":"stdio","command":"npx","args":["-y","hevy-mcp"]}'
```

(Avoid `claude mcp add ... -e KEY=val` — known bug.)

### Env strategy
- **No env block in the MCP config.** The subprocess inherits `HEVY_API_KEY` from the Claude Code parent process at launch.
- `HEVY_API_KEY` must be exported in the shell **before** Claude Code launches for the MCP to connect.
- If `claude mcp list` shows hevy ✘ Failed to connect, the env isn't being inherited → export the key and relaunch Claude Code.
- MCP changes do not take effect mid-session; Claude Code must restart to pick up newly-registered servers.

### Key-handling rules
- Do not commit `HEVY_API_KEY` to any chezmoi-tracked dotfile.
- Do not embed in the MCP `env:` config block (file persistence; hard to rotate).
- Export in the current shell when needed; rotate periodically via Hevy settings.

---

## 5. How to use this repo in future sessions

1. Read `README.md` first — design and program state.
2. This file for any Hevy mechanics: account state, IDs, API, MCP.
3. Updating routines: IDs in §1 are stable; `PUT /v1/routines/{id}`.
4. Creating templates: `POST /v1/exercise_templates` (schema in §3).
5. After any routine change, update `README.md` §4 AND this file's §1.
6. Fresh workout history pull: paginate `/v1/workouts?page=N&pageSize=10` until `page == page_count`.

---

## 6. Open Brain cross-reference

After execution, capture three notes to Open Brain:
- Routine design + reasoning (including the v1/v2 adversarial review synthesis)
- Key analysis findings (volume targets, imbalances, lean-mass context)
- Hevy MCP wired into Claude Code on MiniM1

---

## 7. Change log

- **2026-06-21** — Split from `README.md` so the README stays about the program. Added `Incline Curl (Dumbbell)` and `Nordic Hamstring Curl` as placeholder template IDs for execution-time resolution.
- **2026-06-20** — Initial: API surface, MCP setup, account state, template lookup.
