# 🏛️ Official Code Anatomy Hierarchy Standard

Code Anatomy is not just a collection of creative folder names.

It is a structured architectural system.

To keep projects consistent, Code Anatomy defines which parts belong at the root level and which parts belong inside larger anatomical systems.

> **Not every anatomy part should become a top-level folder.**

Just as the human body is organized into systems, organs, tissues, and cells, a Code Anatomy project should follow a clear hierarchy.

---

# 🧬 The Hierarchy Principle

Code Anatomy follows four structural levels:

```text
BODY
 │
 ├── SYSTEM
 │     │
 │     ├── ORGAN
 │     │     │
 │     │     └── COMPONENT
 │
 └── SUPPORT
```

In software terms:

```text
PROJECT
 │
 ├── MAJOR SYSTEM
 │     │
 │     ├── SPECIALIZED RESPONSIBILITY
 │     │
 │     └── SMALL COMPONENT
 │
 └── PROJECT SUPPORT
```

The hierarchy should move from:

> **Whole → System → Responsibility → Component**

---

# 🧍 Tier 0 — The Body

The entire project is the **body**.

```text
project/
```

The primary application entry point is:

```text
body.py
```

Example:

```text
project/
├── body.py
└── ...
```

> **There is one body for the application.**

---

# 🧠 Tier 1 — Core Systems

These are the primary systems of a Code Anatomy project.

They may exist directly at the root level.

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
├── lung/
├── skin/
│
├── immune/
│
├── skeleton/
│
├── muscle/
│
├── digestive/
│
├── sensory/
│
├── action/
│
├── dna/
│
├── cells/
│
├── lab/
├── doctor/
└── checkup/
```

These folders represent **major systems or major responsibilities**.

---

# 🧠 1. Brain System

```text
brain/
```

The brain is responsible for thinking and decision-making.

```text
brain/
├── decision/
├── workflow/
├── rules/
└── intelligence/
```

### Responsibility

* Business logic
* Decisions
* Rules
* Workflows
* Intelligence

> **The brain decides.**

---

# 🧬 2. Soul System

```text
soul/
```

The soul contains the application's primary purpose and major features.

```text
soul/
├── authentication/
├── payments/
├── users/
└── notifications/
```

### Responsibility

* Features
* Domain modules
* Core capabilities
* Business domains

> **The soul defines what the application is.**

---

# ⚡ 3. Nervous System

The nervous system contains communication and reactive behavior.

```text
nerve/
```

Official structure:

```text
nerve/
├── shared/
├── communication/
└── reflex/
```

Example:

```text
nerve/
├── shared/
│   ├── logger.py
│   ├── validator.py
│   └── formatter.py
│
├── communication/
│   ├── signal.py
│   └── event.py
│
└── reflex/
    ├── trigger.py
    └── handler.py
```

### Responsibility

* Shared utilities
* Internal communication
* Events
* Signals
* Automatic reactions

> **The nervous system connects and reacts.**

---

# ❤️ 4. Circulatory System

The circulatory system moves information and processing throughout the application.

```text
heart/
```

Official structure:

```text
heart/
├── processor/
├── worker/
├── scheduler/
│
└── blood/
    ├── pipeline/
    ├── stream/
    └── flow/
