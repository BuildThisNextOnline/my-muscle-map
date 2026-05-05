# My Muscle Map (MMM)

**Track your strength across 24 muscle groups — calibrated to your age, sex, and bodyweight.**

Live at → [buildthisnextonline.github.io/my-muscle-map](https://buildthisnextonline.github.io/my-muscle-map)

---

## What it does

My Muscle Map is a single-file, no-backend strength tracking tool. It shows you where every major muscle group stands relative to published strength standards for your demographic — not just your personal best.

You log exercises set by set, and the body map colours each muscle from grey (no data) through red → orange → yellow → green → teal as your strength progresses.

---

## Features

### Body Map
- Anatomical front and back SVG diagrams showing all 24 muscle groups simultaneously
- Each muscle coloured by strength level: No Data / Beginner / Novice / Intermediate / Advanced / Elite
- Click any muscle to see its exercises, 1RM history chart, and all logged sets
- Hover tooltip showing muscle name, current level, and best 1RM

### Strength Scoring
- **Adjusted Epley 1RM** — `weight × (1 + reps/30) × (1 + RIR/30)` — accounts for how close you were to failure
- **Demographic-calibrated thresholds** — every muscle group has its own bodyweight-ratio thresholds, adjusted by:
  - **Sex** — female multiplier: 0.65×
  - **Age bracket** — peak at 25–34, scaling down to 0.68× at 65+
- **Historical accuracy** — each session snapshots your weight and age at that point in time, so past scores never retroactively change

### Workout Logging
- Choose exercise by muscle group or by exercise name (both directions work)
- Log sets one at a time: Type (warm-up / target) · Weight · Reps · RIR (0–4+)
- Edit or delete any set after saving
- End session commits everything and updates the body map instantly

### RIR-based tracking
Instead of always training to failure, you log how many reps you had left in reserve:
- **0 RIR** — hit failure
- **1–2 RIR** — stopped close to limit
- **3+ RIR** — well within capacity

Target sets should land at 0–2 RIR. The app adjusts your 1RM estimate upward for sets with RIR remaining.

### Body Metrics
Log your full body composition data by date (weight, BMI, body fat %, muscle mass, BMR, and more). Used for historical bodyweight lookup when scoring past sessions.

---

## Muscle Groups (24)

| Front | Back |
|---|---|
| Upper Chest | Upper Traps |
| Lower Chest | Lower Traps |
| Front Deltoid | Rear Deltoid |
| Side Deltoid | Lats |
| Biceps | Rhomboids |
| Brachialis | Triceps |
| Forearm Flexors | Forearm Extensors |
| Upper Abs | Erector Spinae |
| Lower Abs | Glutes |
| Obliques | Hamstrings |
| Hip Flexors | Calves |
| Quads | |
| Tibialis Anterior | |

---

## Exercise Library

50+ preset exercises mapped to primary muscle groups, including compound lifts (squat, deadlift, bench, OHP, pull-up) and isolation work across all muscle groups. Scoring applies only to the primary muscle for each exercise — a hammer curl scores brachialis, not biceps.

---

## Profile Setup

On first launch you'll set up your profile:
- **Name** and **biological sex** (used for threshold multiplier)
- **Date of Birth** or **Age** — DOB auto-updates your age bracket each year
- **Weight** — kg or lbs (your choice, per field)
- **Height** — cm or ft/in with half-inch increments

All fields editable anytime via the ⚙ Settings button.

---

## Data & Privacy

All data is stored in your browser's `localStorage`. Nothing is sent to any server. Data persists until you clear your browser data.

**Important:** localStorage is per-device, per-browser. Data logged on your laptop will not appear on your phone, and vice versa.

---

## Tech

Single self-contained HTML file. No framework, no build step, no backend. SVG polygon data sourced from [body-highlighter](https://github.com/NathanaelA/body-highlighter) (MIT licence), with hand-crafted splits for sub-muscle regions.

Analytics via [GoatCounter](https://www.goatcounter.com) — privacy-friendly, no cookies.

---

## Part of BuildThisNextOnline

MMM is one of several single-file tools built under the [BuildThisNextOnline](https://github.com/BuildThisNextOnline) organisation. See also: [CheckMyLounge](https://github.com/BuildThisNextOnline/check-my-lounge) — a card-based airport lounge access checker.
