# SE3100 – Architecture Based Development
## Lecture 04 - Monolithic Architectural Styles
### Standardized MCQ Bank for Interactive Exam Papers

> Total: **20 questions**  
> **6 Single Choice + 14 Multiple Answer**  
> Every question includes a lecture label, hint, correct answer, explanation, distractor explanation, and trap.

---

## Q1

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
CQRS is best classified as:

### Options
- A. An architectural style
- B. An architectural pattern
- C. A partitioning approach
- D. A quality attribute
- E. A deployment topology

### Correct Answer
B. An architectural pattern

### 💡 Hint
Focus on the defining characteristic, not a related concept.

### Explanation
Style = overall structure + topology + default characteristics (e.g. Microservices). Pattern = contextualized solution to a particular problem, **applied within** a style (e.g. CQRS).

### Why Other Answers Are Wrong
- A = the slide's style example is Microservices. C = technical/domain are the partitioning options. D = CQRS is a solution, not a measurable property. E = it isn't a deployment shape.

### ⚫ Trap
Treating "style" and "pattern" as synonyms. Style is broader; pattern lives **inside** a style.

---

## Q2

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
Which layer arrangement enables **Layers of Isolation**?

### Options
- A. Open layers
- B. Closed layers
- C. Shared components
- D. Open services layer
- E. Domain modules

### Correct Answer
B. Closed layers

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Layers of Isolation = changes in one layer don't affect others while contracts remain unchanged. Explicitly **enabled by closed layers**, because requests cannot skip layers.

### Why Other Answers Are Wrong
- A/D = bypassing increases coupling and **reduces** isolation. C = shared components are a Business-layer access rule. E = belongs to Modular Monolith.

### ⚫ Trap
Open layers sound more "flexible," so students pick A.

---

## Q3

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
Requests pass down through every layer and back up with no layer performing business logic. This is:

### Options
- A. Layers of Isolation
- B. Architecture Sinkhole Antipattern
- C. Open services layer
- D. Big Ball of Mud
- E. Technical partitioning

### Correct Answer
B. Architecture Sinkhole Antipattern

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Sinkhole = pass-through with **no business logic performed**, causing unnecessary object instantiation and processing → drains memory and performance.

### Why Other Answers Are Wrong
- A = a benefit, not an antipattern. C = a deliberate bypass design. D = mentioned only for Microkernel customization risk. E = the partitioning type, not the antipattern.

### ⚫ Trap
Assuming any sinkhole scenario means the architecture failed — the slide says **every** layered architecture has some.

---

## Q4

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
In Microkernel architecture, plug-ins should primarily communicate with:

### Options
- A. Each other, directly
- B. The core system
- C. The presentation layer
- D. A shared plug-in database
- E. An event broker

### Correct Answer
B. The core system

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Plug-ins should be self-contained, **independent of other plug-ins**, and connected primarily to the core. Typical communication is core→plug-in via method/function call.

### Why Other Answers Are Wrong
- A = plug-in independence is the stated ideal. C = layers are internal to the core. D = plug-ins may own **their own** data stores. E = EDA belongs to L5.

### ⚫ Trap
Ticking A because real plug-in ecosystems often chain.

---

## Q5

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
Which style has the **highest Modularity, Maintainability, Testability, Deployability and Evolvability** ratings among the three monolithic styles?

### Options
- A. Layered
- B. Modular Monolith
- C. Microkernel
- D. All are equal
- E. Layered, because of Layers of Isolation

### Correct Answer
C. Microkernel

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Microkernel scores ★★★ on those five; Modular Monolith ★★; Layered ★ (Testability ★★). All three: 1 quantum, cost $, Scalability/Elasticity/Fault tolerance = ★.

### Why Other Answers Are Wrong
- A = lowest on those. B = middle. D = ratings differ. E = isolation doesn't raise the rating table values.

### ⚫ Trap
Layered has the highest **Simplicity** (★★★★★) — that's a different row.

---

## Q6

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Single Choice

### Question
A modular monolith gives each module its own database. The application is now:

### Options
- A. Distributed, because there are multiple data stores
- B. Service-based architecture
- C. Still monolithic, because deployment is one application unit
- D. Two architectural quanta
- E. Technically partitioned

### Correct Answer
C. Still monolithic, because deployment is one application unit

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
A modular monolith may use one shared database **or** separate module databases. Data topology alone does not change the classification — it remains monolithic because deployment is a single application unit.

### Why Other Answers Are Wrong
- A = distribution requires multiple **deployment units** over a network. B/D = one deployment unit = 1 quantum. E = modular monolith is **domain** partitioned.

### ⚫ Trap
Equating "database per module" with microservices.

---

## Q7

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which aspects does an **architectural style** describe? *(Select all)*

### Options
- A. Component topology
- B. Physical architecture
- C. Deployment
- D. Communication style
- E. Data topology
- F. Project budget approval process

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The 5-row style table: component topology (how components/dependencies organized), physical architecture (monolithic or distributed), deployment, communication style, data topology.

### Why Other Answers Are Wrong
- F = a project-management concern, never listed.

### ⚫ Trap
⚠ **Over-selection warning:** Under-selecting here out of fear. All five are on the slide; only F is bait.

---

## Q8

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which are true of **Layered Architecture**? *(Select all)*

### Options
- A. Technically partitioned
- B. Domain partitioned
- C. Number of quanta = 1
- D. Simplicity ★★★★★
- E. Scalability ★★★★
- F. Common layers: Presentation, Business, Persistence, Database

### Correct Answers
A, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Layered = technical partitioning, 1 quantum, cost $, Simplicity ★★★★★, but Modularity/Maintainability/Deployability/Evolvability/Scalability/Elasticity/Fault tolerance all ★.

### Why Other Answers Are Wrong
- B = that's Modular Monolith. E = Scalability is **★**, the weakest rating.

### ⚫ Trap
⚠ **Over-selection warning:** E. Simplicity being maximal makes people assume other ratings are also high.

---

## Q9

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which statements about **open and closed layers** are correct? *(Select all)*

### Options
- A. A closed layer cannot be skipped by a request
- B. An open layer may be bypassed
- C. Bypassing reduces coupling between layers
- D. More bypassing leads to less isolation
- E. Whether a layer is open or closed is an architectural decision
- F. Open layers are always preferable for performance

### Correct Answers
A, B, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Closed = sequential top-to-bottom, no skipping (enables Layers of Isolation). Open = may be bypassed to avoid unnecessary processing, but more bypassing → higher coupling → less isolation.

### Why Other Answers Are Wrong
- C = inverted; bypassing **increases** coupling. F = "always" — it's a trade-off decision.

### ⚫ Trap
⚠ **Over-selection warning:** C is the exact inversion trick this module reuses constantly.

---

## Q10

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which are correct about the **Architecture Sinkhole Antipattern**? *(Select all)*

### Options
- A. Requests are passed layer to layer with no business logic performed
- B. It causes unnecessary object instantiation and processing
- C. It drains memory consumption and performance
- D. It only occurs in domain-partitioned architectures
- E. Every layered architecture will have some scenarios that qualify
- F. It is solved by making every layer closed

### Correct Answers
A, B, C, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Sinkhole = pure pass-through requests. The lecture explicitly notes that every layered architecture will have some sinkhole scenarios; the concern is **how many**.

### Why Other Answers Are Wrong
- D = it's a **layered** (technically partitioned) antipattern. F = closing layers forces pass-through, which **causes** the sinkhole; open layers relieve it.

### ⚫ Trap
⚠ **Over-selection warning:** F. Closed layers are good for isolation but are exactly what makes sinkholes appear.

---

## Q11

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which are true of the **Modular Monolith**? *(Select all)*

### Options
- A. One deployment unit
- B. Primarily domain partitioned
- C. Layers may exist inside individual domain modules
- D. Must use exactly one shared database
- E. Naturally supports Domain-Driven Design
- F. Number of quanta = 1

