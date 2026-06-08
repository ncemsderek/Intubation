# Intubation Guide

A single-file web app for North Country EMS / Clark Fire District 13 crews. Built for the high-stress, low-frequency intubation call where you need the right number on the screen, fast.

**Live:** `https://ncemsderek.github.io/Intubation/`
**Repo:** `https://github.com/ncemsderek/Intubation/`
**Source:** 2026 Clark County EMS Patient Care Protocols

---

## What's in it

Four buttons on the splash. Pick one. Weight is the first thing on every page.

### 1. DSI
The planned advanced airway workflow. Built around resuscitate-before-intubate.

- Patient weight at the top — drives every drug dose below
- V/S targets visible up front: **SpO₂ ≥94%** and **SBP >90 / MAP >65**
- 3-minute countdown timer — start it when both goals are met
- Live mL calculations for Ketamine, Etomidate, Rocuronium, Succinylcholine
- Collapsible sections for Equipment, LEMON Assessment, and Key Considerations
- Button to jump to Post-Intubation (weight carries over)

### 2. Adult Crash Airway
No time. Act now. Patient weight first → four big mL numbers in red.

- Etomidate · Ketamine (induction)
- Succinylcholine · Rocuronium (paralytic)
- Shock half-dose reminder + Sux/Roc contraindications
- Button to jump to Post-Intubation

### 3. Peds RSI
Age-based reference card. Tap an age (TERM through 12 YR) and you get:

- Weight in kg + lbs
- ETT size + length range
- iGel size
- All seven drug doses calculated (Ket, Eto, Midaz, Roc, Sux, post-Ket, post-Fent)

Pulled from the 2026 Pediatric RSI spreadsheet.

### 4. Post-Intubation
Weight at the top, then huge mL numbers for the three sedation/analgesia options.

- **Fentanyl** — 1 mcg/kg, q5–10 min PRN
- **Ketamine** — 1 mg/kg slow push, q15 min PRN
- **Midazolam** — 5 mg fixed dose with weight-based bolus alternative (0.05 mg/kg)
- Concentration warning on Midazolam (1 mg/mL vs 5 mg/mL)
- Full RASS scale in a collapsible at the bottom

---

## How to use it

1. Open the live URL on your phone (or any device)
2. Tap the section you need from the splash
3. Enter or tap a preset for patient weight (lbs or kg)
4. Push the dose displayed in mL — it's already calculated against the right concentration
5. Verify max-dose flags before pushing (warn banner appears at adult ceilings)

**Add to home screen** for one-tap launch:
- iPhone: Safari → Share → Add to Home Screen
- Android: Chrome → ⋮ → Add to Home screen

If you ever see a stale version after an update, delete the home-screen icon and re-add.

---

## Drug reference

All weight-based doses use the concentrations from the 2026 Clark County EMS reference card:

| Drug | Dose | Concentration | Adult Max |
|---|---|---|---|
| Etomidate | 0.3 mg/kg | 2 mg/mL | 60 mg |
| Ketamine (induction) | 1 mg/kg | 50 mg/mL | 200 mg |
| Midazolam (peds induction) | 0.1 mg/kg | 1 mg/mL | — |
| Succinylcholine | 1.5 mg/kg | 20 mg/mL | 300 mg |
| Rocuronium | 1.5 mg/kg | 10 mg/mL | 300 mg |
| Fentanyl (post) | 1 mcg/kg | 50 mcg/mL | 100 mcg |
| Ketamine (post) | 1 mg/kg | 50 mg/mL | 200 mg |
| Midazolam (post, fixed) | 5 mg | verify on bottle | — |

Peds doses are weight-based with no ceiling applied — no pediatric weight in the spreadsheet (TERM through 12 YR / 36 kg) hits the adult max.

---

## Tech notes

- Single HTML file. No build step. No dependencies. No backend.
- Hosted on GitHub Pages.
- Works offline once the page has loaded once.
- Designed for mobile-first use with large tap targets and gloved-hand UX.
- Forest green agency palette with color coding: green (DSI · post-intubation), red (crash), blue (peds).
- No data is sent anywhere. Nothing is stored. Refresh resets state.

---

## ⚠ Clinical use

This app is a **reference tool** designed to support — not replace — clinical judgment, the printed Clark County protocol manual, and medical control.

- Always verify drug concentrations on the actual vial before drawing.
- Cross-check critical doses against your printed reference card.
- Source of truth is the 2026 Clark County EMS Patient Care Protocols (March 2026 revision).
- Report errors to [maintainer / training admin].

---

## Version history

**v1.3** — Splash buttons stripped to bold titles only. Weight is now the first item on every page. "Adult Crash Airway" renamed. DSI page restructured with weight-first and live drug calculations. Trimmed verbose text throughout.

**v1.2** — Added Peds RSI page (age-based, TERM through 12 YR). Added Midazolam card to Post-Intubation with concentration warning.

**v1.1** — Split into four screens (DSI · Crash · Post-Intubation). DSI rebuilt around V/S targets, 3-min timer, and collapsibles for Equipment / LEMON / Considerations. Crash page redesigned with mL-first dose grid.

**v1.0** — Initial build. DSI checklist + Crash dose calculator.

---

## Maintainer

Built for NCEMS / FD13. Contact Doug for changes, errors, or protocol updates.

Backbone source files:
- `2026_Protocols_v1_22.pdf` — Clark County protocols
- `RSI_ADULT_AND_PEDIATRIC_6_2026.xlsx` — Drug concentration / weight reference
- `dsi_rsi_check_list_publisher.pdf` — Existing DSI checklist
