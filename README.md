# The Ternary Step-0 Field Simulator

An **experimental research repository** exploring the interaction between:

1. ordinary binary-style decision routing;
2. balanced ternary representation `{-1, 0, +1}`;
3. a Step-Zero-style tri-state work gate; and
4. exploratory field / latent N-body / quantum-inspired representations.

The project is intended to test whether ternary state representation and Step-0 subtraction can reduce unnecessary branching or expensive work at the **algorithmic level**.

## Core Step-0 ternary gate

For the simulator's routing experiments:

| State | Meaning |
|---:|---|
| **-1** | subtract / reject |
| **0** | reuse / no-op / preserve |
| **+1** | compute / escalate |

Conceptually:

```text
INPUT
  ↓
STEP 0
  ↓
{-1, 0, +1}
  ├─ -1 → remove / reject unnecessary work
  ├─  0 → preserve / reuse existing state
  └─ +1 → compute / escalate
```

This differs from the related bellaOS **evidence** vocabulary, where `-1` can mean contradicted, `0` unresolved, and `+1` supported. The common idea is preservation of a real neutral state rather than forcing every case into a binary yes/no outcome.

## Balanced ternary representation

For trits ordered least-significant first:

```text
value = Σ trit[i] × 3^i
where trit[i] ∈ {-1, 0, +1}
```

Reference conversion form used in the associated lab work:

```python
sum(int(t) * (3 ** i) for i, t in enumerate(trits))
```

Experiments can also track:

- digit-wise negation;
- balanced-ternary addition;
- normalization back into `{-1,0,+1}`;
- carry events;
- predicate/branch counts;
- work avoided by the neutral/reuse state;
- downstream quality or utility.

## Step Zero

Step Zero asks what can be removed, reused, preserved, or proven unnecessary **before** expensive execution begins.

A related experimental scoring form used in prior work was:

```text
S = U - λC - μR
```

where a thresholded score can determine whether work is rejected, preserved/reused, or escalated.

The broader objective is:

```text
minimize execution cost
subject to a required quality threshold
```

rather than simply minimizing computation at any cost.

## Research context

The simulator belongs to the Subtract Architect Studios **ternary / QST / alternative-computation research lane**. Related work has explored:

- Ternary Subtraction;
- Negative Step Zero;
- ternary routing before model/tool calls;
- RelAI escalation for unresolved work;
- latent N-body and field representations;
- quantum-inspired information and decision models.

These are research relationships, not claims that the simulator implements physical quantum computation or a new physical field theory.

## Scientific and engineering disclaimer

> **This runs on ordinary binary hardware. It does NOT benchmark physical ternary hardware.**

The software can test **representation, branching, work-avoidance, carry behavior, and algorithmic structure**. It cannot establish hardware speedups that would require real ternary circuitry.

Likewise, any N-body, field, or quantum-inspired component in this research line is **conceptual/experimental** unless separately supported by reproducible physical evidence. Visualization, analogy, algorithmic behavior, and established physics must remain clearly separated.

## Prior experimental result context

A related Ternary Step-Zero software harness tested a large synthetic workload and found fewer binary predicates while preserving the same routing result in that experiment. Python wall-clock performance was slower, which is important: that experiment supported an **algorithmic representation hypothesis**, not a ternary-hardware performance claim.

This repository should continue to preserve that distinction.

## Status

**Experimental / research. Not a production system and not an established-physics claim.**

Promotion should require reproducible code, frozen inputs, positive and negative controls, independent computation paths, counterexample-first testing, and explicit ternary evidence states.

---

**Subtract Architect Studios**  
*Intelligence by Subtraction*

<!-- SAS-IP-FOOTER-v1 -->
---
**Subtract Architect Studios™**  
Copyright © 2026 Michael F. Chaves. All rights reserved in original Subtract Architect Studios materials except as expressly licensed. See [IP_NOTICE.md](./IP_NOTICE.md). Existing open-source and third-party licenses remain controlling for materials they cover.
