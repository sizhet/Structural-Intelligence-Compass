# SI-AT-004 — Local Learned Intelligence and Grounded Structural IR

**Series:** Structural Intelligence — Additional Thoughts
**Release Track:** Post-Release Structural Delta
**Status:** Foundational Structural Extension
**Version Context:** SI Compass v0.2.0

---

## Abstract

Structural Intelligence requires more than language, symbolic structure, search, and runtime organization.

It also requires mechanisms that can:

1. learn specialized local mappings where intelligence is needed;
2. convert physical-world observations into computationally usable structural representations.

This article distinguishes two related but different structural roles:

* **Local Learned Intelligence** — small, specialized, node-level learned computational units that may be trained, replaced, or regenerated as local needs evolve;
* **Grounded Structural IR** — computational representations produced from sensors, learned perception, spatial modeling, and other mechanisms that convert the physical world into structures that downstream intelligence can organize and act upon.

These roles are essential because the physical world does not arrive as tokens, rules, or calling graphs.

It arrives through:

* images;
* sound;
* motion;
* geometry;
* radar;
* lidar;
* force;
* temperature;
* biological signals;
* other measurements.

Learned perception and representation systems therefore form a crucial bridge:

```text
Physical World
      |
      v
Sensors
      |
      v
Learned Perception
      |
      v
Grounded Structural IR
      |
      v
Structural Intelligence
```

At the same time, localized runtime nodes may require small specialized intelligences such as:

* ANN;
* classifier;
* regressor;
* learned policy;
* Two-Way CCC;
* deterministic algorithm;
* LLM access;
* external tools.

This motivates a broader interpretation:

> **Per-Node Intelligence is not equivalent to Per-Node Model.**

A node may own an evolving **Intelligence Space** and may learn, generate, select, combine, validate, or retire multiple computational mechanisms.

Together, Local Learned Intelligence and Grounded Structural IR connect Structural Intelligence to perception, spatial intelligence, autonomous systems, robotics, World Models, and other forms of grounded AI.

---

# 1. A Missing Layer in Structural Intelligence

A large portion of Structural Intelligence research can be expressed in terms of already available computational structure:

```text
Differential Tree

Calling Graph

Calling Path

Function Tunnel

Enumeration

Policy

Runtime Reachability

Triggering

Switching
```

But this raises a prior question:

> **Where does the structure come from?**

For symbolic systems, the answer may be straightforward.

A software program already has:

```text
Functions
Variables
Calls
Types
Paths
```

A knowledge system may already have:

```text
Entities
Relations
Categories
Documents
```

A language model already receives:

```text
Tokens
Sequences
Prompts
```

But the physical world does not naturally arrive in any of these forms.

It arrives as signals.

Therefore, a complete Structural Intelligence architecture needs a **Grounding Layer**.

---

# 2. The Physical World Does Not Arrive as Tokens

Consider an autonomous system.

The environment provides:

```text
Photons

Sound Waves

Radar Returns

Lidar Reflections

Inertial Signals

GPS Measurements

Temperature

Pressure

Force

Motion
```

These are not yet high-level computational structures such as:

```text
Car

Pedestrian

Road

Obstacle

Trajectory

Intent

Danger
```

A transformation must occur.

Conceptually:

```text
Physical World
      |
      v
Sensors
      |
      v
Raw Measurements
      |
      v
Perception
      |
      v
Representation
      |
      v
Structural IR
```

Only after this transformation can higher-level structural computation begin.

---

# 3. Grounded Structural IR

This article uses the term **Grounded Structural IR** to describe an intermediate representation derived from real-world observations and suitable for downstream structural computation.

The term **IR** is used in the broad computational sense of **Intermediate Representation**.

A Grounded Structural IR may contain:

```text
Objects

Features

Relations

Positions

Velocities

Boundaries

Temporal Changes

Uncertainty

Affordances

Possible Interactions
```

For example:

