# SE3100 – Architecture Based Development
## Lecture 05 - Distributed Architectural Styles
### Standardized MCQ Bank for Interactive Exam Papers

> Total: **20 questions**  
> **6 Single Choice + 14 Multiple Answer**  
> Every question includes a lecture label, hint, correct answer, explanation, distractor explanation, and trap.

---

## Q1

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
In Event-Driven Architecture, an **event** is best defined as:

### Options
- A. A command instructing a service to act
- B. A description of something that has already happened
- C. A synchronous request for data
- D. A workflow state record
- E. A contract between processors

### Correct Answer
B. A description of something that has already happened

### 💡 Hint
Focus on the defining characteristic, not a related concept.

### Explanation
EDA is based on asynchronous event processing; an event describes something that **has already happened** (Order Placed, Payment Applied). Processors react without the producer coordinating them.

### Why Other Answers Are Wrong
- A = commands are what the **mediator** sends, after the initiating event. C = EDA is asynchronous. D = state is held by the mediator, not by the event definition. E = contracts belong to Microkernel/registry (L4).

### ⚫ Trap
Confusing **event** (past fact, published) with **command** (instruction, directed).

---

## Q2

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
Which distributed style typically uses a **centrally shared monolithic database**?

### Options
- A. Microservices
- B. Event-Driven Architecture
- C. Service-Based Architecture
- D. Space-Based Architecture
- E. None — all distributed styles use database per service

### Correct Answer
C. Service-Based Architecture

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Service-Based = 4–12 coarse domain services, separately deployed, relatively simple topology, **typically one shared monolithic database**. That shared DB is also its main coupling weakness.

### Why Other Answers Are Wrong
- A = Database per Service. B = broker-mediated, not defined by shared DB. D = in-memory grid with async persistence. E = false generalisation.

### ⚫ Trap
Assuming "distributed" always implies data separation.

---

## Q3

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
Over-decomposing into services that are too small produces:

### Options
- A. Distributed monolith by definition
- B. Grains of Sand antipattern
- C. Architecture Sinkhole antipattern
- D. Bounded context violation
- E. Choreography

### Correct Answer
B. Grains of Sand antipattern

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Too-fine granularity → increased communication, harder workflow coordination, higher latency, harder data consistency = **Grains of Sand**, which can lead to a **Distributed Big Ball of Mud**.

### Why Other Answers Are Wrong
- A = the lecture names *Distributed Big Ball of Mud* as the consequence, not "distributed monolith." C = a **Layered** antipattern (L4). D = a different concern. E = a coordination approach.

### ⚫ Trap
Picking C by mixing L4 and L5 antipatterns.

---

## Q4

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
Which style has **Responsiveness ★★★★★, Scalability ★★★★★, Elasticity ★★★★★** but **Fault tolerance ★★**?

### Options
- A. Microservices
- B. Event-Driven Architecture
- C. Service-Based Architecture
- D. Space-Based Architecture
- E. Modular Monolith

### Correct Answer
D. Space-Based Architecture

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Space-Based maxes responsiveness/scalability/elasticity (its whole purpose) but scores Simplicity ★, Testability ★, Fault tolerance ★★, cost $$$$.

### Why Other Answers Are Wrong
- A = Fault tolerance ★★★★★, Responsiveness only ★★. B = Elasticity ★★★. C = mid-range across the board. E = monolithic style with ★ on all three.

### ⚫ Trap
Space-Based is the only style where the "best scaling" style has **weak** fault tolerance.

---

## Q5

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
In the **mediator topology**, communication after the initiating event is received typically uses:

### Options
- A. Events published to a broker
- B. Command messages sent to processors
- C. Synchronous REST calls only
- D. Shared database polling
- E. Publish/subscribe fan-out

### Correct Answer
B. Command messages sent to processors

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The mediator receives the initiating event, knows the required steps, and **sends command messages** to event processors; the mediated topology typically uses **messages rather than events** after the initiating event.

### Why Other Answers Are Wrong
- A/E = describe the **choreographed/broker** topology. C = protocol not specified as REST-only. D = never stated.

