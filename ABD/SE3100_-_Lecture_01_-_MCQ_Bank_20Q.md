# SE3100 – Architecture Based Development
## Lecture 01 - Introduction to Software Architecture
### Standardized MCQ Bank for Interactive Exam Papers

> Total: **20 questions**  
> **6 Single Choice + 14 Multiple Answer**  
> Every question includes a lecture label, hint, correct answer, explanation, distractor explanation, and trap.

---

## Q1

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
Does all software have an architecture?

### Options
- A. No — only systems designed by an architect
- B. No — only systems that documented their structure
- C. Yes — every system has structure, responsibilities, dependencies and rules
- D. Yes — but only after the first release
- E. Only if a recognised architectural style was chosen

### Correct Answer
C. Yes — every system has structure, responsibilities, dependencies and rules

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Any system has some form of structure, elements with responsibilities, relationships, dependencies, data flows, and rules whether explicit or implicit. The real question is whether the architecture has been **consciously understood and managed**.

### Why Other Answers Are Wrong
- A/B/E = confuse *having* an architecture with *deliberately choosing* one. D = architecture exists as soon as structure exists.

### ⚫ Trap
"No architecture" is never the answer. Unplanned = **accidental** architecture.

---

## Q2

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
Which is closest to an **architectural** decision rather than a design decision?

### Options
- A. Choosing a sorting algorithm
- B. Changing the data storage mechanism
- C. Designing a screen layout
- D. Naming a class
- E. Selecting a loop construct

### Correct Answer
B. Changing the data storage mechanism

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
A decision is more architectural when strategic, difficult/expensive to change, long-lasting, relevant to several parts, and associated with significant trade-offs. The lecture names **changing the data storage mechanism** as closer to architecture.

### Why Other Answers Are Wrong
- A, C, D, E = detailed classes, algorithms and screen layouts are explicitly closer to **design**.

### ⚫ Trap
Treating architecture and design as fully separate. They exist on a **continuum**.

---

## Q3

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
"The company expects rapid growth" should be translated by the architect into which prioritized Quality Attributes?

### Options
- A. Usability, Testability, Simplicity
- B. Scalability, Elasticity, Availability, Deployability
- C. Security, Auditability, Data integrity
- D. Modifiability, Interoperability
- E. Performance only

### Correct Answer
B. Scalability, Elasticity, Availability, Deployability

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Business drivers are expressed in business language; the architect must translate them into QAs. The lecture's exact example maps rapid growth to Scalability, Elasticity, Availability, Deployability.

### Why Other Answers Are Wrong
- A/C/D/E = plausible QAs but not the mapping given for growth.

### ⚫ Trap
Answering with the QA you'd personally pick instead of the slide's stated mapping. (**W1 pattern.**)

---

## Q4

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
According to the lecture, architecture usually results in:

### Options
- A. The single best architecture for the system
- B. The least-worst architecture
- C. An architecture with no trade-offs
- D. A style-optimised architecture
- E. The cheapest architecture

### Correct Answer
B. The least-worst architecture

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Everything in software architecture is a trade-off; there is no single best architecture for every system, and usually what we end up with is the **least-worst** architecture.

### Why Other Answers Are Wrong
- A/C = directly contradicted. D/E = never claimed.

### ⚫ Trap
"Best architecture" phrasing appears in L1 **and** L4 ("no universally best style") — both are false.

---

## Q5

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
In an **Agile** approach to intentional architecture:

### Options
- A. No architectural decisions are made
- B. Architecture emerges without direction
- C. Enough architecture is established to begin, then planning continues incrementally
- D. All components and interfaces are identified before implementation
- E. Refactoring is avoided to preserve the original structure

### Correct Answer
C. Enough architecture is established to begin, then planning continues incrementally

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Agile = establish enough architecture to begin and continue planning as the system develops; the architecture evolves through implementation and feedback, refactoring improves structure, and the team participates in decisions.

### Why Other Answers Are Wrong
- A/B = the lecture explicitly corrects this — architecturally significant decisions must still be made **deliberately**. D = plan-driven. E = refactoring is a stated Agile mechanism.

### ⚫ Trap
B. "Emergent" ≠ "directionless."

---

## Q6

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Single Choice

### Question
Which dimension covers rules such as **data ownership and communication mechanisms**?

### Options
- A. Quality Attributes
- B. Logical Components
- C. Architectural Style
- D. Architectural Decisions
- E. Business Drivers

### Correct Answer
D. Architectural Decisions

### 💡 Hint
Match the wording to the exact lecture definition.

### Explanation
Architectural Decisions establish the rules and constraints that guide construction — data ownership, communication mechanisms, access rules, security rules and regulations.

### Why Other Answers Are Wrong
- A = capabilities/success conditions. B = domains, services, workflows. C = layered, microservices, etc. E = not one of the four dimensions.

### ⚫ Trap
E. Business drivers **feed** architecture but are not a dimension of it.

---

