# SE3100 – Architecture Based Development
## Lecture 02 - Quality Attributes, Scenarios and Tactics
### Standardized MCQ Bank for Interactive Exam Papers

> Total: **20 questions**  
> **6 Single Choice + 14 Multiple Answer**  
> Every question includes a lecture label, hint, correct answer, explanation, distractor explanation, and trap.

---

## Q1

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
Which element of a QA scenario specifies the **measurable criterion** used to evaluate the response?

### Options
- A. Stimulus
- B. Environment
- C. Response
- D. Response measure
- E. Artifact

### Correct Answer
D. Response measure

### 💡 Hint
Identify the role of each scenario element before choosing.

### Explanation
Response = the activity the system undertakes; **Response measure** = the measurable criterion used to evaluate that response, making the requirement testable.

### Why Other Answers Are Wrong
- A = the triggering event/condition. B = the conditions in which it occurs. C = the activity itself, not its metric. E = the affected part of the system.

### ⚫ Trap
Response vs Response measure. "Displays results" = Response; "95% within 2 seconds" = Response measure.

---

## Q2

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
A tactic is best defined as:

### Options
- A. A reusable architectural style
- B. A design decision that influences the achievement of a QA response
- C. A measurable criterion for evaluating a response
- D. A contextualized solution to an architectural problem
- E. A stakeholder prioritisation technique

### Correct Answer
B. A design decision that influences the achievement of a QA response

### 💡 Hint
Focus on the defining characteristic, not a related concept.

### Explanation
Tactics are design techniques an architect uses to achieve required QA responses; a tactic **directly affects the system's response to some stimulus**. Flow: Stimulus → Tactics → Response.

### Why Other Answers Are Wrong
- A = style is the overall structure (L4). C = response measure. D = that's an architectural **pattern** (L4). E = the three-QA prioritisation technique.

### ⚫ Trap
Tactic vs Pattern. Tactic = a design decision controlling a response; Pattern = a contextualized solution.

---

## Q3

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
"Caching may improve performance but complicate consistency" illustrates:

### Options
- A. Architectural significance
- B. A quality attribute trade-off
- C. A response measure
- D. A prevent-faults tactic
- E. Functionality vs quality attributes

### Correct Answer
B. A quality attribute trade-off

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
QAs cannot be considered in isolation; achieving one may positively or negatively affect others. Architecture therefore involves **trade-off analysis** rather than independent optimisation.

### Why Other Answers Are Wrong
- A = about needing structural decisions. C = a metric. D = availability tactic category. E = a different distinction (what vs how well).

### ⚫ Trap
Answering "performance" — the question asks what the **statement illustrates**, not which QA appears in it. (W1 check.)

---

## Q4

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
In the general **Performance** scenario, which is a valid stimulus?

### Options
- A. A fault: omission, crash, incorrect timing
- B. Arrival of a periodic, sporadic, or stochastic event
- C. A developer wishing to change the UI
- D. An attempt to modify data
- E. Degraded operation

### Correct Answer
B. Arrival of a periodic, sporadic, or stochastic event

### 💡 Hint
Identify the role of each scenario element before choosing.

### Explanation
Performance stimulus = arrival of a **periodic, sporadic, or stochastic** event. Response measure = latency, deadline, throughput, jitter, miss rate.

### Why Other Answers Are Wrong
- A = **Availability** stimulus (fault). C = Modifiability. D = Security. E = an environment value, not a stimulus.

### ⚫ Trap
Mixing the general scenarios across QAs — this is the most-tested confusion in L2.

---

## Q5

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
Richards and Ford recommend that stakeholders select how many highest-priority Quality Attributes as primary architectural drivers?

### Options
- A. One
- B. Two
- C. Three
- D. Five
- E. As many as the stakeholders wish

### Correct Answer
C. Three

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Shortlist candidates → stakeholders select the **three** highest-priority QAs → use as the primary drivers for design and trade-off analysis. Keep the driving list as short as reasonably possible.

### Why Other Answers Are Wrong
- A/B/D = not the stated number. E = contradicts "as short as reasonably possible."