### Correct Answers
A, B, C, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Modular Monolith = one deployment unit organized around business domains; layers may exist inside modules; supports DDD because it is domain partitioned; may use one shared DB **or** module-owned DBs.

### Why Other Answers Are Wrong
- D = "must" is false; both data topologies are permitted.

### ⚫ Trap
⚠ **Over-selection warning:** D contains a hidden absolute. Also note C — domain partitioning does **not** abolish layers.

---

## Q12

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
A product's UI and database technologies are replaced frequently across the whole system. Which statements match the lecture? *(Select all)*

### Options
- A. Modular Monolith is a poor fit for this situation
- B. Technical changes may affect many or all domain modules
- C. Such changes require significant coordination between domain teams
- D. Layered architecture may be a better choice
- E. Microkernel is required because plug-ins isolate technical change

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Because the Modular Monolith is domain partitioned, technical concerns are repeated inside every module, so cross-cutting technical change hits many modules → Layered is recommended instead.

### Why Other Answers Are Wrong
- E = Microkernel isolates **variable/customizable feature** behaviour, not UI/DB technology swaps; and "required" is absolute.

### ⚫ Trap
⚠ **Over-selection warning:** E. Microkernel is the answer for **customization/variability**, not for technical technology churn.

---

## Q13

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which describe **plug-ins** in Microkernel architecture? *(Select all)*

### Options
- A. Specialized, variable, customizable functionality
- B. More likely to change than the core
- C. Should ideally be independent of other plug-ins
- D. May be compile-based or runtime-based
- E. Must always share the core's database
- F. May own their own data store

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Core = minimum, stable functionality; plug-ins = specialized/variable/customizable/likely-to-change, self-contained, connected primarily to the core; compile-based (redeploy) vs runtime-based (hot add/remove); plug-ins can own their own data stores.

### Why Other Answers Are Wrong
- E = the data-ownership diagram explicitly shows plug-in-owned data stores.

### ⚫ Trap
⚠ **Over-selection warning:** E — "must always" again.

---

## Q14

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
What may a **Plug-in Registry** contain, and what do **contracts** define? *(Select all)*

### Options
- A. Plug-in name
- B. Plug-in location or reference
- C. Contract information
- D. Expected behaviour, input data, output data
- E. The core's business rules
- F. Deployment cost estimates

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The core must know which plug-ins exist and how to reach them → registry holds name, location/reference, contract info. Contracts define expected behaviour, input data, output data, allowing plug-ins to vary **without specialized core logic for each one**.

### Why Other Answers Are Wrong
- E = core rules aren't registry content. F = never mentioned.

### ⚫ Trap
⚠ **Over-selection warning:** Forgetting the *purpose* clause — contracts exist so the core doesn't need per-plug-in special-case code.

---

## Q15

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
A commercial product has a stable core plus optional customer-specific features that change often, with **no need to scale those features independently**. Which statements are correct? *(Select all)*

### Options
- A. Microkernel is the most appropriate choice
- B. Variability can be isolated without introducing distributed-system complexity
- C. Deploying each optional feature as a remote service adds network and operational complexity
- D. Event-Driven Architecture is required because features change independently
- E. The core should hold the stable, minimum functionality

### Correct Answers
A, B, C, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Microkernel is a natural fit for product-based applications needing customization/extensibility; it moves variation away from a stable core. Remote plug-ins via REST/messaging introduce distributed-system complexity, which isn't justified when independent scaling isn't required.

### Why Other Answers Are Wrong
- D = "required" is false; frequent change alone does not mandate async distribution.

### ⚫ Trap
⚠ **Over-selection warning:** This is the **sample paper's scenario question**. The tempting wrong logic is "frequently changing ⇒ separate deployment." Independent **scaling** need is what would justify distribution.

---

## Q16

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which rows of the three-style comparison table are correct? *(Select all)*