```

For large systems:

```text
heart/
├── processor/
├── worker/
├── scheduler/
│
├── blood/
│
└── vessel/
```

### Responsibility

#### ❤️ Heart

* Central processing
* Scheduling
* Workers
* Continuous operations

#### 🩸 Blood

* Data movement
* Data pipelines
* Streams
* Information flow

#### 🩸 Vessel

* Channels
* Connections
* Data transport paths

> **The heart drives. Blood moves. Vessels connect.**

---

# 🫁 5. Respiratory System

External communication belongs to the respiratory system.

```text
lung/
```

Official structure:

```text
lung/
├── api/
├── client/
├── websocket/
└── airway/
```

### Responsibility

#### 🫁 Lung

* External APIs
* Network communication
* Third-party services
* WebSockets

#### 🌬️ Airway

* Transport channels
* Communication paths
* Requests
* Responses

> **The lungs communicate with the outside world.**

---

# 🍽️ 6. Digestive System

Information processing follows a structured pipeline: receive, parse, prepare, transform, extract, filter.

```text
digestive/
```

Official full hierarchy (six stages, including filtering — see below):

```text
digestive/
├── mouth/
├── teeth/
├── stomach/
├── liver/
├── intestine/
└── kidney/
```

### 🟢 Default structure (Level 1 / Level 2 projects)

Six folders for one pipeline is more ceremony than most projects need. Unless a project genuinely runs each stage as a separately maintained phase, default to two:

```text
digestive/
├── intake/      # mouth + teeth — receiving and parsing raw input
└── process/     # stomach + liver + intestine + kidney — prepare, transform, extract, filter
```

Expand `process/` back into its full six-stage form only when a project has enough independent logic at each stage to justify separate files or separate maintainers per stage (for example, a data-engineering service where extract, transform, and filter are separately deployable jobs).

---

## 🗣️ Mouth

```text
digestive/mouth/
```

Use for:

* Input
* Output
* Messages
* Requests
* Responses

---

## 🦷 Teeth

```text
digestive/teeth/
```

Use for:

* Parsing
* Splitting
* Tokenization

---

## 🍽️ Stomach

```text
digestive/stomach/
```

Use for:

* Raw processing
* Data preparation
* Initial processing

---

## 🧪 Liver

```text
digestive/liver/
```

Use for:

* Transformation
* Normalization
* Conversion

---

## 🌀 Intestine

```text
digestive/intestine/
```

Use for:

* Extended processing
* Extraction
* Distribution

---

## 🫘 Kidney

```text
digestive/kidney/
```

Kidney is the digestive system's final stage: filtering. It is documented here, not as a separate numbered system, so the full pipeline is defined in exactly one place.

Use for:

* Filtering
* Cleaning
* Sanitization
* Removing unnecessary information

For projects where filtering is a major independent responsibility rather than the tail end of an input pipeline (e.g. a dedicated data-sanitization service), `kidney/` may be promoted to the project root instead of nesting under `digestive/`. That is an explicit expansion, not the default — see the Level 1/2/3 examples in this document, none of which include a top-level `kidney/`.

The full flow:

```text
Input
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
kidney/
  ↓