```text
Camera / Lidar / Radar
          |
          v
Perception Models
          |
          v
Object / Scene Representation
          |
          v
Grounded Structural IR
```

The importance of this layer is that it transforms:

> **physical signals**

into:

> **computationally addressable structure**

---

# 4. Structural IR Is More Than Feature Extraction

A feature vector may be useful without being a rich structural representation.

For example:

```text
Input Image
    |
    v
Feature Vector
```

may support classification.

But Structural Intelligence often requires more:

```text
Object A
    |
    +---- left-of ---- Object B
    |
    +---- moving-toward ---- Object C
    |
    +---- distance ---- d
```

A richer Grounded Structural IR may therefore expose:

* identity;
* geometry;
* relations;
* order;
* temporal state;
* reachability;
* uncertainty;
* hierarchy.

The goal is not necessarily symbolic purity.

The goal is:

> **Make relevant structure computationally usable.**

---

# 5. Learned Perception as a Structural Gateway

Modern learned perception systems are especially important because they can transform raw signals into increasingly useful internal representations.

Examples include:

* convolutional networks;
* vision transformers;
* learned encoders;
* multimodal models;
* sensor-fusion systems;
* spatial models;
* predictive models.

A simplified process is:

```text
Raw Signal
    |
    v
Learned Representation
    |
    v
Detected Structure
    |
    v
Structural IR
```

This makes learned models an important gateway into Structural Intelligence.

They need not replace structural reasoning.

They can supply the structures over which structural reasoning operates.

---

# 6. From Grounding to Structural Intelligence

Once Grounded Structural IR exists, the SI computational chain becomes clearer:

```text
Physical World
      |
      v
Grounding
      |
      v
Structural IR
      |
      v
Enumeration
      |
      v
Organization
      |
      v
Calling / Routing
      |
      v
Policy
      |
      v
Runtime
      |
      v
Action
```

This gives Structural Intelligence a complete physical-world entry path.

Without this layer, SI risks remaining primarily a framework for structures that already exist inside computational systems.

With Grounded Structural IR, SI can participate in:

* robotics;
* autonomous driving;
* spatial intelligence;
* embodied AI;
* scientific sensing;
* industrial control;
* biological observation;
* real-world decision systems.

---

# 7. Local Learned Intelligence

A second missing structure appears at the opposite end of the stack.

Once a problem has been localized to a node, the system may require a specialized computational solution.

A node does not necessarily need a universal intelligence.

It may need only:

```text
A small classifier

A local regressor

A specialized ANN

A learned score

A tiny policy network

A local anomaly detector
```

This motivates **Local Learned Intelligence**.

A simple example is:

```text
Local Data
    |
    v
Training
    |
    v
Local Model
    |
    v
Node-Specific Decision
```

The model may be narrow.

That is not a weakness.

Its narrowness may be exactly what makes it useful.

---

# 8. Local Intelligence and Scope

Consider a node responsible for a specific region of the problem space.

The node may receive only:

```text
X within Region R
```

The relevant task may therefore be:

```text
f_R(X) -> Y
```

rather than:

```text
f_everything(X) -> Y
```

This difference can be computationally significant.

Local intelligence may benefit from:

* smaller training sets;
* narrower input distributions;
* simpler models;
* lower inference cost;
* easier validation;
* easier replacement;
* clearer scope.

Thus:

> **Localization can reduce the amount of intelligence required at any single node.**

---

# 9. Learn-on-Demand Intelligence

A particularly important possibility is that local intelligence can be created when needed.

Instead of:

```text
Train One Large Model
        |
        v
Use Everywhere
```

a system may perform:

```text
Node Receives Experience
        |
        v
Local Data Accumulates
        |
        v
Training Threshold Reached
        |
        v
Generate Local Intelligence
        |
        v
Use at Runtime
```

This can be called **Learn-on-Demand Intelligence**.

The model does not need to exist before the node develops a meaningful local problem.

It may emerge from runtime experience.

---

# 10. Intelligence Can Become Disposable

