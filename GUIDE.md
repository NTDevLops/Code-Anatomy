# 🧭 Code Anatomy Guide

> **A practical guide for deciding where your code belongs.**

This guide helps developers apply the **Code Anatomy** convention to real projects.

It includes:

* 🧭 The Code Anatomy Decision Tree
* 🐍 Python examples
* 🟨 JavaScript examples
* 🔷 TypeScript examples
* 📁 Real project structures
* 🧠 Practical naming guidance

The main rule is simple:

> **Organize code by responsibility.**

The human-body metaphor should help developers understand where code belongs.

---

# 🧭 The Code Anatomy Decision Tree

Before creating a new file or folder, ask the following questions.

```text
START
  │
  ▼
Does this code start the application?
  │
  ├── YES → body.py
  │
  └── NO
        │
        ▼
Does it contain major business decisions?
        │
        ├── YES → brain/
        │
        └── NO
              │
              ▼
Is it a major application feature?
              │
              ├── YES → soul/
              │
              └── NO
                    │
                    ▼
Is it shared support code?
                    │
                    ├── YES → nerve/
                    │
                    └── NO
                          │
                          ▼
Does it automatically react to events?
                          │
                          ├── YES → nerve/reflex/
                          │
                          └── NO
                                │
                                ▼
Does it run continuous or central processes?
                                │
                                ├── YES → heart/
                                │
                                └── NO
                                      │
                                      ▼
Does it store or remember information?
                                      │
                                      ├── YES → memory/
                                      │
                                      └── NO
                                            │
                                            ▼
Does it communicate with external services?
                                            │
                                            ├── YES → lung/
                                            │
                                            └── NO
                                                  │
                                                  ▼
Does it receive, parse, or process input?
                                                  │
                                                  ├── YES → digestive/
                                                  │
                                                  └── NO
                                                        │
                                                        ▼
Does it define models or structure?
                                                        │
                                                        ├── YES → skeleton/
                                                        │
                                                        └── NO
                                                              │
                                                              ▼
Does it perform heavy computation?
                                                              │
                                                              ├── YES → muscle/
                                                              │
                                                              └── NO
                                                                    │
                                                                    ▼
Does it configure the application?
                                                                    │
                                                                    ├── YES → dna/
                                                                    │
                                                                    └── NO
                                                                          │
                                                                          ▼
Does it observe or listen?
                                                                          │
                                                                          ├── YES → sensory/
                                                                          │
                                                                          └── NO
                                                                                │
                                                                                ▼
Does it perform an action?
                                                                                │
                                                                                ├── YES → action/
                                                                                │
                                                                                └── NO
                                                                                      │
                                                                                      ▼
Does it expose an interface?
                                                                                      │
                                                                                      ├── YES → skin/
                                                                                      │
                                                                                      └── NO
                                                                                            │
                                                                                            ▼
Does it protect the system?
                                                                                            │
                                                                                            ├── YES → immune/
                                                                                            │
                                                                                            └── NO
                                                                                                  │
                                                                                                  ▼
Does it test the application?
                                                                                                  │
                                                                                                  ├── YES → checkup/
                                                                                                  │
                                                                                                  └── NO
                                                                                                        │
                                                                                                        ▼
                                                                                                  Reconsider
                                                                                                  the responsibility.
```

---

# 🧠 Quick Decision Guide

## Does it think?

```text
brain/
```

Examples:

* Business rules
* Decisions
* Complex workflows
* Application logic

---

## Is it a major feature?

```text
soul/
```

Examples:

* Authentication
* Payments
* User management
* Notifications

---

## Does it support multiple parts?

```text
nerve/
```

Examples:

* Logging
* Validation
* Formatting
* Shared helpers

---

## Does it remember?

```text
memory/
```

Examples:

* Database access
* Cache
* Sessions
* Application state

---

## Does it communicate outside?

```text
lung/
```

Examples:

* External APIs
* HTTP clients
* WebSockets
* Third-party services

---

## Does it process incoming information?

```text
digestive/
```

Examples:

* Parsing
* Tokenization
* Transformation
* Filtering

---

## Does it define structure?

```text
skeleton/
```

Examples:

* Models
* Schemas
* Interfaces
* Base classes

---

## Does it perform heavy work?

```text
muscle/
```

Examples:

* Workers
* Computation
* Background processing

---

## Does it define behavior?

```text
dna/
```

Examples:

* Configuration
* Settings
* Constants
* Feature flags

---

## Does it observe or listen?

```text
sensory/
```

Examples:

* Monitoring
* Event listeners
* Detection
* Scanning

---

## Does it perform actions?

```text
action/
```

Examples:

* Commands
* Operations
* Execution
* Navigation

---

## Does it protect?

```text
immune/
```

Examples:

* Authentication
* Authorization
* Security
* Threat detection

---

# 🐍 Python Example

A Python project using Code Anatomy.