Processed Data
```

> **The digestive system receives, processes, transforms, extracts, and filters information.**

---

# 🦴 7. Skeletal System

The skeletal system provides structural support.

```text
skeleton/
```

Official structure:

```text
skeleton/
├── models/
├── schemas/
├── interfaces/
│
├── bone/
│
└── joint/
```

### 🦴 Bone

```text
skeleton/bone/
```

Use for:

* Base classes
* Foundations
* Core abstractions

### 🔗 Joint

```text
skeleton/joint/
```

Use for:

* Adapters
* Integrations
* Bridges
* Connections

> **The skeleton provides structure. Bones support it. Joints connect it.**

---

# 💪 8. Muscular System

The muscular system performs work.

```text
muscle/
```

Official structure:

```text
muscle/
├── workers/
├── compute/
├── execution/
│
└── tendon/
```

### 🧵 Tendon

```text
muscle/tendon/
```

Use for:

* Bindings
* Execution connections
* Action connections

> **Muscles perform work. Tendons connect movement.**

---

# 🧬 9. Genetic System

The genetic system defines instructions and behavior.

```text
dna/
```

Official structure:

```text
dna/
├── settings/
├── environment/
├── constants/
└── gene/
```

### 🧬 Gene

```text
dna/gene/
```

Use for:

* Feature flags
* Individual settings
* Rules
* Specific behavioral instructions

> **DNA defines the system. Genes define individual characteristics.**

---

# 🧫 10. Cellular System

The cellular system contains small building blocks.

```text
cells/
```

Official structure:

```text
cells/
├── components/
├── units/
│
├── membrane/
│
└── nucleus/
```

### 🧫 Membrane

```text
cells/membrane/
```

Use for:

* Boundaries
* Contracts
* Encapsulation
* Interfaces

### 🔵 Nucleus

```text
cells/nucleus/
```

Use for:

* Internal control
* Component state
* Local coordination

> **Cells build. Membranes protect boundaries. Nuclei control.**

---

# 🧠 11. Memory System

```text
memory/
```

Official structure:

```text
memory/
├── short_term/
├── long_term/
├── cache/
└── state/
```

### Responsibility

* Databases
* Persistent storage
* Cache
* Sessions
* State

> **The memory remembers.**

---

# 👁️ 12. Sensory System

Sensory organs should be grouped together.

```text
sensory/
```

Official structure:

```text
sensory/
├── eye/
├── ear/
└── nose/
```

---

## 👁️ Eye

```text
sensory/eye/
```

Use for:

* Monitoring
* Observation
* Visual input
* Scanning

---

## 👂 Ear

```text
sensory/ear/
```

Use for:

* Event listeners
* Message consumers
* Webhooks
* Signals

---

## 👃 Nose

```text
sensory/nose/
```

Use for:

* Detection
* Pattern recognition
* Discovery

> **The sensory system observes, listens, and detects.**

---

# ✋ 13. Action and Movement System

Actions should be grouped together.

```text
action/
```

### 🟢 Default structure (Level 1 / Level 2 projects)

Splitting coarse actions from fine-grained ones is a judgment call with no clear test until a project has enough distinct commands to need it. Default to a flat split by concern instead:

```text
action/
├── commands/    # hand + finger — all direct actions, coarse or fine
└── nav/         # leg — navigation, routing, transitions
```

### 🔴 Full structure (expand once `commands/` earns the split)

```text
action/
├── hand/
├── finger/
└── leg/
```

---

## ✋ Hand

```text
action/hand/
```

Use for:

* Commands
* Operations
* Major actions

---

## ☝️ Finger

```text
action/finger/
```

Use for:

* Small actions
* Fine-grained operations
* Precise commands

---

## 🦵 Leg

```text
action/leg/
```

Use for:

* Navigation
* Routing
* Transitions

> **Hands act. Fingers perform precise actions. Legs move.**

---

# 🛡️ 14. Immune System

Security belongs to the immune system.

```text
immune/
```

Official structure:

```text
immune/
├── authentication/
├── authorization/
├── security/
│
└── antibody/
```

### 🧪 Antibody

```text
immune/antibody/
```

Use for:

* Security rules
* Specific threat detection
* Protection policies

> **The immune system protects. Antibodies defend against specific threats.**

---

# 🩹 15. External System

The external-facing layer is the skin.

```text
skin/
```

Official structure:

```text
skin/
├── api/
├── routes/
├── views/
└── interface/
```

### Responsibility

* Public APIs
* User interfaces
* Views
* Routes
* Presentation

> **The skin connects the application with the outside world.**

---

# 🩺 16. Development and Maintenance System

Development support should be clearly separated from application logic.

```text
lab/
doctor/
checkup/
```

---

## 🔬 Lab

```text
lab/
```

Use for:

* Experiments
* Prototypes
* Research
* Proofs of concept

---

## 🩺 Doctor

```text
doctor/
```

Use for:

* Debugging
* Diagnostics
* Repair
* Maintenance

---

## 🧫 Checkup

```text
checkup/
```

Official structure:

```text
checkup/
├── unit/
├── integration/
└── system/
```

Use for:

* Unit tests
* Integration tests
* System tests
* Health checks

---

# 🏗️ The Official Complete Structure

This is the recommended complete hierarchy.

```text
project/
│
├── body.py
│
├── brain/
│   ├── decision/
│   ├── workflow/
│   ├── rules/
│   └── intelligence/
│
├── soul/
│   └── features/
│
├── nerve/
│   ├── shared/
│   ├── communication/
│   └── reflex/
│
├── heart/
│   ├── processor/
│   ├── worker/
│   ├── scheduler/
│   ├── blood/
│   └── vessel/
│
├── lung/
│   ├── api/
│   ├── client/
│   ├── websocket/
│   └── airway/
│
├── digestive/
│   ├── mouth/
│   ├── teeth/
│   ├── stomach/
│   ├── liver/
│   ├── intestine/
│   └── kidney/
│
├── skeleton/
│   ├── models/
│   ├── schemas/
│   ├── interfaces/
│   ├── bone/
│   └── joint/
│
├── muscle/
│   ├── workers/
│   ├── compute/
│   ├── execution/
│   └── tendon/
│
├── dna/
│   ├── settings/
│   ├── environment/
│   ├── constants/
│   └── gene/
│
├── cells/
│   ├── components/
│   ├── units/
│   ├── membrane/
│   └── nucleus/
│
├── memory/
│   ├── short_term/
│   ├── long_term/
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
│   ├── finger/
│   └── leg/
│
├── skin/
│   ├── api/
│   ├── routes/
│   ├── views/
│   └── interface/
│
├── immune/
│   ├── authentication/
│   ├── authorization/
│   ├── security/
│   └── antibody/
│
├── lab/
│
├── doctor/
│
└── checkup/
    ├── unit/
    ├── integration/
    └── system/
