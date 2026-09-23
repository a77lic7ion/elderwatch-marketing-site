# ElderWatch — marketing site v2 (working copy)

**Not deployed.** The live site is untouched; this is a separate copy to work on.

Open `index.html` in a browser to preview (double-click it, or `xdg-open index.html`).

## What's here
- `index.html` — the whole site (one file, no build step)
- `assets/` — the logo, plus three crops taken from the **live production dashboard**:
  the five status tiles, the filter row, and the "phone unpaired" screen

## Decisions worth remembering
- **Screens mirror production.** Wording, statuses, tile behaviour and colours are taken
  from the app itself (`AdminPanel.tsx`, `ResidentCheckInScreen.tsx`). Only the DATA is
  invented — example residents, no phone numbers, no internal ids, no home identifiers.
- **No QR codes anywhere.** Linking is the real process: staff generate a one-time pairing
  code, it's verified once on the phone, and the phone locks to that resident.
- **No stack talk.** No mention of the backend, the APK, or any vendor — IP is not on show.
- Crops deliberately exclude: the resident profile form, the resident cards with phone
  numbers, the group overview (internal ids + account email) and the home-screen shot.

## Checks run
- HTML structure validated (balanced tags), all assets present.
- Driven in headless Chromium over the DevTools protocol: alert on tap, tile filtering,
  search, the morning run, and zero JavaScript errors.
- Length: ~6.5 screens / ~975 words, against ~10.2 screens / ~1,300 words for the live site.