This leads to an important architectural shift.

Traditional AI often treats a trained model as a central asset.

But in a localized architecture:

```text
Data + Scope + Policy
        |
        v
Generate Model
```

the model itself may become replaceable.

A node may:

```text
Train

Validate

Deploy

Measure

Replace

Retrain

Retire
```

Thus:

> **The durable asset may be the organized experience and local structure, not the current model instance.**

This creates a different computational economy.

---

# 11. Learn-on-Demand Is Not Limited to ANN

A crucial point is that local learning should not be equated with ANN training.

A node may learn or construct different forms of intelligence.

For example:

```text
Local Experience
      |
      +---- Train ANN
      |
      +---- Learn Thresholds
      |
      +---- Build Statistical Model
      |
      +---- Construct Two-Way CCC
      |
      +---- Learn Routing Policy
      |
      +---- Generate Rule
```

This suggests:

> **Learn-on-Demand is an organizational capability, not a neural-network-specific capability.**

The node learns whatever computational structure best fits its local problem.

---

# 12. Learning a Mapping vs Learning a Structure

ANN-based local learning often produces:

```text
X -> Y
```

or:

```text
X -> P(Y)
```

Two-Way CCC may produce a different computational object.

Conceptually:

```text
Positive Experience
        +
Negative Experience
        |
        v
Preserve / Subtract
        |
        v
Local Structural Invariants
        |
        v
Two-Way CCC
        |
        v
Recognition / Trigger
```

Thus:

```text
ANN
    ->
Learned Mapping
```

while:

```text
Two-Way CCC
    ->
Explicit Structural Discriminator
```

Both may be learned locally.

But the products of learning are structurally different.

---

# 13. Per-Node Intelligence Is Broader Than Per-Node Model

This distinction leads to an important principle:

> **Per-Node Intelligence is not equivalent to Per-Node Model.**

A node may contain:

```text
Node N
 |
 +---- Rule
 |
 +---- Deterministic Algorithm
 |
 +---- ANN
 |
 +---- Statistical Model
 |
 +---- Two-Way CCC
 |
 +---- LLM
 |
 +---- Search
 |
 +---- External Tool
 |
 +---- Human Review
```

Therefore, the node is better understood as owning an **Intelligence Space**.

---

# 14. The Per-Node Intelligence Space

The Intelligence Space can be represented as:

```text
                 Node N
                   |
         +---------+---------+
         |                   |
         v                   v
Local Memory          Intelligence Space
                           |
                           +---- Algorithm
                           +---- ANN
                           +---- CCC
                           +---- LLM
                           +---- Search
                           +---- Tool
                           +---- Human
```

Policy determines how this space is used.

The node may:

```text
Select

Generate

Combine

Validate

Retire
```

intelligence.

This is a much richer architecture than assigning one model to one node.

---

# 15. Local Intelligence as a Runtime Resource

A Local Learned Intelligence unit should not necessarily have permanent runtime authority.

Instead:

```text
Problem
   |
   v
Node
   |
   v
Policy
   |
   +---- Local ANN
   |
   +---- Two-Way CCC
   |
   +---- LLM
   |
   +---- Algorithm
   |
   v
Runtime
```

The local model is one available resource.

Its use depends on:

* context;
* confidence;
* cost;
* latency;
* novelty;
* risk;
* policy.

This fits naturally into Policy-Driven Structural Intelligence.

---

# 16. Local Intelligence and X-Y-M Memory

A node can accumulate structured experience.

For example:

```text
X = local context

Y = selected intelligence / action

M = measured result
```

Repeated experience produces:

```text
(X1, ANN1, M1)

(X2, CCC1, M2)

(X3, LLM, M3)

(X4, ANN1 + CCC1, M4)
```

This allows the node to learn not only:

> What output is correct?

but also:

> Which intelligence tends to perform well under which local conditions?

This is **local organizational learning**.

---

# 17. Grounded IR and Per-Node Intelligence Connect Naturally