### ⚫ Trap
Assuming "event-driven" means everything downstream is an event.

---

## Q6

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Single Choice

### Question
In Space-Based Architecture, persistent database updates occur:

### Options
- A. Synchronously within each transaction
- B. Asynchronously, outside the normal transaction path
- C. Only on system shutdown
- D. Through the API gateway
- E. Via the event mediator

### Correct Answer
B. Asynchronously, outside the normal transaction path

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
SBA removes the central database as a **synchronous constraint**. Transactional data is held primarily in memory with replicated in-memory caching; persistent updates happen asynchronously via the **Data Writer**, so the DB is not involved in every normal transaction.

### Why Other Answers Are Wrong
- A = exactly what SBA eliminates. C = never stated. D = microservices component. E = EDA component.

### ⚫ Trap
Thinking SBA has no database at all. It has one — just off the hot path.

---

## Q7

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which does distribution usually **increase**? *(Select all)*

### Options
- A. Communication complexity
- B. Infrastructure cost
- C. Operational complexity
- D. Simplicity of testing
- E. Debugging difficulty
- F. Data consistency and workflow coordination problems

### Correct Answers
A, B, C, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Trade-off table — improves: scalability, deployability, fault tolerance, team autonomy, evolvability, technology flexibility. Increases: communication complexity, infrastructure cost, operational complexity, testing difficulty, debugging difficulty, data consistency/coordination problems.

### Why Other Answers Are Wrong
- D = inverted; **testing difficulty** increases.

### ⚫ Trap
⚠ **Over-selection warning:** D is the standard inversion bait. Read "increases **testing difficulty**", not "increases simplicity."

---

## Q8

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which are characteristics of **Service-Based Architecture**? *(Select all)*

### Options
- A. Usually 4 to 12 domain services
- B. Coarse-grained functionality
- C. Database per service is mandatory
- D. Separately deployed services
- E. Relatively simple distributed topology
- F. Domain partitioned

### Correct Answers
A, B, D, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Service-Based = pragmatic distributed style, coarse domain services, separately deployed, simple topology, typically **shared** monolithic DB, domain partitioning, cost $$.

### Why Other Answers Are Wrong
- C = the opposite — it typically uses a **centrally shared** database. That's Microservices' rule.

### ⚫ Trap
⚠ **Over-selection warning:** C. Both are domain-partitioned distributed styles; the **data topology** is the separator.

---

## Q9

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which statements about **bounded contexts** in Microservices are correct? *(Select all)*

### Options
- A. They define the boundaries of each service partition
- B. Implementation details may be coupled **inside** the boundary
- C. Other services should not depend on internal code, schema or database structures
- D. They come from Domain-Driven Design
- E. They require all services to share one schema for consistency

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Microservices is strongly influenced by DDD. A bounded context keeps domain concepts, code and data internally consistent; inside, coupling is acceptable; outside, no dependence on internals. Microservices **avoids** shared schemas/databases as integration mechanisms.

### Why Other Answers Are Wrong
- E = directly contradicted.

### ⚫ Trap
⚠ **Over-selection warning:** B looks wrong ("coupling is bad") but internal coupling inside a bounded context is explicitly allowed — same logic as **locality of connascence** in L3.

---

## Q10

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which are consequences of making microservices **too fine-grained**? *(Select all)*

### Options
- A. Communication increases
- B. Workflows become harder to coordinate
- C. Latency increases
- D. Data consistency becomes harder
- E. Fault tolerance automatically improves
- F. Risk of Distributed Big Ball of Mud

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Granularity is the hardest microservices decision; boundaries should consider **Purpose, Transactions, Choreography**. Over-decomposition = Grains of Sand → Distributed Big Ball of Mud.

### Why Other Answers Are Wrong
- E = more services ≠ better fault tolerance; excessive interservice communication is listed as a **weakness**.

### ⚫ Trap
⚠ **Over-selection warning:** E — "more independent services must mean more resilience."

---

## Q11

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which describe **Choreography** (as opposed to Orchestration)? *(Select all)*

