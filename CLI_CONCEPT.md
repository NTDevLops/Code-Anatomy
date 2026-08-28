# 🛠️ Code Anatomy CLI — Concept Doc

This is a design sketch, not shipped software. It describes two commands that become possible now that `anatomy.yaml` exists as a machine-readable manifest (see `anatomy.yaml` at the repo root).

---

## `code-anatomy init`

Scaffolds a new project at a chosen adoption level and generates a starter `anatomy.yaml`.

```bash
code-anatomy init --level standard --lang python my-project
```

What it does:

1. Creates the folder set for the requested level, exactly as defined in `ARCHITECTURE.md` → "Recommended Adoption Levels" (Level 1 / Level 2 / Level 3).
2. Writes an `anatomy.yaml` with `level` set accordingly and `organs` populated for that level's folder set.
3. Drops a placeholder file in each generated organ folder (e.g. `brain/.gitkeep` or a minimal `brain/__init__.py`) so the structure survives a first `git add`.
4. Optionally scaffolds `body.py` / `body.js` / `body.go` with a minimal composition-root stub, depending on `--lang`.

Flags:

| Flag | Values | Default |
|---|---|---|
| `--level` | `minimal`, `standard`, `full` | `minimal` |
| `--lang` | `python`, `js`, `ts`, `go` | `python` |

---

## `code-anatomy lint`

Walks a repo and flags files that appear to be sitting in the wrong organ, using the `aliases` map already defined in `anatomy.yaml`.

```bash
code-anatomy lint
```

Example output:

```text
brain/save_order_to_postgres.py
  ⚠ contains a database query — this looks like a `memory/` responsibility, not `brain/`
  (rule: brain/ should only import from soul/, nerve/, and memory/ — CONVENTIONS.md § 15. Anti-Patterns → Random Anatomy)

soul/
  ⚠ 23 files with no subfolders — consider subdividing by feature
  (rule: "God soul/" — CONVENTIONS.md § 15. Anti-Patterns)

whisker/
  ⚠ organ contains only 1 file and isn't part of the official vocabulary
  (rule: CONVENTIONS.md Rule 3 — Do Not Create Folders for Single Random Files; also § 15. Anti-Patterns → Organ-per-File)
```

### What the first version should check (naive but useful)

A first version doesn't need real static analysis — regex/keyword heuristics driven entirely by data that already exists in this repo are enough to be useful:

1. **Misplaced files** — for each organ, check whether a file matches a *different* organ's `aliases` keywords (e.g. a class name matching `.*Repository`, `.*Database`, `.*Cache` found under `brain/` instead of `memory/`).
2. **God `soul/`** — flag when `soul/` (or any organ) has more files directly inside it than a configurable threshold (default: 15, matching the number already used in the "God `soul/`" anti-pattern in `CONVENTIONS.md`) with no subfolders.
3. **Organ-per-file** — flag any top-level folder that (a) isn't in the official vocabulary listed in `GLOSSARY.md`, and (b) contains exactly one file.
4. **Empty anatomy** — flag any folder from the official vocabulary that exists but is empty, per `CONVENTIONS.md` Rule 1 — No Empty Anatomy.

None of these checks require inventing new rules — they mechanically enforce rules and thresholds that are already written down in `CONVENTIONS.md` and `GLOSSARY.md`. The linter's job is to catch drift, not to define policy.

---

## Non-goals for v1

- No attempt at full static/semantic analysis (e.g. actually tracing import graphs to catch circular dependencies) — that's a natural v2 once the heuristic version proves useful.
- No auto-fix / auto-move of files. Flag, don't move — misplaced-file heuristics will have false positives, and moving files silently would erode trust in the tool.