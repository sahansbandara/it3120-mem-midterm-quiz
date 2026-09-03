# SE3100 – Architecture Based Development
## Lecture 03 - Architectural Thinking
### Standardized MCQ Bank for Interactive Exam Papers

> Total: **20 questions**  
> **6 Single Choice + 14 Multiple Answer**  
> Every question includes a lecture label, hint, correct answer, explanation, distractor explanation, and trap.

---

## Q1

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
Which term describes the number of elements affected by a dependency?

### Options
- A. Strength
- B. Locality
- C. Degree
- D. Cohesion
- E. Afferent coupling

### Correct Answer
C. Degree

### 💡 Hint
Match the wording to the exact lecture definition.

### Explanation
Connascence has 3 properties — Strength (ease of refactoring), Locality (closeness), Degree (how many elements affected).

### Why Other Answers Are Wrong
- A = ease of refactoring, not count. B = distance between elements. D = internal relatedness, not a connascence property. E = incoming connections.

### ⚫ Trap
Strength ↔ Degree swap. Strength = *how hard*, Degree = *how many*.

---

## Q2

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
An application cannot operate without its database. According to the lecture, the database:

### Options
- A. Is a separate architectural quantum
- B. Forms part of the same architectural quantum as the application
- C. Is excluded because it is infrastructure
- D. Creates static connascence of timing
- E. Makes the system automatically distributed

### Correct Answer
B. Forms part of the same architectural quantum as the application

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
A quantum contains the components necessary to function independently; operational dependencies belong to the quantum. Two services sharing one DB are in the **same** quantum.

### Why Other Answers Are Wrong
- A = contradicts independent-operation rule. C = infrastructure needed to run is included. D = timing is *dynamic*, not static. E = distribution needs multiple deployment units + remote protocols.

### ⚫ Trap
Thinking "database is just storage, not architecture."

---

## Q3

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
Which is the defining characteristic of a monolithic architecture?

### Options
- A. It contains no modules
- B. It uses only technical partitioning
- C. It is deployed as a single unit
- D. It has exactly one quality attribute
- E. It cannot use domain partitioning

### Correct Answer
C. It is deployed as a single unit

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
A monolith may contain multiple modules, components, strong internal boundaries, and domain and/or technical partitioning. Only the **single deployment unit** defines it.

### Why Other Answers Are Wrong
- A, B, E = the lecture explicitly permits all of these inside a monolith. D = confuses QA scope with deployment.

### ⚫ Trap
Equating "monolith" with "badly structured big ball of mud."

---

## Q4

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
Connascence is best described as:

### Options
- A. Components that communicate with each other
- B. Components deployed together
- C. A change in one component requiring another to change for system correctness
- D. Elements inside a module being related
- E. Incoming connections to an artifact

### Correct Answer
C. A change in one component requiring another to change for system correctness

### 💡 Hint
Focus on the defining characteristic, not a related concept.

### Explanation
Exact definition wording — *a change in one requires the other to be modified to maintain overall correctness*. It is a more precise vocabulary for coupling.

### Why Other Answers Are Wrong
- A = communication alone doesn't force change. B = deployment ≠ connascence. D = that's cohesion. E = afferent coupling.

### ⚫ Trap
Option A sounds right and is the most-picked distractor.

---

## Q5

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
"Convert strong forms of connascence into weaker forms" refers to which property?

### Options
- A. Locality
- B. Degree
- C. Strength
- D. Cohesion
- E. Granularity

### Correct Answer
C. Strength

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Strength = ease of refactoring; the strength ladder (Name→Type→Meaning→Algorithm→Position→Execution→Timing→Value→Identity) gives the refactoring **direction**.

### Why Other Answers Are Wrong
- A = about distance. B = about count. D/E = not connascence properties.

### ⚫ Trap
Reading the ladder as "best to worst list" instead of a refactoring direction.

---

## Q6

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Single Choice

### Question
Two independently deployed services communicate **synchronously**. What does the lecture say this introduces?

### Options
- A. Static connascence of name
- B. Dynamic coupling that lets one quantum's operational QAs affect another
- C. Automatic merging into a monolith
- D. Higher cohesion in both services
- E. Removal of the quantum boundary

