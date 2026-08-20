# SI-AT-001 — Structural Differential Computation for Personalized Target Discovery

**Series:** Structural Intelligence — Additional Thoughts
**Release Track:** Post-Release Structural Delta
**Status:** Research Hypothesis and Computational Direction
**Version Context:** SI Compass v0.2.0

---

## Abstract

Personalized therapeutic design introduces a computational problem that differs fundamentally from conventional population-level target selection.

Instead of asking only:

> What target is generally associated with this disease?

a personalized system must increasingly ask:

> What structure is specifically different in this patient, which differences are actionable, and which computational path should evaluate them?

The emergence of individualized cancer vaccines provides a particularly clear example. A personalized cancer vaccine may be constructed from molecular differences associated with an individual patient's tumor, requiring candidate differences to be detected, organized, filtered, evaluated, and validated before therapeutic use.

This article proposes that such problems can be viewed as **Structural Differential Computation**.

Under this view, target discovery is not merely a prediction task over a flat candidate set. It is a structured process involving:

1. reference and target structures;
2. differential extraction;
3. preservation and subtraction;
4. organization of candidate differences;
5. localized evaluation;
6. policy-driven selection; and
7. downstream validation.

Structural Intelligence mechanisms such as **Differential Trees** and **Two-Way Common Concept Core (Two-Way CCC)** may therefore provide useful computational abstractions for organizing personalized target-discovery pipelines.

This is a research hypothesis, not a claim of demonstrated biomedical efficacy. Its purpose is to identify a structural computational pattern that can be experimentally evaluated.

---

# 1. A New Computational Requirement

Many conventional therapeutic approaches operate primarily at the population level.

A disease category is identified, common biological mechanisms are studied, therapeutic targets are selected, and standardized treatments are developed for large patient populations.

The computational abstraction is approximately:

```text
Disease Population
        |
        v
Common Mechanisms
        |
        v
Candidate Targets
        |
        v
Therapeutic Design
```

Personalized medicine introduces another dimension.

The important question becomes not only:

```text
What is characteristic of this disease?
```

but also:

```text
What is specifically different in this patient?
```

This changes the computational structure of the problem.

A simplified personalized target-discovery pipeline becomes:

```text
Patient Reference Structure
            |
            |
            +--------------------+
                                 |
                                 v
                         Structural Comparison
                                 ^
                                 |
            +--------------------+
            |
Patient Disease Structure
            |
            v
Patient-Specific Differences
            |
            v
Candidate Targets
            |
            v
Localized Evaluation
            |
            v
Validation
            |
            v
Therapeutic Design
```

The central computational object is therefore no longer merely a disease class.

It is a **patient-specific structural difference space**.

---

# 2. Personalized Cancer Vaccines as a Motivating Example

Recent progress in individualized cancer vaccines makes this problem especially visible.

A patient's tumor may contain molecular alterations that distinguish tumor cells from normal cells. Some of these alterations may produce candidate neoantigens capable of becoming therapeutic targets.

The practical pipeline is substantially more complex than the following abstraction, but structurally it contains a recognizable sequence:

```text
Patient
   |
   +---- Normal / Reference Data
   |
   +---- Tumor Data
             |
             v
      Molecular Differences
             |
             v
      Candidate Alterations
             |
             v
     Candidate Neoantigens
             |
             v
      Target Evaluation
             |
             v
     Therapeutic Selection
```

The difficult computational problem is not simply detecting differences.

There may be many differences.

The more important problem is:

> Which differences matter?

This immediately creates several structural tasks:

* distinguish shared structure from disease-specific structure;
* distinguish inherited variation from acquired variation;
* organize large candidate spaces;
* identify persistent or meaningful differences;
* prioritize locally relevant candidates;
* route candidates to appropriate evaluation methods;
* preserve structural provenance;
* validate downstream decisions.

This is naturally compatible with the Structural Intelligence perspective.

---

# 3. From Difference Detection to Differential Organization

A flat target-discovery pipeline may be represented as:

```text
Candidate 1
Candidate 2
Candidate 3
Candidate 4
...
Candidate N
```

Each candidate can then be scored independently.

This approach may work, but it does not necessarily expose relationships among candidates.

Structural Differential Computation asks a different question:

> Can the candidate space first be organized according to meaningful structural differences?

Instead of:

```text
Large Candidate Set
        |
        v
Global Scoring
```

consider:

```text
Large Candidate Set
        |
        v
Differential Organization
        |
        +---- Branch A
        |
        +---- Branch B
        |
        +---- Branch C
        |
        +---- ...
        |
        v
Localized Candidate Evaluation
```

The organization itself becomes computationally useful.

