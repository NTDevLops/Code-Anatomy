# 🧠 Code Anatomy

> **Organize software like a living system.**

**Code Anatomy** is a human-body-inspired coding convention for organizing files, folders, and application architecture.

Instead of viewing a project as a random collection of technical directories, this approach treats software as a living system where every part has a meaningful role.

A program has:

* 🧍 A **body** that brings everything together.
* 🧠 A **brain** that thinks and makes decisions.
* 🧬 A **soul** that defines its purpose.
* ⚡ A **nervous system** that connects its parts.
* ❤️ A **heart** that keeps processes moving.
* 🩸 A **circulatory system** that moves information.
* 🫁 A **respiratory system** that communicates externally.
* 🍽️ A **digestive system** that processes information.
* 🦴 A **skeleton** that provides structure.
* 💪 A **muscular system** that performs heavy work.
* 🧬 A **genetic system** that defines instructions.
* 🧫 **Cells** that build the system.
* 👁️ Sensory organs that observe and receive signals.
* ✋ Parts that perform actions.
* 🛡️ An **immune system** that protects it.
* 🩺 Tools that diagnose, test, and maintain it.

The goal is not to replace standard conventions simply for the sake of creativity.

The goal is to create a naming system that is:

* 🧠 Meaningful
* 🫀 Consistent
* 🧬 Memorable
* 🦴 Structured
* 🔧 Scalable

---

# 🫀 The Core Principle

> **Every piece of code should have a role.**
>
> **Every role should have a meaningful place.**

Before creating a new file or folder, ask:

> **What role does this code play in the software body?**

If it makes decisions, it belongs to the **brain**.

If it represents a major feature, it belongs to the **soul**.

If it supports communication, it belongs to the **nervous system**.

If it stores information, it belongs to **memory**.

If it processes incoming information, it may belong to the **digestive system**.

If it protects the application, it belongs to the **immune system**.

If it observes something, it belongs to the **sensory system**.

If it performs an action, it belongs to the **action system**.

The structure should describe the responsibility of the code—not just its technical category.

---

# 🧍 The Anatomy of a Project

Code Anatomy is divided into major biological systems.

* 🧍 Core Anatomy
* 🧠 Nervous System
* ❤️ Circulatory System
* 🫁 Respiratory System
* 🍽️ Digestive System
* 🦴 Skeletal System
* 💪 Muscular System
* 🧬 Genetic System
* 🧫 Cellular System
* 🧠 Memory System
* 👁️ Sensory System
* ✋ Action and Movement System
* 🛡️ Immune System
* 🧍 External System
* 🩺 Development and Maintenance

> **Not every project needs every anatomy part.**

Start with the core anatomy and expand only when the project needs additional responsibilities.

---

# 🧍 Core Anatomy

These components form the foundation of Code Anatomy.

```text
project/
│
├── body.py       # Application entry point
├── brain/        # Decisions and application logic
├── soul/         # Core features and domain modules
└── nerve/        # Shared support and communication
```

---

## 🧍 `body.py`

The **body** brings the entire application together.

It is the primary entry point of the system.

Traditional equivalents:

```text
main.py
app.py
program.py
```

### Use `body.py` for:

* Starting the application
* Initializing major components
* Connecting major systems
* Managing the application lifecycle

> **The body brings the entire system together.**

---

## 🧠 `brain/`

The **brain** thinks.

This is where important decisions and application logic belong.

```text
brain/
├── decision.py
├── workflow.py
├── rules.py
└── intelligence.py
```

### Use `brain/` for:

* Decision-making
* Business logic
* Application workflows
* Rules
* Complex processing
* Intelligent systems

> **The brain decides what the system should do.**

---

## 🧬 `soul/`

The **soul** represents what makes the application what it is.

It contains the major capabilities and domain features.

```text
soul/
├── authentication/
├── payments/
├── users/
└── notifications/
```

### Use `soul/` for:

* Major features
* Domain functionality
* Core modules
* Business capabilities

> **The soul gives the application its purpose.**

---

# 🧠 Nervous System

The nervous system allows different parts of the application to communicate.

---

## ⚡ `nerve/`

```text
nerve/
├── logger.py
├── validator.py
├── formatter.py
└── helper.py
```