### ⚫ Trap
The slide adds that this is a **prioritisation technique, not a universal numerical rule** — so a question asking "must there always be exactly three?" answers **no**.

---

## Q6

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Single Choice

### Question
"Increase Semantic Coherence" belongs to which tactic category?

### Options
- A. Reduce Coupling
- B. Increase Cohesion
- C. Defer Binding
- D. Reduce Size of a Module
- E. Manage Resources

### Correct Answer
B. Increase Cohesion

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Modifiability tactic categories: Reduce Size of a Module (Split Module), **Increase Cohesion (Increase Semantic Coherence)**, Reduce Coupling (Encapsulate…), Defer Binding.

### Why Other Answers Are Wrong
- A = Encapsulate etc. C = binding-time decisions. D = Split Module. E = a Performance category.

### ⚫ Trap
"Coherence" sounds like coupling; it's **cohesion**.

---

## Q7

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are the **six elements** of a Quality Attribute Scenario? *(Select all)*

### Options
- A. Source of stimulus
- B. Stimulus
- C. Environment
- D. Artifact
- E. Response
- F. Response measure
- G. Tactic

### Correct Answers
A, B, C, D, E, F

### 💡 Hint
Identify the role of each scenario element before choosing.

### Explanation
The six elements make a QA requirement operational and testable: source, stimulus, environment, artifact, response, response measure.

### Why Other Answers Are Wrong
- G = a tactic is a design decision used to achieve the response — not a scenario element.

### ⚫ Trap
⚠ **Over-selection warning:** Adding "Tactic" or "Quality Attribute" as a seventh element. Exactly six.

---

## Q8

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are the **three differentiating features** of an architectural characteristic? *(Select all)*

### Options
- A. Specifies a non-domain design consideration
- B. Influences a structural aspect of the design
- C. Is important to the success of the system
- D. Is always measurable in seconds
- E. Is documented in the requirements specification
- F. Must be selected by stakeholders

### Correct Answers
A, B, C

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
The triangle model: explicit (specifies a non-domain design consideration), implicit (influences some structural aspect of the design), and critical/important to the success of the system.

### Why Other Answers Are Wrong
- D = "always in seconds" is false; measures vary (%, throughput, hours). E/F = process concerns, not defining features.

### ⚫ Trap
⚠ **Over-selection warning:** F. Stakeholder selection is the **prioritisation** step, not part of the definition.

---

## Q9

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are correct trade-off examples from the lecture? *(Select all)*

### Options
- A. Redundancy may improve availability but increase cost and complexity
- B. Caching may improve performance but complicate consistency
- C. Additional abstraction may improve modifiability but introduce overhead
- D. Strong security controls may reduce usability
- E. Increasing modularity improves every quality attribute simultaneously

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
All four are the lecture's stated examples. The conclusion is that architecture involves trade-off analysis rather than independent optimisation of each quality.

### Why Other Answers Are Wrong
- E = contradicts the entire trade-off principle.

### ⚫ Trap
⚠ **Over-selection warning:** E is the "everything improves" fallacy — never correct in this module.

---

## Q10

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which questions help identify **architecturally significant** Quality Attributes? *(Select all)*

### Options
- A. Which qualities are essential for system success?
- B. Which failures would be unacceptable?
- C. Which qualities require early structural decisions?
- D. Which qualities would be difficult to add later?
- E. Which qualities are cheapest to implement?
- F. Which qualities the development team prefers?

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
A QA is architecturally significant when supporting it requires important structural decisions. It is not practical to treat every desirable quality as equally important; supporting more QAs adds substantial complexity.

### Why Other Answers Are Wrong
- E/F = not on the slide; cost and team preference are not significance criteria.

### ⚫ Trap
⚠ **Over-selection warning:** F echoes L4's "not fashion" principle — preference never decides architecture.

---

## Q11

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are valid **response measures** in the general Performance scenario? *(Select all)*

### Options
- A. Latency
- B. Deadline
- C. Throughput
- D. Jitter
- E. Miss rate
- F. Availability percentage

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify the role of each scenario element before choosing.

