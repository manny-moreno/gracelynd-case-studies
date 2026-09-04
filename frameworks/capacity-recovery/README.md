# Capacity Recovery

**A practical framework for deciding what work people, deterministic automation, and AI agents should perform.**

Capacity Recovery is Gracelynd & Company's method for identifying recurring operational effort that can be redesigned so people spend less time performing repeatable processing and more time on work that requires judgment, accountability, relationships, creativity, or decision-making.

The framework is summarized as:

> **Discover → Measure → Separate → Automate → Recover**

And its core operating principle is:

> **Technology handles repeatability. People handle judgment. The organization recovers capacity.**

## The problem Capacity Recovery addresses

Organizations often accumulate recurring work that is necessary but operationally inefficient: rebuilding reports, reconciling routine data, moving information between systems, preparing recurring communications, performing repetitive checks, or manually coordinating predictable workflow steps.

The objective is not simply to "automate more." Automation that is poorly targeted can move risk rather than remove work.

Capacity Recovery instead asks:

> **What work should humans perform, what should deterministic systems perform, and what should agents perform?**

## The five stages

### 1. Discover

Identify where recurring human effort is being consumed.

Useful signals include:

- recurring manual preparation;
- repetitive data transformation or reconciliation;
- copying information between systems;
- repeated status checks;
- predictable routing or coordination;
- recurring content preparation; and
- processes where people must complete substantial mechanical work before reaching a decision.

The output of Discover is a clearly bounded operational problem—not a predetermined technology solution.

### 2. Measure

Establish a defensible baseline before changing the process.

Depending on the workflow, useful measures may include:

- staff-hours per cycle;
- frequency;
- number of people involved;
- handoffs;
- processing time;
- error or rework frequency;
- queue or wait time; and
- volume of transactions, reports, requests, or cases.

Measurement prevents vague efficiency claims and provides a basis for evaluating whether an intervention creates meaningful value.

A workload baseline should not automatically be treated as realized labor or financial savings.

### 3. Separate

Decompose the workflow according to the nature of the work.

#### Human judgment

Keep people responsible where work requires context, accountability, relationships, interpretation, creativity, ethical judgment, exception handling, or consequential decisions.

#### Deterministic automation

Use conventional automation where the rule can be expressed reliably as:

```text
When X happens → perform Y
```

Examples include structured data transformations, scheduled processing, field mappings, routing rules, repeatable calculations, API transactions, and known workflow sequences.

#### Agentic reasoning

Consider an AI agent where the work requires interpreting information, choosing among possible next actions, using multiple tools, adapting to context, or reasoning across less-structured inputs.

Agentic capability should not be introduced merely because it is available. Where deterministic automation is sufficient, deterministic automation is generally easier to test, govern, and operate reliably.

### 4. Automate

Implement the repeatable or agent-suitable portions using technology proportionate to the problem.

The technology may be as simple as a spreadsheet transformation or as sophisticated as a governed multi-system agent. The objective is not maximum technical complexity. It is the smallest reliable intervention that improves the operating model.

Automation should preserve appropriate controls, observability, error handling, and human authorization boundaries.

### 5. Recover

Return capacity to work where people create greater value.

Recovered capacity may appear as:

- fewer hours spent on repetitive processing;
- faster cycle times;
- reduced rework;
- improved consistency;
- faster response to exceptions;
- greater throughput without proportional staffing growth; or
- more time available for analysis, service, decision-making, and improvement.

Capacity Recovery does not assume that recovered time becomes headcount reduction. The value depends on what the organization is able to do with the capacity returned to it.

## Decision model

A simplified decision model is:

```text
                    Work activity
                         │
                         ▼
             Is the work repeatable?
                  /             \
                Yes              No
                 │                │
                 ▼                ▼
       Can rules reliably     Does it require
       determine the action?  interpretation or judgment?
            /       \              /       \
          Yes        No           Yes       No
           │          │            │         │
           ▼          ▼            ▼         ▼
    Deterministic   Consider     Human or   Re-examine
     automation     agentic     human-agent  the process
                    reasoning   collaboration
```

This is a starting model rather than a substitute for process analysis, risk assessment, or governance.

## Governance principles

Capacity Recovery follows several operating principles:

1. **Measure before claiming value.** Establish the baseline and distinguish measured facts from estimates or derived calculations.
2. **Automate work, not accountability.** A system performing a task does not eliminate ownership of the outcome.
3. **Use the least-complex reliable technology.** AI is not required when deterministic rules solve the problem better.
4. **Keep consequential judgment appropriately human-controlled.** Human approval boundaries should be explicit where risk warrants them.
5. **Design for failure and retry.** Automated systems should make state, errors, and recovery paths observable.
6. **Protect source information.** Public proof-of-work should be sanitized independently from private operational records.
7. **Evaluate the recovered capacity.** The final question is not whether an automation ran successfully, but whether the operating system became meaningfully better.

## Example: recurring reporting

The first published Capacity Recovery case study documents a recurring reporting portfolio at a large public university.

The process consumed more than 50 staff-hours on average per biweekly operating cycle across preparation and review. Repeatable processing was redesigned using Microsoft Excel and Power Query so automated processing could run in minutes once current source data was available, while people retained review, exception handling, follow-up, and accountability.

See:

[`Reporting Automation at a Large Public University`](../../case-studies/large-public-university-reporting-automation/)

## Applying the framework

A useful starting question for an operational workflow is:

> **Which parts of this work should people no longer have to perform manually—and which parts should remain distinctly human?**

From there, Discover and Measure establish the evidence, Separate determines the appropriate execution model, Automate changes the repeatable layer, and Recover evaluates the resulting organizational capacity.

---

Capacity Recovery is an evolving Gracelynd & Company operating framework. Public documentation will develop as additional implementations and case studies provide evidence for refining the model.