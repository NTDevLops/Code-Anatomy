# 🤝 Contributing to Code Anatomy

> **Help us build a meaningful and consistent architecture for organizing software like a living system.**

Thank you for your interest in contributing to **Code Anatomy**.

Code Anatomy is more than a collection of creative folder names. It is an architectural convention based on one central idea:

> **Every piece of code has a responsibility. Every responsibility should have a meaningful place.**

This document explains how to contribute to the project while preserving consistency, clarity, and the philosophy of Code Anatomy.

---

# 📚 Table of Contents

* [1. Before You Contribute](#1-before-you-contribute)
* [2. Ways to Contribute](#2-ways-to-contribute)
* [3. The Core Contribution Principle](#3-the-core-contribution-principle)
* [4. Proposing a New Anatomy Name](#4-proposing-a-new-anatomy-name)
* [5. Anatomy Naming Requirements](#5-anatomy-naming-requirements)
* [6. Proposing Architecture Changes](#6-proposing-architecture-changes)
* [7. Documentation Contributions](#7-documentation-contributions)
* [8. Examples and Language Support](#8-examples-and-language-support)
* [9. Rules for Pull Requests](#9-rules-for-pull-requests)
* [10. Commit Guidelines](#10-commit-guidelines)
* [11. What We Avoid](#11-what-we-avoid)
* [12. Final Checklist](#12-final-checklist)

---

# 1. Before You Contribute

Before making a contribution, please read:

```text
README.md
```

```text
ARCHITECTURE.md
```

```text
GUIDE.md
```

```text
CONVENTIONS.md
```

Each document has a different purpose.

| File              | Purpose                                    |
| ----------------- | ------------------------------------------ |
| `README.md`       | Introduces Code Anatomy and its philosophy |
| `ARCHITECTURE.md` | Defines the official architecture          |
| `GUIDE.md`        | Helps developers decide where code belongs |
| `CONVENTIONS.md`  | Defines naming and organization rules      |
| `CONTRIBUTING.md` | Explains how to contribute                 |

Before proposing a change, make sure you understand the existing philosophy.

---

# 2. Ways to Contribute

You can contribute in many ways.

## 📖 Improve Documentation

You can:

* Fix spelling or grammar.
* Improve explanations.
* Add clearer examples.
* Improve project structures.
* Add missing documentation.

---

## 🌐 Add Language-Specific Examples

Code Anatomy should be understandable across programming languages.

You may contribute examples for:

* Python
* JavaScript
* TypeScript
* Java
* C#
* Go
* Rust
* PHP
* Ruby
* Kotlin
* Swift
* Other languages

The architecture may adapt to the language.

The philosophy should remain consistent.

---

## 🧠 Improve the Decision System

You may improve:

* Decision trees.
* Responsibility definitions.
* Folder placement guidance.
* Architecture examples.

However, changes should make the system clearer.

---

## 🧬 Propose New Anatomy

New anatomy names may be proposed when an important responsibility is missing from the current system.

This is discussed in detail later in this document.

---

# 3. The Core Contribution Principle

Every contribution should follow the same central question:

> **Does this improve clarity?**

Code Anatomy is not trying to replace technical vocabulary with biological vocabulary for entertainment.

The anatomy metaphor exists to help developers understand responsibility.

A contribution should improve at least one of the following:

* Clarity
* Consistency
* Maintainability
* Discoverability
* Scalability
* Understanding

If a change only makes the architecture more complicated, it should probably not be added.

> **More anatomy does not automatically mean better architecture.**

---

# 4. Proposing a New Anatomy Name

New anatomy names should not be added casually.

Before proposing one, ask:

> **Is there a real architectural responsibility that the existing anatomy does not describe clearly?**

For example, do not propose a new anatomy name simply because a body part exists.

Bad reasoning:

> "Humans have this organ, so Code Anatomy should have a folder for it."

Good reasoning:

> "This responsibility appears repeatedly in software architecture and is not clearly represented by the existing anatomy."

---

## Required Questions

Every proposal for a new anatomy name should answer:

### 1. What responsibility does it represent?

Explain exactly what type of code belongs there.

---

### 2. Why is an existing anatomy insufficient?

Check whether the responsibility already belongs to:

```text
brain/
soul/
nerve/
heart/
memory/
lung/
digestive/
skeleton/
muscle/
dna/
cells/
sensory/
action/
skin/
immune/
```

Do not create duplicate responsibilities.

---

### 3. What does not belong there?

Every anatomy name needs boundaries.

For example:

```text
memory/
```

is for storing information.

It is not automatically for:

* Business decisions
* Authentication logic
* API routes

Clear boundaries prevent architecture confusion.

---

### 4. Is the name understandable?

The biological metaphor should be reasonably understandable.

A contributor should explain:

* Why this anatomy was chosen.
* How it relates to the software responsibility.
* How developers should use it.

---

### 5. Is it reusable?

The proposed responsibility should be useful beyond one specific project.

Avoid anatomy names created for extremely narrow use cases.

---

# 5. Anatomy Naming Requirements

A new anatomy name should meet the following requirements.

---

## 🧠 Requirement 1 — Clear Responsibility

The anatomy must represent a recognizable responsibility.

Bad:

```text
mystery/
```

Good:

```text
memory/
```

The responsibility should be understandable.

---

## 🦴 Requirement 2 — No Duplicate Meaning

Do not introduce multiple anatomy names for the same responsibility.

For example:

```text
memory/
```

and:

```text
storage/
```

should not both represent exactly the same thing.

One responsibility should have one primary meaning.

---

## 🧬 Requirement 3 — Biological Relevance

The name should have a meaningful connection to the human body or biological systems.

The relationship does not need to be perfect.

However, it should be understandable.

---

## 🔧 Requirement 4 — Practical Use

The anatomy must be useful in real software projects.

The system should not become a biological encyclopedia.

> **If developers cannot reasonably use it, it probably does not belong in the standard.**

---

## 📖 Requirement 5 — Documentation

Every accepted anatomy name should document:

* Purpose
* Responsibility
* Examples
* Boundaries
* Common use cases
* Relationship to other anatomy

---

# 6. New Anatomy Proposal Template

Use the following structure when proposing a new anatomy name.

---

## 🧬 Anatomy Name

```text
Name:
```

---

## 🧠 Software Responsibility

```text
What does this part represent?
```

---

## 🧍 Biological Meaning

```text
What does this part do in the human body?
```

---

## 💻 Software Meaning

```text
What responsibility does it represent in software?
```

---

## 📁 Suggested Structure

```text
anatomy/
├── example_one/
└── example_two/
```

---

## 🔄 Traditional Equivalent

```text
Traditional name:
```

---

## ⚖️ Why Existing Anatomy Is Not Enough

Explain why the responsibility cannot clearly belong somewhere else.

---

## ❌ What Does Not Belong Here

Clearly define boundaries.

---

## 🧪 Example Usage

Provide at least one practical example.

---

# 7. Proposing Architecture Changes

Changes to the official architecture should be considered carefully.

Architecture changes may affect:

```text
README.md
ARCHITECTURE.md
GUIDE.md
CONVENTIONS.md
CONTRIBUTING.md
```

If a change affects the meaning of an anatomy name, all relevant documentation should be updated.

---

## Major Architecture Changes

Examples include:

* Adding new anatomy.
* Removing official anatomy.
* Changing responsibility definitions.
* Changing dependency rules.
* Changing the official hierarchy.

These changes should include a clear explanation of:

1. The current problem.
2. The proposed solution.
3. Why the change improves the architecture.
4. Possible alternatives.
5. Possible disadvantages.

---

# 8. Documentation Contributions

Documentation is an important part of Code Anatomy.

When contributing documentation:

* Use clear language.
* Avoid unnecessary complexity.
* Keep terminology consistent.
* Preserve the philosophy of the project.
* Add examples when useful.

---

## Preferred Writing Style

Prefer:

> Clear and direct explanations.

Avoid:

> Unnecessarily complicated language.

Prefer:

```text
The brain makes decisions.
```

Instead of:

```text
The cerebral architectural abstraction layer is responsible for computational decision orchestration.
```

Simple language is usually better.

---

# 9. Examples and Language Support

Code Anatomy should support multiple programming languages.

However, Code Anatomy should not force a language to abandon its ecosystem conventions.

For example:

Python:

```text
body.py
```

JavaScript:

```text
body.js
```

TypeScript:

```text
body.ts
```

The anatomy name remains consistent.

The language-specific file convention can remain different.

---

## Framework Compatibility

When contributing framework examples, respect the framework.

For example, a framework may require:

```text
src/
public/
components/
```

Code Anatomy should adapt intelligently.

Do not break required framework conventions simply to rename everything anatomically.

> **Framework requirements come before metaphor.**

---

# 10. Rules for Pull Requests

Before submitting a pull request, ensure that the contribution:

* Has a clear purpose.
* Follows existing conventions.
* Does not create unnecessary duplication.
* Includes documentation when required.
* Includes examples when useful.
* Does not introduce unrelated changes.

---

## Keep Pull Requests Focused

Bad pull request:

```text
Fix spelling
+
Add five anatomy systems
+
Rewrite the architecture
+
Change all examples
+
Reorganize documentation
```

Better:

```text
Add a clear proposal for one anatomy responsibility.
```

Focused contributions are easier to review.

---

# 11. Commit Guidelines

Use clear commit messages.

Recommended format:

```text
type: short description
```

Examples:

```text
docs: improve memory examples
```

```text
docs: add TypeScript project example
```

```text
feat: propose new anatomy responsibility
```

```text
fix: correct anatomy naming inconsistency
```

---

## Suggested Commit Types

| Type       | Purpose                  |
| ---------- | ------------------------ |
| `docs`     | Documentation changes    |
| `fix`      | Corrections              |
| `feat`     | New features or concepts |
| `refactor` | Structural improvements  |
| `example`  | New examples             |
| `test`     | Testing improvements     |
| `chore`    | Maintenance work         |

---

# 12. What We Avoid

Code Anatomy should avoid unnecessary complexity.

---

## ❌ Anatomy for Everything

Not every body part needs a software equivalent.

Avoid creating anatomy folders simply because they exist biologically.

Example:

```text
eyelash/
fingernail/
toenail/
earlobe/
```

unless there is a clear and useful architectural purpose.

---

## ❌ Duplicate Responsibilities

Avoid:

```text
storage/
memory/
data/
repository/
```

all meaning the same thing.

The goal is consistency.

---

## ❌ Metaphor Over Clarity

Do not choose a name simply because it sounds creative.

Bad:

```text
galaxy/
```

for a database system.

It may sound interesting, but it does not belong to the Code Anatomy model.

---

## ❌ Unnecessary Renaming

Do not rename framework-required files simply to fit the metaphor.

For example, if a framework requires:

```text
package.json
```

do not rename it.

Code Anatomy should coexist with existing ecosystem conventions.

---

# 13. When a Proposal Should Be Rejected

A proposal may not be suitable if it:

* Duplicates an existing responsibility.
* Adds unnecessary complexity.
* Has no clear software meaning.
* Is too specific to one project.
* Breaks existing consistency.
* Requires excessive explanation to understand.
* Exists only because the biological body part exists.

> **The purpose of Code Anatomy is useful structure, not complete biological simulation.**

---

# 14. Improving Existing Anatomy

Contributions do not always need to add new anatomy.

You can improve existing anatomy by:

* Clarifying boundaries.
* Adding examples.
* Improving explanations.
* Adding language support.
* Improving the decision tree.
* Explaining common mistakes.

Improving clarity is often more valuable than adding new concepts.

---

# 15. Contribution Philosophy

A healthy software architecture should evolve carefully.

The same principle applies to Code Anatomy.

```text
Observe the problem.

Understand the responsibility.

Check existing anatomy.

Avoid duplication.

Choose the clearest solution.

Document the decision.

Keep the architecture understandable.
```

---

# 16. Final Checklist

Before submitting a contribution, ask:

```text
[ ] Does this solve a real problem?

[ ] Does it improve clarity?

[ ] Does it avoid duplicate responsibilities?

[ ] Does it follow Code Anatomy conventions?

[ ] Is the biological metaphor meaningful?

[ ] Is the responsibility clearly defined?

[ ] Are boundaries documented?

[ ] Are examples included when necessary?

[ ] Does it work across different projects?

[ ] Does it avoid unnecessary complexity?
```

---

# 🧍 The Contribution Rule

> **Do not add anatomy because it exists.**

> **Add anatomy because a meaningful responsibility needs a place.**

---

# 🧬 The Code Anatomy Philosophy

```text
A body is not a random collection of organs.

A software project should not be a random collection of folders.

Every part should have a responsibility.

Every responsibility should have a place.

Every place should have meaning.
```

---

# 🤝 Thank You

Thank you for helping improve Code Anatomy.

Whether you:

* Fix documentation,
* Add examples,
* Improve explanations,
* Propose architecture changes,
* Or contribute a new perspective,

your contribution helps make the system clearer and more useful.

> **Build with creativity.**

> **Organize with meaning.**

> **Keep the system healthy.**

# 🧠 Code like you are building a living system.