```text
my_project/
│
├── body.py
│
├── brain/
│   ├── __init__.py
│   ├── decision.py
│   └── workflow.py
│
├── soul/
│   ├── __init__.py
│   │
│   ├── users/
│   │   ├── __init__.py
│   │   └── service.py
│   │
│   └── authentication/
│       ├── __init__.py
│       └── service.py
│
├── nerve/
│   ├── __init__.py
│   ├── logger.py
│   └── validator.py
│
├── heart/
│   ├── __init__.py
│   ├── processor.py
│   └── scheduler.py
│
├── memory/
│   ├── __init__.py
│   ├── database.py
│   └── cache.py
│
├── skeleton/
│   ├── __init__.py
│   └── models.py
│
├── dna/
│   ├── __init__.py
│   └── settings.py
│
├── immune/
│   ├── __init__.py
│   └── security.py
│
└── checkup/
    ├── __init__.py
    └── test_system.py
```

---

## Python Entry Point

### Traditional

```python
main.py
```

### Code Anatomy

```python
body.py
```

Example:

```python
from brain.workflow import run
from dna.settings import settings


def body():
    run(settings)


if __name__ == "__main__":
    body()
```

---

# 🐍 Python Example: Feature

Traditional structure:

```text
modules/
└── authentication/
    └── auth.py
```

Code Anatomy:

```text
soul/
└── authentication/
    └── service.py
```

Example:

```python
class Authentication:
    def login(self, username, password):
        pass
```

The authentication system is part of the application's purpose.

Therefore:

```text
soul/authentication/
```

---

# 🐍 Python Example: Business Logic

Traditional:

```text
services/
└── payment_service.py
```

Code Anatomy:

```text
brain/
└── payment/
    └── decision.py
```

If the code contains important decisions:

```python
def can_process_payment(user, amount):
    return user.balance >= amount
```

It belongs to:

```text
brain/
```

Because:

> **The brain decides.**

---

# 🟨 JavaScript Example

A JavaScript project can use the same Code Anatomy structure.

```text
my-project/
│
├── body.js
│
├── brain/
│   ├── decision.js
│   └── workflow.js
│
├── soul/
│   ├── authentication/
│   │   └── service.js
│   │
│   └── users/
│       └── service.js
│
├── nerve/
│   ├── logger.js
│   └── validator.js
│
├── memory/
│   ├── database.js
│   └── cache.js
│
├── lung/
│   └── apiClient.js
│
├── dna/
│   └── settings.js
│
└── checkup/
    └── system.test.js
```

---

## JavaScript Entry Point

Traditional:

```javascript
index.js
```

or:

```javascript
app.js
```

Code Anatomy:

```javascript
body.js
```

Example:

```javascript
import { run } from "./brain/workflow.js";

function body() {
    run();
}

body();
```

---

# 🔷 TypeScript Example

A TypeScript project.

```text
my-project/
│
├── body.ts
│
├── brain/
│   ├── decision.ts
│   └── workflow.ts
│
├── soul/
│   ├── authentication/
│   │   ├── service.ts
│   │   └── types.ts
│   │
│   └── users/
│       └── service.ts
│
├── nerve/
│   ├── logger.ts
│   └── validator.ts
│
├── skeleton/
│   ├── models/
│   └── interfaces/
│
├── memory/
│   ├── database.ts
│   └── cache.ts
│
├── immune/
│   └── security.ts
│
└── checkup/
    └── system.test.ts
```

---

# 🔷 TypeScript Models

Traditional:

```text
models/
```

Code Anatomy:

```text
skeleton/
```

Example:

```text
skeleton/
├── models/
│   └── User.ts
│
└── interfaces/
    └── UserRepository.ts
```

The model provides structural support.

Therefore:

> **The skeleton provides structure.**

---

# 🌐 Web Application Example

A web application using Code Anatomy.

```text
web-app/
│
├── body.py
│
├── brain/
│   ├── workflow/
│   └── rules/
│
├── soul/
│   ├── users/
│   ├── authentication/
│   └── payments/
│
├── nerve/
│   ├── logger/
│   ├── validator/
│   └── communication/
│
├── heart/
│   ├── workers/
│   └── scheduler/
│
├── lung/
│   ├── clients/
│   └── websocket/
│
├── digestive/
│   ├── mouth/
│   ├── teeth/
│   ├── stomach/
│   └── liver/
│
├── skeleton/
│   ├── models/
│   ├── schemas/
│   └── interfaces/
│
├── memory/
│   ├── database/
│   ├── cache/
│   └── state/
│
├── sensory/
│   ├── eye/
│   ├── ear/
│   └── nose/
│
├── action/
│   ├── hand/
│   └── leg/
│
├── skin/
│   ├── api/
│   ├── routes/
│   └── views/
│
├── immune/
│   ├── authentication/
│   ├── authorization/
│   └── security/
│
├── dna/
│   └── settings/
│
└── checkup/
```

---

# 🔄 Traditional Names vs Code Anatomy