This reflects a recurring principle of Structural Intelligence:

> **Organization can be computation.**

A good organizational structure may reduce unnecessary comparisons, localize expensive evaluation, preserve provenance, and expose meaningful relationships that are difficult to observe in a flat candidate space.

---

# 4. Differential Trees as Candidate-Space Organizers

A **Differential Tree** provides one possible abstraction.

Consider a simplified hierarchy:

```text
Observed Molecular Differences
            |
            +---- Shared / Background Variation
            |
            +---- Disease-Associated Differences
                     |
                     +---- Weakly Supported
                     |
                     +---- Strongly Supported
                              |
                              +---- Low Expression
                              |
                              +---- High Expression
                                       |
                                       +---- Low Priority
                                       |
                                       +---- Candidate Target
```

This is only an illustrative structure.

Actual biomedical target discovery may require many additional dimensions, including biological mechanism, expression, clonality, molecular processing, presentation, immune recognition, uncertainty, and experimental evidence.

The Structural Intelligence claim is not that one universal tree should replace those methods.

The more modest and potentially useful hypothesis is:

> **A differential organizational layer may make heterogeneous candidate evidence easier to localize, route, compare, and validate.**

The Differential Tree therefore acts primarily as an **organizational computational structure**.

---

# 5. Preserve and Subtract

Personalized target discovery contains another important structural pattern.

Given:

```text
Reference Structure R
Disease Structure D
```

two complementary questions arise.

### Preserve

What structure should be regarded as shared, stable, expected, or non-target?

### Subtract

What structure appears specifically in the disease state and therefore deserves further examination?

Conceptually:

```text
Reference --------+
                  |
                  +---- Structural Comparison
                  |
Disease ----------+
                  |
                  v
          +-------+-------+
          |               |
       Preserve        Subtract
          |               |
          v               v
     Shared Core     Candidate Delta
```

This resembles the **Preserve / Subtract** interpretation of Two-Way CCC developed elsewhere in the Structural Intelligence research program.

The significance is not that biological comparison can be reduced to a trivial set subtraction.

It cannot.

Rather, the structural abstraction suggests that useful target discovery may require both directions:

> **What should remain invariant?**

and:

> **What should be isolated as meaningful variation?**

The combination is more informative than difference detection alone.

---

# 6. Two-Way CCC as a Structural Hypothesis

Two-Way CCC can therefore be considered as a candidate structural operator for personalized comparison.

A simplified conceptual process is:

```text
Reference Evidence
        |
        +------------------+
                           |
                           v
                    Two-Way CCC
                           ^
                           |
        +------------------+
        |
Disease Evidence
        |
        v

Preserved Structure
        +
Subtracted / Differential Structure
        |
        v
Candidate Structural Delta
```

The resulting structural delta could then enter downstream evaluation.

Importantly, this does **not** imply that Two-Way CCC should replace established biomedical methods such as variant calling, expression analysis, antigen-presentation prediction, statistical modeling, molecular modeling, or experimental assays.

A more realistic architecture is:

```text
Established Biomedical Analysis
             |
             v
      Candidate Evidence
             |
             v
Structural Differential Organization
             |
             v
Localized Candidate Evaluation
             |
             v
Established Validation
```

Structural Intelligence should complement specialized domain intelligence rather than attempt to replace it.

---

# 7. The Importance of Structural Provenance

Personalized therapeutic decisions may require strong traceability.

For a candidate target, useful questions include:

```text
Where did this candidate originate?

Which comparison produced it?

Which branch selected it?

Which evidence supported it?

Which evidence rejected competing candidates?

Which computational method evaluated it?

Which policy caused that method to be selected?

What validation followed?
```

A structural pipeline can preserve this information as **Structural Provenance**.

For example:

```text
Patient
   |
   v
Tumor / Reference Comparison
   |
   v
Differential Branch D7
   |
   v
Candidate C42
   |
   v
Evaluation Method E3
   |
   v
Measure M
   |
   v
Validation V2
```

This differs from returning only:

```text
Candidate C42
Score = 0.93
```

The latter provides a result.

The former provides a computational history.

For high-consequence scientific applications, that distinction can be important.

---

# 8. From Global Prediction to Localized Evaluation

Once a candidate space has been structurally organized, different branches may require different computational methods.

One branch may be best evaluated by:

* deterministic biological rules;

another by:

* statistical analysis;

another by:

* a specialized learned model;

another by:

* structural comparison;

another by:

* a large pretrained model;

and another by:

* experimental validation.

This leads naturally to:

```text
Differential Tree
       |
       +---- Node A --> Method A
       |
       +---- Node B --> Method B
       |
       +---- Node C --> Method C
       |
       +---- Node D --> Method D
```