### Use `nerve/` for:

* Shared utilities
* Logging
* Validation
* Formatting
* Communication helpers
* Reusable support functions

> **The nerves connect different parts of the system.**

---

## ⚡ `reflex/`

A reflex is an immediate automatic reaction.

```text
reflex/
├── trigger.py
├── handler.py
└── reaction.py
```

### Use `reflex/` for:

* Event handlers
* Automatic triggers
* Immediate reactions
* Reactive systems

> **The reflex reacts automatically.**

---

# ❤️ Circulatory System

The circulatory system keeps important resources moving.

---

## ❤️ `heart/`

The heart keeps the system active.

```text
heart/
├── processor.py
├── scheduler.py
└── worker.py
```

### Use `heart/` for:

* Central processing
* Background workers
* Schedulers
* Continuous operations
* Core workflows

> **The heart keeps the system moving.**

---

## 🩸 `blood/`

Blood represents the movement of information.

```text
blood/
├── pipeline.py
├── stream.py
└── flow.py
```

### Use `blood/` for:

* Data pipelines
* Data streams
* Information flow
* Data transformation pipelines

> **The blood moves information.**

---

## 🩸 `vessel/`

Vessels provide channels through which blood moves.

```text
vessel/
├── channel.py
├── connector.py
└── stream.py
```

### Use `vessel/` for:

* Internal channels
* Data connections
* Communication paths
* Message routes

> **The vessels carry information between systems.**

---

# 🫁 Respiratory System

The respiratory system connects the body with the outside world.

---

## 🫁 `lung/`

```text
lung/
├── api.py
├── client.py
└── websocket.py
```

### Use `lung/` for:

* External APIs
* Network communication
* WebSockets
* Third-party services
* External clients

> **The lungs communicate with the outside world.**

---

## 🌬️ `airway/`

Airways provide communication paths.

```text
airway/
├── request.py
├── response.py
└── channel.py
```

### Use `airway/` for:

* Communication channels
* Request paths
* Response paths
* Transport layers

> **The airway provides a path for communication.**

---

# 🍽️ Digestive System

The digestive system receives, breaks down, processes, and transforms incoming information.

```text
Raw Input
    ↓
mouth/
    ↓
teeth/
    ↓
stomach/
    ↓
liver/
    ↓
intestine/
    ↓
Processed Information
```

---

## 🗣️ `mouth/`

The mouth receives and produces information.

```text
mouth/
├── request.py
├── response.py
└── message.py
```

### Use `mouth/` for:

* Input interfaces
* Output responses
* Message generation
* Request handling

> **The mouth receives and expresses information.**

---

## 🦷 `teeth/`

Teeth break things into smaller pieces.

```text
teeth/
├── parser.py
├── tokenizer.py
└── splitter.py
```

### Use `teeth/` for:

* Parsing
* Tokenization
* Data splitting
* Breaking complex input into smaller parts

> **The teeth break information into manageable pieces.**

---

## 🍽️ `stomach/`

The stomach processes raw material.

```text
stomach/
├── processor.py
├── parser.py
└── prepare.py
```

### Use `stomach/` for:

* Raw data processing
* Data preparation
* Initial transformation
* Input processing

> **The stomach processes what enters the system.**

---

## 🧪 `liver/`

The liver transforms and processes substances.

```text
liver/
├── transform.py
├── normalize.py
└── convert.py
```

### Use `liver/` for:

* Data transformation
* Normalization
* Conversion
* Processing

> **The liver transforms information into a useful form.**

---

## 🌀 `intestine/`

The intestine continues processing and extracting useful information.

```text
intestine/
├── extract.py
├── process.py
└── distribute.py
```

### Use `intestine/` for:

* Extended processing
* Information extraction
* Data distribution
* Pipeline stages

> **The intestine processes and distributes useful information.**

---

# 🫘 Filtering System

---

## 🫘 `kidney/`

The kidneys filter and remove unnecessary material.

```text
kidney/
├── filter.py
├── clean.py
└── sanitize.py
```

### Use `kidney/` for:

* Filtering
* Data cleaning
* Sanitization
* Removing unnecessary data

> **The kidney filters what the system does not need.**

---

# 🦴 Skeletal System