The two major themes of this article now connect.

A physical system may operate as follows:

```text
Physical World
      |
      v
Sensors
      |
      v
Grounded Structural IR
      |
      v
Differential / Spatial Organization
      |
      v
Localized Node
      |
      v
Per-Node Intelligence Space
      |
      v
Policy
      |
      v
Runtime Action
```

This provides a complete path:

> **World -> Structure -> Local Intelligence -> Action**

---

# 18. World Models as Learned Structural Representation Systems

World Models fit naturally into this architecture, but at a higher level than a single local ANN.

A World Model may represent:

```text
Objects

Relations

Geometry

Temporal Dynamics

Uncertainty

Possible Futures
```

Conceptually:

```text
Current Observation
       |
       v
Perception
       |
       v
State Representation
       |
       v
World Model
       |
       +---- Future State A
       |
       +---- Future State B
       |
       +---- Future State C
```

Thus a World Model can be interpreted as:

> **Learned Structural IR + Dynamics**

It does not merely classify the present.

It provides computational structure for possible future states.

---

# 19. World Models and Enumeration

World Models naturally connect to Enumerative Structure.

For example:

```text
Current State
     |
     v
World Model
     |
     v
Possible Futures
```

The generated futures form a state possibility space.

Then:

```text
Possible Futures
      |
      v
Evaluation
      |
      v
Policy
      |
      v
Action
```

Thus:

> **Grounding creates state structure.
> World Models extend that structure into possible futures.
> Enumeration exposes alternatives.
> Policy selects among them.**

This gives World Models a precise structural role within SI.

---

# 20. Spatial Intelligence

Spatial intelligence also fits naturally.

A spatial system may need to represent:

```text
Objects

Positions

Distances

Containment

Occlusion

Movement

Orientation

Interaction
```

This is fundamentally structural.

A useful computational chain is:

```text
Visual / Sensor Input
        |
        v
Spatial Representation
        |
        v
Grounded Structural IR
        |
        v
Relation / State Space
        |
        v
Planning / Runtime Action
```

The important contribution of learned perception is not merely classification.

It is the construction of **usable world structure**.

---

# 21. Autonomous Driving as a Structural Example

Autonomous driving provides a clear application.

A simplified architecture is:

```text
Camera / Radar / Lidar
          |
          v
Perception
          |
          v
Scene Representation
          |
          v
Grounded Structural IR
          |
          +---- Vehicles
          +---- Pedestrians
          +---- Lanes
          +---- Obstacles
          +---- Motion
          +---- Uncertainty
          |
          v
Possible Futures
          |
          v
Policy / Planning
          |
          v
Runtime Action
```

Different intelligence mechanisms may participate at different layers.

For example:

```text
Learned Perception
        ->
Structural IR

World Model
        ->
Possible Futures

Search / Planning
        ->
Candidate Actions

Policy
        ->
Action Selection

Runtime Control
        ->
Execution
```

No single mechanism needs to monopolize the architecture.

---

# 22. LLMs and Grounded Intelligence Perform Different Jobs

Language Models and grounded perception systems often appear in unnecessary competition.

Structurally, their jobs differ.

An LLM primarily operates over:

```text
Language
Knowledge
Symbolic Sequences
Folded Linguistic Structure
```

Grounded perception operates over:

```text
Sensors
Physical Signals
Geometry
Motion
Spatial Relations
```

Thus:

```text
LLM
    ->
Folded Language-Mediated Intelligence
```

while:

```text
Grounded Model
    ->
Physical-World Structural Representation
```

These roles are complementary.

---

# 23. CCC and Grounded Intelligence Also Perform Different Jobs

Two-Way CCC may operate over already available structural evidence:

```text
Structure A
    +
Structure B
    |
    v
Preserve / Subtract
    |
    v
Recognition / Trigger
```

But a physical system must first construct the structures to be compared.

Thus:

```text
Physical World
      |
      v
Grounding
      |
      v
Structural IR
      |
      v
Two-Way CCC
```

This clarifies the division of labor.

Grounding produces usable structure.

CCC operates over structure.

---

# 24. The Three Major Per-Node Intelligence Sources

At a node, three especially important intelligence classes emerge.

## 24.1 Local Learned Intelligence

Examples:

* ANN;
* classifier;
* regressor;
* learned policy.

Strength:

> Learn a specialized local mapping from local data.

## 24.2 Folded General Intelligence

Example:

* LLM.

Strength:

> Provide broad language-mediated knowledge and generalized capability.

## 24.3 Explicit Structural Intelligence

Examples:

* CCC;
* Two-Way CCC;
* structural trigger;
* explicit algorithm.

Strength:

> Preserve explicit structural relationships and decision logic.

A simplified triangle is:

```text
                Per-Node Intelligence
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
     Local Learned     LLM        Structural
     Intelligence    Folding      Intelligence
```

These are not mutually exclusive.

They are computationally complementary.

---

# 25. From Model Competition to Structural Placement

Many AI debates ask:

```text
Which paradigm will win?
```

For example:

```text
LLM vs World Model

Neural vs Symbolic

Learning vs Search
```

Structural Intelligence reframes the question:

> **Which computational job does each paradigm perform, and where should it be placed?**

For example:

```text
Grounded Learned Model
    ->
Construct Structural IR

World Model
    ->
Represent Dynamics / Possible Futures

Enumeration
    ->
Expose Alternatives

Differential Tree
    ->
Organize Candidate Differences

LLM
    ->
Provide Folded General Intelligence

CCC
    ->
Provide Explicit Structural Recognition

Policy
    ->
Select Computational Strategy

Runtime
    ->
Execute
```

This transforms paradigm competition into architectural composition.

---

# 26. Many AI Conflicts Are Placement Problems

A useful principle follows:

> **Many AI paradigm conflicts are not conflicts of capability, but failures of structural placement.**

A technique may be excellent at one layer and inappropriate at another.

For example:

```text
ANN
```

may be excellent for perceptual representation but poor as an explicit provenance mechanism.

```text
LLM
```

may be excellent for language-mediated reasoning but inappropriate for hard real-time control without additional structure.

```text
Rule System
```

may be excellent for explicit constraints but weak in high-dimensional perception.

The correct question is therefore not:

> Which one is intelligence?

but:

> **Where does each one belong?**

---

# 27. Grounded Structural IR as a Bridge Between Two Worlds

Structural Intelligence can now be viewed as connecting two large computational domains.

## Symbolic / Digital World

```text
Programs
Documents
Graphs
Tokens
Rules
APIs
```

## Physical World

```text
Images
Sound
Motion
Geometry
Forces
Biological Signals
```

Grounded Structural IR provides the bridge:

```text
Physical World
      |
      v
Grounded Structural IR
      |
      v
Digital Structural Computation
```

This is essential for any SI architecture intended to operate beyond purely digital systems.

---

# 28. Grounded IR and Structural Provenance

Grounding should ideally preserve provenance.

For example:

```text
Observed Object O
       |
       +---- Camera Frame 182
       |
       +---- Lidar Cluster 51
       |
       +---- Radar Track 7
       |
       v
Fused Structural Object
```

This gives a structured lineage from physical evidence to computational representation.

Such provenance can support:

* validation;
* debugging;
* uncertainty estimation;
* sensor disagreement analysis;
* downstream audit.

This is particularly important in high-consequence systems.

---

# 29. Grounded IR and Uncertainty

Physical observation is rarely exact.

Thus a Grounded Structural IR should often represent uncertainty:

```text
Object:
    type = vehicle
    confidence = high

position:
    estimate = p
    uncertainty = u

velocity:
    estimate = v
    uncertainty = w
```

This allows downstream policy to respond differently under uncertainty.

For example:

```text
Low Uncertainty
      ->
Fast Local Policy

High Uncertainty
      ->
Additional Sensor Fusion
      ->
Alternative Model
      ->
Human Review
```

Thus grounding naturally connects to Policy Surfaces.

---

# 30. Learn-on-Demand Grounding

Grounding mechanisms may themselves become local and adaptive.

Suppose a system repeatedly encounters a specific environment.

It may accumulate:

```text
Local Sensor Patterns
        |
        v
Local Training Data
        |
        v
Specialized Perception Model
```

Thus Local Learned Intelligence may exist not only at the decision layer but also at the representation layer.

For example:

```text
Generic Perception
        +
Local Learned Adapter
        |
        v
Improved Structural IR
```

This creates a multi-level localized intelligence architecture.

---

# 31. Intelligence Generation as a General Node Capability

A mature node may be able to generate several forms of local intelligence:

```text
Node Experience
      |
      v
Analysis
      |
      +---- Train ANN
      |
      +---- Construct CCC
      |
      +---- Learn Policy
      |
      +---- Generate Rule
      |
      +---- Build Cache / Index
```

This leads to a broader principle:

> **A node should not merely own intelligence. It may own the capability to create intelligence.**

This is a deeper interpretation of Per-Node Intelligence.

---

# 32. From Intelligence Object to Intelligence Ecology

If a node can:

* generate intelligence;
* select intelligence;
* combine intelligence;
* measure intelligence;
* retire intelligence;

then the node begins to resemble a local computational ecology.

For example:

```text
                  Node
                   |
          +--------+--------+
          |                 |
          v                 v
     Local Memory     Intelligence Space
                           |
                  +--------+--------+
                  |        |        |
                 ANN      CCC      LLM
                  |        |        |
                  +--------+--------+
                           |
                           v
                         Policy
                           |
                           v
                         Runtime
                           |
                           v
                        Measure
                           |
                           v
                        Feedback
```

This is more than modular AI.

It is an adaptive organizational runtime.

---

# 33. A Complete Grounded Structural Intelligence Stack

The ideas developed in this article can be assembled into a broader stack:

```text
Physical World
      |
      v
Sensors
      |
      v
Learned Perception / Grounding
      |
      v
Grounded Structural IR
      |
      v
Enumerative Possibility Space
      |
      v
Structural Organization
      |
      v
Localized Node
      |
      v
Per-Node Intelligence Space
      |
      +---- Algorithm
      +---- ANN
      +---- Two-Way CCC
      +---- LLM
      +---- Search
      +---- Tool
      +---- Human
      |
      v
Policy
      |
      v
Runtime
      |
      v
Action
      |
      v
Physical World
```

This closes the loop.

---

# 34. The Physical Runtime Loop

A grounded intelligent system is ultimately cyclic:

```text
World(t)
   |
   v
Sense
   |
   v
Represent
   |
   v
Organize
   |
   v
Decide
   |
   v
Act
   |
   v
World(t+1)
```

This is fundamentally different from a purely static inference problem.

The output changes the next input.

Therefore:

> **Grounded Structural Intelligence is inherently runtime intelligence.**

This connects perception, World Models, policy, and runtime switching.

---

# 35. Research Questions

This extension creates several research questions.

### 35.1 Structural IR Design

Which representations expose enough structure for downstream organization without becoming excessively expensive?

### 35.2 Learned vs Explicit Structure

Which structures should remain latent and which should become explicit?

### 35.3 Local Model Generation

When should a node train a specialized model?

### 35.4 Structural Intelligence Generation

When should local experience produce a Two-Way CCC or other explicit structural mechanism?

### 35.5 Model Retirement

When should local intelligence be replaced?

### 35.6 Grounding Provenance

How should raw sensor evidence remain connected to structural decisions?

### 35.7 Policy

How should ANN, CCC, LLM, algorithms, and human review be selected?

### 35.8 World Models

How should learned dynamics connect to enumerative future spaces?

### 35.9 Runtime

How should structural representations change under real-world feedback?