### Options
- A. No central coordinator
- B. Each service calls or reacts to other services as needed
- C. Preserves the highly decoupled philosophy of microservices
- D. Creates additional coupling between participants and a coordinator
- E. Avoids coupling services to a central coordinator

### Correct Answers
A, B, C, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Choreography = no central coordinator, direct service collaboration, preserves decoupling; error handling and coordination become harder. Orchestration = localized mediator/orchestration service coordinating calls, adding coupling to the orchestrator.

### Why Other Answers Are Wrong
- D = that's Orchestration's cost.

### ⚫ Trap
⚠ **Over-selection warning:** This is the **sample paper's** question shape ("no central component controlling execution" ⇒ **choreographed/broker**).

---

## Q12

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which are **advantages** of the choreographed/broker EDA topology? *(Select all)*

### Options
- A. Strong decoupling
- B. High responsiveness
- C. High scalability
- D. Easy workflow state tracking
- E. Good fault tolerance
- F. Parallel processing

### Correct Answers
A, B, C, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Choreographed advantages: strong decoupling, high responsiveness, high scalability, good fault tolerance, parallel processing. Challenges: workflow visibility, **state tracking**, error handling, debugging, knowing when the workflow completed.

### Why Other Answers Are Wrong
- D = state tracking is a listed **challenge**.

### ⚫ Trap
⚠ **Over-selection warning:** D. Decoupling buys speed and pays with visibility.

---

## Q13

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
What can the **event mediator** do? *(Select all)*

### Options
- A. Receive the initiating event
- B. Know the steps needed to process it
- C. Send command messages to event processors
- D. Maintain workflow state
- E. Support error handling, recoverability and restart
- F. Eliminate the need for event processors

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Mediator topology: initiating event → event queue → event mediator → channels/commands → event processors. The mediator holds workflow knowledge and state.

### Why Other Answers Are Wrong
- F = processors still perform the work; the mediator only coordinates.

### ⚫ Trap
⚠ **Over-selection warning:** Reading "central controller" as "does everything itself."

---

## Q14

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which statements about **Space-Based Architecture** are correct? *(Select all)*

### Options
- A. Requests are processed by Processing Units
- B. Transactional data is held primarily in memory
- C. Replicated in-memory caching is the standard model
- D. The database is involved in every normal transaction
- E. Virtualized Middleware handles messaging, data, processing and deployment
- F. It targets high scalability, elasticity and concurrency

### Correct Answers
A, B, C, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
SBA exists because replicating web/app servers still leaves the **central database as the limiting resource**. It removes the DB from the synchronous path; persistence is asynchronous via Data Reader/Data Writer.

### Why Other Answers Are Wrong
- D = explicitly the opposite — the DB is **no longer** involved in every normal transaction.

### ⚫ Trap
⚠ **Over-selection warning:** D is a near-verbatim inversion of the slide sentence.

---

## Q15

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which pairs of style → **partitioning type** are correct? *(Select all)*

### Options
- A. Service-Based → Domain
- B. Microservices → Domain
- C. Event-Driven → Technical
- D. Space-Based → Technical
- E. Microservices → Technical
- F. Event-Driven → Domain

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Ratings tables: Service-Based = Domain, Microservices = Domain, EDA = **Technical**, Space-Based = **Technical**. (From L4: Layered = Technical, Modular Monolith = Domain, Microkernel = both.)

### Why Other Answers Are Wrong
- E and F are the direct inversions of B and C.

### ⚫ Trap
⚠ **Over-selection warning:** Assuming every *distributed* style is domain partitioned. EDA and Space-Based are **technical**.

---

## Q16

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
A system needs excellent deployability, testability, evolvability, scalability and fault tolerance, has clean domain data isolation, multiple owning teams, and a mature operations organisation. Which statements match the lecture? *(Select all)*

### Options
- A. Microservices is suitable
- B. Clear bounded contexts must be establishable
- C. Microservices rates ★★★★★ on modularity, maintainability, testability, deployability and evolvability
- D. Overall cost is expected to be low
- E. Strong operational automation is required
- F. Microservices is unsuitable if the domain is highly semantically coupled