### Correct Answer
B. Dynamic coupling that lets one quantum's operational QAs affect another

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Synchronous communication ⇒ dynamic coupling ⇒ operational QAs of one quantum affect the other ⇒ may influence effective quantum boundaries.

### Why Other Answers Are Wrong
- A = static forms come from source code. C/E = "may influence boundaries" ≠ boundary destroyed. D = cohesion is internal, unaffected.

### ⚫ Trap
Choosing E — the slide says *influence*, not *eliminate*.

---

## Q7

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which are **static** connascence types? *(Select all)*

### Options
- A. Name
- B. Execution
- C. Meaning
- D. Position
- E. Identity
- F. Algorithm
- G. Timing

### Correct Answers
A, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Static (5) = **N**ame, **T**ype, **M**eaning, **P**osition, **A**lgorithm — detectable from source code. Dynamic (4) = Execution, Timing, Value, Identity — arise at runtime.

### Why Other Answers Are Wrong
- B, E, G are all dynamic (runtime behaviour).

### ⚫ Trap
⚠ **Over-selection warning:** "Position" *sounds* runtime (argument order at call time) but is **static** — you see it in the code. Ticking B/E/G here is the classic over-selection that zeroes the question.

---

## Q8

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which are characteristics of an **architectural quantum**? *(Select all)*

### Options
- A. Independent deployment
- B. High functional cohesion
- C. Zero communication with other quanta
- D. Low external implementation static coupling
- E. Shared database with other quanta
- F. Smallest part that can be deployed and run independently

### Correct Answers
A, B, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The 3 stated characteristics are independent deployment, high functional cohesion, low external implementation static coupling; the simple definition is the smallest independently deployable and runnable part.

### Why Other Answers Are Wrong
- C = quanta *do* communicate; that creates dynamic coupling. E = sharing a DB puts them in the **same** quantum, so it's not a characteristic of separate quanta.

### ⚫ Trap
⚠ **Over-selection warning:** Ticking C. "Independent deployment" ≠ "no communication."

---

## Q9

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which statements about **technical partitioning** are correct? *(Select all)*

### Options
- A. Top-level components organized around technical capabilities
- B. Examples include presentation, business rules, service, persistence
- C. Business workflows tend to stay inside one partition
- D. Related technical code is easy to locate
- E. Aligns naturally with layered architecture
- F. Aligns naturally with microservices

### Correct Answers
A, B, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Technical partitioning = organized by technical capability; advantages = clear separation of technical concerns + easy code location + aligns with layered; trade-off = **workflows cut across several partitions**.

### Why Other Answers Are Wrong
- C = the exact opposite; workflows **cross** partitions. F = microservices align with **domain** partitioning.

### ⚫ Trap
⚠ **Over-selection warning:** C is the single most common wrong tick. The whole point of technical partitioning is that workflows do **not** stay together.

---

## Q10

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
A good architectural boundary should achieve which of the following? *(Select all)*

### Options
- A. High cohesion
- B. Localized strong coupling
- C. Maximum number of modules
- D. Low external coupling
- E. Elimination of all coupling
- F. Related behaviour kept together

### Correct Answers
A, B, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Good module = keep related behaviour together (high cohesion) + keep strongly dependent elements together (localize coupling) + reduce dependencies crossing the boundary (low external coupling).

### Why Other Answers Are Wrong
- C = "more modules" is explicitly warned against — splitting cohesive functionality adds coupling. E = coupling is minimized, never eliminated.

### ⚫ Trap
⚠ **Over-selection warning:** E feels architecturally virtuous. No slide claims zero coupling.

---

## Q11

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which are **fallacies of distributed computing**? *(Select all)*

### Options
- A. Latency is zero
- B. The network is secure
- C. Transport cost is significant
- D. The topology never changes
- E. Bandwidth is infinite
- F. There are many administrators

### Correct Answers
A, B, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The 8 fallacies: network reliable, latency zero, bandwidth infinite, network secure, topology never changes, **one** administrator, **transport cost zero**, network homogeneous.