These questions form a broad SI research program.

---

# 36. A Testable Experimental Direction

A minimal experimental architecture could compare:

```text
Pipeline A
Global Model Only
```

with:

```text
Pipeline B
Grounded Structural IR
        +
Local Models
```

and:

```text
Pipeline C
Grounded Structural IR
        +
Per-Node Intelligence Space
        +
Policy Selection
```

Possible measures include:

* accuracy;
* inference cost;
* local training cost;
* latency;
* retraining frequency;
* explainability;
* provenance;
* robustness;
* adaptation speed;
* policy efficiency.

A second benchmark could compare:

```text
Local ANN
```

versus:

```text
Local Two-Way CCC
```

versus:

```text
ANN + Two-Way CCC
```

for node-specific tasks where structural invariants can be learned.

Such experiments would help distinguish which kinds of local intelligence are most useful under which conditions.

---

# 37. Boundary of the Claim

This article does **not** claim that:

* all physical-world representation should be neural;
* all World Models should use the same architecture;
* ANN and World Models are equivalent structures;
* learned perception automatically produces optimal Structural IR;
* Two-Way CCC can replace learned perception;
* LLMs are unnecessary in grounded systems;
* every node should train its own model.

The narrower claim is:

> **Structural Intelligence requires explicit attention to how physical observations become usable computational structure and how localized intelligence can be created and deployed within organized runtime systems.**

The hypothesis is that these two layers — Grounded Structural IR and Local Learned Intelligence — are foundational components of a complete SI architecture.

---

# 38. From Grounded Representation to Structural Synthesis

Once physical structure is available and nodes own multiple intelligence mechanisms, the next problem becomes synthesis.

For example:

```text
Grounded Structural IR
        |
        v
Local Node
        |
        +---- ANN
        +---- CCC
        +---- LLM
        +---- Search
        |
        v
Policy
        |
        v
Runtime Composition
```

This directly leads toward:

> **Policy-Driven Structural Hybrid Intelligence**

Thus Grounding and Local Learned Intelligence are not isolated additions.

They supply essential components for the broader SI synthesis layer.

---

# 39. Conclusion

Structural Intelligence cannot remain complete if it begins only after structure has already been provided.

The physical world must first be converted into computationally usable form.

This requires:

```text
Sensors
    ->
Perception
    ->
Grounded Structural IR
```

At the same time, localized structural organization creates another requirement:

```text
Local Problem
    ->
Local Intelligence
```

That local intelligence need not be a single ANN.

It may be:

```text
ANN

Two-Way CCC

Algorithm

LLM

Search

Tool

Human
```

and it may be generated, selected, combined, validated, replaced, or retired.

The resulting principle is:

> **Per-Node Intelligence is broader than Per-Node Model.**

And the larger architecture becomes:

```text
Physical World
      |
      v
Grounded Structural IR
      |
      v
Structural Organization
      |
      v
Per-Node Intelligence Space
      |
      v
Policy
      |
      v
Runtime
      |
      v
Action
```

This connects Structural Intelligence directly to World Models, spatial intelligence, robotics, autonomous systems, and embodied AI.

---

## Closing Perspective

Language models demonstrate how enormous symbolic and linguistic capability can be folded into reusable computational systems.

But intelligence does not begin with language.

Before language, a system must often determine:

```text
What is here?

Where is it?

How is it moving?

What is changing?

What might happen next?
```

These questions require grounding.

After grounding, another question appears:

```text
Which local intelligence should act on this structure?
```

That question requires organization.

A complete Structural Intelligence architecture therefore needs both:

> **Grounded Structural IR to bring the world into computation.**

and:

> **Local Intelligence Spaces to bring specialized computation to the right place.**

Together, they create the bridge:

```text
World
  ->
Structure
  ->
Localized Intelligence
  ->
Policy
  ->
Runtime Action
  ->
World
```

This bridge is essential if Structural Intelligence is to extend from computational organization into real-world intelligence systems.