## Q7

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which are the **four dimensions** of software architecture? *(Select all)*

### Options
- A. Quality Attributes (Architectural Characteristics)
- B. Logical Components
- C. Architectural Style
- D. Architectural Decisions
- E. Business Drivers
- F. Stakeholder Concerns

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The four dimensions each answer a different question: what qualities matter, what parts exist, how they are arranged, what rules constrain implementation. All four apply across the **complete system**, not one module.

### Why Other Answers Are Wrong
- E/F = inputs/influences (business drivers, ABC), not dimensions.

### ⚫ Trap
⚠ **Over-selection warning:** Adding E or F. Both appear later in the same lecture, which is exactly why they're tempting.

---

## Q8

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
When is a decision considered **more architectural**? *(Select all)*

### Options
- A. Strategic rather than tactical
- B. Difficult or expensive to change
- C. Long-lasting
- D. Relevant to several parts of the system
- E. Associated with significant trade-offs
- F. Made by a senior developer

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
All five are the stated criteria on the architecture-vs-design continuum.

### Why Other Answers Are Wrong
- F = **who** makes a decision does not determine whether it is architectural.

### ⚫ Trap
⚠ **Over-selection warning:** Under-selecting. All five listed criteria are correct; only the "who" option is bait.

---

## Q9

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which describe **Accidental Architecture**? *(Select all)*

### Options
- A. Structure results from unrelated local decisions
- B. Dependencies grow without control
- C. Decisions may not be documented or understood
- D. Problems become visible only when the system is difficult to change
- E. The system has no architecture at all
- F. Frameworks are allowed to determine the system structure

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Accidental architecture emerges without sufficient architectural reasoning. Not planning does **not** produce a system without architecture — it produces an architecture that was **not deliberately selected**.

### Why Other Answers Are Wrong
- E = explicitly contradicted.

### ⚫ Trap
⚠ **Over-selection warning:** E. The most-picked wrong option in the whole lecture.

---

## Q10

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which are correct **trade-off** examples from Lecture 01? *(Select all)*

### Options
- A. Greater security may reduce usability
- B. Greater consistency may reduce availability
- C. Greater flexibility may increase complexity
- D. Greater isolation may increase communication overhead
- E. Faster delivery may increase technical debt
- F. Greater modularity eliminates trade-offs

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
All five are stated. Conclusion: there is no single best architecture for every system; the result is usually the least-worst architecture.

### Why Other Answers Are Wrong
- F = contradicts "everything in software architecture is a trade-off."

### ⚫ Trap
⚠ **Over-selection warning:** F. Same "everything improves" fallacy as L2 Q9 — always wrong.

---

## Q11

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which are correct about **Plan-driven** intentional architecture? *(Select all)*

### Options
- A. Most major architectural planning is performed up front
- B. Requirements are studied early
- C. Major components and interfaces are identified early
- D. Significant changes may require the architecture to be revised
- E. It does not involve deliberate architectural decisions
- F. Waterfall is a given example

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Plan-driven treats architecture as an **early foundation** for development. Both plan-driven and Agile involve **deliberate** architectural decisions.

### Why Other Answers Are Wrong
- E = false for both approaches.

### ⚫ Trap
⚠ **Over-selection warning:** Assuming "intentional" belongs only to plan-driven. Agile is also intentional.

---

## Q12

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which factors influence architecture in the **Architecture Business Cycle**? *(Select all)*

### Options
- A. Stakeholder concerns
- B. Developing organization
- C. Technical environment
- D. Architect's experience
- E. The resulting architecture influences those environments in return
- F. The programming language syntax

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The ABC describes the relationship between architecture and its environment, and how architecture itself influences that environment in return — a **feedback** relationship.

### Why Other Answers Are Wrong
- F = never listed.

### ⚫ Trap
⚠ **Over-selection warning:** Missing E. The **feedback direction** is the defining idea of the ABC, not just the list of influences.

---

## Q13

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which are **business drivers** as defined in the lecture? *(Select all)*

### Options
- A. Reducing time to market
- B. Improving user satisfaction
- C. Gaining a competitive advantage
- D. Meeting a fixed deadline
- E. Remaining within a limited budget
- F. Achieving 99.99% uptime

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Business drivers are business goals, pressures and constraints, normally expressed in **business language**. The architect translates them into Quality Attributes.

### Why Other Answers Are Wrong
- F = a **quality attribute response measure** (Availability), expressed in technical language — the *output* of the translation, not the driver.

### ⚫ Trap
⚠ **Over-selection warning:** F. Test = "is it in business language or technical language?"

---

## Q14

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
In what order do the four dimensions connect to produce an architecture? *(Select all correct statements)*

### Options
- A. Understanding the problem domain comes first
- B. Quality Attributes are identified before logical components
- C. The architectural style is selected before quality attributes are known
- D. Architectural decisions are established after the style is selected
- E. A style alone does not represent the complete architecture

