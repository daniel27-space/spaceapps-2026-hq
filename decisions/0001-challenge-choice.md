# 0001: Challenge choice
Status: DECIDED 2026-11-06 — Lunar Landing Site Navigator
Deciders: Daniel, Nich
Full statements: research/statement-lunar-landing-site-navigator-2026-10-30.md, research/statement-flame-in-freefall-2026-10-30.md

## Sourced facts (statements, scraped 2026-10-30)
- Site banner: "Do not begin work on your projects until the hackathon begins." Resources tabs for both: "Resources will be available on Friday, November 13." No dataset links yet.
- Both: difficulty Advanced/Intermediate.
- Lunar Landing Site Navigator (LLSN): intuitive tool to compare south-pole landing sites and dates, showing Sun and Earth against the horizon for power and direct-to-Earth comms. Suggested: curated site list + custom coords, side-by-side comparison, date/season exploration, time to sunset/Earthset, solar elevation, sunlight duration, Earth visibility, 2D/3D views, animations, novice-to-expert audience. Data named: JPL Horizons or precomputed ephemeris, LOLA topography; existing tools Quickmap, Moon Trek, Horizons called hard for non-specialists. Considerations: no refraction, terrain horizon, libration.
- Flame in Freefall (FiF): "SI-powered" web dashboard that summarizes, ranks and interprets microgravity combustion investigations in NASA PSI for fire-safety insights (spacecraft, stations, lunar/Mars bases, rovers). Suggested: relevance ranking, extract data for flammability modelling, highlight research for fire-safety equipment, compare objectives/fuels/O2/flow/sensors across investigations; Earth spin-offs optional. Named investigations: BASS/BASS-II, Saffire I-III, SAME/SAME-R, FLEX/FLEX-2, CFI, ACME (BRE, CFI-G, E-FIELD), SPICE, SLICE, DAFT. Notes: no partial-gravity data in PSI yet; Moon Base atmosphere likely >=30% O2 at <=10.2 psi. Audience: researchers, students, engineers. Rockets out of scope.

## Judgement (Selene), scores 1-5
| Criterion | LLSN | FiF | Why |
|---|---|---|---|
| Impact | 4 | 4 | LLSN: real CLPS replanning pain. FiF: crew safety, Moon Base O2 angle is timely. |
| Creativity | 3 | 4 | LLSN space is crowded (Quickmap etc., many teams). FiF "SI" ranking is fresher, fewer obvious templates. |
| Validity | 4 | 3 | LLSN numbers can be checked vs published illumination studies (we know how). FiF relies on LLM summaries of papers; hallucination risk, harder to validate. |
| Relevance | 5 | 5 | Both can hit every objective. |
| Presentation | 5 | 3 | LLSN is visual by nature (sky chart, 3D). FiF is a dashboard of text/tables; harder to wow in 30 s. |
| Data availability | 4 | 3 | LLSN: Horizons/SPICE + LOLA are open, known, tested. FiF: PSI needs a free login for many files, data is heterogeneous (PDFs, videos, CSV); not tested by us. |
| Buildable in ~14 h solo | 4 | 3 | Daniel has done LLSN end to end (knowledge, not code). FiF: new domain, ingestion of PSI unknown, needs an LLM API at runtime (cost/keys) or precomputed summaries. |
| Total | 29 | 25 | |

## Prior-work risk (LLSN)
- Fact: Daniel's public practice app (daniel27-space.github.io/strength-trainer/clps-practice/v3/) already does south-pole Sun/Earth horizon analysis; the entry must start from a fresh repo; banner says no project work before 09:00 SGT 14 Nov.
- Judgement: medium risk. Rules allow learning; reusing practice code or data would look like pre-built work. Mitigation: fresh repo at 09:00 Sat, recompute all data during the event, write new code (no copy-paste, no imported assets/JSON from v3), keep commit history from 14 Nov, and disclose in the submission that a practice prototype was built before to learn the domain. Consider making the practice app private/unlisted only if Daniel wants (no change made). Ask local lead/organisers if unsure (draft needs Daniel's approval).
- FiF has no prior-work risk.

## Recommendation
LLSN, with the fresh-build discipline above. Reasons: highest score on Validity, Presentation, data and buildability for a solo builder with a hard Sunday cut-off; Daniel's domain knowledge is legitimate and de-risks the calc. Choose FiF instead if Daniel judges the prior-work look too risky or wants novelty; then precompute summaries offline during the event and validate PSI access on 13 Nov.

## Decision
**Lunar Landing Site Navigator** (locked 2026-11-06 by Daniel via Billy).
Flame in Freefall is the documented fallback only.
Fresh-build rules above are mandatory: new repo at 09:00 SGT Sat 14 Nov, recompute data during the event, no practice code/assets/JSON, disclose the learning prototype in the submission.
