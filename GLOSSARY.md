# 📖 Code Anatomy Glossary

> **The official vocabulary of Code Anatomy.**

This glossary defines the core terms used throughout the **Code Anatomy** convention.

Use this document when you need to understand:

* 🧠 What an anatomy term means
* 📁 Where a type of code belongs
* 🧬 The difference between similar anatomy parts
* 📏 The official meaning of Code Anatomy terminology

> **One term should have one clear meaning.**

---

# 📚 Table of Contents

## Core Anatomy

* [Body](#body)
* [Brain](#brain)
* [Soul](#soul)
* [Nerve](#nerve)
* [Heart](#heart)
* [Memory](#memory)
* [Blood](#blood)
* [Lung](#lung)
* [Digestive System](#digestive-system)
* [Skeleton](#skeleton)
* [Muscle](#muscle)
* [DNA](#dna)
* [Cell](#cell)
* [Sensory System](#sensory-system)
* [Action System](#action-system)
* [Skin](#skin)
* [Immune System](#immune-system)

## Development Anatomy

* [Checkup](#checkup)
* [Doctor](#doctor)
* [Lab](#lab)

## General Terms

* [Anatomy](#anatomy)
* [Responsibility](#responsibility)
* [Role](#role)
* [Boundary](#boundary)
* [Feature](#feature)
* [Shared Code](#shared-code)
* [Architecture](#architecture)
* [Convention](#convention)
* [Dependency](#dependency)

---

# 🧍 Body

### Official Name

```text id="7e2qaa"
body
```

### Responsibility

The **body** represents the complete application.

It brings the major parts of the system together.

### Typical Use

```text id="jx7k7j"
body.py
body.js
body.ts
```

### Contains

* Application startup
* Application initialization
* Lifecycle coordination
* System assembly

### Traditional Equivalent

```text id="9vpe1h"
main.py
app.py
index.js
program.py
```

### Core Meaning

> **The body brings the application together.**

---

# 🧠 Brain

### Official Name

```text id="9ky1q2"
brain/
```

### Responsibility

The **brain** contains decision-making and application intelligence.

### Typical Use

* Business rules
* Decision logic
* Workflows
* Policies
* Complex processing decisions

### Traditional Equivalent

```text id="qej2yo"
services/
business/
logic/
rules/
```

### Core Meaning

> **The brain thinks and decides.**

---

# 🧬 Soul

### Official Name

```text id="mtkkh1"
soul/
```

### Responsibility

The **soul** contains the major features and core capabilities of an application.

It represents what makes the application what it is.

### Typical Use

* Authentication
* Users
* Payments
* Orders
* Notifications

### Traditional Equivalent

```text id="hliohh"
modules/
features/
domains/
```

### Core Meaning

> **The soul defines what the application does.**

---

# ⚡ Nerve

### Official Name

```text id="a5t2bf"
nerve/
```

### Responsibility

The **nerve system** provides internal communication and shared support.

### Typical Use

* Shared utilities
* Logging
* Validation
* Events
* Internal communication
* Reusable helpers

### Traditional Equivalent

```text id="4cytct"
utils/
helpers/
common/
shared/
```

### Core Meaning

> **The nerves connect and support the system.**

---

# ❤️ Heart

### Official Name

```text id="gmgtit"
heart/
```

### Responsibility

The **heart** drives central and continuous system activity.

### Typical Use

* Background processes
* Workers
* Schedulers
* Processing loops
* Central coordination

### Traditional Equivalent

```text id="ibw9nc"
workers/
scheduler/
processor/
engine/
```

### Core Meaning

> **The heart drives the system.**

---

# 🧠 Memory

### Official Name

```text id="wgyn8v"
memory/
```

### Responsibility

The **memory** stores and retrieves information.

### Typical Use

* Databases
* Cache
* Sessions
* State
* Persistent storage

### Traditional Equivalent

```text id="p4ysv8"
database/
storage/
cache/
state/
```

### Core Meaning

> **The memory remembers.**

---

# 🩸 Blood

### Official Name

```text id="m8ohax"
blood/
```

### Responsibility

The **blood** represents the movement of information throughout the system.

### Typical Use

* Data pipelines
* Data transport
* Data flow
* Event streams
* Message movement

### Traditional Equivalent

```text id="ad29ve"
pipeline/
stream/
transport/
dataflow/
```

### Core Meaning

> **The blood moves information.**

---

# 🫁 Lung

### Official Name

```text id="glvt2s"
lung/
```

### Responsibility

The **lungs** handle communication between the application and external systems.

### Typical Use

* API clients
* HTTP communication
* WebSockets
* Third-party integrations
* External services

### Traditional Equivalent

```text id="6pms00"
network/
clients/
integrations/
external/
```

### Core Meaning

> **The lungs communicate with the outside world.**

---

# 🍽️ Digestive System

### Official Name

```text id="yhzs3q"
digestive/
```

### Responsibility

The **digestive system** receives and processes incoming information.

It breaks raw input into usable information.

### Typical Use

* Parsing
* Extraction
* Transformation
* Filtering
* Input processing

### Traditional Equivalent

```text id="vf22y6"
parser/
processor/
transformer/
input/
```

### Core Meaning

> **The digestive system processes what enters the application.**

---

# 🦴 Skeleton

### Official Name

```text id="wwr3t6"
skeleton/
```

### Responsibility

The **skeleton** provides the structural foundation of the application.

### Typical Use

* Models
* Schemas
* Interfaces
* Types
* Base structures

### Traditional Equivalent

```text id="jpn3uc"
models/
schemas/
types/
interfaces/
```

### Core Meaning

> **The skeleton provides structure.**

---

# 💪 Muscle

### Official Name

```text id="p3b2l9"
muscle/
```

### Responsibility

The **muscles** perform specific work.

### Typical Use

* Heavy computation
* Background execution
* Processing tasks
* Intensive operations

### Traditional Equivalent

```text id="t7zqky"
workers/
tasks/
jobs/
processors/
```

### Core Meaning

> **The muscles perform work.**

---

# 🧬 DNA

### Official Name

```text id="s6k2wc"
dna/
```

### Responsibility

The **DNA** defines the configuration and fundamental behavior of the application.

### Typical Use

* Settings
* Configuration
* Constants
* Environment definitions
* Feature flags

### Traditional Equivalent

```text id="8c28zk"
config/
settings/
environment/
constants/
```

### Core Meaning

> **DNA defines how the system behaves.**

---

# 🧫 Cell

### Official Name

```text id="im2s7d"
cells/
```

### Responsibility

**Cells** represent small, independent building blocks that combine to create larger systems.

### Typical Use

* Reusable components
* Small units
* Independent building blocks
* Isolated functional parts

### Traditional Equivalent

```text id="4e5kmf"
components/
units/
parts/
```

### Core Meaning

> **Cells are the small building blocks of the system.**

---

# 👁️ Sensory System

### Official Name

```text id="ntoe1z"
sensory/
```

### Responsibility

The **sensory system** observes, listens, detects, and monitors.

### Typical Use

* Monitoring
* Event listening
* Detection
* Scanning
* Observation

### Common Subsystems

```text id="c0sgt1"
sensory/
├── eye/
├── ear/
└── nose/
```

### Core Meaning

> **The sensory system observes the environment.**

---

# ✋ Action System

### Official Name

```text id="bc3ozo"
action/
```

### Responsibility

The **action system** performs direct actions.

### Typical Use

* Commands
* Operations
* Execution
* Navigation
* Triggered actions

### Common Subsystems

```text id="xq2nvi"
action/
├── hand/
├── finger/
└── leg/
```

### Core Meaning

> **The action system performs actions.**

---

# 🛡️ Skin

### Official Name

```text id="wn6kt9"
skin/
```

### Responsibility

The **skin** represents the boundary between the application and its users or external consumers.

### Typical Use

* APIs
* Routes
* Controllers
* Views
* Public interfaces

### Traditional Equivalent

```text id="a2t3jk"
api/
routes/
controllers/
presentation/
```

### Core Meaning

> **The skin exposes the system.**

---

# 🛡️ Immune System

### Official Name

```text id="clw3y6"
immune/
```

### Responsibility

The **immune system** protects the application from unauthorized access, invalid behavior, and threats.

### Typical Use

* Authentication
* Authorization
* Security
* Threat detection
* Defensive mechanisms

### Traditional Equivalent

```text id="n9b59m"
security/
auth/
protection/
```

### Core Meaning

> **The immune system protects the body.**

---

# 🧪 Checkup

### Official Name

```text id="rqrf3f"
checkup/
```

### Responsibility

A **checkup** verifies that the software system is healthy.

### Typical Use

* Unit tests
* Integration tests
* System tests
* Health checks

### Traditional Equivalent

```text id="gj91fk"
tests/
testing/
```

### Core Meaning

> **The checkup verifies system health.**

---

# 🩺 Doctor

### Official Name

```text id="w2ntmx"
doctor/
```

### Responsibility

The **doctor** helps diagnose and repair problems in the system.

### Typical Use

* Debugging tools
* Diagnostics
* Repair scripts
* Maintenance tools

### Traditional Equivalent

```text id="l1w37u"
debug/
diagnostics/
tools/
maintenance/
```

### Core Meaning

> **The doctor diagnoses and repairs.**

---

# 🔬 Lab

### Official Name

```text id="gm5y7s"
lab/
```

### Responsibility

The **lab** is used for experimentation and research.

### Typical Use

* Experiments
* Prototypes
* Research
* Proofs of concept

### Traditional Equivalent

```text id="gqvhkx"
experiments/
research/
prototype/
sandbox/
```

### Core Meaning

> **The lab experiments.**

---

# 🧬 Anatomy

### Definition

An **anatomy** is an officially defined organizational concept within Code Anatomy.

Examples:

```text id="7c0w4g"
brain/
soul/
memory/
immune/
```

Each anatomy has a specific responsibility.

> **An anatomy name is not just a creative label. It represents an architectural role.**

---

# 🎯 Responsibility

### Definition

A **responsibility** is the primary purpose of a piece of code.

Examples:

```text id="jq86yz"
Makes decisions
    ↓
brain/
```

```text id="eb65g5"
Stores information
    ↓
memory/
```

```text id="jyo5s2"
Protects the system
    ↓
immune/
```

### Core Principle

> **One piece of code should have one primary responsibility whenever possible.**

---

# 🎭 Role

### Definition

A **role** describes the function that a part of the system performs.

Example:

```text id="dw8g7m"
brain/
```

Role:

```text id="5l8lnq"
Decision-making
```

The role determines where code belongs.

---

# 🚧 Boundary

### Definition

A **boundary** defines what belongs inside an anatomy and what does not.

Example:

```text id="tkh74a"
memory/
```

belongs to:

* Storage
* Retrieval
* State

It does not automatically contain:

* Business decisions
* API routes
* User interfaces

Clear boundaries prevent architectural confusion.

---

# 🧩 Feature

### Definition

A **feature** is a major capability provided by an application.

Examples:

```text id="gw3lrx"
authentication
payments
users
notifications
```

In Code Anatomy, major features usually belong to:

```text id="erau66"
soul/
```

---

# ⚡ Shared Code

### Definition

**Shared code** is functionality used by multiple parts of the application.

Examples:

* Logging
* General validation
* Formatting
* Common helpers

Shared support generally belongs in:

```text id="t4xg0v"
nerve/
```

> **Code should not be placed in `nerve/` simply because its location is unclear.**

---

# 🏗️ Architecture

### Definition

**Architecture** describes how different parts of a software system are organized and connected.

In Code Anatomy, architecture focuses on:

* Responsibility
* Structure
* Boundaries
* Relationships
* Dependencies

---

# 📏 Convention

### Definition

A **convention** is an agreed rule for organizing and naming code.

Examples include:

* Folder naming
* File naming
* Import direction
* Anatomy responsibilities

The official Code Anatomy conventions are defined in:

```text id="qny7qz"
CONVENTIONS.md
```

---

# 🔗 Dependency

### Definition

A **dependency** exists when one part of the application requires another part to function.

Example:

```text id="m8crz8"
brain/
   │
   ▼
memory/
```

Dependencies should remain:

* Clear
* Limited
* Understandable

Avoid unnecessary circular dependencies.

---

# 🔄 Related Anatomy

Some anatomy terms are closely related.

---

## 🧠 Brain vs 🧬 Soul

```text id="goc6wi"
Brain → Decides how something works.

Soul → Contains what the application does.
```

Example:

```text id="ikuvxy"
soul/payments/
```

contains the payment capability.

```text id="8de45l"
brain/
```

may contain rules that decide whether a payment is allowed.

---

## ⚡ Nerve vs 🫁 Lung

```text id="zc4sck"
Nerve → Internal communication.

Lung → External communication.
```

---

## ❤️ Heart vs 💪 Muscle

```text id="1fdosr"
Heart → Drives continuous system activity.

Muscle → Performs specific work.
```

---

## 🧠 Memory vs 🦴 Skeleton

```text id="u9n78m"
Memory → Stores information.

Skeleton → Defines the structure of information.
```

---

## 🛡️ Skin vs 🫁 Lung

```text id="vcguxj"
Skin → Exposes the application.

Lung → Communicates with external systems.
```

---

## 👁️ Sensory vs ✋ Action

```text id="35s3qu"
Sensory → Observes.

Action → Performs.
```

---

# 🧭 Quick Reference Table

| Anatomy         | Primary Responsibility                    |
| --------------- | ----------------------------------------- |
| 🧍 `body`       | Application assembly and lifecycle        |
| 🧠 `brain`      | Decisions and logic                       |
| 🧬 `soul`       | Features and capabilities                 |
| ⚡ `nerve`       | Shared support and internal communication |
| ❤️ `heart`      | Central and continuous processing         |
| 🧠 `memory`     | Storage and state                         |
| 🩸 `blood`      | Data movement and flow                    |
| 🫁 `lung`       | External communication                    |
| 🍽️ `digestive` | Input and data processing                 |
| 🦴 `skeleton`   | Models and structural definitions         |
| 💪 `muscle`     | Heavy work and execution                  |
| 🧬 `dna`        | Configuration and fundamental behavior    |
| 🧫 `cells`      | Small building blocks                     |
| 👁️ `sensory`   | Observation and detection                 |
| ✋ `action`      | Commands and actions                      |
| 🛡️ `skin`      | Public-facing interfaces                  |
| 🛡️ `immune`    | Security and protection                   |
| 🧪 `checkup`    | Testing and health verification           |
| 🩺 `doctor`     | Diagnostics and maintenance               |
| 🔬 `lab`        | Experiments and research                  |

---

# 🧠 The Glossary Rule

When an anatomy term is used in Code Anatomy:

> **Its meaning should remain consistent.**

Do not redefine an existing anatomy differently from project to project without documentation.

Consistency allows developers to build a shared mental model.

---

# 🧍 Final Principle

```text id="t6mkrw"
A name represents a role.

A role represents a responsibility.

A responsibility determines a place.

A place belongs to the system.
```

> **Clear vocabulary creates clear architecture.**

---

# 📖 Learn More

For the complete Code Anatomy documentation:

```text id="c2ngip"
README.md
```

Introduction and philosophy.

```text id="2gvcmp"
ARCHITECTURE.md
```

Official architecture hierarchy.

```text id="h9xj04"
GUIDE.md
```

Decision tree and practical examples.

```text id="pmfxpm"
CONVENTIONS.md
```

Official naming and organization rules.

```text id="w4z8k7"
CONTRIBUTING.md
```

Contribution guidelines.

---

# 🧬 Code Anatomy

> **Every part has a name.**

> **Every name has a meaning.**

> **Every meaning has a responsibility.**

> **Every responsibility has a place.**