### Correct Answers
A, B, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Sequence: understand problem domain → identify QAs → identify logical components → select style → establish decisions.

### Why Other Answers Are Wrong
- C = inverted; do not select a style before understanding domain and qualities (also matches L3's "requirements before style" and L4's "not fashion").

### ⚫ Trap
⚠ **Over-selection warning:** C. This same principle is tested in **three separate lectures** — expect it in the exam.

---

## Q15

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which stakeholder-to-concern mappings from the ABC diagram are correct? *(Select all)*

### Options
- A. Maintenance organization → modifiability
- B. End user → behaviour, performance, security, reliability, usability
- C. Marketing → new features, short time to market, parity with competitors
- D. Developing organization management → low cost, keeping people employed
- E. Customer → maximum feature count regardless of cost

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Customer concerns are **low cost, timely delivery, and not changing often** — the opposite of E.

### Why Other Answers Are Wrong
- E = contradicts the customer row.

### ⚫ Trap
⚠ **Over-selection warning:** Confusing **customer** (buys it) with **end user** (uses it). They have different concerns in this diagram.

---

## Q16

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which items may form part of a software system beyond source code? (Select all that apply.)

### Options
- A. Data and databases
- B. Configurations, libraries and frameworks
- C. External services
- D. Interfaces to other systems
- E. Deployment and runtime environments
- F. Only executable source files

### Correct Answers
A, B, C, D, E

### 💡 Hint
Recall the slide explaining that software is more than source code.

### Explanation
A software system may include data and databases, configurations, libraries and frameworks, external services, interfaces to other systems, and deployment/runtime environments.

### Why Other Answers Are Wrong
- F. The lecture explicitly states that software is more than source code and executable programs.

### ⚫ Trap
⚠ **Over-selection warning:** Do not reduce a software system to code only.

---

## Q17

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which factors can make software systems more complex? (Select all that apply.)

### Options
- A. Increasing functionality
- B. More users and stakeholders
- C. More modules, components and services
- D. More relationships and dependencies
- E. Integration with external systems
- F. Changing requirements and technologies

### Correct Answers
A, B, C, D, E, F

### 💡 Hint
Think about growth in both the number of system elements and their interactions.

### Explanation
The lecture lists increasing functionality, more users and stakeholders, more modules/components/services, dependencies, external integrations, quality expectations, and changing requirements and technologies as causes of complexity.

### Why Other Answers Are Wrong
- All listed options are correct; there is no incorrect distractor in this item.

### ⚫ Trap
⚠ **Over-selection warning:** All listed choices are lecture-supported causes.

---

## Q18

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which actions help manage software complexity? (Select all that apply.)

### Options
- A. Divide the system into meaningful parts
- B. Assign clear responsibilities
- C. Establish boundaries
- D. Control dependencies
- E. Define how parts communicate
- F. Allow unrestricted dependencies among all parts

### Correct Answers
A, B, C, D, E

### 💡 Hint
Look for actions that impose structure and controlled interaction.

### Explanation
Complexity is managed by meaningful decomposition, clear responsibilities, boundaries, dependency control, defined communication, and consistent rules.

### Why Other Answers Are Wrong
- F. Unrestricted dependencies increase complexity rather than control it.

### ⚫ Trap
⚠ **Over-selection warning:** More connectivity is not the goal; controlled dependencies are.

---

## Q19

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which statements describe Intentional Architecture? (Select all that apply.)

### Options
- A. Important Quality Attributes are identified
- B. Responsibilities are assigned clearly
- C. Dependencies are controlled
- D. An appropriate structural approach is selected
- E. Important decisions are communicated
- F. Every architectural decision must be made before implementation starts

### Correct Answers
A, B, C, D, E

### 💡 Hint
Intentional means deliberate architectural reasoning, not deciding everything up front.

### Explanation
Intentional architecture results from deliberate decisions about Quality Attributes, responsibilities, dependencies, structure, communication, and review as the system changes.

### Why Other Answers Are Wrong
- F. The lecture states that intentional architecture does not mean every decision must be made at the beginning.

### ⚫ Trap
⚠ **Over-selection warning:** Do not confuse intentional architecture with fully up-front architecture.

---

## Q20

**Lecture:** Lecture 01 - Introduction to Software Architecture  
**Type:** Multiple Answer

### Question
Which factors can influence architectural decisions? (Select all that apply.)

### Options
- A. Business needs
- B. Available technologies
- C. Cost and time
- D. Development skills
- E. Operational environment and existing systems
- F. Organizational constraints

### Correct Answers
A, B, C, D, E, F

### 💡 Hint
Architecture is context-dependent; consider business, technical, people and organizational constraints.

### Explanation
The lecture lists business needs, technologies, cost, time, development skills, operational environment, existing systems and organizational constraints as architectural influences.

### Why Other Answers Are Wrong
- All listed options are correct; there is no incorrect distractor in this item.

### ⚫ Trap
⚠ **Over-selection warning:** The same architecture is not automatically suitable for every system.

---