### Why Other Answers Are Wrong
- C = inverted (fallacy is "transport cost is **zero**"). F = inverted (fallacy is "there is only **one** administrator").

### ⚫ Trap
⚠ **Over-selection warning:** C and F are the *true* statements dressed as options. The fallacy is always the naive/optimistic version.

---

## Q12

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
According to the lecture, which factors help determine architectural **quantum boundaries**? *(Select all)*

### Options
- A. Quality Attribute scope
- B. Programming language used
- C. Domain boundaries
- D. Static coupling
- E. Shared dependencies
- F. Team size

### Correct Answers
A, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Four listed determinants: QA scope (different QA needs?), domain boundaries (what belongs together?), static coupling (shared structural dependencies?), shared dependencies (common infrastructure/data?).

### Why Other Answers Are Wrong
- B, F = not mentioned anywhere on this slide; organizational/implementation concerns, not quantum determinants.

### ⚫ Trap
⚠ **Over-selection warning:** F is plausible real-world (Conway's Law) but is **not in this lecture** — that's an auto-zero tick.

---

## Q13

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which are true of **Page-Jones's guidelines** for managing connascence? *(Select all)*

### Options
- A. Minimize overall connascence by creating encapsulated elements
- B. Minimize connascence that crosses encapsulation boundaries
- C. Minimize connascence within encapsulation boundaries
- D. Maximize connascence within encapsulation boundaries
- E. Maximize connascence across boundaries

### Correct Answers
A, B, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Minimize overall → minimize **across** boundaries → maximize **within** boundaries. Inside a boundary, high cohesion and stronger internal relationships are acceptable; across boundaries, coupling must be minimized.

### Why Other Answers Are Wrong
- C contradicts D. E is the exact inversion of B.

### ⚫ Trap
⚠ **Over-selection warning:** C looks safe ("minimize is always good") but the guideline is deliberately asymmetric.

---

## Q14

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
A system has three areas with different QA needs: public-facing, back-office, and frequently changing. Which conclusions match the lecture? *(Select all)*

### Options
- A. Different QA clusters can indicate different architectural boundaries
- B. All quality attributes should be applied uniformly to avoid inconsistency
- C. Applying every QA uniformly can create unnecessary and complex trade-offs
- D. The system must be implemented as microservices
- E. The relevant question is the **scope** of each QA set

### Correct Answers
A, C, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Scoped QA = different parts need different combinations/levels. Uniform application creates unnecessary trade-offs; the clusters suggest boundaries; scope → boundaries → architectural quantum.

### Why Other Answers Are Wrong
- B = directly contradicted. D = scoped QAs *may* imply multiple quanta, never *must* imply microservices.

### ⚫ Trap
⚠ **Over-selection warning:** D. Multiple quanta ⇒ distributed **may be required**, not "must be microservices."

---

## Q15

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Two strongly connascent elements are moved from one module into two separate modules, dependency unchanged. Which statements are correct? *(Select all)*

### Options
- A. The coupling is now more problematic because it crosses a module boundary
- B. The dependency is removed by the separation
- C. Locality has worsened, so a weaker form of connascence should now be preferred
- D. The strong coupling was more acceptable while both were in the same module
- E. The coupling has become cohesion

### Correct Answers
A, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Locality — strong coupling may be acceptable **within** the same module; across modules/systems the same coupling becomes more problematic. As distance increases, prefer weaker connascence.

### Why Other Answers Are Wrong
- B = moving code does not remove a dependency. E = cohesion is internal relatedness; a cross-module dependency is coupling by definition.

### ⚫ Trap
⚠ **Over-selection warning:** Believing separation itself is an improvement. Splitting without weakening the dependency makes it **worse**.

---

## Q16

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which statements correctly compare **static and dynamic** connascence? *(Select all)*

### Options
- A. Static is at source-code level; dynamic occurs at runtime
- B. Static can be identified through code analysis
- C. Dynamic is generally easier to refactor
- D. Dynamic can create significant runtime dependencies
- E. Static forms are always harmless
- F. Weaker, more manageable forms are preferable where possible

### Correct Answers
A, B, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The 4 comparison dimensions — level, detection, manageability, preference/impact. Static: source-code, code-analysable, easier to refactor, preferred over stronger dynamic forms.

### Why Other Answers Are Wrong
- C = inverted; static is easier. E = "always harmless" is absolute; the slide says weaker forms are preferable *where possible*, not that static = safe.

### ⚫ Trap
⚠ **Over-selection warning:** E. Any option containing **always / never / all** is nearly always a wrong tick in this module.

---

## Q17

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Under the lecture's decision logic, which conditions point toward a **distributed** architecture? *(Select all)*

### Options
- A. Multiple distinct sets of Quality Attributes with independent scopes
- B. Multiple independently deployable quanta are identified
- C. One coherent set of Quality Attributes across the system
- D. The team wants to use a fashionable architecture
- E. Different parts require different combinations or levels of QAs

### Correct Answers
A, B, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
One QA scope → one quantum → **monolith viable**. Multiple independent scopes → multiple quanta → **distributed may be required**. The decision begins with architectural requirements, not with a style.

### Why Other Answers Are Wrong
- C = points to monolith. D = explicitly rejected ("rather than from being chosen for being fashionable").

### ⚫ Trap
⚠ **Over-selection warning:** Ticking B *and* thinking it's automatic — the slide says distributed **may be** required. Direction of reasoning: requirements → scope → quanta → style. Never reverse it.

---

## Q18

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which statements correctly distinguish cohesion, coupling and connascence? (Select all that apply.)

### Options
- A. Cohesion concerns how closely elements inside a module belong together
- B. Coupling concerns dependencies between software elements
- C. Connascence means a change in one component can require another to change for correctness
- D. High cohesion is generally desirable inside a module
- E. Coupling should be maximized across module boundaries
- F. Connascence provides a more precise vocabulary for coupling

### Correct Answers
A, B, C, D, F

### 💡 Hint
Separate internal relatedness from dependency, then recall the more precise coupling vocabulary.

### Explanation
The lecture defines cohesion as internal relatedness, coupling as dependency, and connascence as change-linked dependency needed to preserve correctness.

### Why Other Answers Are Wrong
- E. Dependencies crossing architectural boundaries should be minimized, not maximized.

### ⚫ Trap
⚠ **Over-selection warning:** Strong internal relationships may be acceptable inside a boundary, not across boundaries.

---

## Q19

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which statements about Domain Partitioning are correct? (Select all that apply.)

### Options
- A. Top-level components are organized around business domains or workflows
- B. Related business behaviour tends to stay together
- C. It aligns naturally with domain-oriented architectures
- D. It can reduce cross-partition coupling for a business workflow
- E. It means every technical concern must exist only once globally
- F. Microservices commonly use domain partitioning

### Correct Answers
A, B, C, D, F

### 💡 Hint
Think vertically by business capability rather than horizontally by technical layer.

### Explanation
Domain partitioning organizes architecture around business domains, subdomains, workflows or capabilities and keeps related business behaviour together.

### Why Other Answers Are Wrong
- E. Domain modules may still contain technical layers or technical concerns.

### ⚫ Trap
⚠ **Over-selection warning:** Domain partitioning does not mean technical layers disappear.

---

## Q20

**Lecture:** Lecture 03 - Architectural Thinking  
**Type:** Multiple Answer

### Question
Which statements describe a distributed architecture according to Lecture 03? (Select all that apply.)

### Options
- A. It contains multiple deployment units
- B. Deployment units communicate through remote access protocols
- C. It introduces physical separation between parts of the system
- D. It can support qualities such as performance, scalability and availability
- E. It introduces additional architectural trade-offs
- F. It is defined by having multiple modules inside one deployment unit

### Correct Answers
A, B, C, D, E

### 💡 Hint
The key separator is physical deployment and remote communication, not internal modularity.

### Explanation
Lecture 03 defines distributed architecture as multiple deployment units communicating remotely. It may support important Quality Attributes but introduces additional trade-offs.

### Why Other Answers Are Wrong
- F. Multiple modules can exist within a monolith; one deployment unit is still monolithic.

### ⚫ Trap
⚠ **Over-selection warning:** Multiple modules do not automatically mean multiple deployment units.

---