### Correct Answers
A, B, C, E, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Microservices suitability list plus the automation requirements (containers, service discovery, monitoring, distributed tracing, API gateways). Ratings: cost $, Simplicity ★, Responsiveness ★★.

### Why Other Answers Are Wrong
- D = cost is the **highest** of all styles ($$$$$).

### ⚫ Trap
⚠ **Over-selection warning:** D. Excellent ratings everywhere makes people forget the price and the ★ simplicity.

---

## Q17

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which are **weaknesses** of Event-Driven Architecture? *(Select all)*

### Options
- A. Low simplicity
- B. Low testability
- C. Nondeterministic workflows
- D. Difficult recoverability
- E. Poor evolvability
- F. Difficult workflow-state tracking

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
EDA ratings: Simplicity ★★, Testability ★★, but **Evolvability ★★★★★, Responsiveness ★★★★★, Fault tolerance ★★★★★**. Strengths also include high modularity/maintainability and asynchronous parallel processing.

### Why Other Answers Are Wrong
- E = Evolvability is one of EDA's **strongest** ratings (★★★★★).

### ⚫ Trap
⚠ **Over-selection warning:** E. "Hard to test and debug" ≠ "hard to evolve." EDA is difficult to *observe*, easy to *extend*.

---

## Q18

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
A team must choose between Service-Based and Microservices. Which statements correctly justify **Service-Based**? *(Select all)*

### Options
- A. Conventional ACID transactions within domain boundaries are valuable
- B. Moderate scalability is sufficient
- C. Lower cost and lower operational complexity are important
- D. The system is moving gradually from monolithic toward distributed
- E. Fine-grained independent scaling of every capability is required
- F. Modularity is needed without microservices-level complexity

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Service-Based is the pragmatic middle: cost $$, Simplicity ★★★, Scalability ★★★, Elasticity ★★, strong ACID support inside domain boundaries. Microservices: cost $$$$$, Simplicity ★, Scalability ★★★★★.

### Why Other Answers Are Wrong
- E = coarse-grained deployment/scaling units are a listed **weakness** of Service-Based; fine-grained scaling points to Microservices.

### ⚫ Trap
⚠ **Over-selection warning:** E. Independent **scaling granularity** is the decisive discriminator between these two styles.

---

## Q19

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which needs can justify considering a distributed architecture? (Select all that apply.)

### Options
- A. Independent deployment of major parts
- B. Independent scalability
- C. Improved fault isolation
- D. Separate team ownership
- E. Frequent change in selected areas
- F. Choosing a fashionable architecture

### Correct Answers
A, B, C, D, E

### 💡 Hint
Select architectural needs that benefit from physical separation, not fashion.

### Explanation
The lecture lists independent deployment/scalability, improved fault isolation, separate ownership and frequent change among the reasons to consider distribution.

### Why Other Answers Are Wrong
- F. Distribution should be driven by architectural need, not fashion.

### ⚫ Trap
⚠ **Over-selection warning:** Modern or fashionable is not an architectural driver.

---

## Q20

**Lecture:** Lecture 05 - Distributed Architectural Styles  
**Type:** Multiple Answer

### Question
Which concerns are introduced when a local component call becomes a remote interaction? (Select all that apply.)

### Options
- A. Network latency
- B. Serialization and deserialization
- C. Endpoint security
- D. Partial failures
- E. Contract management and operational monitoring
- F. Guaranteed elimination of data consistency problems

### Correct Answers
A, B, C, D, E

### 💡 Hint
Remote boundaries add network, failure, contract and operational concerns.

### Explanation
Distribution adds concerns including latency, serialization, endpoint security, partial failures, contract management, monitoring and distributed data/transaction issues.

### Why Other Answers Are Wrong
- F. Distribution usually increases data consistency and workflow coordination problems rather than eliminating them.

### ⚫ Trap
⚠ **Over-selection warning:** Distribution gains flexibility but adds operational and consistency complexity.

---
