# Low-Level Design (LLD) — Google Interview Preparation

> **Goal:** Master object-oriented design principles and design patterns  
> to demonstrate clean, extensible, production-grade code in Google interviews.

---

## 📁 Repository Structure

```
lld/
├── solid/              — SOLID Principles (the foundation)
├── decorator/          — Decorator Pattern (structural)
├── observer/           — Observer Pattern (behavioral)
└── README.md           — This file
```

---

## 📚 Modules

### 1. SOLID Principles — `solid/`

The five foundational OOP principles every Google engineer must know.

| File | Principle | One-Liner |
|---|---|---|
| [00_SOLID_Cheatsheet.md](solid/00_SOLID_Cheatsheet.md) | All 5 | Quick reference & interview script |
| [01_S_SingleResponsibility.java](solid/01_S_SingleResponsibility.java) | **S**RP | A class should have only one reason to change |
| [02_O_OpenClosed.java](solid/02_O_OpenClosed.java) | **O**CP | Open for extension, closed for modification |
| [03_L_LiskovSubstitution.java](solid/03_L_LiskovSubstitution.java) | **L**SP | Subtypes must be substitutable for base types |
| [04_I_InterfaceSegregation.java](solid/04_I_InterfaceSegregation.java) | **I**SP | Prefer many small interfaces over one fat one |
| [05_D_DependencyInversion.java](solid/05_D_DependencyInversion.java) | **D**IP | Depend on abstractions, not concretions |

---

### 2. Decorator Pattern — `decorator/`

Structural pattern: attach new behavior to objects dynamically without modifying their class.

| File | Level | Focus |
|---|---|---|
| [00_Basic_Theory.md](decorator/00_Basic_Theory.md) | Theory | When & why to use Decorator, UML, trade-offs |
| [01_Basic_Decorator_Code.java](decorator/01_Basic_Decorator_Code.java) | Basic | Coffee shop example — classic Decorator walkthrough |
| [02_Intermediate_Decorator_Code.java](decorator/02_Intermediate_Decorator_Code.java) | Intermediate | I/O streams, real-world Java Decorator usage |
| [03_Advanced_Decorator_Code.java](decorator/03_Advanced_Decorator_Code.java) | Advanced | Combining with other patterns, thread safety |

---

### 3. Observer Pattern — `observer/`

Behavioral pattern: one-to-many dependency where subjects notify observers of state changes.

| File | Level | Focus |
|---|---|---|
| [00_theory_staff_swe.md](observer/00_theory_staff_swe.md) | Staff-level Theory | Deep dive — push vs pull, distributed systems |
| [01_ObserverPatternDeepDive.java](observer/01_ObserverPatternDeepDive.java) | Advanced | Production-grade Observer with generics |
| [02_Basic_Theory.md](observer/02_Basic_Theory.md) | Theory | Core concepts, UML, event-driven design |
| [03_Basic_Observer_Code.java](observer/03_Basic_Observer_Code.java) | Basic | Weather station example — classic Observer |

---

## 🗺️ Study Order

```
1. SOLID Principles     → Foundation for ALL design patterns
2. Observer Pattern     → Most common behavioral pattern
3. Decorator Pattern    → Most common structural pattern
```

---

## 🎯 What Google Looks For in LLD Interviews

| Criteria | What They Assess |
|---|---|
| **Clean API design** | Are your interfaces intuitive and minimal? |
| **SOLID compliance** | Does your design respect the 5 principles? |
| **Extensibility** | Can new features be added without modifying existing code? |
| **Pattern knowledge** | Can you identify and apply the right pattern? |
| **Trade-off discussion** | Can you articulate WHY you chose a particular design? |
| **Code quality** | Naming, readability, separation of concerns |

---

## 📋 Patterns Roadmap (Future Modules)

| Pattern | Category | Priority | Use Case |
|---|---|---|---|
| **Strategy** | Behavioral | 🔴 High | Swappable algorithms at runtime |
| **Factory / Abstract Factory** | Creational | 🔴 High | Object creation without exposing logic |
| **Singleton** | Creational | 🟡 Medium | Single instance (thread-safe) |
| **Builder** | Creational | 🟡 Medium | Complex object construction |
| **Adapter** | Structural | 🟡 Medium | Interface compatibility |
| **Command** | Behavioral | 🟡 Medium | Undo/redo, task queuing |
| **State** | Behavioral | 🟢 Lower | Finite state machines |
| **Proxy** | Structural | 🟢 Lower | Lazy loading, access control |

---

## 💡 Interview Communication Template

When asked to design a system:

> "Let me start by identifying the **core entities** and their **responsibilities**.  
> I'll apply **SRP** — each class handles one concern.  
> For extensibility, I'll use **OCP** — new features via new classes, not modification.  
> I'll define **interfaces** first (ISP + DIP), then implement.  
> For [specific behavior], the **[Pattern Name]** pattern fits because [reason]."

This structured approach signals senior-level thinking.
