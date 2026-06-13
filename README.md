# NCEMS Intubation Guide

Field airway management reference for North Country EMS / Clark Fire District 13 paramedics. Single-file web app — no build step, no dependencies, hosted on GitHub Pages.

**Current version: v2.2**

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
- **Concentrations (Admin)** — tap the version button on the splash to verify drug concentrations + contact info

## Key features

- Weight dosing in **kg (default)** or lbs with quick presets; doses in mL (large, inline) and mg.
- Switching units keeps the entered number (re-label without retyping).
- Ketamine + Rocuronium marked preferred (red-bordered column).
- Tap a med card to log it **GIVEN** with timestamp; multi-dose; running count.
- **Meds Given log** — per-dose timestamps, delete one dose with its x, or Clear All (confirms, then closes).
- **Max-dose warning** (Ketamine/Rocuronium/Etomidate/SUX/Midazolam) — shows ONCE per drug, “Give Dose Anyway” / “Return to Last Page.”
- **Post-intubation re-dose timers** — Fentanyl 5 min, Ketamine 15 min, Midazolam 15 min; blinks when due.
- **3-minute timer met** blinks a “3 MIN MET — PROCEED” notice (DSI + Peds).
- **1-hour session reset** to the warning page; clears prior call’s meds and timers.
- Disclaimer / warning page on first load and each session.
- iPad-optimized large fonts, high-contrast Target Vital Signs buttons, SF Mono numbers.

## Easter egg

Tap anywhere on the splash background 5 times quickly -> a Bigfoot strides across the bottom for 3 seconds.

## Changelog

### v2.2

- **Concentrations page:** added a “Questions, comments, concerns — contact” note with an email link to [d.boyce@northcountryems.org](mailto:d.boyce@northcountryems.org).
- **Concentrations table:** Succinylcholine shortened to **SUX** so columns line up; matching table font.
- **Consistent scroll anchors:** weight-entry auto-scroll and vital-sign-timer-met scroll now use the same anchor/behavior (block:start, 200 ms).
- **Max-dose warning:** now shows only **once per drug** per call. Reworded buttons: **Give Dose Anyway** / **Return to Last Page** (replaces the OS confirm box).
- **Midazolam “?”:** now opens a **red popup box** that closes when you tap anywhere (replaces the inline note).
- (Pending) Bigfoot easter egg upgrade — still the custom SVG; swapping to a better animation when a suitable file is available.

### v2.1

- Concentrations admin page, max-dose warning, single-dose delete in Meds Given, Midazolam concentration “?” toggle, default unit kg, unit-switch keeps number, 3-minute timer-met blink.

### v2.0

- Version checkpoint rolling up v1.6-v1.9: clickable/multi-dose med cards, Meds Given log, Target Vital Signs buttons + auto-scroll, peds DSI integration, disclaimer page, DOPE boxes, walking Bigfoot, 1-hour reset, post-intubation re-dose timers, Midazolam warning, SF Mono font.

## Protocol basis

Built on the **2026 Clark County EMS Patient Care Protocols**. Other agencies may stock different concentrations — verify on the Concentrations page before use.

## Disclaimer

Reference tool only. Does not supersede clinical judgment. Do not work outside your scope of practice. Verify all doses, concentrations, and protocols against your service’s current standards before administration.