The skeletal system provides structure and support.

---

## 🦴 `skeleton/`

```text
skeleton/
├── models.py
├── schemas.py
└── interfaces.py
```

### Use `skeleton/` for:

* Data models
* Schemas
* Interfaces
* Base structures
* Architectural foundations

> **The skeleton gives the system structure.**

---

## 🦴 `bone/`

Bones are the strong structural components.

```text
bone/
├── base.py
├── foundation.py
└── core.py
```

### Use `bone/` for:

* Base classes
* Core abstractions
* Foundational components

> **Bones support the structure.**

---

## 🔗 `joint/`

Joints connect different structural components.

```text
joint/
├── adapter.py
├── bridge.py
└── integration.py
```

### Use `joint/` for:

* Adapters
* Bridges
* Integrations
* Component connections

> **Joints allow separate parts to work together.**

---

# 💪 Muscular System

The muscular system performs work and creates movement.

---

## 💪 `muscle/`

```text
muscle/
├── worker.py
├── compute.py
└── execute.py
```

### Use `muscle/` for:

* Heavy computation
* Intensive processing
* Workers
* Performance-heavy operations

> **Muscles perform the heavy work.**

---

## 🧵 `tendon/`

Tendons connect muscles to structural parts.

```text
tendon/
├── binding.py
├── connector.py
└── trigger.py
```

### Use `tendon/` for:

* Execution bindings
* Action connections
* Trigger connections

> **Tendons connect actions to structure.**

---

# 🧬 Genetic System

The genetic system defines the instructions of the application.

---

## 🧬 `dna/`

```text
dna/
├── settings.py
├── environment.py
└── constants.py
```

### Use `dna/` for:

* Configuration
* Environment settings
* Constants
* Application behavior
* Global instructions

> **The DNA defines how the system behaves.**

---

## 🧬 `gene/`

A gene represents an individual instruction or capability.

```text
gene/
├── feature_flag.py
├── rule.py
└── setting.py
```

### Use `gene/` for:

* Feature flags
* Individual settings
* Specific configuration units
* Behavioral rules

> **Genes define individual characteristics.**

---

# 🧫 Cellular System

Cells are the smallest functional building blocks of a system.

---

## 🦠 `cells/`

```text
cells/
├── component.py
├── unit.py
└── element.py
```

### Use `cells/` for:

* Small reusable components
* Independent units
* Low-level building blocks

> **Small cells come together to build larger systems.**

---

## 🧫 `membrane/`

A membrane defines a boundary.

```text
membrane/
├── boundary.py
├── interface.py
└── contract.py
```

### Use `membrane/` for:

* Component boundaries
* Encapsulation
* Contracts
* Interfaces

> **The membrane defines what belongs inside and outside.**

---

## 🔵 `nucleus/`

The nucleus controls the internal activities of a cell.

```text
nucleus/
├── controller.py
├── state.py
└── core.py
```

### Use `nucleus/` for:

* Internal component control
* Component state
* Local coordination
* Component-level logic

> **The nucleus controls the cell.**

---

# 🧠 Memory System

The memory system stores information.

---

## 🧠 `memory/`

```text
memory/
├── short_term/
├── long_term/
└── cache/
```

### Use `memory/` for:

* Databases
* Cache
* Sessions
* Persistent storage
* Application state

> **The memory remembers.**

---

# 👁️ Sensory System

The sensory system observes and receives information.

---

## 👁️ `eye/`

```text
eye/
├── scanner.py
├── observer.py
└── monitor.py
```

### Use `eye/` for:

* Monitoring
* Observation
* Visual input
* Data collection
* Sensors

> **The eye observes.**

---

## 👂 `ear/`

The ear receives signals.

```text
ear/
├── listener.py
├── consumer.py
└── webhook.py
```

### Use `ear/` for:

* Event listeners
* Message consumers
* Signal receivers
* Webhooks

> **The ear listens.**

---

## 👃 `nose/`

The nose detects and discovers.

```text
nose/
├── detector.py
├── scanner.py
└── discovery.py
```

### Use `nose/` for:

* Detection
* Pattern recognition
* Discovery
* Monitoring signals

> **The nose detects what is present.**

---

# ✋ Action and Movement System

The system needs ways to act and move.

