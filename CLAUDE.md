# Arkana Fantastic Four — Time Planner

## About the user (important — read first)
Sean is new to coding, git, and the terminal. This project is partly a learning
exercise. Always:
- Explain what you're doing in plain lay terms as you go, including any git
  commands and why you're running them.
- Keep explanations concise; lead with the answer.
- Before anything irreversible (force push, deleting things), stop and explain.

## What this project is
A single-page website for a 4-person ayahuasca integration group spread across
the world, used to find civilised hours for monthly video catch-ups.
Built in Claude Cowork; now maintained here.

- Live site: https://seanhuangemail-png.github.io/Arkana-Fantastic-Four/
- Hosting: GitHub Pages, "Deploy from a branch", `main` / root.
  Pushing to `main` redeploys automatically (allow a few minutes).
- Everything is in one file: `index.html` (inline CSS + JS, no build step,
  no dependencies, no framework). Keep it that way unless Sean asks otherwise.

## How the page works
- Members are defined in the `EDIT DEFAULTS HERE` block near the top of the
  script in `index.html` — name + IANA timezone. This is where to edit when
  someone moves (e.g. Toby: Dubai → Thailand).
- `quality(hour)` defines "reasonable hours": good = 8am–9pm, stretch = 7am and
  9–11pm, otherwise asleep. Adjust here if the group wants different limits.
- `EVENT_TITLE` sets the name used on Google Calendar invites and WhatsApp
  messages.
- The grid's columns are hours of the chosen date in the VIEWER's device
  timezone; all conversions use the Intl API, so DST is handled automatically.
- No backend, no storage: edits made in the browser (names/zones) last only
  until reload. Permanent changes go in this repo. Do not add
  localStorage/accounts/databases without discussing trade-offs with Sean first.

## The group (for context)
Sean — Australia (Sydney, travels often) · Matan — Peru (Lima, travelling) ·
Corey — Minnesota (Chicago time) · Toby — Thailand (Bangkok, was Dubai).
They coordinate on WhatsApp; the site proposes times, WhatsApp confirms.

## Typical tasks
- Update someone's timezone or name in the defaults block, commit, push.
- Tweak colours, wording, or the reasonable-hours definition.
- After any change: sanity-check one known conversion (e.g. 11am Sydney =
  8pm previous day in Lima/Chicago, 8am same day in Bangkok, outside DST shifts)
  before pushing.