```

---

# 📏 Official Hierarchy Rules

## Rule 1 — Systems Come First

Major biological systems can exist at the project root.

```text
brain/
nerve/
heart/
lung/
digestive/
skeleton/
muscle/
immune/
```

---

## Rule 2 — Organs Belong Inside Their Systems

Avoid unnecessary top-level folders.

Bad:

```text
project/
├── heart/
├── blood/
├── vessel/
├── eye/
├── ear/
├── nose/
├── hand/
├── finger/
└── leg/
```

Recommended:

```text
project/
├── heart/
│   ├── blood/
│   └── vessel/
│
├── sensory/
│   ├── eye/
│   ├── ear/
│   └── nose/
│
└── action/
    ├── hand/
    ├── finger/
    └── leg/
```

> **The project structure should represent anatomical relationships.**

---

## Rule 3 — Avoid Empty Anatomy

Do not create:

```text
eye/
```

unless the application actually needs observation functionality.

Do not create:

```text
immune/
```

unless the application contains meaningful security or protection responsibilities.

> **An anatomy part exists because the software needs its responsibility—not because the human body has that organ.**

---

## Rule 4 — Do Not Force Biological Accuracy

Code Anatomy is inspired by human anatomy.

It is **not a medical classification system**.

The goal is conceptual clarity.

For example:

```text
digestive/
└── kidney/
```

may be useful architecturally for filtering responsibilities even though the kidney belongs to a different biological system.

Software structure takes priority over biological precision.

> **Meaning comes before medical accuracy.**

---

# 🌱 Recommended Adoption Levels

## 🟢 Level 1 — Minimal

Recommended for small projects.

```text
body.py
brain/
soul/
nerve/
checkup/
```

---

## 🟡 Level 2 — Standard

Recommended for medium applications.

```text
body.py

brain/
soul/
nerve/

heart/
memory/

skin/
immune/

dna/

checkup/
```

---

## 🔴 Level 3 — Full Anatomy

Recommended only for large and complex applications.

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

---

# 🧬 The Golden Rule

Before creating a new folder, ask:

> **What does this code do?**

Then ask:

> **Which part of the Code Anatomy system represents that responsibility?**

Do not ask:

> **Which anatomy name sounds cool?**

The correct structure is determined by responsibility.

---

# 🧍 Final Code Anatomy Philosophy

```text
The project is the body.

Systems organize major responsibilities.

Organs provide specialized responsibilities.

Components perform individual tasks.

Every part has a role.

Every role has a place.

Every place has meaning.
```

> **A clean architecture should feel alive—not because it uses anatomy names, but because every part works together with purpose.**