---

## ✋ `hand/`

Hands perform actions.

```text
hand/
├── create.py
├── update.py
├── delete.py
└── execute.py
```

### Use `hand/` for:

* Commands
* Actions
* Operations
* Execution
* User-triggered actions

> **The hands perform actions.**

---

## ☝️ `finger/`

Fingers perform smaller, precise actions.

```text
finger/
├── click.py
├── select.py
└── action.py
```

### Use `finger/` for:

* Small commands
* Fine-grained operations
* Precise actions

> **Fingers perform precise actions.**

---

## 🦵 `leg/`

Legs move the body from one place to another.

```text
leg/
├── navigation.py
├── routing.py
└── transition.py
```

### Use `leg/` for:

* Navigation
* Routing
* State transitions
* Movement between application sections

> **Legs move the system forward.**

---

# 🧍 External System

---

## 🛡️ `skin/`

The skin is the outer layer of the system.

```text
skin/
├── routes.py
├── views.py
└── interface.py
```

### Use `skin/` for:

* User interfaces
* API routes
* Views
* Public interfaces
* Presentation layers

> **The skin is the boundary between the system and the outside world.**

---

# 🛡️ Immune System

The immune system protects the application.

---

## 🛡️ `immune/`

```text
immune/
├── authentication.py
├── authorization.py
└── security.py
```

### Use `immune/` for:

* Authentication
* Authorization
* Access control
* Security
* Threat detection

> **The immune system protects the body.**

---

## 🧪 `antibody/`

Antibodies provide specific protection against threats.

```text
antibody/
├── rule.py
├── validator.py
└── detector.py
```

### Use `antibody/` for:

* Security rules
* Threat detection
* Specific validation
* Protection policies

> **Antibodies recognize and respond to specific threats.**

---

# 🔬 Development Anatomy

These components help developers experiment, diagnose, and maintain the system.

---

## 🔬 `lab/`

```text
lab/
├── experiment.py
├── prototype.py
└── research.py
```

### Use `lab/` for:

* Experiments
* Prototypes
* Research
* Proofs of concept

> **The lab is where new ideas are tested.**

---

## 🩺 `doctor/`

```text
doctor/
├── diagnose.py
├── debug.py
└── repair.py
```

### Use `doctor/` for:

* Debugging
* Diagnostics
* Maintenance
* Error analysis
* Repair tools

> **The doctor keeps the system healthy.**

---

## 🧫 `checkup/`

```text
checkup/
├── unit/
├── integration/
└── system/
```

### Use `checkup/` for:

* Unit tests
* Integration tests
* System tests
* Health checks
* Quality verification

Traditional equivalent:

```text
tests/
```

> **A healthy system should be regularly checked.**

---

# 🗺️ Where Does My Code Belong?

Ask what responsibility the code has.

```text
Does it start the application?
        │
        └── body.py


Does it make decisions?
        │
        └── brain/


Is it a major feature?
        │
        └── soul/


Does it support multiple parts?
        │
        └── nerve/


Does it automatically react?
        │
        └── reflex/


Does it run central processes?
        │
        └── heart/


Does it move information?
        │
        └── blood/


Does it provide communication channels?
        │
        └── vessel/ or airway/


Does it communicate externally?
        │
        └── lung/


Does it receive or produce messages?
        │
        └── mouth/


Does it parse or split data?
        │
        └── teeth/


Does it process raw information?
        │
        └── stomach/


Does it transform information?
        │
        └── liver/


Does it filter or clean information?
        │
        └── kidney/


Does it define structure?
        │
        └── skeleton/


Does it provide a foundation?
        │
        └── bone/


Does it connect components?
        │
        └── joint/


Does it perform heavy work?
        │
        └── muscle/


Does it configure the application?
        │
        └── dna/ or gene/


Is it a small reusable unit?
        │
        └── cells/


Does it define a component boundary?
        │
        └── membrane/


Does it control a component internally?
        │
        └── nucleus/


Does it store information?
        │
        └── memory/


Does it observe?
        │
        └── eye/


Does it listen for signals?
        │
        └── ear/


Does it detect patterns?
        │
        └── nose/


Does it perform actions?
        │
        └── hand/ or finger/


Does it navigate?
        │
        └── leg/


Does it expose the application?
        │
        └── skin/


Does it protect the application?
        │
        └── immune/ or antibody/


Is it experimental?
        │
        └── lab/


Does it diagnose problems?
        │
        └── doctor/


Does it test the system?
        │
        └── checkup/
```