### Options
- A. Layered → primary structure = technical layers
- B. Modular Monolith → main structural benefit = domain modularity
- C. Microkernel → main structural benefit = extensibility
- D. Microkernel → partitioning = technical and/or domain
- E. Modular Monolith → typical deployment = distributed
- F. Layered → best fit = customizable systems

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
All three are typically **monolithic** deployment. Best fit: Layered = simple technical structure; Modular Monolith = domain-oriented; Microkernel = customizable systems.

### Why Other Answers Are Wrong
- E = Modular Monolith deploys monolithically. F = customizable systems = **Microkernel**.

### ⚫ Trap
⚠ **Over-selection warning:** Assuming "modular" implies distributed deployment.

---

## Q17

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which are stated advantages of monolithic architectures over distributed ones? *(Select all)*

### Options
- A. Fewer deployment units
- B. No required remote communication between internal components
- C. Lower infrastructure and network complexity
- D. Lower overall cost
- E. Higher fault tolerance and elasticity
- F. Local calls avoid the problems of remote communication

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Monolith benefits list, tied back to the Fallacies of Distributed Computing from L3. All three monolithic styles rate Scalability, Elasticity and Fault tolerance at ★.

### Why Other Answers Are Wrong
- E = fault tolerance and elasticity are the **weakest** ratings (★) for all monolithic styles; those are distributed-architecture strengths.

### ⚫ Trap
⚠ **Over-selection warning:** E. "Simpler = more reliable" feels intuitive but contradicts the ratings table.

---

## Q18

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which statements about monolithic architectural styles are correct? (Select all that apply.)

### Options
- A. A monolith may contain many components and modules
- B. A monolith may have strong internal modularity
- C. Its elements normally belong to a single application deployment boundary
- D. Layered, Modular Monolith and Microkernel are monolithic styles discussed in the lecture
- E. Monolithic means the system cannot be domain partitioned
- F. Monolithic architectures avoid required remote calls between internal application components

### Correct Answers
A, B, C, D, F

### 💡 Hint
Monolithic describes the deployment boundary, not the absence of internal structure.

### Explanation
Monoliths can be richly structured internally while remaining within one application deployment boundary.

### Why Other Answers Are Wrong
- E. A Modular Monolith is domain partitioned while still remaining monolithic.

### ⚫ Trap
⚠ **Over-selection warning:** Do not equate monolith with a Big Ball of Mud.

---

## Q19

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which situations are suitable for Layered Architecture? (Select all that apply.)

### Options
- A. Small, simple applications
- B. Websites
- C. Tight budgets
- D. Tight development schedules
- E. Development must begin before long-term architectural direction is clear
- F. Systems requiring very high scalability, agility and deployability

### Correct Answers
A, B, C, D, E

### 💡 Hint
Layered Architecture trades advanced scalability and deployability for simplicity and lower cost.

### Explanation
The lecture recommends Layered Architecture for small/simple systems, websites, tight budgets/schedules, and uncertain long-term architectural direction.

### Why Other Answers Are Wrong
- F. It is less suitable for large systems that require high scalability, agility and deployability.

### ⚫ Trap
⚠ **Over-selection warning:** High simplicity does not imply high scalability.

---

## Q20

**Lecture:** Lecture 04 - Monolithic Architectural Styles  
**Type:** Multiple Answer

### Question
Which statements explain why Microkernel Architecture is suitable for customizable products? (Select all that apply.)

### Options
- A. It isolates variable behaviour from a stable core
- B. Plug-ins support addition, removal and modification of features
- C. It can reduce complex customization logic in the core
- D. It is useful where variation among deployments is common
- E. It requires every plug-in to directly depend on every other plug-in
- F. Typical examples include development tools and browser extensions

### Correct Answers
A, B, C, D, F

### 💡 Hint
The stable part stays in the core; changeable capabilities move into extensions.

### Explanation
Microkernel supports a stable core plus variable plug-ins, making it suitable for customization and frequent feature variation.

### Why Other Answers Are Wrong
- E. Plug-ins should ideally remain independent of other plug-ins.

### ⚫ Trap
⚠ **Over-selection warning:** Extensibility depends on plug-in independence, not plug-in-to-plug-in coupling.

---
