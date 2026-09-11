# Sonoma Align

A personal phone-sensor wheel-alignment app for James — camber, caster, and toe
measurement using an iPhone's accelerometer/gyroscope, plus a floor-slope
compensation step and vehicle profiles (1999 GMC Sonoma 2WD, Porsche Cayenne,
Toyota Highlander). Nothing to do with trading, algos, or the TradingAlgos repo —
if you're seeing this file, you're in the right, unrelated project.

## What this is

Single-file HTML/CSS/JS app (`index.html`), no build step, no dependencies beyond
two Google Fonts loaded via `<link>`. Deployed as a static site via GitHub Pages.

- Live app: https://hamcowart.github.io/sonoma-align/
- Repo: https://github.com/HamCowart/sonoma-align (branch `main`)
- Edit `index.html` directly, commit, `git push` — Pages redeploys automatically
  within about a minute.

## Working style

- Small, direct edits to the one file. No frameworks, no build tooling — keep it
  that way; the whole point is that it's a page anyone can open and run.
- Before pushing a fix for a sensor/math bug, sanity-check the change makes sense
  by reasoning through the physics/geometry in a comment near the code, the way
  the existing code does (see the header comment block and the flat-check
  rewrite for the style). This app has no unit-test harness on real hardware —
  James is the only tester, so a clear before/after explanation in the commit
  message matters more than usual.
- After pushing, no need to ask before deploying — this is a low-stakes personal
  tool, not shared infrastructure. Just push and tell James what changed.
- Only James has an iPhone to test on — sensor bugs can only really be confirmed
  by him reporting back what he sees on the device.