---

# 📁 Complete Code Anatomy

```text
project/
│
├── body.py
│
├── brain/
├── soul/
│
├── nerve/
├── reflex/
│
├── heart/
├── blood/
├── vessel/
│
├── lung/
├── airway/
│
├── mouth/
├── teeth/
├── stomach/
├── liver/
├── intestine/
│
├── kidney/
│
├── skeleton/
├── bone/
├── joint/
│
├── muscle/
├── tendon/
│
├── dna/
├── gene/
│
├── cells/
├── membrane/
├── nucleus/
│
├── memory/
│   ├── short_term/
│   ├── long_term/
│   └── cache/
│
├── eye/
├── ear/
├── nose/
│
├── hand/
├── finger/
├── leg/
│
├── skin/
│
├── immune/
├── antibody/
│
├── lab/
├── doctor/
│
└── checkup/
```

---

# 📖 Quick Reference

| Code Anatomy    | Traditional Equivalent       | Purpose                 |
| --------------- | ---------------------------- | ----------------------- |
| 🧍 `body.py`    | `main.py`, `app.py`          | Application entry point |
| 🧠 `brain/`     | `logic/`, `core/`            | Decisions and logic     |
| 🧬 `soul/`      | `modules/`, `features/`      | Major features          |
| ⚡ `nerve/`      | `utils/`, `helpers/`         | Shared support          |
| ⚡ `reflex/`     | `handlers/`                  | Automatic reactions     |
| ❤️ `heart/`     | `services/`, `engine/`       | Central processing      |
| 🩸 `blood/`     | `pipeline/`, `stream/`       | Data movement           |
| 🩸 `vessel/`    | `channels/`, `connectors/`   | Internal communication  |
| 🫁 `lung/`      | `clients/`, `network/`       | External communication  |
| 🌬️ `airway/`   | `transport/`                 | Communication paths     |
| 🗣️ `mouth/`    | `requests/`, `responses/`    | Input and output        |
| 🦷 `teeth/`     | `parser/`, `tokenizer/`      | Breaking data           |
| 🍽️ `stomach/`  | `processor/`                 | Raw processing          |
| 🧪 `liver/`     | `transformer/`               | Transformation          |
| 🌀 `intestine/` | `pipeline/`                  | Extended processing     |
| 🫘 `kidney/`    | `filter/`, `sanitizer/`      | Filtering               |
| 🦴 `skeleton/`  | `models/`, `schemas/`        | Structure               |
| 🦴 `bone/`      | `base/`, `foundation/`       | Core structure          |
| 🔗 `joint/`     | `adapters/`, `integrations/` | Connections             |
| 💪 `muscle/`    | `workers/`, `compute/`       | Heavy work              |
| 🧵 `tendon/`    | `bindings/`                  | Action connections      |
| 🧬 `dna/`       | `config/`, `settings/`       | Configuration           |
| 🧬 `gene/`      | `flags/`, `rules/`           | Individual instructions |
| 🦠 `cells/`     | `components/`, `units/`      | Small building blocks   |
| 🧫 `membrane/`  | `contracts/`, `boundaries/`  | Encapsulation           |
| 🔵 `nucleus/`   | `controllers/`               | Internal control        |
| 🧠 `memory/`    | `database/`, `cache/`        | Storage                 |
| 👁️ `eye/`      | `monitor/`, `input/`         | Observation             |
| 👂 `ear/`       | `listeners/`, `consumers/`   | Signal reception        |
| 👃 `nose/`      | `detectors/`                 | Detection               |
| ✋ `hand/`       | `actions/`, `commands/`      | Actions                 |
| ☝️ `finger/`    | `commands/`                  | Small actions           |
| 🦵 `leg/`       | `routing/`, `navigation/`    | Movement                |
| 🛡️ `skin/`     | `interface/`, `views/`       | External layer          |
| 🛡️ `immune/`   | `security/`                  | General protection      |
| 🧪 `antibody/`  | `security_rules/`            | Specific protection     |
| 🔬 `lab/`       | `experiments/`               | Experiments             |
| 🩺 `doctor/`    | `debug/`, `diagnostics/`     | Maintenance             |
| 🧫 `checkup/`   | `tests/`                     | Testing                 |

