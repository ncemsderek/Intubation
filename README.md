# NCEMS Intubation Guide

Field airway management reference for North Country EMS / Clark Fire District 13 paramedics. Single-file web app — no build step, no dependencies, hosted on GitHub Pages.

**Current version: v2.0**

## Links

- **Live app:** <https://ncemsderek.github.io/Intubation/>
- **Repo:** <https://github.com/ncemsderek/Intubation>
- **Upload new version:** <https://github.com/ncemsderek/Intubation/upload/main>

## Files in this repo

- `index.html` — the entire app (HTML, CSS, JS in one file)
- `NCEMS_logo_transparent.png` — logo backdrop on the splash screen
- `README.md` — this file

## How to deploy an update (iPhone)

1. Save the new `index.html` from Claude to your Files app.
1. Open the upload link above in **Safari** (not the GitHub app — it can’t upload files).
1. Tap “choose your files,” pick `index.html`, scroll down, tap **Commit changes**.
1. Confirm the committed file is named exactly `index.html` (no spaces, no number).

**iOS cache note:** After every deploy, anyone using the home-screen icon must **delete and re-add it** to see the update. Test in plain Safari first to confirm the new version loaded.

## What’s in the app

Four sections from the splash screen:

- **DSI** — Delayed Sequence Intubation: weight-based dosing, Target Vital Signs gate, 3-minute timer, LEMON assessment, Mallampati, equipment checklist, considerations, DOPE troubleshooting
- **Adult Crash Airway** — weight-based dosing, failure path, DOPE
- **Peds RSI** — Broselow color-coded age selection or length-based sizing, full peds dosing, integrated Target Vital Signs + timer
- **Post-Intubation** — Fentanyl / Ketamine / Midazolam dosing with re-dose reminder timers

## Key features

- **Weight-based dosing** in lbs or kg with quick presets; doses shown in mL (large, next to the number) and mg.
- **Ketamine + Rocuronium** marked as preferred (red-bordered column).
- **Tap a med card to log it as given** with a timestamp. Multi-dose supported — tap again to log another dose. Running count on each card.
- **Meds Given log** — red pill button (top right of every page) shows every dose with time. “Clear All” resets for a new call.
- **Post-intubation re-dose timers** — per 2026 Clark County protocol: Fentanyl 5 min, Ketamine 15 min, Midazolam 15 min. Card blinks red when it’s time to reassess.
- **1-hour session reset** — one hour after accepting the warning, the app clears the prior call’s data and returns to the warning page.
- **Disclaimer / warning page** on first load and after each session.
- **iPad-optimized** large fonts and high-contrast Target Vital Signs buttons.

## Easter egg

Tap anywhere on the splash background **5 times quickly** → a Bigfoot strides across the bottom of the screen for 3 seconds, then clears.

## Changelog

### v2.0

- Version checkpoint. Rolls up all changes from the v1.6–v1.9 working sessions into a clean release number.
- Walking Bigfoot easter egg (profile mid-stride, scissoring legs + swinging arms).
- 1-hour session reset to the warning page; clears prior call’s meds and timers.
- Midazolam warning reworded: protocol is based on **5 mg per 5 mL** (1 mg/mL); verify your agency’s concentration.
- Post-intubation re-dose reminder timers with blink (Fentanyl 5 min, Ketamine 15 min, Midazolam 15 min), confirmed against 2026 Clark County protocol.
- SF Mono font throughout (replaced Courier New) for cleaner numbers, especially on iPad.

### v1.6–v1.9 (folded into v2.0)

- Clickable med cards with “GIVEN” timestamp + multi-dose tracking.
- Meds Given log modal with per-dose timestamps and Clear All.
- Target Vital Signs renamed + high-contrast tappable buttons.
- Auto-scroll: weight entry → Target Vital Signs; both VS tapped → timer.
- Peds page integrated with Target Vital Signs + 3-minute timer + post-intubation nav.
- Disclaimer / warning page (does not supersede clinical judgment; scope of practice; verify doses; liability).
- DOPE troubleshooting box on DSI, Crash, and Post-Intubation.
- mL shown inline next to the number; bigger/bolder fonts; iPad media query.

## Protocol basis

Built on the **2026 Clark County EMS Patient Care Protocols**. Drug concentrations and re-dose intervals reflect that document. Other agencies may stock different concentrations — verify before use.

## Disclaimer

This is a reference tool only. It does not supersede clinical judgment. Do not work outside your scope of practice. Verify all doses, concentrations, and protocols against your service’s current standards before administration.