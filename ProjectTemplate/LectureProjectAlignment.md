# Lecture contents ↔ project sections ↔ weekly reports

**Yes:** project documentation sections follow the **same order as the lectures**.  
**Yes:** teams submit a **short weekly project report (WR)** that grows the final pack / LaTeX report.

Individual homework **A1–A11** stays separate (personal learning).  
**WR** is the **team** progress log for the 40% project.

---

## Master map (12 weeks)

| Week | Lecture focus | Project section / docs file | Weekly report (WR) focus | Feeds final LaTeX § |
| --- | --- | --- | --- | --- |
| 1 | Software, products, myths, responsibility | Theme choice; draft vision notes | **WR01:** team roster + theme G? + 5-sentence vision draft | §1 Vision |
| 2 | Process models; agile | `docs/process.md` | **WR02:** process choice + 3 Scrum↔framework maps | §2 Process |
| 3 | RE; personas & stories | `docs/srs.md` + stories | **WR03:** FR/NFR excerpt + 2 personas + 4 Must stories | §3 Requirements |
| 4 | Requirements modeling; features | `docs/requirements-model.md` | **WR04:** CRC/state update + epic→feature list | §4 Modeling |
| 5 | Design; reliable programming | `docs/design.md` | **WR05:** FinePolicy/policy seam + 3 validation rules | §5 Design |
| 6 | Architecture; cloud/MS options | `docs/architecture.md` + code slice | **WR06:** style + 2 QAs + why-not-microservices + running search/borrow | §6 Architecture |
| 7 | Quality, FTR; security & privacy | `docs/security-privacy.md`, `docs/qa-reviews.md` | **WR07:** ≥5 threats + FTR issue log (≥3) | §7–8 Security / QA |
| 8 | Testing; TDD/automation | `docs/test-design.md` + pytest | **WR08:** V(G) or equivalence table + blocking-rule tests green | §9 Testing |
| 9 | Formal methods; failure mgmt | `docs/formal.md` | **WR09:** safety property + illegal/rejected trace + failure strategy | §10 Formal |
| 10 | Metrics; estimation; DevOps measures | `docs/metrics-estimate.md` | **WR10:** two V(G) + COCOMO drivers + 3 DevOps metrics | §11 Metrics |
| 11 | PM, EVA, risk; DevOps; responsibility | `docs/rmmm-ethics.md`, `docs/devops.md` | **WR11:** RMMM≥6 + EVA numbers + CI policy + feature freeze | §12 Ops / risk |
| 12 | Presentations; exam review | `v1.0` + final report + talk | **WR12:** final checklist + talk roles + tag `v1.0` | Full report + demo |

---

## How WR relates to A1–A11

| | Assignments A1–A11 | Weekly reports WR01–WR12 |
| --- | --- | --- |
| Who | Individual | Team |
| Goal | Learn dual-book ideas | Advance the shared product |
| Length | As specified per A | **½–1 page** (or ≤400 words) + links |
| Grade | Inside 20% homework | Inside **40% project** (process/documentation) |

Teams may **reuse** ideas from their A’s, but WR must be **team-owned**, in the project repo, and specific to the group theme (G1–G7).

---

## Final LaTeX report = merged weekly evidence

The sample report sections are the **compiled** form of WR01–WR11:

`sample-report/main.tex` §1←WR01 … §12←WR11, plus implementation & appendices at Week 12.

Students should **not** rewrite everything in Week 12 from scratch—polish and assemble.