This is **Localized Intelligence**.

The central idea is:

> The entire candidate space does not necessarily require one universal computational method.

Instead, organization can determine where a candidate belongs, and local policy can determine which method should evaluate it.

---

# 9. Per-Node Intelligence

A node in such a structure may possess several possible computational instruments:

```text
Node N
 |
 +---- Rule / Algorithm
 |
 +---- Statistical Model
 |
 +---- Local ANN
 |
 +---- Two-Way CCC
 |
 +---- LLM
 |
 +---- Specialized Scientific Tool
 |
 +---- Experimental Assay
 |
 +---- Human Review
```

The node therefore contains not merely a model but an **Intelligence Space**.

A policy determines how that space is used.

The relevant question becomes:

> Which computational instrument should evaluate this candidate under the current evidence, uncertainty, cost, risk, and validation requirements?

This converts target evaluation into a **policy-controlled localized intelligence problem**.

---

# 10. Learn-on-Demand Intelligence

Some local intelligence may also be generated from accumulating local evidence.

For example:

```text
Local Observations
        |
        v
Local Training Data
        |
        v
Small Learned Model
        |
        v
Node-Specific Evaluation
```

But learn-on-demand intelligence need not be restricted to ANN or conventional machine learning.

Structural evidence may also permit construction or refinement of:

```text
Positive Evidence
        +
Negative Evidence
        |
        v
Preserve / Subtract Analysis
        |
        v
Local Structural Invariants
        |
        v
Two-Way CCC
        |
        v
Node-Specific Recognition / Trigger
```

Thus:

> **Per-Node Intelligence is broader than Per-Node Model.**

A node may learn a mapping, construct a structural discriminator, select a deterministic procedure, invoke a pretrained model, or combine several mechanisms.

---

# 11. Policy-Driven Target Discovery

Once several computational instruments can operate at the same node, a new problem appears.

The system must decide:

```text
Which method?

Under which condition?

At what cost?

With what confidence?

In what order?

With what fallback?

With what validation?
```

This creates a **Policy Surface**.

A simplified policy-controlled pipeline is:

```text
Candidate
    |
    v
Local Context
    |
    v
Policy
    |
    +---- Algorithm
    |
    +---- ANN
    |
    +---- Two-Way CCC
    |
    +---- Specialized Model
    |
    +---- Human Review
    |
    v
Result
    |
    v
Measure
    |
    v
Feedback
```

This connects personalized target discovery with the broader concept of **Policy-Driven Structural Intelligence**.

---

# 12. X-Y-M and Local Computational Experience

A node can accumulate runtime experience in a simple structural form:

```text
X = local input and context

Y = computational strategy selected

M = measured result
```

Repeated execution produces:

```text
(X1, Y1, M1)
(X2, Y2, M2)
(X3, Y3, M3)
...
(Xn, Yn, Mn)
```

This creates a local decision landscape.

Over time, the system may learn:

```text
Given X,
under Policy P,
which Y tends to produce the preferred M?
```

The optimization target therefore shifts from:

```text
Predict the target directly.
```

toward:

```text
Organize the candidate.

Select the appropriate computational strategy.

Measure the outcome.

Improve the policy.
```

This represents a higher organizational layer of intelligence.

---

# 13. A Structural Target-Discovery Architecture

The preceding ideas can be assembled into a conceptual architecture:

```text
                    Patient-Specific Data
                            |
                            v
                   Reference / Disease
                      Structural IR
                            |
                            v
                   Differential Extraction
                            |
                            v
                 Preserve / Subtract Analysis
                            |
                            v
                   Differential Organization
                            |
                            v
                     Candidate Space
                            |
                            v
                     Localized Routing
                            |
                            v
                 Per-Node Intelligence Space
                  /      |       |       \
               ANN      CCC     LLM    Domain Tools
                  \      |       |       /
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
                        Validation
                            |
                            v
                         Feedback
```

This should be understood as a research architecture rather than a validated biomedical pipeline.

Its purpose is to expose the computational roles that may exist inside personalized target discovery.

---

# 14. Beyond Cancer Vaccines

The same structural pattern may apply beyond individualized cancer vaccines.

Possible research domains include:

* personalized therapeutic target discovery;
* disease-subtype differentiation;
* biomarker discovery;
* pathogen-variant analysis;
* protein and molecular structure comparison;
* drug-response stratification;
* individualized treatment selection;
* biological anomaly detection;
* longitudinal patient-state comparison;
* experimental candidate prioritization.

The recurring pattern is:

```text
Reference
    |
Target / Observation
    |
    v
Structural Difference
    |
    v
Differential Organization
    |
    v
Candidate Localization
    |
    v
Specialized Evaluation
    |
    v
Validation
```