### Explanation
Performance measures = latency, deadline, throughput, jitter, miss rate. Availability measures = availability %, time in degraded mode, time to detect fault, repair time, proportion of faults handled.

### Why Other Answers Are Wrong
- F = an **Availability** measure.

### ⚫ Trap
⚠ **Over-selection warning:** F. Every distractor in L2 scenario questions is a real measure — just from the wrong QA.

---

## Q12

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are possible **stimuli or environments** in the general **Availability** scenario? *(Select all)*

### Options
- A. Fault: omission
- B. Fault: crash
- C. Fault: incorrect timing
- D. Environment: degraded operation
- E. Environment: startup
- F. Stimulus: arrival of a stochastic event

### Correct Answers
A, B, C, D, E

### 💡 Hint
Identify the role of each scenario element before choosing.

### Explanation
Availability stimulus = fault (omission, crash, incorrect timing, incorrect response). Environment = normal operation, startup, shutdown, repair mode, degraded operation, overloaded operation.

### Why Other Answers Are Wrong
- F = **Performance** stimulus.

### ⚫ Trap
⚠ **Over-selection warning:** F again — cross-QA contamination.

---

## Q13

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Match the tactic **categories** correctly. *(Select all)*

### Options
- A. Availability → Detect Faults, Recover from Faults, Prevent Faults
- B. Performance → Control Resource Demand, Manage Resources
- C. Security → Detect, Resist, React to, Recover from Attacks
- D. Modifiability → Reduce Size of a Module, Increase Cohesion, Reduce Coupling, Defer Binding
- E. Usability → Detect Faults, Manage Resources

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
These are the four tactic diagrams in the lecture (Pages 30–33). Availability has 3 categories, Performance 2, Security 4, Modifiability 4.

### Why Other Answers Are Wrong
- E = no usability tactic diagram is given; those categories belong to Availability and Performance.

### ⚫ Trap
⚠ **Over-selection warning:** The **count** is examinable: 3-2-4-4.

---

## Q14

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which are **Detect Faults** (Availability) tactics? *(Select all)*

### Options
- A. Ping/Echo
- B. Heartbeat
- C. Monitor
- D. Voting
- E. Encapsulate
- F. Prioritize Events

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Detect Faults: Ping/Echo, Monitor, Heartbeat, Timestamp, Sanity Checking, Condition Monitoring, Voting, Exception Detection, Self-Test.

### Why Other Answers Are Wrong
- E = Modifiability (Reduce Coupling). F = Performance (Control Resource Demand).

### ⚫ Trap
⚠ **Over-selection warning:** Sanity Checking and Self-Test are also Detect Faults — don't reject them if they appear.

---

## Q15

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
"Registered student requests the examination results page during the peak result-release period; the Results service retrieves and displays the results; 95% of requests complete within two seconds." Which mappings are correct? *(Select all)*

### Options
- A. Source of stimulus = Registered student
- B. Environment = Peak result-release period
- C. Artifact = Results service
- D. Response measure = 95% of requests within two seconds
- E. Stimulus = Results service
- F. Response = Peak-load operation

### Correct Answers
A, B, C, D

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Concrete Performance scenario mapping: source = registered student, stimulus = requests the results page, environment = peak-load operation, artifact = results service, response = retrieves and displays results, measure = 95% within two seconds.

### Why Other Answers Are Wrong
- E = Results service is the **artifact**; stimulus is the request. F = peak-load is the **environment**.

### ⚫ Trap
⚠ **Over-selection warning:** Swapped element labels. Read the element name, not the familiar words. (**W1 pattern.**)

---

## Q16

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which statements about **functionality vs quality attributes** are correct? *(Select all)*

### Options
- A. Functionality describes what the system does
- B. Quality attributes describe how well the system does it
- C. The same functionality can be delivered by many different structures
- D. Quality attributes largely drive the choice of structure
- E. Delivering correct functionality is sufficient for a successful architecture
- F. Both functionality and quality attributes are necessary

### Correct Answers
A, B, C, D, F

