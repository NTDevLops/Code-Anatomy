# 📏 Code Anatomy Conventions

> **The official naming, structure, and organization rules for Code Anatomy.**

This document defines the conventions used by the **Code Anatomy** architecture.

While `README.md` explains the philosophy, `ARCHITECTURE.md` defines the hierarchy, and `GUIDE.md` explains how to use the system, this document defines the practical rules developers should follow.

These conventions exist to keep Code Anatomy projects:

* 🧠 Understandable
* 🧬 Consistent
* 🦴 Structured
* 🔧 Maintainable
* 📈 Scalable

> **Creativity is encouraged. Consistency is required.**

---

# 📚 Table of Contents

* [1. Core Rules](#1-core-rules)
* [2. Naming Rules](#2-naming-rules)
* [3. File Naming](#3-file-naming)
* [4. Folder Naming](#4-folder-naming)
* [5. Anatomy Naming Rules](#5-anatomy-naming-rules)
* [6. Responsibility Rules](#6-responsibility-rules)
* [7. Folder Creation Rules](#7-folder-creation-rules)
* [8. Import Rules](#8-import-rules)
* [9. Dependency Rules](#9-dependency-rules)
* [10. Feature Rules](#10-feature-rules)
* [11. Shared Code Rules](#11-shared-code-rules)
* [12. Configuration Rules](#12-configuration-rules)
* [13. Testing Rules](#13-testing-rules)
* [14. Growth Rules](#14-growth-rules)
* [15. Anti-Patterns](#15-anti-patterns)
* [16. The Final Code Anatomy Rules](#16-the-final-code-anatomy-rules)

---

# 1. Core Rules

Code Anatomy follows a responsibility-first approach.

## Rule 1 — Every Code Unit Has a Role

Every file should have a clear responsibility.

Ask:

> **What does this code do?**

Do not ask:

> **What anatomy name sounds interesting?**

---

## Rule 2 — Every Role Has a Place

Once the responsibility is clear, place the code in the appropriate anatomical location.

Example:

```text
Stores information
        ↓
memory/
```

```text
Makes decisions
        ↓
brain/
```

```text
Protects the system
        ↓
immune/
```

---

## Rule 3 — One Primary Responsibility

A file should preferably have one primary responsibility.

Bad:

```text
brain/
└── everything.py
```

Better:

```text
brain/
├── decision.py
├── rules.py
└── workflow.py
```

---

## Rule 4 — Meaning Before Metaphor

The anatomy metaphor must never make the project harder to understand.

If the anatomy name creates confusion:

1. Clarify the responsibility.
2. Follow the official hierarchy.
3. Document unusual decisions.
4. Prefer consistency over creativity.

> **Code Anatomy should simplify architecture, not complicate it.**

---

# 2. Naming Rules

All names should be:

* Clear
* Predictable
* Consistent
* Descriptive

Avoid names that are vague.

Bad:

```text
thing.py
stuff.py
random.py
misc.py
final.py
new.py
test2.py
```

Better:

```text
validator.py
payment_service.py
user_repository.py
event_listener.py
```

---

# 3. File Naming

File naming should follow the conventions of the programming language whenever possible.

## Python

Use:

```text
snake_case.py
```

Examples:

```text
user_service.py
payment_processor.py
event_handler.py
```

---

## JavaScript

Choose one convention and keep it consistent.

Example:

```text
camelCase.js
```

or:

```text
kebab-case.js
```

Example:

```text
userService.js
paymentProcessor.js
```

---

## TypeScript

Choose the project's established convention.

Examples:

```text
user.service.ts
```

or:

```text
userService.ts
```

> **Consistency inside a project is more important than the specific style chosen.**

---

# 4. Folder Naming

Folder names should generally be:

```text
lowercase
```

For multiple words, follow the language or ecosystem convention.

Examples:

```text
authentication/
user_management/
payment_processing/
```

Avoid:

```text
UserManagement/
RANDOM_FOLDER/
My-New-Folder/
```

unless the language or framework strongly requires another convention.

---

# 5. Anatomy Naming Rules

Official anatomy names are reserved for specific responsibilities.

Do not use them randomly.

---

## 🧍 `body`

Reserved for:

* Application startup
* Application lifecycle
* Main application coordination

Examples:

```text
body.py
body.js
body.ts
```

Do not use:

```text
body/
```

as a replacement for every project folder without a clear purpose.

> **The body represents the application as a whole.**

---

## 🧠 `brain`

Reserved for:

* Decisions
* Rules
* Workflows
* Business logic
* Complex reasoning

Do not place:

* Database storage
* Random utilities
* UI components

inside `brain/`.

---

## 🧬 `soul`

Reserved for:

* Major features
* Domain functionality
* Core capabilities

Example:

```text
soul/
├── authentication/
├── payments/
└── users/
```

> **The soul represents what the application does.**

---

## ⚡ `nerve`

Reserved for:

* Shared support
* Internal communication
* Logging
* Validation
* Reusable helpers
* Events

Example:

```text
nerve/
├── shared/
├── communication/
└── reflex/
```

Do not turn `nerve/` into a dumping ground for unrelated code.

---

## ❤️ `heart`

Reserved for:

* Central processing
* Continuous operations
* Workers
* Schedulers
* System coordination

> **The heart drives the system.**

---

## 🧠 `memory`

Reserved for:

* Databases
* Cache
* Sessions
* Persistent state
* Temporary state

Example:

```text
memory/
├── database/
├── cache/
└── state/
```

---

## 🫁 `lung`

Reserved for:

* External communication
* HTTP clients
* APIs
* WebSockets
* Third-party services

> **The lungs communicate outside the system.**

---

## 🍽️ `digestive`

Reserved for:

* Input processing
* Parsing
* Transformation
* Extraction
* Filtering pipelines

Full example (large projects — see `ARCHITECTURE.md` for when to expand into this):

```text
digestive/
├── mouth/
├── teeth/
├── stomach/
├── liver/
├── intestine/
└── kidney/
```

Default example (small/medium projects):

```text
digestive/
├── intake/      # mouth + teeth
└── process/     # stomach + liver + intestine + kidney
```

---

## 🦴 `skeleton`

Reserved for:

* Models
* Schemas
* Interfaces
* Structural foundations

Example:

```text
skeleton/
├── models/
├── schemas/
├── interfaces/
├── bone/
└── joint/
```

---

## 💪 `muscle`

Reserved for:

* Heavy computation
* Intensive work
* Background execution
* Processing operations

> **Muscles perform work.**

---

## 🧬 `dna`

Reserved for:

* Configuration
* Settings
* Constants
* Environment definitions
* Feature configuration

Example:

```text
dna/
├── settings/
├── environment/
├── constants/
└── gene/
```

---

## 🧫 `cells`

Reserved for:

* Small components
* Independent units
* Reusable building blocks

Example:

```text
cells/
├── components/
├── units/
├── membrane/
└── nucleus/
```

---

## 👁️ `sensory`

Reserved for:

* Observation
* Listening
* Detection
* Monitoring

Example:

```text
sensory/
├── eye/
├── ear/
└── nose/
```

---

## ✋ `action`

Reserved for:

* Commands
* Operations
* Execution
* Navigation

Default (small/medium projects) — flat, no coarse/fine split until it's earned:

```text
action/
├── commands/    # hand + finger
└── nav/         # leg — routing, navigation, transitions
```

Full example (large projects, once there are enough distinct commands to justify separating coarse actions from fine-grained ones):

```text
action/
├── hand/
├── finger/
└── leg/
```

---

## 🩹 `skin`

Reserved for:

* Public interfaces
* Routes
* Views
* APIs
* Presentation layers

> **The skin exposes the system.**

---

## 🛡️ `immune`

Reserved for:

* Authentication
* Authorization
* Security
* Threat protection
* Defensive rules

Example:

```text
immune/
├── authentication/
├── authorization/
├── security/
└── antibody/
```

---

## 🔬 `lab`

Reserved for:

* Experiments
* Prototypes
* Research
* Proofs of concept

Experimental code should not become permanent production architecture without being moved to its correct location.

---

## 🩺 `doctor`

Reserved for:

* Diagnostics
* Debugging
* Maintenance
* Repair tools

Do not place normal application logic inside `doctor/`.

---

## 🧫 `checkup`

Reserved for:

* Tests
* Health checks
* Quality verification

Example:

```text
checkup/
├── unit/
├── integration/
└── system/
```

---

# 6. Responsibility Rules

Every folder should answer one question:

> **Why does this code exist?**

Every anatomy location should answer another:

> **Why does this code belong here?**

If these questions cannot be answered clearly, reconsider the structure.

---

## Do Not Mix Responsibilities

Bad:

```text
brain/
├── database.py
├── logger.py
├── security.py
├── payment.py
└── decision.py
```

Better:

```text
brain/
└── decision.py

memory/
└── database.py

nerve/
└── logger.py

immune/
└── security.py

soul/
└── payment/
```

---

# 7. Folder Creation Rules

## Rule 1 — No Empty Anatomy

Do not create anatomy folders that have no responsibility.

Bad:

```text
project/
├── eye/
├── ear/
├── nose/
├── heart/
├── lung/
└── kidney/
```

when the application does not use them.

---

## Rule 2 — Create When Needed

Start small:

```text
project/
├── body.py
├── brain/
├── soul/
├── nerve/
└── checkup/
```

Expand when necessary.

---

## Rule 3 — Do Not Create Folders for Single Random Files

Avoid unnecessary nesting.

Bad:

```text
brain/
└── rules/
    └── rules.py
```

Better:

```text
brain/
└── rules.py
```

Create a subfolder only when it represents a meaningful group.

---

# 8. Import Rules

Imports should respect architectural boundaries.

Prefer clear dependency direction.

Recommended:

```text
body
 ↓
brain
 ↓
soul
 ↓
support systems
```

The exact structure may vary by application.

However, dependencies should remain understandable.

---

## Avoid Circular Dependencies

Bad:

```text
brain
  ↓
soul
  ↓
brain
```

Circular dependencies create tight coupling.

Prefer:

```text
brain
  ↓
soul
```

or introduce an abstraction.

---

## Prefer Explicit Dependencies

Bad:

```python
from somewhere import *
```

Better:

```python
from memory.database import Database
```

Clear imports make the anatomy easier to understand.

---

# 9. Dependency Rules

Code Anatomy should encourage loose coupling.

## Prefer

```text
brain/
    ↓
interface
    ↓
memory/
```

over tightly coupling every system directly.

---

## Systems Should Not Know Everything

A module should depend only on what it needs.

Bad:

```text
soul/
    ↓
directly accesses everything
```

Better:

```text
soul/
    ↓
uses defined dependencies
```

> **A healthy software body should not have every organ directly controlling every other organ.**

---

# 10. Feature Rules

Major features belong in `soul/`.

Example:

```text
soul/
├── authentication/
├── payments/
└── users/
```

A feature should contain functionality directly related to that domain.

Example:

```text
soul/
└── payments/
    ├── service.py
    ├── rules.py
    └── types.py
```

Do not split a feature across many locations without a clear architectural reason.

---

## Feature Ownership

A feature owns its domain behavior.

Shared infrastructure should remain outside the feature when it is genuinely reusable.

Example:

```text
soul/
└── payments/

nerve/
└── logger.py

memory/
└── database.py
```

---

# 11. Shared Code Rules

Shared code belongs in `nerve/` only when it is genuinely reusable.

Bad:

```text
nerve/
├── payment_logic.py
├── user_logic.py
└── order_logic.py
```

if those files are only used by one feature.

Better:

```text
soul/
├── payments/
├── users/
└── orders/
```

Use `nerve/` for true shared functionality.

---

# 12. Configuration Rules

Application configuration belongs in `dna/`.

Example:

```text
dna/
├── settings/
├── environment/
├── constants/
└── gene/
```

Do not scatter configuration throughout the project.

Bad:

```text
brain/settings.py
soul/config.py
memory/environment.py
```

Better:

```text
dna/
```

---

# 13. Testing Rules

All tests belong to the application's health system.

```text
checkup/
```

Recommended structure:

```text
checkup/
├── unit/
├── integration/
├── system/
└── health/
```

---

## Test Naming

Follow the language's ecosystem conventions.

Python examples:

```text
test_user.py
test_payment.py
```

JavaScript examples:

```text
user.test.js
payment.test.js
```

TypeScript examples:

```text
user.test.ts
payment.spec.ts
```

The test structure should remain predictable.

---

# 14. Growth Rules

A Code Anatomy project should grow gradually.

## Level 1 — Minimal

```text
body.py
brain/
soul/
nerve/
checkup/
```

---

## Level 2 — Standard

```text
body.py

brain/
soul/
nerve/

heart/
memory/

dna/
skin/
immune/

checkup/
```

---

## Level 3 — Full Anatomy

```text
body.py

brain/
soul/
nerve/

heart/
lung/
digestive/

skeleton/
muscle/

dna/
cells/
memory/

sensory/
action/

skin/
immune/

lab/
doctor/

checkup/
```

> **Architecture should grow with responsibility, not with imagination.**

---

# 15. Anti-Patterns

## ❌ Anatomy Dumping

Using anatomy folders as generic containers.

```text
nerve/
└── everything.py
```

This defeats the purpose of Code Anatomy.

---

## ❌ Random Anatomy

Bad:

```text
brain/
└── database.py
```

```text
lung/
└── user_model.py
```

```text
eye/
└── payment_service.py
```

Anatomy names must match responsibilities.

`brain/database.py` is a specific, recurring version of this mistake — persistence code slowly migrating into `brain/` because "it's already there." **Fix:** `brain/` should only ever import from `soul/`, `nerve/`, and `memory/` — never contain a SQL query or an HTTP route directly. If a file in `brain/` talks to a database or a network socket, it belongs in `memory/` or `lung/` instead.

---

## ❌ God `soul/`

Every feature dropped straight into `soul/` with no subfolders, long after the project has outgrown that:

```text
soul/
├── login.py
├── signup.py
├── orders.py
├── invoices.py
├── refunds.py
├── notifications.py
├── users.py
└── ... (20+ files, no grouping)
```

**Fix:** subdivide by feature once `soul/` crosses roughly 15 files:

```text
soul/
├── auth/
├── orders/
└── notifications/
```

---

## ❌ Over-Anatomizing

Creating too many folders.

Bad:

```text
project/
├── eye/
│   └── scanner/
│       └── image/
│           └── processor/
│               └── ...
```

Do not create deep hierarchy without meaningful separation.

---

## ❌ Duplicate Responsibilities

Bad:

```text
brain/
├── validation.py

nerve/
├── validation.py

immune/
├── validation.py
```

If the same responsibility exists in multiple places, define clear ownership.

For example:

```text
nerve/
└── validation.py
```

General validation belongs in `nerve/`.

Security-specific validation may belong in:

```text
immune/
```

Context matters.

---

## ❌ Forcing Every Biological Organ Into Code

Code Anatomy is inspired by biology.

It does not require reproducing the entire human body as folders.

Do not create folders simply because an organ exists.

Examples of unnecessary folders:

```text
project/
├── eyebrow/
├── toenail/
├── appendix/
└── earlobe/
```

unless your architecture has a genuinely useful and clearly documented responsibility for them.

> **No responsibility, no anatomy.**

---

## ❌ Organ-per-File

Inventing a brand-new anatomy folder — outside the official vocabulary — for a single file, because the metaphor happened to fit:

```text
project/
├── brain/
├── soul/
└── whisker/          # one file, invented because "sensing small signals" sounded like a whisker
    └── ping.py
```

This is a specific case of the two problems above at once: it invents anatomy that was never proposed (see the RFC process in `.github/ISSUE_TEMPLATE/anatomy_proposal.md`) to hold what Rule 3 already says shouldn't get its own folder. Put it in the closest existing organ, or in `nerve/` if it's genuinely shared support.

---

# 16. The Final Code Anatomy Rules

## 🧠 Rule One

> **Responsibility comes before naming.**

---

## 🧬 Rule Two

> **Meaning comes before creativity.**

---

## 🦴 Rule Three

> **Every anatomy name has a defined responsibility.**

---

## ⚡ Rule Four

> **Shared code must be genuinely shared.**

---

## ❤️ Rule Five

> **Keep dependencies understandable.**

---

## 🧫 Rule Six

> **Do not create anatomy without responsibility.**

---

## 🛡️ Rule Seven

> **Do not mix unrelated responsibilities.**

---

## 📈 Rule Eight

> **Start small and grow naturally.**

---

## 🧭 Rule Nine

> **Follow the official hierarchy when possible.**

See:

```text
ARCHITECTURE.md
```

---

## 📖 Rule Ten

> **When uncertain, follow the decision guide.**

See:

```text
GUIDE.md
```

---

# 🧍 The Code Anatomy Convention

```text
Every file has a responsibility.

Every responsibility has an owner.

Every owner has a place.

Every place has a meaning.

Every name should remain consistent.
```

---

# 🧬 Final Principle

Code Anatomy is not about making software sound biological.

It is about creating an architecture where developers can understand:

* What a piece of code does.
* Why it exists.
* Where it belongs.
* What it depends on.
* How it connects to the rest of the system.

> **A good architecture should make the correct location feel obvious.**

---

# 🧠 Remember

> **Do not organize code by random technical habit.**

> **Organize code by responsibility.**

> **Give responsibility a meaningful place.**

> **Build software like a living system.**