This suggests that **Structural Differential Computation** may represent a reusable computational pattern rather than a technique limited to one biomedical application.

---

# 15. Structural Intelligence and Scientific Target Discovery

This observation suggests a broader role for Structural Intelligence.

Structural Intelligence need not be limited to organizing AI computation.

It may also help organize **scientific discovery spaces**.

Many scientific problems contain:

```text
Large Observation Space
        |
        v
Large Difference Space
        |
        v
Large Candidate Space
        |
        v
Expensive Evaluation
```

If structural organization can reduce, localize, or better route this space, the value of SI may lie not in replacing scientific models but in determining:

> **Where specialized intelligence should be applied.**

This is closely related to the distinction between:

```text
Solving every candidate globally
```

and:

```text
Structurally organizing candidates
        +
Applying intelligence locally
```

The second architecture may become increasingly important as scientific data spaces grow.

---

# 16. A Testable Research Hypothesis

The ideas in this article should ultimately be evaluated experimentally.

A useful benchmark could compare:

```text
Pipeline A
Flat Candidate Evaluation

Pipeline B
Differential-Tree Organization
        +
Localized Evaluation

Pipeline C
Differential Tree
        +
Two-Way Structural Comparison
        +
Policy-Driven Local Evaluation
```

Possible measures include:

* candidate-space reduction;
* recall of validated targets;
* precision of candidate prioritization;
* computational cost;
* evaluation latency;
* structural traceability;
* robustness to noisy observations;
* reproducibility;
* downstream experimental hit rate.

Such experiments would allow the hypothesis to be tested rather than merely asserted.

---

# 17. Boundary of the Claim

This article does **not** claim that:

* Differential Trees have been clinically validated for personalized cancer vaccines;
* Two-Way CCC has demonstrated superior neoantigen discovery;
* Structural Intelligence should replace established biomedical pipelines;
* structural organization alone is sufficient for therapeutic target selection;
* computational target identification establishes clinical efficacy.

Instead, the claim is narrower:

> **Personalized target discovery contains a strong structural differential component, and Structural Intelligence provides computational abstractions that may be useful for organizing, localizing, routing, and validating such difference spaces.**

Whether those abstractions improve real scientific or clinical pipelines is an empirical question.

That question should be tested.

---

# 18. From Personalized Medicine to Personalized Computation

The deeper implication extends beyond medicine.

Personalization changes computation itself.

A conventional architecture often assumes:

```text
Global Model
     |
     v
Many Inputs
```

A structurally personalized architecture may instead use:

```text
Global Knowledge
       +
Individual Structural Delta
       +
Localized Intelligence
       +
Runtime Policy
       |
       v
Individual Decision
```

This leads to an important distinction:

> **Global knowledge describes what may be possible.
> Local structural difference identifies what matters here.**

Personalized medicine is therefore not only a biomedical development.

It is also an example of a broader computational transition:

```text
Global Intelligence
        |
        v
Structural Localization
        |
        v
Per-Instance Intelligence
```

---

# 19. Conclusion

Personalized target discovery provides a natural application domain for Structural Intelligence because its central problem is inherently differential.

The system must determine:

* what should be preserved;
* what should be subtracted;
* which differences deserve attention;
* how those differences should be organized;
* which intelligence should evaluate them;
* how decisions should be validated; and
* how experience should improve future decisions.

This produces a general computational pattern:

```text
Preserve
   |
Subtract
   |
Organize Differences
   |
Localize
   |
Select Intelligence
   |
Execute
   |
Validate
   |
Learn
```

Differential Trees may provide organizational structure.

Two-Way CCC may provide preserve/subtract structural operators.

Per-Node Intelligence may provide specialized local computation.

Policy may determine how heterogeneous computational instruments are selected and combined.

Measurement and feedback may allow the resulting system to improve.

The broader research hypothesis is therefore:

> **Scientific target discovery may increasingly become not only a prediction problem, but a problem of structural organization over large differential spaces.**

If this hypothesis holds, Structural Intelligence may have a role beyond organizing artificial intelligence itself.

It may help organize the computational processes through which scientific targets are discovered.

---

## Closing Perspective

The transition from standardized therapy toward individualized therapeutic design illustrates a larger computational trend:

> **From modeling populations to computing meaningful structural differences within individuals.**

Where differences become numerous, organization becomes necessary.

Where multiple evaluation methods become available, policy becomes necessary.

Where decisions become consequential, provenance and validation become necessary.

And where all of these meet, target discovery becomes a problem not merely of intelligence, but of **Structural Intelligence**.