### 💡 Hint
Identify exactly what the question asks and compare each option with the lecture wording.

### Explanation
Functionality can be achieved through many different structures; the QAs are what make one structure preferable, so architectural design starts from QA concerns and produces architectural responses.

### Why Other Answers Are Wrong
- E = both are necessary; functionality alone is insufficient.

### ⚫ Trap
⚠ **Over-selection warning:** E. The whole lecture exists to reject that claim.

---

## Q17

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which Quality Attribute → main concern mappings are correct? (Select all that apply.)

### Options
- A. Performance → how quickly the system responds
- B. Availability → whether the system is operational when required
- C. Security → protection against unauthorized access and modification
- D. Modifiability → ease of making changes
- E. Scalability → ability to support increasing demand
- F. Testability → ability to exchange information with other systems

### Correct Answers
A, B, C, D, E

### 💡 Hint
Match each Quality Attribute to its direct concern from the lecture table.

### Explanation
Performance concerns response speed, Availability concerns operational readiness, Security concerns protection, Modifiability concerns ease of change, and Scalability concerns increasing demand.

### Why Other Answers Are Wrong
- F. Exchanging and using information with other systems is Interoperability, not Testability.

### ⚫ Trap
⚠ **Over-selection warning:** Do not confuse Testability with Interoperability.

---

## Q18

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which architectural responses are paired correctly with their Quality Attributes? (Select all that apply.)

### Options
- A. Performance → caching and concurrency
- B. Availability → redundancy and recovery mechanisms
- C. Security → authentication and access control
- D. Modifiability → modularisation and dependency control
- E. Scalability → distribution and replication
- F. Interoperability → removing interfaces and protocols

### Correct Answers
A, B, C, D, E

### 💡 Hint
Choose structural responses that actually help the named quality.

### Explanation
The lecture pairs Performance with caching/concurrency, Availability with redundancy/recovery, Security with authentication/access control, Modifiability with modularisation/dependency control, and Scalability with distribution/replication.

### Why Other Answers Are Wrong
- F. Interoperability depends on protocols, interfaces and data formats, not removing them.

### ⚫ Trap
⚠ **Over-selection warning:** Watch for an option that reverses the purpose of interoperability.

---

## Q19

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which statements make a Quality Attribute requirement operational and testable? (Select all that apply.)

### Options
- A. State what event occurs
- B. State the conditions under which it occurs
- C. Identify the affected artifact
- D. Specify how the system should respond
- E. Define how success will be measured
- F. Use only a vague phrase such as 'the system must be fast'

### Correct Answers
A, B, C, D, E

### 💡 Hint
A testable requirement must specify event, conditions, affected part, response and measurement.

### Explanation
A concrete Quality Attribute requirement identifies the event, environment, affected artifact, response and measurable success criterion.

### Why Other Answers Are Wrong
- F. 'The system must be fast' is explicitly presented as too vague to test.

### ⚫ Trap
⚠ **Over-selection warning:** A Quality Attribute name by itself is not a complete scenario.

---

## Q20

**Lecture:** Lecture 02 - Quality Attributes, Scenarios and Tactics  
**Type:** Multiple Answer

### Question
Which statements about architectural tactics are correct? (Select all that apply.)

### Options
- A. A tactic is a design decision intended to influence a Quality Attribute response
- B. Tactics directly affect how the system responds to a stimulus
- C. Availability tactics include detecting, recovering from and preventing faults
- D. Performance tactics include controlling resource demand and managing resources
- E. Modifiability tactics include reducing coupling and increasing cohesion
- F. A tactic is the same thing as an architectural style

### Correct Answers
A, B, C, D, E

### 💡 Hint
Think of tactics as targeted design moves, not the overall architecture shape.

### Explanation
Tactics are design decisions used to influence Quality Attribute responses. The lecture groups them under Availability, Performance, Security and Modifiability.

### Why Other Answers Are Wrong
- F. An architectural style describes the overall structure; a tactic is a focused design decision.

### ⚫ Trap
⚠ **Over-selection warning:** Do not treat tactic, pattern and style as synonyms.

---
