# Fresh entry repo — Lunar Landing Site Navigator
Locked challenge. Event: Sat 14 Nov 09:00 → Sun 15 Nov 23:59 SGT. Daniel feature freeze Sat 23:00; handoff Sun 11:00; Nich submits.

## Hard rules
- Create the entry repo **at or after 09:00 SGT Sat 14 Nov**. No challenge code before then.
- Fresh repo only. Do **not** copy files, JSON, assets, or commits from `clps-practice/` / strength-trainer practice apps.
- Reuse **knowledge** only: method (skyfield/DE421 or Horizons + LOLA horizons), validation sites, UI lessons, pitfalls from `research/practice-mvp-lessons.md`.
- Recompute all ephemeris and site stats during the event. New code, new data files, commit history starting 14 Nov.
- Disclose in the submission that a pre-event learning prototype existed (domain practice), and that this entry was built from scratch during the hackathon.

## 09:00 Sat — create repo (Daniel)
1. Create empty public repo under `daniel27-space` (name TBD on the call, e.g. `lunar-landing-site-navigator` or team name).
2. Invite Nich (GitHub username still pending as of 6 Nov — get it before Friday).
3. Clone once; first commit: README with challenge name, team, and "built during Space Apps 2026".
4. Do **not** fork or import practice trees.

## Parallel tracks after kickoff
| Track | Owner | First deliverable |
|---|---|---|
| Calc / data | Daniel + AI | CONTRACT.md: sites list, date window, outputs (sunlit %, Earth %, both, horizon mask) |
| UI skeleton | Nich + AI | Static site (GitHub Pages or equivalent) with empty panels; phone-readable shell |
| Demo script | Daniel | 90-second script before building features |

## Minimum viable wow (build this first)
One real-data flow end to end: pick a south-pole site → pick a date → see Sun/Earth vs terrain horizon → see power/comms windows. Validate numbers against one published reference (e.g. Mazarico / Gläser / published illumination %).

## Parking lot (after feature freeze)
Calendar compare, multi-site side-by-side polish, 3D globe niceties, tour — only if the wow path is solid.

## Handoff (Sun 11:00)
Working demo URL, public repo URL, known bugs, validation table, demo video draft, submission draft fields. Nich owns polish + submit by Sun 22:00 target (23:59 hard stop).

## Signup reminder (by Fri 13 Nov)
Daniel and Nich: spaceappschallenge.org hub accounts, Singapore local event, same team. Meetup RSVP optional by Thu 12 Nov 23:59 SGT.
