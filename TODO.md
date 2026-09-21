# SkyVega site — status & next steps

First-draft single-page site (`index.html`) for the СКАЙВЕГА consulting
brand, built from copy the founder supplied directly (problem, process,
services, why-us, audiences, team). Everything below is what a fresh
session picking this up should know before touching the file.

## Live now
- Hosted via GitHub Pages from branch `claude/claude-capabilities-setup-kqxpxf`
  (root, single `index.html`, no build step).
- "Обсудить проект" buttons (nav, hero, contact section) open a modal form:
  project description, name/email/phone, referral source, required
  consent checkbox. Submits via FormSubmit.co AJAX.

## Known placeholders — do not treat as real data
- Form target email is `maxim.nebov@googlemail.com` — **test address only**,
  swap for the real company inbox before this goes live for actual clients.
  FormSubmit requires a one-time confirmation click on the target inbox
  after the *first* submission before it forwards anything.
- Contact section email (`info@skyvega.ru`) and Telegram (`@skyvega`) are
  invented placeholders, not real handles — replace before publishing.
- The consent checkbox's "Что это значит?" disclosure is placeholder text,
  not a real privacy policy. Needs an actual policy page/text before this
  is legally meaningful (152-ФЗ data processing consent).
- Insights section has no real content yet (three "материал готовится"
  cards) — founder hasn't provided posts/case studies.

## Open questions for the founder
- Real company email/Telegram/phone for the contact section.
- Actual domain name — user said one is "theoretically" ready but hasn't
  named it. Once given: add `CNAME` file at repo root with the domain,
  set it in GitHub Settings → Pages, and set DNS (4 A records for apex,
  or a CNAME record for a `www` subdomain — see chat history / ask again).
- Whether FormSubmit.co is reliably reachable from Russian ISPs — untested.
  If it turns out to be blocked/flaky, swap to Web3Forms or similar; only
  the `fetch()` URL + hidden fields in the modal's JS need to change.
- Real privacy policy copy for the consent disclosure.

## Design notes (so style stays consistent if extended)
- Dark theme, gold accent (`--accent: #cda45e`), serif headings
  (Playfair Display) + sans body (Manrope), both loaded with Cyrillic
  subset from Google Fonts.
- Single file, no framework, no build step — keep it that way unless the
  site's scope grows enough to justify one.