| Traditional Name | Code Anatomy         |
| ---------------- | -------------------- |
| `main.py`        | `body.py`            |
| `app.py`         | `body.py`            |
| `utils/`         | `nerve/`             |
| `helpers/`       | `nerve/`             |
| `modules/`       | `soul/`              |
| `features/`      | `soul/`              |
| `services/`      | `brain/` or `heart/` |
| `config/`        | `dna/`               |
| `models/`        | `skeleton/`          |
| `schemas/`       | `skeleton/`          |
| `database/`      | `memory/`            |
| `cache/`         | `memory/cache/`      |
| `network/`       | `lung/`              |
| `clients/`       | `lung/`              |
| `security/`      | `immune/`            |
| `tests/`         | `checkup/`           |
| `debug/`         | `doctor/`            |
| `experiments/`   | `lab/`               |

---

# 🧩 How to Choose Between Similar Anatomy Parts

Some responsibilities may appear similar.

This guide helps differentiate them.

---

## 🧠 Brain vs ❤️ Heart

### Brain

Use when code decides.

```text
brain/
```

Example:

```python
if user.is_admin:
    allow_access()
```

### Heart

Use when code continuously drives processing.

```text
heart/
```

Example:

```python
while True:
    process_jobs()
```

### Rule

> **Brain decides. Heart drives.**

---

## 🧬 Soul vs 🧠 Brain

### Soul

Contains major application features.

```text
soul/
└── payments/
```

### Brain

Contains the logic that decides how things work.

```text
brain/
└── payment_decision.py
```

### Rule

> **Soul provides the capability. Brain decides how it behaves.**

---

## ⚡ Nerve vs 🫁 Lung

### Nerve

Internal communication.

```text
nerve/
```

### Lung

External communication.

```text
lung/
```

### Rule

> **Nerves communicate inside. Lungs communicate outside.**

---

## 🧠 Memory vs 🦴 Skeleton

### Memory

Stores information.

```text
memory/
```

### Skeleton

Defines the structure of information.

```text
skeleton/
```

### Rule

> **Memory stores the data. Skeleton defines its shape.**

---

## 💪 Muscle vs ❤️ Heart

### Muscle

Performs specific heavy work.

```text
muscle/
```

### Heart

Coordinates and continuously drives the system.

```text
heart/
```

### Rule

> **Muscles execute. The heart drives.**

---

## 👂 Ear vs ⚡ Reflex

### Ear

Receives a signal.

```text
sensory/ear/
```

### Reflex

Automatically reacts to a signal.

```text
nerve/reflex/
```

### Rule

```text
ear → receives
reflex → reacts
```

---

## 🛡️ Skin vs 🫁 Lung

### Skin

The public-facing boundary.

```text
skin/
```

### Lung

Communication with external systems.

```text
lung/
```

### Rule

> **Skin exposes. Lungs communicate.**

---

# 🏗️ Recommended Starting Structures

## Small Application

```text
project/
│
├── body.py
├── brain/
├── soul/
├── nerve/
├── dna/
└── checkup/
```

---

## Medium Application

```text
project/
│
├── body.py
│
├── brain/
├── soul/
├── nerve/
│
├── heart/
├── memory/
│
├── skeleton/
├── dna/
│
├── skin/
├── immune/
│
└── checkup/
```

---

## Large Application

```text
project/
│
├── body.py
│
├── brain/
├── soul/
├── nerve/
│
├── heart/
├── lung/
├── digestive/
│
├── skeleton/
├── muscle/
│
├── dna/
├── cells/
├── memory/
│
├── sensory/
├── action/
│
├── skin/
├── immune/
│
├── lab/
├── doctor/
│
└── checkup/
```

---

# ⚠️ Common Mistakes

## ❌ Creating Every Folder

Bad:

```text
project/
├── brain/
├── heart/
├── lung/
├── kidney/
├── eye/
├── ear/
├── nose/
└── ...
```

when most folders are empty.

### Better

Create anatomy only when the application needs it.

> **No responsibility, no folder.**

---

## ❌ Choosing Names Only Because They Sound Cool

Bad:

```text
brain/
└── random_utils.py
```

Better:

```text
nerve/
└── utility.py
```

The responsibility should determine the location.

---

## ❌ Mixing Responsibilities

Bad:

```text
brain/
├── database.py
├── logger.py
├── security.py
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
```

---

# 🧬 The Final Decision Rule

When uncertain, ask these questions in order:

```text
1. What does this code do?

2. Is it a feature?

3. Is it decision-making?

4. Is it support code?

5. Does it store information?

6. Does it communicate?

7. Does it process information?

8. Does it define structure?

9. Does it perform actions?

10. Does it protect the application?
```

Then choose the anatomy that best represents the responsibility.

---

# 🧠 Final Principle

> **Code Anatomy is not about replacing every technical word with a body part.**

It is about creating a meaningful mental model for software architecture.

```text
The body contains the system.

The brain thinks.

The soul provides purpose.

The nerves connect.

The heart drives.

The memory remembers.

The skeleton provides structure.

The muscles work.

The lungs communicate.

The senses observe.

The hands act.

The skin exposes.

The immune system protects.

The DNA defines behavior.

The checkup ensures health.
```

> **A good architecture is not the one with the most folders.**

> **A good architecture is the one where every developer knows where code belongs.**

---

# 🧍 Code Like a Living System

> **Every part has a role.**
>
> **Every role has a place.**
>
> **Every place has meaning.**

**Build software like a living system.**