---

# 🧭 Naming Rules

## Rule 1 — Meaning Before Creativity

Do not use anatomy names randomly.

Bad:

```text
brain/
└── database.py
```

Better:

```text
memory/
└── database.py
```

The name should describe the responsibility of the code.

---

## Rule 2 — One Role, One Meaning

Once an anatomy name has a responsibility, keep it consistent.

For example:

* `brain/` → decisions
* `memory/` → storage
* `immune/` → protection
* `heart/` → central processing
* `nerve/` → support and communication

Do not give the same anatomy part multiple unrelated meanings.

---

## Rule 3 — Start Small

Do not create every folder just because it exists in the Code Anatomy vocabulary.

A small application may only need:

```text
body.py
brain/
soul/
nerve/
checkup/
```

A larger application may gradually add more systems.

> **The architecture should grow with the application.**

---

## Rule 4 — Use Anatomy by Responsibility

Choose the folder based on what the code does.

Do not choose a folder simply because the name sounds interesting.

> **The metaphor exists to improve understanding, not replace it.**

---

## Rule 5 — Avoid Duplicate Responsibilities

Do not create multiple anatomy folders that perform exactly the same job without a clear reason.

For example:

```text
brain/     → decides
soul/      → provides features
nerve/     → supports
memory/    → stores
immune/    → protects
```

Every major responsibility should have a clear home.

---

## Rule 6 — Clarity Beats Metaphor

The human-body metaphor should help developers understand the architecture.

If an anatomy name creates confusion, choose the clearest structure for the project.

> **Creativity should never come at the cost of clarity.**

---

# 🌱 Philosophy

Software is more than a collection of files.

It is a system of interconnected parts.

```text
The body brings everything together.

The brain thinks.

The soul defines purpose.

The nerves connect.

The reflex reacts.

The heart drives.

The blood moves information.

The vessels carry it.

The lungs communicate.

The mouth receives and responds.

The teeth break information apart.

The stomach processes.

The liver transforms.

The intestine extracts and distributes.

The kidneys filter.

The skeleton provides structure.

The bones support.

The joints connect.

The muscles perform work.

The tendons connect movement.

The DNA defines instructions.

The genes define characteristics.

The cells build the system.

The membrane creates boundaries.

The nucleus controls internal activity.

The memory remembers.

The eyes observe.

The ears listen.

The nose detects.

The hands act.

The fingers perform precise actions.

The legs navigate.

The skin exposes the system.

The immune system protects.

The antibodies defend against specific threats.

The lab experiments.

The doctor diagnoses.

The checkup tests.
```

---

# ⚠️ A Note on Convention

Code Anatomy is an architectural philosophy.

Traditional names such as:

```text
main.py
utils/
modules/
services/
config/
models/
tests/
```

are widely recognized across the software industry.

Code Anatomy intentionally uses a different vocabulary.

That can make a project more memorable and conceptually structured, but it can also create a learning curve for new contributors.

When working with teams or open-source projects, documentation is essential.

The purpose of Code Anatomy is not to be different.

The purpose is to create meaningful structure.

> **Creativity should never come at the cost of clarity.**

---

# 🧬 Complete Does Not Mean Use Everything

The Code Anatomy vocabulary is intentionally broad.

That does **not** mean every project should contain every anatomy folder.

A complete vocabulary allows the architecture to grow when necessary.

### Small Project

```text
body.py
brain/
soul/
nerve/
checkup/
```

### Medium Project

```text
body.py
brain/
soul/
nerve/
heart/
memory/
skin/
immune/
checkup/
```

### Large Project

A large system may use multiple specialized anatomy systems depending on its responsibilities.

> **Use the anatomy your software needs.**

> **Do not create anatomy without responsibility.**

---

# 🧍 The Code Anatomy Rule

> **A program is a body.**
>
> **Every part has a role.**
>
> **Every role has a place.**
>
> **Every place should have meaning.**

# Code like you are building a living system.
