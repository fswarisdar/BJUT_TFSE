# Term project — Library Management System (dual-book)

**Weight:** 40% (completeness 16 · code quality 12 · documentation 8 · creativity 4).  
**Teams:** 3 (preferred for 21 students) or 3–4. **Stack:** Python 3.11+, pytest, linter. CLI or small web UI.

**P** = Pressman work products · **S** = Sommerville product artefacts.

| Student handout | Path |
| --- | --- |
| Group themes G1–G7 | [`ProjectIdeas_Groups.md`](ProjectIdeas_Groups.md) |
| Lecture ↔ project ↔ weekly reports | [`LectureProjectAlignment.md`](LectureProjectAlignment.md) |
| Weekly report template | [`weekly-reports/TEMPLATE.md`](weekly-reports/TEMPLATE.md) |
| Sample LaTeX final report | [`sample-report/`](sample-report/) |

---

## Alignment principle

**Project sections follow lecture order.** Each week you (1) learn the idea in class, (2) file a short **team weekly report (WR)**, (3) update the matching `docs/` file and/or code.  
The Week 12 LaTeX report is the **assembled** dual-book pack—not a new document invented at the end.

Individual **A1–A11** remain personal homework (20%). **WR01–WR12** count toward project documentation/process (inside 40%).

---

## Must-have scope

| ID | Capability |
| --- | --- |
| M1–M2 | Register patrons/titles; search |
| M3–M4 | Borrow / return with overdue fines (policy module separate) |
| M5–M6 | Holds + notify (mock OK); librarian reports |
| M7–M8 | SQLite (or equiv.); automated tests incl. blocking-fine case |
| M9 | Basic authn for librarian vs patron roles (**S Ch 7**) |
| M10 | Input validation on borrow/return quantities and dates (**S Ch 8**) |

Theme variants (G2–G7): same responsibilities under your domain nouns (reserves, ILL, equipment, licenses, …).

---

## Documentation pack (= final report chapters)

| Path | Lecture week | Book |
| --- | --- | --- |
| `docs/vision.md` | W1 | S Ch 1 product vision |
| `docs/process.md` | W2 | P Ch 2–3, S Ch 2 |
| `docs/srs.md` + stories appendix | W3 | P Ch 5, S Ch 3 |
| `docs/requirements-model.md` + features | W4 | P Ch 6–7, S 3.4 |
| `docs/design.md` | W5 | P Ch 8/10, S Ch 8 notes |
| `docs/architecture.md` | W6 | P Ch 9, S Ch 4–6 rationale |
| `docs/security-privacy.md` | W7 | S Ch 7 |
| `docs/qa-reviews.md` | W7 | P Ch 15–16, S 9.5 |
| `docs/test-design.md` | W8 | P Ch 17–18, S Ch 9 |
| `docs/formal.md` | W9 | P Ch 21 (+ S 8.3 failure note) |
| `docs/metrics-estimate.md` | W10 | P Ch 23, 26 (+ S 10.3) |
| `docs/rmmm-ethics.md` | W11 | P Ch 28, 32 |
| `docs/devops.md` | W11 | S Ch 10 branching/CI policy |
| `README.md` | ongoing | Run/test; AI declaration |
| `report/` (LaTeX) | W12 | Assembled final report |
| `weekly-reports/WRXX.md` | each week | Team progress (see below) |

---

## Weekly reports (required)

Submit **WR01–WR12** in the team repo: `weekly-reports/WR01.md` … `WR12.md`.

| Rule | Detail |
| --- | --- |
| Length | **½–1 page** or ≤400 words (+ links to commits/docs) |
| Due | Start of **next** lecture (WR01 due start of Week 2, …; WR12 with final) |
| Template | Copy [`weekly-reports/TEMPLATE.md`](weekly-reports/TEMPLATE.md) |
| Must include | Lecture link · done · evidence path · **one numeric check** · risks · next plan · AI note |
| Grading cue | Missing WR streak hurts the **documentation (8)** and process side of completeness |

Full week-by-week WR focus: [`LectureProjectAlignment.md`](LectureProjectAlignment.md).

---

## Milestones (code + docs; WR runs every week)

| When | Major deliverable (in addition to that week’s WR) |
| --- | --- |
| W1 | Team + theme registration; vision draft (WR01) |
| W2 | Repo + `vision.md` + `process.md` |
| W3 | `srs.md` + personas/stories |
| W4 | Models + feature list |
| W5 | `design.md` + policy module stub |
| W6 | `architecture.md` + search/borrow slice running |
| W7 | Security-privacy + FTR issue log |
| W8 | Tests for blocking rule (M3–M4 / theme equivalent) |
| W9 | Formal safety property artefact |
| W10 | Metrics + estimate |
| W11 | Freeze; RMMM; devops.md; ethics |
| W12 | Tag `v1.0` + LaTeX report + 12+3 min talk |

---

## Creative increment (pick one)

Recommendation engine · public catalog API · ISBN merge · formal Ch 21 artefact · simple SaaS multi-tenant design essay (S Ch 5) without full implementation · theme-specific extra (see ProjectIdeas).

---

## Presentation (12+3 min)

Vision → story/FR trace → architecture & security → test/formal evidence → live demo of **blocking rule** → top risk / DevOps / responsibility.
