# NCEMS Intubation Guide

Field airway management reference for North Country EMS / Clark Fire District 13 paramedics. Single-file web app — no build step, no dependencies, hosted on GitHub Pages.

**Current version: v2.1**

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
1. Open the upload link above in **Safari** (the GitHub app can’t upload files).
1. Tap “choose your files,” pick `index.html`, scroll down, tap **Commit changes**.
1. Confirm the committed file is named exactly `index.html`.

**iOS cache note:** After every deploy, anyone using the home-screen icon must **delete and re-add it** to see the update. Test in plain Safari first.

## Sections

- **DSI** — weight dosing, Target Vital Signs gate, 3-min timer, LEMON, Mallampati, equipment, considerations, DOPE
- **Adult Crash Airway** — weight dosing, failure path, DOPE
- **Peds RSI** — Broselow color-coded ages or length sizing, full dosing, integrated Target Vital Signs + timer
- **Post-Intubation** — Fentanyl / Ketamine / Midazolam with re-dose reminder timers
- **Concentrations (Admin)** — tap the version button on the splash to verify drug concentrations

## Key features

- Weight dosing in **kg (default)** or lbs with quick presets; doses in mL (large, inline) and mg.
- Ketamine + Rocuronium marked preferred (red-bordered column).
- Tap a med card to log it **GIVEN** with timestamp; multi-dose supported; running count.
- **Meds Given log** (pill button top-right) — per-dose timestamps, delete a single dose with its **x** button, or **Clear All** (confirms, then closes).
- **Max-dose warning** — repeat-dosing Ketamine, Rocuronium, Etomidate, Succinylcholine, or Midazolam prompts a confirm showing the protocol max (catches accidental double-taps).
- **Post-intubation re-dose timers** — Fentanyl 5 min, Ketamine 15 min, Midazolam 15 min; card blinks red when due.
- **3-minute timer met** now blinks a green “3 MIN MET — PROCEED” notice (DSI + Peds).
- **1-hour session reset** to the warning page; clears the prior call’s meds and timers.
- Disclaimer / warning page on first load and each session.
- iPad-optimized large fonts, high-contrast Target Vital Signs buttons, SF Mono numbers.

## Easter egg

Tap anywhere on the splash background 5 times quickly -> a Bigfoot strides across the bottom for 3 seconds.

## Changelog

### v2.1

- **Concentrations admin page** — version button on the splash opens a read-only concentration/dose/max table for verification.
- **Max-dose warning** on repeat dosing (Ketamine 200 mg, Rocuronium 300 mg, Etomidate 60 mg, Succinylcholine 300 mg, Midazolam 5 mg/dose) — confirm popup, can still proceed.
- **Meds Given:** delete a single dose with its **x** button; **Clear All** now confirms then closes the log.
- **Midazolam (post):** now shows “Concentration: 1 mg/mL” with a **?** button that reveals the 5 mg / 5 mL protocol warning (was always-on before).
- **Default unit is now kg** on all weight screens (presets show kg).
- **Switching units keeps the entered number** instead of clearing it (re-label/correct a unit without retyping).
- **3-minute timer met** gives a blinking notice, matching the post-intubation re-dose style.

### v2.0

- Version checkpoint rolling up v1.6-v1.9: clickable/multi-dose med cards, Meds Given log, Target Vital Signs high-contrast buttons + auto-scroll, peds DSI integration, disclaimer page, DOPE boxes, walking Bigfoot, 1-hour reset, post-intubation re-dose timers, Midazolam concentration warning, SF Mono font.

## Protocol basis

Built on the **2026 Clark County EMS Patient Care Protocols**. Other agencies may stock different concentrations — verify on the Concentrations page before use.

## Disclaimer

Reference tool only. Does not supersede clinical judgment. Do not work outside your scope of practice. Verify all doses, concentrations, and protocols against your service’s current standards before administration.