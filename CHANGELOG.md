# 📜 Code Anatomy Spec Changelog

Code Anatomy follows semver for the **spec itself**, independent of any implementation or tooling version. A project pinning `anatomy.yaml: version: 1` is on the `v1.0` baseline — check below for what changed since.

- **Major** — a breaking change to an existing organ's meaning or official path.
- **Minor** — a new organ, or a new officially-endorsed default/expansion pattern for an existing organ.
- **Patch** — documentation clarification, example fixes, or cross-document consistency fixes with no change to meaning.

New organs are proposed via `.github/ISSUE_TEMPLATE/anatomy_proposal.md` and only ship in a minor version.

---

## v1.1 — released 2026-08-29

### Fixed
- Reconciled the Filtering System / `kidney/` inconsistency across `ARCHITECTURE.md`, `README.md`, `CONVENTIONS.md`, and `GLOSSARY.md`. `kidney/` is now documented in exactly one place — as the final stage of the Digestive System — instead of sometimes appearing as its own numbered system and sometimes missing entirely (it previously had no `GLOSSARY.md` entry at all).
- Renumbered Digestive System's downstream sibling systems in `ARCHITECTURE.md` (Skeletal System through Development and Maintenance System) after merging the former "7. Filtering System" into "6. Digestive System".
- Fixed the Web Application Example in `GUIDE.md`, whose `digestive/` listing previously omitted `intestine/` and `kidney/` entirely.
- Added the missing `dna` organ to `anatomy.yaml`'s `organs` map — it was part of the documented Standard-level structure in `ARCHITECTURE.md`/`CONVENTIONS.md`/`README.md` but absent from the manifest despite `level: standard`.
- Completed and reconciled `anatomy.yaml`'s `aliases` map against `GLOSSARY.md`'s "Traditional Equivalent" lists: `heart`, `dna`, and `checkup` previously had no aliases at all; `brain`, `soul`, `memory`, `skin`, and `immune` were each missing documented terms.
- Renamed ARCHITECTURE.md's structural-hierarchy headings ("Level 0 — The Body", "Level 1 — Core Systems") to "Tier 0"/"Tier 1" — they collided with the unrelated "Level 1/2/3" adoption levels defined later in the same document.
- Aligned `CONVENTIONS.md` § 14 Growth Rules terminology ("Stage 1/2/3", "Stage 3 — Advanced") with the "Level 1/2/3" / "Level 3 — Full Anatomy" naming already used consistently by `ARCHITECTURE.md`, `README.md`, `CLI_CONCEPT.md`, and `anatomy.yaml`.
- Gave `skin` its own icon (🩹) instead of reusing the immune system's 🛡️ shield, which was applied to both organs identically across `ARCHITECTURE.md`, `GLOSSARY.md`, `CONVENTIONS.md`, `GUIDE.md`, and `README.md`.
- Fixed `README.md`'s Quick Reference table, which listed `services/` as `heart/`'s traditional equivalent (contradicting `GLOSSARY.md` and `anatomy.yaml`, which document `services` under `brain/`); `heart/`'s row now reads `workers/`, `scheduler/` and `brain/`'s row includes `services/`.
- Rebuilt `CONTRIBUTING.md`'s Table of Contents: an unlisted "6. New Anatomy Proposal Template" section had shifted every subsequent numbered section by one, breaking the anchor links for sections 6–12 and omitting sections 13–16 entirely.
- Added `anatomy.yaml`, `CLI_CONCEPT.md`, and `CHANGELOG.md` to the file lists in `.github/ISSUE_TEMPLATE/bug_report.md`, `.github/ISSUE_TEMPLATE/feature_request.md`, and `.github/PULL_REQUEST_TEMPLATE.md`, which still only referenced the original six docs.
- Added `kidney` to the existing-anatomy checklists in `.github/ISSUE_TEMPLATE/anatomy_proposal.md` and `.github/PULL_REQUEST_TEMPLATE.md`, now that it has its own official `GLOSSARY.md` entry.
- Normalized `README.md` to CRLF line endings to match every other file in the repo.
- Added `dna/` to README's "Medium Project" example — it was missing despite matching the Standard level everywhere else in the repo, including README's own earlier worked example.
- Added a "Documentation Map" to `README.md` pointing to `ARCHITECTURE.md`, `GUIDE.md`, `CONVENTIONS.md`, `GLOSSARY.md`, `CONTRIBUTING.md`, `CHANGELOG.md`, `anatomy.yaml`, and `CLI_CONCEPT.md` — README previously mentioned only `ARCHITECTURE.md`, in passing, and never oriented readers to the rest of the docs.

### Added
- A default, collapsed structure for `digestive/` (`intake/` + `process/`) for Level 1/2 projects, with the full six-stage pipeline (`mouth/teeth/stomach/liver/intestine/kidney`) documented as an explicit Level 3 / opt-in expansion.
- A default, collapsed structure for `action/` (`commands/` + `nav/`) alongside the existing full `hand/finger/leg/` form, in `ARCHITECTURE.md`, `CONVENTIONS.md`, and `GLOSSARY.md`.
- An explicit note that `blood/` alone is the default for the Circulatory System and `vessel/` is an opt-in expansion, cross-referenced between `README.md` and `ARCHITECTURE.md`.
- Two new anti-patterns in `CONVENTIONS.md` § 15 Anti-Patterns — "God `soul/`" and "Organ-per-File" — plus a fix note added to the existing "Random Anatomy" anti-pattern explaining why `brain/database.py` is wrong (brain/ should only import from soul/, nerve/, and memory/).
- A Rosetta Stone table in `GUIDE.md` mapping Code Anatomy organs to MVC / Clean-Hexagonal / typical Node-Django names.
- A Go example in `GUIDE.md`, alongside the existing Python/JS/TS examples.
- A worked "See It in Practice" example (a small e-commerce API at the Standard level) in `README.md`.
- `anatomy.yaml` — a machine-readable manifest schema for a project's Code Anatomy layout, using the existing Level 1/2/3 naming and the "Traditional Equivalent" aliases already documented per organ in `GLOSSARY.md`.
- `CLI_CONCEPT.md` — a design sketch for `code-anatomy init` and `code-anatomy lint`, built entirely on rules and thresholds that already exist in `CONVENTIONS.md` and `GLOSSARY.md`.
- Two new fields in `.github/ISSUE_TEMPLATE/anatomy_proposal.md`: target spec version, and whether the proposal overlaps with a previously collapsed organ.

---

## v1.0 — baseline

The original, unversioned Code Anatomy convention (`README.md`, `ARCHITECTURE.md`, `GUIDE.md`, `CONVENTIONS.md`, `GLOSSARY.md`, `CONTRIBUTING.md`) as it existed before this changelog was introduced. Treated as `v1.0` since it had no prior version marker — this is also the version `anatomy.yaml: version: 1` refers to.