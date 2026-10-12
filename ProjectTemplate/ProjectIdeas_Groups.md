# Term project ideas — 7 groups (21 students)

**Course:** Theoretical Foundations of Software Engineering · BJUT Fall 2026  
**Format:** Engineering product project (not a research thesis) · **teams of 3** · **40%**  
**Shared rules:** All groups must satisfy `ProjectSpec.md` must-haves (M1–M10), dual-book docs pack, pytest, AI declaration, Week 12 talk.  
**Differentiation:** Each group picks **one theme below** (first-come / instructor assignment). Same grading rubric; different product focus.

| Group | Theme (EN) | 主题（中文） | Core differentiator | Suggested creative increment |
| --- | --- | --- | --- | --- |
| **G1** | Classic Campus Circulation LMS | 经典校园流通图书馆系统 | Full borrow/return/fines/holds for general stacks | ISBN merge **or** recommendation engine |
| **G2** | Course Reserves Desk | 课程指定参考书架 | Short-loan reserves for a course; instructor lists; peak-load QA | Public catalog API for course list |
| **G3** | Inter-Library Loan Mini-Hub | 馆际互借小枢纽 | External request lifecycle (request→ship→receive→return) | Formal Ch 21 artefact for “no double ship” |
| **G4** | Lab Equipment Checkout | 实验室设备借还 | Assets ≠ books; damage deposit; serial numbers | SaaS multi-tenant *design essay* (no full impl.) |
| **G5** | Digital Resource License Desk | 数字资源授权台 | Seat licenses, expiry, concurrent access caps | API for “license remaining seats” |
| **G6** | Accessibility-First Catalog | 无障碍优先书目检索 | NFR-heavy search (time, clarity of errors, keyboard-first CLI/UI) | Formal acceptance measures + TDD transcript |
| **G7** | Staff Analytics & Compliance Console | 馆员分析与合规控制台 | Librarian reports, audit log, least privilege; thinner student UX | Privacy impact note + role matrix deep dive |

## How to choose (students)

1. Form a team of **3** by end of Week 2.  
2. Submit theme preference (1st / 2nd / 3rd choice) to the instructor.  
3. Instructor assigns unique themes so no two groups share the same row.  
4. Freeze theme in `docs/vision.md` (out-of-scope must mention other themes you are *not* building).

## Common MVP (all groups)

Regardless of theme, every team must demonstrate:

- Register entities relevant to the theme (patrons + titles **or** assets/licenses)  
- Search  
- Checkout / return (or equivalent state transitions) with a **separate policy module** (fines / deposits / seat caps)  
- At least one blocking rule (e.g. unpaid fine, expired license, damaged asset hold)  
- Holds or waitlist **or** equivalent queue  
- Librarian (staff) vs patron (user) roles  
- SQLite (or equiv.) + automated tests for the blocking rule  
- Input validation on trust boundaries  

## Theme briefs (one paragraph each)

### G1 — Classic Campus Circulation LMS
Build the reference LMS in `ProjectSpec.md`: patrons, titles/copies, borrow/return, overdue fines in `FinePolicy`, holds + mock notify, librarian reports. Best baseline if the team wants maximum alignment with lecture examples.

### G2 — Course Reserves Desk
Focus on **short-loan** items tied to a `Course` and `ReserveList`. Borrow windows are hours/days, not weeks. Emphasize conflict between student demand and fairness (one copy, many students). Reports: “most contended reserve titles.”

### G3 — Inter-Library Loan Mini-Hub
Model requests to a partner library: states such as `requested → approved → in_transit → available_here → returned_to_partner`. Blocking rule example: cannot create a local loan while an ILL item is still `in_transit` to the wrong site. Notify can be mocked.

### G4 — Lab Equipment Checkout
Replace “book copy” with **equipment items** (laptop, sensor kit) with serial numbers and condition. Policy module: deposit / late fee / “damaged → quarantine.” Architecture note must argue why microservices are unnecessary for one lab.

### G5 — Digital Resource License Desk
Manage **license seats** for e-resources (e.g. max 5 concurrent readers). Checkout = acquire seat; return = release seat; overdue = forced expire. Privacy: minimise which student IDs appear in shared logs.

### G6 — Accessibility-First Catalog
Same core circulation as G1, but grading emphasis on **measurable NFRs**: search p95, error message clarity, no colour-only status, validation messages that state the repair action. Creative increment: publish NFR test table + TDD evidence.

### G7 — Staff Analytics & Compliance Console
Student borrow path can be thinner; invest in **librarian console**: overdue summary, privacy-sensitive history access (authz), audit log of who viewed what. Security-privacy.md is the star artefact.

## Team roster template (paste into README)

```text
Group ID: G?
Theme: ...
Members (3):
  1. Name / Student ID / GitHub
  2. ...
  3. ...
Module owners: FinePolicy/Policy=... ; Borrow flow=... ; Docs lead=...
AI tools used (if any): ...
```

## What is *not* acceptable as the main project

- A research survey / “novel algorithm” paper with no running system  
- Seven identical G1 clones with different logos only  
- Mobile social network “for books” with no circulation policy  
- Microservices for fashion without QA rationale  

## Mapping to Week 12 talk (12+3 min)

Use the same talk spine for every theme: vision → FR/story trace → architecture & security → tests/formal → live demo of **your** blocking rule → risk/DevOps/responsibility.
