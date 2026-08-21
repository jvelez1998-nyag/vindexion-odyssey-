# RSK-080 — Quantum-Readiness Risk Score (Crypto-Agility Index)

## Domain 01 — Risk Management & Quantification

### Part 1 — Feature Definition, Crypto-Agility Model, Quantum Exposure & Core Product Experience

---

# Feature Identity

- **Feature ID:** RSK-080
- **Canonical Source:** Claude RSK-505
- **Canonical Name:** Quantum-Readiness Risk Score (Crypto-Agility Index)
- **Capability Area:** Risk Management — Gen 5
- **Domain:** Domain 01 — Risk Management & Quantification
- **Generation:** Gen 5 — Moonshot / Frontier
- **Status:** Not Started
- **Primary Dependencies:** RSK-001, RSK-005
- **Primary Workspace:** Risk Detail View
- **Primary Users:** CISO, CRO, Technology Risk, Cybersecurity, Enterprise Architecture
- **Moonshot Tie:** Quantum-Readiness Governance
- **Interaction Model:** First-Class Risk Sub-Score

---

# Canonical Definition

RSK-080 introduces a dedicated risk sub-score quantifying two related conditions:

1. An entity's exposure to **quantum-enabled cryptographic compromise**
2. Its **crypto-agility** — the ability to migrate from vulnerable cryptographic mechanisms to post-quantum alternatives

The score is surfaced alongside the standard enterprise risk score rather than buried in narrative commentary.

The canonical requirement is:

# **QUANTUM READINESS MUST BECOME A MEASURABLE RISK STATE.**

---

# Canonical Acceptance Criteria

The original Claude requirement establishes two minimum conditions:

```text
DEFINED CRYPTO-AGILITY INPUTS
        ↓
QUANTUM-READINESS SCORE
        ↓
STANDARD RISK DETAIL VIEW
        ↓
DISTINCT FIRST-CLASS SUB-SCORE
```

Specifically:

- The score must derive from defined crypto-agility inputs, including **algorithm inventory** and **migration readiness**
- The resulting score must appear on **RSK-005 — Risk Detail View**
- It must be displayed as a distinct score rather than hidden in narrative text

---

# Core Product Thesis

# **YOU CANNOT GOVERN QUANTUM RISK IF YOU CANNOT SEE WHICH CRYPTOGRAPHY YOU DEPEND ON OR HOW FAST YOU CAN REPLACE IT.**

Traditional technology risk may identify:

```text
CRYPTOGRAPHIC RISK
```

but still fail to answer:

```text
WHICH ALGORITHMS?
      ↓
WHERE ARE THEY USED?
      ↓
WHICH ARE QUANTUM-EXPOSED?
      ↓
WHAT DEPENDS ON THEM?
      ↓
CAN THEY BE REPLACED?
      ↓
HOW LONG WILL MIGRATION TAKE?
```

RSK-080 turns those questions into a measurable risk posture.

---

# Why This Capability Exists

Quantum computing creates a distinctive enterprise risk problem.

The risk is not simply:

```text
QUANTUM COMPUTER EXISTS
      ↓
ENCRYPTION FAILS
```

The enterprise problem is the transition path.

Organizations may have cryptography embedded across:

- Applications
- APIs
- Databases
- Identity systems
- Certificates
- Network protocols
- Devices
- Cloud services
- Third-party integrations
- Archived information

The critical question becomes:

# **HOW PREPARED IS THE ENTERPRISE TO CHANGE ITS CRYPTOGRAPHIC FOUNDATION BEFORE EXISTING MECHANISMS BECOME UNSUITABLE?**

---

# Two-Dimensional Model

RSK-080 should distinguish:

## Quantum Exposure

How materially the entity depends on cryptographic mechanisms that may become vulnerable in a quantum-computing future.

and:

## Crypto-Agility

How capable the entity is of discovering, replacing, testing, and migrating those mechanisms.

Conceptually:

```text
QUANTUM EXPOSURE
        +
CRYPTO-AGILITY
        ↓
QUANTUM-READINESS RISK
```

These dimensions should not be collapsed prematurely.

---

# Core Scoring Dimensions

The initial score should be built from a compact set of meaningful inputs.

| Dimension | Core Question |
|---|---|
| Algorithm Inventory | Do we know what cryptography exists? |
| Quantum Exposure | How much relies on potentially vulnerable mechanisms? |
| Migration Readiness | Can affected cryptography be replaced? |
| Dependency Criticality | What critical services depend on it? |
| Data Longevity | Will protected information remain sensitive long enough for future compromise to matter? |
| Third-Party Dependency | Are critical cryptographic dependencies outside enterprise control? |

This is intentionally concise.

Detailed scoring calibration belongs in subsequent implementation work.

---

# Dimension 01 — Algorithm Inventory

The first requirement is visibility.

The enterprise should be able to answer:

```text
WHAT CRYPTOGRAPHIC ALGORITHMS
ARE IN USE?
```

Representative inventory objects:

```text
ALGORITHM
KEY TYPE
KEY LENGTH
PROTOCOL
CERTIFICATE
LIBRARY
SYSTEM
APPLICATION
SERVICE
DATA ASSET
VENDOR
```

The objective is not to create another asset inventory.

It is to establish the cryptographic dependency layer necessary to calculate readiness.

---

# Inventory Coverage

A useful measure is:

# **Cryptographic Inventory Coverage**

Example:

```text
IN-SCOPE SYSTEMS
2,480

SYSTEMS WITH VERIFIED
CRYPTOGRAPHIC INVENTORY
1,984

COVERAGE
80%
```

Unknown cryptography should increase uncertainty rather than silently appear safe.

---

# Dimension 02 — Quantum Exposure

Each discovered cryptographic dependency should be evaluated for quantum relevance.

Representative classification:

```text
LOW
MODERATE
ELEVATED
HIGH
UNKNOWN
```

The purpose is not to predict the exact arrival date of cryptographically relevant quantum computing.

The purpose is to understand enterprise exposure **if and as the threat matures**.

---

# Exposure Object

Example:

```text
SYSTEM
Digital Payments Gateway

ALGORITHM
RSA-2048

USE
Key Exchange

BUSINESS CRITICALITY
Critical

QUANTUM EXPOSURE
High

REPLACEMENT PATH
Identified
```

This makes the exposure actionable.

---

# Dimension 03 — Migration Readiness

Crypto-agility depends on whether the organization can replace affected cryptography.

Representative maturity states:

```text
NOT ASSESSED
      ↓
DEPENDENCY KNOWN
      ↓
REPLACEMENT IDENTIFIED
      ↓
MIGRATION PLANNED
      ↓
TESTED
      ↓
MIGRATION READY
```

This dimension should materially influence the readiness score.

---

# Migration Readiness Example

```text
SYSTEM
Digital Payments Gateway

CURRENT
RSA-2048

TARGET
Approved PQC Architecture

OWNER
Payments Engineering

PLAN
Defined

TESTING
In Progress

TARGET MIGRATION
Q2 2028
```

The product should distinguish between knowing a problem exists and being capable of resolving it.

---

# Dimension 04 — Dependency Criticality

Not all cryptographic exposure carries equal enterprise consequence.

Example:

```text
SYSTEM A
Legacy internal utility
HIGH QUANTUM EXPOSURE
LOW BUSINESS CRITICALITY

SYSTEM B
Payment authorization
HIGH QUANTUM EXPOSURE
CRITICAL BUSINESS SERVICE
```

System B should contribute materially more to enterprise quantum-readiness risk.

---

# Critical Service Linkage

The score should be able to connect:

```text
ALGORITHM
      ↓
SYSTEM
      ↓
BUSINESS SERVICE
      ↓
CRITICAL PROCESS
      ↓
RISK
```

Example:

```text
RSA-2048
      ↓
PAYMENT GATEWAY
      ↓
DIGITAL PAYMENTS
      ↓
CUSTOMER TRANSACTIONS
      ↓
QUANTUM-READINESS RISK
```

This prevents quantum readiness from becoming an isolated cryptography exercise.

---

# Dimension 05 — Data Longevity

Some information may remain sensitive for many years.

This creates a distinctive risk:

```text
CAPTURE ENCRYPTED DATA TODAY
        ↓
STORE
        ↓
FUTURE QUANTUM CAPABILITY
        ↓
DECRYPT LATER
```

RSK-080 should therefore recognize the relationship between:

```text
DATA SENSITIVITY
        +
REQUIRED CONFIDENTIALITY PERIOD
        +
CRYPTOGRAPHIC EXPOSURE
```

---

# Long-Lived Data Example

```text
DATA CLASS
Strategic M&A

CONFIDENTIALITY HORIZON
10+ Years

CRYPTOGRAPHIC DEPENDENCY
Quantum-Exposed

READINESS
Low
```

This may justify remediation earlier than systems protecting short-lived information.

---

# Dimension 06 — Third-Party Dependency

Crypto-agility may be constrained by vendors.

Example:

```text
CRITICAL SERVICE
Identity Platform

CRYPTOGRAPHY CONTROLLED BY
External Vendor

CUSTOMER MIGRATION CONTROL
Limited

VENDOR PQC ROADMAP
Unconfirmed
```

The organization may understand the exposure but lack direct authority to remediate it.

That constraint should be visible.

---

# Crypto-Agility Index™

RSK-080 should expose a distinct:

# **Crypto-Agility Index™**

Illustrative scale:

```text
0 ───────────────────────────── 100

LOW AGILITY                    HIGH AGILITY
```

Example:

# **62 / 100 — DEVELOPING**

Supporting indicators:

```text
INVENTORY COVERAGE       80%
MIGRATION READINESS      54%
CRITICAL DEPENDENCIES    17
UNKNOWN DEPENDENCIES     23
VENDOR ROADMAP COVERAGE  61%
```

---

# Score Direction

For usability, the interface must make score direction explicit.

Recommended:

```text
HIGHER CRYPTO-AGILITY
=
BETTER READINESS
```

while:

```text
HIGHER QUANTUM EXPOSURE
=
GREATER RISK
```

These should not use ambiguous labels.

---

# Risk Detail View

RSK-080's defining product requirement is its integration into RSK-005.

Example:

```text
RISK DETAIL
────────────────────────

ENTERPRISE RISK SCORE
82 / 100
HIGH

QUANTUM EXPOSURE
78 / 100
HIGH

CRYPTO-AGILITY INDEX™
62 / 100
DEVELOPING
```

The user should not need to open a separate quantum module to discover the risk.

---

# Combined Readiness Interpretation

The product may derive an overall readiness state from exposure and agility.

Example:

```text
QUANTUM EXPOSURE
78 — HIGH

CRYPTO-AGILITY
62 — DEVELOPING

        ↓

QUANTUM-READINESS POSTURE
WATCH
```

The underlying dimensions remain visible.

---

# Quantum-Readiness Posture

Representative states:

```text
READY
WATCH
ELEVATED
CRITICAL
UNKNOWN
```

The state should summarize—not replace—the underlying score components.

---

# Hero Risk Example

## RSK-2841 — Digital Payments Cryptographic Dependency

```text
ENTERPRISE RISK
82 / 100 — HIGH

QUANTUM EXPOSURE
88 / 100 — HIGH

CRYPTO-AGILITY
54 / 100 — LOW

CRITICAL SYSTEMS
6

QUANTUM-EXPOSED DEPENDENCIES
14

MIGRATION READY
5

UNKNOWN
3
```

### Primary Driver

```text
RSA-2048 dependency remains embedded
across payment authorization services.
```

### Recommended Priority

# **ACCELERATE CRYPTOGRAPHIC MIGRATION PLANNING**

---

# Exposure-to-Readiness Matrix

A compact matrix can help prioritize action.

| Quantum Exposure | Crypto-Agility | Interpretation |
|---|---|---|
| Low | High | Strong |
| High | High | Managed Exposure |
| Low | Low | Readiness Gap |
| High | Low | Priority Exposure |

The most concerning state is:

# **HIGH EXPOSURE + LOW AGILITY**

---

# Portfolio View

The capability should roll upward from individual risk to portfolio.

Example:

| Business Service | Exposure | Agility | State |
|---|---:|---:|---|
| Digital Payments | 88 | 54 | Elevated |
| Identity | 82 | 71 | Watch |
| Treasury | 76 | 43 | Elevated |
| HR Platforms | 41 | 78 | Strong |
| Collaboration | 37 | 81 | Strong |

This enables prioritization based on enterprise consequence.

---

# Concentration Intelligence

Quantum-readiness risk may cluster around shared technologies.

Example:

```text
RSA-2048

USED BY
47 SYSTEMS

SUPPORTS
11 CRITICAL SERVICES

BUSINESS UNITS
6
```

The product should identify these concentrations.

A single migration initiative may reduce exposure across many risks simultaneously.

---

# Migration Leverage™

RSK-080 should introduce a useful prioritization concept:

# **Migration Leverage™**

Definition:

> The amount of enterprise quantum exposure that can be reduced by migrating a shared cryptographic dependency.

Example:

```text
IDENTITY CRYPTOGRAPHY UPGRADE

SYSTEMS AFFECTED
31

CRITICAL SERVICES
8

RISKS IMPROVED
12
```

### Migration Leverage

# **HIGH**

This helps prioritize remediation with the greatest enterprise effect.

---

# Unknown Exposure

Unknown should remain a first-class state.

Example:

```text
CRITICAL SYSTEMS
42

VERIFIED CRYPTOGRAPHY
31

UNKNOWN
11
```

The system should not interpret the 11 unknown systems as low exposure.

Instead:

# **UNKNOWN CRYPTOGRAPHY = UNRESOLVED RISK**

---

# Crypto-Agility Evidence

Representative evidence supporting the score:

- Cryptographic inventory
- System dependency mapping
- Algorithm classification
- Migration roadmap
- Architecture decision
- PQC testing results
- Vendor readiness statement
- Replacement timeline

The score should be traceable to these inputs.

---

# Readiness Confidence

A readiness score built on incomplete inventory should communicate reduced confidence.

Example:

```text
CRYPTO-AGILITY
62 / 100

CONFIDENCE
71%

PRIMARY LIMITATION
20% of in-scope systems lack verified
cryptographic inventory
```

This prevents false precision.

---

# Time Dimension

Quantum readiness should be trended.

Example:

```text
Q1      44
Q2      49
Q3      57
CURRENT 62
```

Supporting changes:

```text
INVENTORY COVERAGE
61% → 80%

MIGRATION-READY SYSTEMS
18% → 37%
```

This allows leadership to see whether readiness is improving.

---

# Target State

An organization may establish:

```text
CURRENT CRYPTO-AGILITY
62

TARGET
85

TARGET DATE
Q4 2028
```

The platform can then track the readiness gap.

---

# Readiness Gap

Example:

```text
TARGET
85

CURRENT
62

GAP
23 POINTS
```

The gap should be explainable through underlying dimensions rather than presented as an unexplained number.

---

# Migration Portfolio

A concise remediation portfolio may show:

| Initiative | Exposure Reduced | Readiness |
|---|---:|---|
| Payment Gateway PQC Migration | High | Testing |
| Identity Certificate Upgrade | High | Planned |
| API Crypto Library Replacement | Medium | Ready |
| Vendor Crypto Roadmap | Medium | Awaiting Vendor |

This converts the score into action.

---

# Primary User Journey

```text
OPEN RISK
      ↓
SEE STANDARD SCORE
      ↓
SEE QUANTUM EXPOSURE
      ↓
SEE CRYPTO-AGILITY
      ↓
IDENTIFY PRIMARY DEPENDENCY
      ↓
TRACE CRITICAL SERVICES
      ↓
REVIEW MIGRATION READINESS
      ↓
PRIORITIZE ACTION
```

The quantum score should fit naturally inside the existing risk workflow.

---

# CISO Experience

The CISO should be able to answer:

```text
WHERE ARE WE MOST EXPOSED?
WHICH CRYPTOGRAPHY DRIVES IT?
WHICH CRITICAL SERVICES DEPEND ON IT?
WHICH MIGRATIONS ARE NOT READY?
WHERE DO WE HAVE UNKNOWN EXPOSURE?
```

without assembling separate spreadsheets.

---

# CRO Experience

The CRO should be able to see quantum readiness in enterprise-risk terms:

```text
BUSINESS SERVICES
RISK CONCENTRATION
REMEDIATION PRIORITY
TREND
TARGET STATE
```

rather than cryptographic implementation detail alone.

---

# Enterprise Architecture Experience

Architecture teams need:

```text
CURRENT ALGORITHM
      ↓
DEPENDENCY
      ↓
TARGET MECHANISM
      ↓
MIGRATION STATE
```

This creates a direct bridge between enterprise risk and technology transformation.

---

# AI Marker

### AI-Assisted Quantum-Readiness Interpretation

AI may assist by:

- Summarizing primary readiness drivers
- Identifying concentration patterns
- Highlighting incomplete inventory
- Explaining score movement
- Suggesting high-leverage migration candidates

Example:

> Digital Payments remains the largest quantum-readiness concentration. Five shared RSA dependencies account for 41% of the business service's measured exposure.

AI interpretation should derive from the underlying structured evidence.

---

# Minimum Viable Capability

The MVP should remain focused.

Required:

```text
CRYPTOGRAPHIC INPUTS
        ↓
QUANTUM EXPOSURE
        +
CRYPTO-AGILITY
        ↓
FIRST-CLASS SCORE
        ↓
RSK-005 RISK DETAIL
```

Minimum requirements:

- Defined algorithm inventory inputs
- Migration-readiness inputs
- Quantum exposure score
- Crypto-Agility Index™
- Readiness confidence
- Distinct presentation on Risk Detail
- Traceability to source inputs

---

# Acceptance Test 01 — Score Computation

Given:

```text
VERIFIED ALGORITHM INVENTORY
+
MIGRATION READINESS DATA
```

Expected:

```text
CRYPTO-AGILITY INDEX
COMPUTED
```

### Result

# **PASS / FAIL**

---

# Acceptance Test 02 — Risk Detail Visibility

Open:

```text
RSK-005
RISK DETAIL VIEW
```

Expected:

```text
STANDARD RISK SCORE
+
QUANTUM EXPOSURE
+
CRYPTO-AGILITY INDEX
```

The quantum-readiness score must be a visible first-class component.

### Result

# **PASS / FAIL**

---

# Acceptance Test 03 — Unknown Inventory

Given incomplete cryptographic inventory:

Expected:

```text
UNKNOWN EXPOSURE
+
REDUCED CONFIDENCE
```

The system must not silently classify missing inventory as low risk.

---

# Acceptance Test 04 — Dependency Trace

Select a high-exposure cryptographic dependency.

Expected:

```text
ALGORITHM
→ SYSTEM
→ BUSINESS SERVICE
→ RISK
```

The user can understand why the dependency matters.

---

# Acceptance Test 05 — Migration Readiness

Update:

```text
MIGRATION STATE
PLANNED → TESTED
```

Expected:

```text
CRYPTO-AGILITY
RECALCULATED
```

with the score movement attributable to the changed readiness input.

---

# Unique Product Metrics

| Metric | Purpose |
|---|---|
| Crypto-Agility Index™ | Migration capability |
| Quantum Exposure Score | Exposure magnitude |
| Cryptographic Inventory Coverage | Visibility |
| Unknown Dependency Rate | Uncertainty |
| Migration-Ready Percentage | Execution readiness |
| Critical Services Exposed | Business consequence |
| Readiness Confidence | Evidence strength |
| Migration Leverage™ | Remediation prioritization |

---

# Product Boundary

RSK-080 does **not**:

- Predict the date of cryptographically relevant quantum computing
- Replace cryptographic asset discovery
- Select cryptographic standards
- Perform cryptographic migration
- Guarantee future cryptographic security
- Replace Domain 11 quantum-readiness governance

Its purpose is narrower:

# **QUANTIFY QUANTUM-RELATED CRYPTOGRAPHIC EXPOSURE AND MIGRATION READINESS AS ENTERPRISE RISK.**

---

# Cross-Domain Role

RSK-080 becomes the risk-layer counterpart of the broader quantum-readiness governance architecture.

Its role is:

```text
QUANTUM / CRYPTOGRAPHIC REALITY
        ↓
RISK QUANTIFICATION
        ↓
ENTERPRISE PRIORITIZATION
```

Other domains may subsequently consume that quantified risk state.

---

# Part 1 Compression Boundary

The following established material is intentionally not repeated:

- General risk governance doctrine
- Standard human authority principles
- Generic model lineage
- Common audit requirements
- Standard security controls
- Generic API architecture
- Common AI explainability doctrine
- Standard evidence architecture
- Generic RBAC
- Shared platform telemetry

Those requirements remain inherited.

This Part captures only information materially unique to **quantum exposure, crypto-agility, cryptographic dependency, migration readiness, and the first-class quantum-readiness risk score**.

---

# Part 1 Closing Perspective

Quantum readiness should not live in a strategy paper waiting for the future to arrive.

The enterprise already has cryptographic dependencies.

Those dependencies already support critical systems.

Some data already needs to remain confidential for years.

Migration already takes time.

And organizations cannot replace cryptography they do not know they have.

RSK-080 converts that uncertainty into something enterprise leaders can govern:

```text
KNOW THE CRYPTOGRAPHY
        ↓
MEASURE THE EXPOSURE
        ↓
ASSESS THE AGILITY
        ↓
IDENTIFY THE DEPENDENCIES
        ↓
PRIORITIZE THE MIGRATION
        ↓
TRACK READINESS
```

The question is no longer merely:

> **When will quantum computing become a threat?**

The more useful governance question is:

# **IF THE THREAT ARRIVES, HOW READY ARE WE TO CHANGE?**

---

## End of Part 1

---

# RSK-080 — Quantum-Readiness Risk Score (Crypto-Agility Index)

## Domain 01 — Risk Management & Quantification

### Part 2 — Customer Experience, Portfolio Prioritization, Migration Intelligence & Commercial Value

---

# Part 2 Purpose

Part 1 established the unique scoring model:

```text
QUANTUM EXPOSURE
        +
CRYPTO-AGILITY
        ↓
QUANTUM-READINESS POSTURE
```

Part 2 defines the **customer experience and business value** created by making that posture visible and actionable across risks, systems, services, and migration programs.

This Part captures only RSK-080-specific material.

---

# Primary Customer Journey

```text
OPEN RISK
      ↓
SEE QUANTUM-READINESS STATE
      ↓
IDENTIFY EXPOSURE DRIVER
      ↓
TRACE DEPENDENCY
      ↓
ASSESS MIGRATION READINESS
      ↓
COMPARE PORTFOLIO
      ↓
PRIORITIZE MIGRATION
      ↓
TRACK READINESS IMPROVEMENT
```

The feature should convert quantum readiness from a technical concern into a prioritized enterprise-risk workflow.

---

# Experience 01 — Risk Detail

The user opens a standard risk record.

Example:

```text
RISK
Digital Payments Cryptographic Dependency

ENTERPRISE RISK
82 / 100 — HIGH

QUANTUM EXPOSURE
88 / 100 — HIGH

CRYPTO-AGILITY INDEX™
54 / 100 — LOW

QUANTUM-READINESS POSTURE
ELEVATED
```

The quantum-readiness state appears immediately beside the ordinary risk score.

---

# Experience 02 — Why Is the Score Elevated?

The user selects:

```text
WHY?
```

The feature presents the major drivers.

Example:

| Driver | Contribution |
|---|---:|
| RSA-2048 Critical-Service Dependence | High |
| Migration Readiness | Low |
| Vendor Dependency | Medium |
| Long-Lived Data Exposure | Medium |
| Inventory Unknowns | Medium |

### Primary Driver

# **CRITICAL PAYMENT SERVICES REMAIN DEPENDENT ON QUANTUM-EXPOSED CRYPTOGRAPHY WITH INCOMPLETE MIGRATION READINESS.**

The user should understand the score without reverse-engineering the model.

---

# Experience 03 — Dependency Trace

From the risk record:

```text
RSA-2048
      ↓
PAYMENT GATEWAY
      ↓
DIGITAL PAYMENTS
      ↓
CUSTOMER TRANSACTIONS
```

The user can see why one cryptographic dependency matters to the business.

This is more useful than a standalone cryptographic inventory.

---

# Experience 04 — Migration Readiness

Selecting the dependency shows:

```text
CURRENT ALGORITHM
RSA-2048

TARGET STATE
Approved PQC Architecture

CURRENT PHASE
Testing

OWNER
Payments Engineering

TARGET MIGRATION
Q2 2028

BLOCKERS
2
```

The feature should connect risk state to migration execution.

---

# Experience 05 — Portfolio Prioritization

A CISO should be able to compare major services.

| Business Service | Exposure | Agility | Posture |
|---|---:|---:|---|
| Digital Payments | 88 | 54 | Elevated |
| Identity | 82 | 71 | Watch |
| Treasury | 76 | 43 | Elevated |
| HR Platforms | 41 | 78 | Strong |
| Collaboration | 37 | 81 | Strong |

The portfolio should answer:

# **WHERE DOES HIGH EXPOSURE INTERSECT WITH LOW AGILITY?**

---

# Priority Quadrant

The most useful portfolio view is a 2×2 matrix.

```text
                    HIGH CRYPTO-AGILITY
                           ↑

LOW EXPOSURE        STRONG / MAINTAIN
HIGH AGILITY

HIGH EXPOSURE       MANAGED EXPOSURE
HIGH AGILITY

--------------------------------------------→ QUANTUM EXPOSURE

LOW EXPOSURE        READINESS GAP
LOW AGILITY

HIGH EXPOSURE       PRIORITY EXPOSURE
LOW AGILITY
```

The upper-right / high-exposure-low-agility population should drive executive attention.

---

# Experience 06 — Migration Leverage™

A migration initiative may improve multiple risks simultaneously.

Example:

## Identity Cryptography Upgrade

```text
SYSTEMS AFFECTED
31

CRITICAL SERVICES
8

RISKS IMPROVED
12

ESTIMATED EXPOSURE REDUCTION
High
```

### Migration Leverage™

# **HIGH**

This helps avoid prioritizing migrations purely system by system.

---

# Portfolio Leverage View

| Migration Initiative | Systems | Critical Services | Risks Improved | Leverage |
|---|---:|---:|---:|---|
| Identity Crypto Upgrade | 31 | 8 | 12 | High |
| Payment Gateway PQC | 14 | 3 | 6 | High |
| Internal API Library | 42 | 2 | 9 | Medium |
| Legacy Archive Migration | 7 | 1 | 2 | Low |

The feature should surface where one modernization effort creates broad risk reduction.

---

# Experience 07 — Unknown Exposure

A strong user experience should make incomplete visibility impossible to ignore.

Example:

```text
IN-SCOPE SYSTEMS
2,480

VERIFIED CRYPTOGRAPHY
1,984

UNKNOWN
496

INVENTORY COVERAGE
80%
```

The portfolio should distinguish:

```text
LOW EXPOSURE
```

from:

```text
UNKNOWN EXPOSURE
```

These are not equivalent.

---

# Unknown Exposure Queue

Example:

| System | Criticality | Inventory State | Action |
|---|---|---|---|
| Treasury Gateway | Critical | Unknown | Prioritize Discovery |
| Legacy CRM | High | Unknown | Assess |
| HR Archive | Moderate | Partial | Complete Inventory |

This gives architecture and security teams a concrete discovery backlog.

---

# Experience 08 — Long-Lived Data

A user should be able to filter:

# **HARVEST-NOW-DECRYPT-LATER EXPOSURE**

Representative result:

```text
LONG-LIVED SENSITIVE DATA
23 DATA CLASSES

QUANTUM-EXPOSED
11

CRITICAL
4
```

This identifies migration urgency that may not be apparent from system criticality alone.

---

# Long-Lived Data Portfolio

| Data Class | Confidentiality Horizon | Exposure | Priority |
|---|---:|---|---|
| Strategic M&A | 10+ Years | High | Critical |
| Research IP | 15+ Years | High | Critical |
| Customer Records | 7+ Years | Medium | High |
| Session Logs | <1 Year | Medium | Lower |

This helps distinguish near-term migration priority.

---

# Experience 09 — Third-Party Constraint

A vendor-controlled cryptographic dependency should be visible as a distinct constraint.

Example:

```text
SERVICE
Identity Platform

CONTROL
External Vendor

QUANTUM EXPOSURE
High

CUSTOMER MIGRATION CONTROL
Limited

VENDOR ROADMAP
Unconfirmed
```

### Implication

# **READINESS IS CONSTRAINED BY EXTERNAL DEPENDENCY**

This may require vendor engagement rather than internal engineering work.

---

# Vendor Readiness Queue

Example:

| Vendor | Critical Services | Roadmap | Risk |
|---|---:|---|---|
| Vendor A | 6 | Confirmed | Watch |
| Vendor B | 4 | Unconfirmed | Elevated |
| Vendor C | 2 | Testing | Moderate |

This connects quantum readiness to third-party action.

---

# Experience 10 — Readiness Trend

The customer should be able to see progress.

Example:

```text
CRYPTO-AGILITY INDEX™

Q1       44
Q2       49
Q3       57
CURRENT  62
```

Supporting changes:

```text
INVENTORY COVERAGE
61% → 80%

MIGRATION-READY SYSTEMS
18% → 37%

UNKNOWN DEPENDENCIES
42 → 23
```

The feature should show *why* the score improved.

---

# Experience 11 — Target State

Example:

```text
CURRENT
62

TARGET
85

TARGET DATE
Q4 2028

READINESS GAP
23
```

The target should be decomposed.

Example:

```text
INVENTORY
80 → 98

MIGRATION READINESS
54 → 85

VENDOR ROADMAP COVERAGE
61 → 95
```

This makes the target operational.

---

# Experience 12 — Executive Attention

A CRO or CISO should receive a concise queue.

```text
TOP QUANTUM-READINESS PRIORITIES

1. DIGITAL PAYMENTS
   Exposure 88 / Agility 54

2. TREASURY
   Exposure 76 / Agility 43

3. IDENTITY VENDOR DEPENDENCY
   Roadmap Unconfirmed

4. 11 LONG-LIVED DATA CLASSES
   Quantum-Exposed
```

This is the executive product outcome.

---

# Quantum-Readiness Portfolio

Representative enterprise roll-up:

```text
ENTERPRISE CRYPTO-AGILITY
67 / 100

HIGH-EXPOSURE SERVICES
14

LOW-AGILITY SERVICES
9

HIGH EXPOSURE + LOW AGILITY
6

UNKNOWN CRITICAL DEPENDENCIES
11

MIGRATION-READY
37%
```

This creates one clear portfolio view.

---

# Readiness Segmentation

The portfolio may classify entities as:

```text
READY
WATCH
ELEVATED
CRITICAL
UNKNOWN
```

Example:

| State | Services |
|---|---:|
| Ready | 18 |
| Watch | 22 |
| Elevated | 11 |
| Critical | 4 |
| Unknown | 7 |

The Unknown population should remain visible.

---

# CISO Workflow

The CISO should be able to move from:

```text
ENTERPRISE READINESS
      ↓
HIGH-EXPOSURE SERVICES
      ↓
CRYPTOGRAPHIC DEPENDENCY
      ↓
MIGRATION INITIATIVE
      ↓
OWNER / TARGET
```

without switching between disconnected security tools and risk spreadsheets.

---

# CRO Workflow

The CRO needs a more business-oriented path:

```text
ENTERPRISE RISK
      ↓
BUSINESS SERVICE
      ↓
QUANTUM-READINESS POSTURE
      ↓
BUSINESS CONSEQUENCE
      ↓
REMEDIATION PRIORITY
```

The CRO should not need detailed cryptographic expertise to interpret the risk.

---

# Architecture Workflow

Enterprise Architecture needs:

```text
CRYPTOGRAPHIC DEPENDENCY
      ↓
TARGET ARCHITECTURE
      ↓
MIGRATION STATE
      ↓
BLOCKER
      ↓
TARGET DATE
```

This makes the score directly useful for transformation planning.

---

# Program Management Workflow

A quantum-readiness program office may manage:

```text
DISCOVERY
      ↓
ASSESSMENT
      ↓
TARGET DESIGN
      ↓
TESTING
      ↓
MIGRATION
      ↓
VALIDATION
```

RSK-080 should summarize the resulting readiness state rather than recreate the entire migration program.

---

# AI-Assisted Interpretation

Example:

### CISO

> Why did our crypto-agility improve this quarter?

### Vindexion

> Inventory coverage increased from 72% to 80%, six critical payment systems advanced from Planned to Testing, and vendor roadmap confirmation improved across three identity-service providers. The largest remaining constraint is Treasury, where five high-criticality systems have no tested migration path.

This is a useful AI experience because it explains movement in structured readiness inputs.

---

# AI-Assisted Prioritization

Example:

### User

> What migration would reduce the most exposure?

### Vindexion

> The Identity Cryptography Upgrade has the highest modeled Migration Leverage™. It affects 31 systems, eight critical services, and twelve current risk records.

This converts dependency analysis into prioritization.

---

# Commercial Value Proposition

RSK-080 creates value by moving quantum readiness from:

```text
FUTURE-STATE SECURITY DISCUSSION
```

to:

```text
CURRENT ENTERPRISE RISK MEASUREMENT
```

Customers gain:

- Quantified readiness
- Business-service prioritization
- Migration visibility
- Unknown-exposure visibility
- Portfolio progress tracking
- Executive reporting

---

# Commercial Positioning

Recommended category:

# **QUANTUM-READINESS RISK INTELLIGENCE**

Supporting description:

> Quantify cryptographic exposure and migration agility as a first-class enterprise risk posture.

Avoid positioning it simply as:

- PQC dashboard
- Cryptography inventory
- Quantum security checklist

The differentiation is risk quantification and enterprise prioritization.

---

# Buyer Narrative — CISO

# **KNOW WHICH CRYPTOGRAPHIC DEPENDENCIES CREATE THE GREATEST FUTURE EXPOSURE AND WHICH ONES YOU ARE LEAST READY TO MIGRATE.**

Primary value:

- Migration prioritization
- Unknown exposure reduction
- Critical-system visibility

---

# Buyer Narrative — CRO

# **MAKE QUANTUM READINESS VISIBLE IN THE SAME ENTERPRISE-RISK LANGUAGE USED FOR EVERY OTHER MATERIAL EXPOSURE.**

Primary value:

- Portfolio comparability
- Executive prioritization
- Board visibility

---

# Buyer Narrative — CIO / Architecture

# **TURN CRYPTOGRAPHIC MODERNIZATION INTO A RISK-PRIORITIZED TRANSFORMATION ROADMAP.**

Primary value:

- Dependency traceability
- Migration sequencing
- Criticality-based prioritization

---

# Buyer Narrative — Board Risk Committee

# **UNDERSTAND WHETHER THE ENTERPRISE CAN MIGRATE CRITICAL CRYPTOGRAPHY BEFORE THE RISK BECOMES URGENT.**

Board focus should remain:

- Exposure
- Readiness
- Critical services
- Trend
- Target state

not algorithm-level implementation details.

---

# Commercial Differentiation

Traditional readiness assessment:

```text
QUESTIONNAIRE
      ↓
MATURITY SCORE
      ↓
REPORT
```

RSK-080:

```text
CRYPTOGRAPHIC DEPENDENCIES
      +
BUSINESS CRITICALITY
      +
MIGRATION STATE
      +
DATA LONGEVITY
      ↓
FIRST-CLASS RISK SCORE
      ↓
PORTFOLIO PRIORITIZATION
```

The distinction is:

# **READINESS IS GROUNDED IN ACTUAL ENTERPRISE DEPENDENCIES, NOT A GENERIC MATURITY CHECKLIST.**

---

# Migration Economics

RSK-080 may eventually support prioritization using:

```text
EXPOSURE REDUCTION
        ÷
MIGRATION EFFORT
```

Conceptually:

# **Migration Efficiency**

Example:

| Initiative | Exposure Reduction | Effort | Priority |
|---|---|---|---|
| Identity Upgrade | High | Medium | Very High |
| Payment Gateway | High | High | High |
| Legacy Archive | Medium | High | Medium |

This should be treated as future decision intelligence, not part of the canonical score.

---

# Customer Use Case 01 — Payment Modernization

### Situation

Critical payment systems depend on RSA-based cryptography.

### RSK-080

Shows:

```text
QUANTUM EXPOSURE
88

CRYPTO-AGILITY
54

STATE
ELEVATED
```

### Outcome

Payment cryptographic migration moves into a higher-priority transformation roadmap.

---

# Customer Use Case 02 — Unknown Estate

### Situation

The enterprise has only 60% verified cryptographic inventory coverage.

### RSK-080

Shows a reduced confidence score and an Unknown Exposure queue.

### Outcome

Discovery becomes a formal risk-reduction initiative rather than an inventory-cleanup exercise.

---

# Customer Use Case 03 — Vendor Constraint

### Situation

A critical identity provider has not published a credible PQC migration roadmap.

### RSK-080

Shows low customer migration control and elevated third-party dependency.

### Outcome

Vendor engagement and contingency planning are prioritized.

---

# Customer Use Case 04 — Long-Lived Data

### Situation

Sensitive research data must remain confidential for 15 years.

### RSK-080

Highlights harvest-now-decrypt-later exposure.

### Outcome

Migration urgency increases even though the current application itself is stable.

---

# Customer Use Case 05 — Board Progress Review

### Situation

The board asks whether quantum readiness is improving.

### RSK-080

Shows:

```text
CRYPTO-AGILITY
44 → 62

INVENTORY
61% → 80%

MIGRATION READY
18% → 37%
```

### Outcome

The board sees measurable progress rather than a narrative update.

---

# Success Measures

Primary product measures:

| Measure | Desired Direction |
|---|---|
| Cryptographic Inventory Coverage | ↑ |
| Crypto-Agility Index™ | ↑ |
| Unknown Dependency Rate | ↓ |
| Migration-Ready Percentage | ↑ |
| High Exposure + Low Agility Population | ↓ |
| Vendor Roadmap Coverage | ↑ |
| Readiness Confidence | ↑ |
| Migration Leverage Realized | ↑ |

---

# Commercial Success Standard

RSK-080 succeeds when a customer can say:

> **We know where our most important quantum-related cryptographic exposures are, how ready we are to migrate them, and which modernization actions will reduce the most enterprise risk.**

That is the commercial outcome.

---

# Strategic Value

The deeper strategic value is not predicting quantum computing.

It is creating a durable enterprise capability for:

```text
CRYPTOGRAPHIC DISCOVERY
      ↓
EXPOSURE MEASUREMENT
      ↓
MIGRATION READINESS
      ↓
PRIORITIZATION
      ↓
READINESS TRACKING
```

This remains useful regardless of the exact timing of future quantum capabilities.

---

# Part 2 Feature Boundary

This Part deliberately does not repeat:

- General quantum-governance doctrine
- Generic risk controls
- Common evidence requirements
- Standard model governance
- Generic platform integrations
- Shared human-agency principles
- Common reporting architecture

Only the **customer experience, portfolio prioritization, migration intelligence, and commercial implications unique to RSK-080** are captured here.

---

# Part 2 Closing Perspective

Quantum readiness is ultimately a migration problem.

The enterprise needs to know:

```text
WHAT DO WE DEPEND ON?
      ↓
HOW EXPOSED IS IT?
      ↓
HOW CRITICAL IS IT?
      ↓
CAN WE REPLACE IT?
      ↓
HOW FAR ALONG ARE WE?
      ↓
WHAT SHOULD MOVE FIRST?
```

RSK-080 turns those questions into a portfolio the enterprise can manage.

Not because anyone knows the exact date the threat becomes material.

But because the cost of discovering and replacing cryptography across a large enterprise can itself take years.

# **MEASURE THE EXPOSURE. MEASURE THE AGILITY. MIGRATE BEFORE URGENCY BECOMES CRISIS.**

---

## End of Part 2

---

# RSK-080 — Quantum-Readiness Risk Score (Crypto-Agility Index)

## Domain 01 — Risk Management & Quantification

### Part 3 — Scoring Architecture, Cryptographic Dependency Model, Data Requirements & Technical Implementation

---

# Part 3 Purpose

Part 3 defines only the engineering capabilities unique to calculating and operationalizing the Quantum-Readiness Risk Score.

It does not restate:

- Common Vindexion data architecture
- Generic risk-scoring services
- Standard RBAC
- Shared audit telemetry
- Common model governance
- Generic evidence lineage
- Standard API conventions
- Broader quantum-governance doctrine

The unique engineering problem is:

# **HOW DO WE CONVERT CRYPTOGRAPHIC INVENTORY, QUANTUM EXPOSURE, BUSINESS CRITICALITY, AND MIGRATION READINESS INTO A RELIABLE FIRST-CLASS ENTERPRISE RISK SUB-SCORE?**

---

# Core Technical Architecture

```text
CRYPTOGRAPHIC INVENTORY
        +
SYSTEM / SERVICE DEPENDENCIES
        +
BUSINESS CRITICALITY
        +
MIGRATION READINESS
        +
DATA LONGEVITY
        +
VENDOR READINESS
        ↓
QUANTUM-READINESS SCORING ENGINE
        ↓
QUANTUM EXPOSURE SCORE
        +
CRYPTO-AGILITY INDEX™
        +
CONFIDENCE
        ↓
RSK-005 RISK DETAIL
        +
PORTFOLIO VIEW
```

The engine should consume governed enterprise data rather than create a separate cryptographic system of record.

---

# Primary Feature-Specific Objects

RSK-080 requires a compact set of specialized objects:

- Cryptographic Dependency
- Algorithm Classification
- Migration Readiness Record
- Quantum Exposure Assessment
- Crypto-Agility Assessment
- Quantum-Readiness Score
- Vendor Crypto Readiness
- Data Longevity Exposure
- Migration Initiative

These objects should reference existing systems, services, risks, vendors, and data assets.

---

# Cryptographic Dependency Object

Representative fields:

```text
DEPENDENCY ID
ALGORITHM
ALGORITHM FAMILY
KEY SIZE / PARAMETERS
PROTOCOL
USAGE TYPE
SYSTEM ID
SERVICE ID
DATA ASSET ID
VENDOR ID
BUSINESS CRITICALITY
DISCOVERY SOURCE
VERIFICATION STATE
LAST VERIFIED
```

A single system may contain multiple cryptographic dependencies.

---

# Usage Type

The platform should distinguish how cryptography is used.

Examples:

```text
KEY EXCHANGE
DIGITAL SIGNATURE
ENCRYPTION AT REST
ENCRYPTION IN TRANSIT
AUTHENTICATION
CERTIFICATE
CODE SIGNING
DATA INTEGRITY
```

Usage matters because migration impact differs materially across cryptographic functions.

---

# Algorithm Classification

The scoring engine needs a governed classification of cryptographic mechanisms.

Representative fields:

```text
ALGORITHM FAMILY
QUANTUM EXPOSURE CLASS
CURRENT ACCEPTABILITY
PQC REPLACEMENT PATH
TRANSITION STATUS
ASSESSMENT VERSION
```

The classification should remain separate from the individual system dependency.

This allows one classification update to affect all dependent assets consistently.

---

# Exposure States

A compact normalized taxonomy should be used.

```text
NOT EXPOSED
LOW
MODERATE
HIGH
CRITICAL
UNKNOWN
```

The classification should be evidence-driven.

---

# Unknown Classification

If the algorithm cannot be confidently identified:

```text
ALGORITHM
UNKNOWN

QUANTUM EXPOSURE
UNKNOWN
```

The scoring engine should not infer safety from missing information.

---

# Dependency Graph

RSK-080 requires the relationship:

```text
ALGORITHM
      ↓
IMPLEMENTATION
      ↓
SYSTEM
      ↓
BUSINESS SERVICE
      ↓
DATA
      ↓
RISK
```

Optional extension:

```text
ALGORITHM
      ↓
VENDOR
      ↓
SERVICE
      ↓
ENTERPRISE DEPENDENCY
```

This graph is essential to translating cryptographic exposure into business consequence.

---

# Many-to-Many Dependency Model

The relationship is inherently many-to-many.

Example:

```text
RSA-2048
      ↓
47 SYSTEMS
      ↓
11 CRITICAL SERVICES
      ↓
18 RISKS
```

and:

```text
DIGITAL PAYMENTS
      ↓
14 CRYPTOGRAPHIC DEPENDENCIES
      ↓
5 ALGORITHM FAMILIES
```

The architecture must support both directions.

---

# Migration Readiness Object

Representative fields:

```text
DEPENDENCY ID
CURRENT MECHANISM
TARGET MECHANISM
TARGET ARCHITECTURE
MIGRATION PHASE
OWNER
PLAN STATUS
TEST STATUS
TARGET DATE
BLOCKERS
DEPENDENCY CONTROL
LAST UPDATED
```

---

# Migration Phase

Recommended normalized states:

```text
NOT ASSESSED
DISCOVERED
TARGET IDENTIFIED
PLANNED
IN DEVELOPMENT
TESTING
READY
MIGRATED
VALIDATED
```

These states should feed directly into Crypto-Agility.

---

# Migration Blocker Types

Feature-specific blocker examples:

```text
NO TARGET ALGORITHM
LEGACY PLATFORM
VENDOR DEPENDENCY
HARDWARE LIMITATION
APPLICATION REWRITE
CERTIFICATE DEPENDENCY
INTEROPERABILITY
TESTING GAP
BUDGET / PROGRAM DELAY
```

The scoring engine should be able to distinguish readiness from execution constraints.

---

# Quantum Exposure Assessment

The Quantum Exposure Score should measure potential enterprise consequence if current cryptographic mechanisms become unsuitable.

Representative inputs:

| Input | Meaning |
|---|---|
| Algorithm Exposure | Quantum relevance of mechanism |
| Business Criticality | Importance of dependent service |
| Data Longevity | Duration confidentiality must hold |
| Dependency Concentration | Breadth of shared use |
| External Dependency | Degree of third-party control |
| Unknown Exposure | Unverified cryptographic state |

The exact production weighting should be governed separately.

---

# Quantum Exposure Calculation Concept

Conceptually:

```text
ALGORITHM EXPOSURE
        ×
BUSINESS CRITICALITY
        ×
DEPENDENCY IMPACT
        +
DATA LONGEVITY
        +
EXTERNAL CONSTRAINT
        +
UNKNOWN PENALTY
        ↓
QUANTUM EXPOSURE SCORE
```

The formula shown here defines the input structure, not a locked mathematical weighting.

---

# Crypto-Agility Assessment

Crypto-Agility should measure the organization's ability to transition.

Representative inputs:

| Input | Meaning |
|---|---|
| Inventory Coverage | How much cryptography is known |
| Target Identification | Whether replacement path exists |
| Migration Planning | Whether a plan exists |
| Testing | Whether target mechanisms are tested |
| Deployment Readiness | Whether migration can be executed |
| Vendor Readiness | External dependency preparedness |

---

# Crypto-Agility Calculation Concept

```text
INVENTORY VISIBILITY
        +
TARGET READINESS
        +
MIGRATION PLANNING
        +
TEST COMPLETION
        +
DEPLOYMENT READINESS
        +
VENDOR READINESS
        ↓
CRYPTO-AGILITY INDEX™
```

Higher values represent better readiness.

---

# Score Direction Contract

The interface and APIs must preserve clear directional semantics.

```text
QUANTUM EXPOSURE
HIGHER = WORSE
```

```text
CRYPTO-AGILITY
HIGHER = BETTER
```

This should be explicitly encoded in metadata to prevent downstream interpretation errors.

---

# Quantum-Readiness State Derivation

The product may derive a combined state.

Conceptually:

```text
HIGH EXPOSURE
+
LOW AGILITY
=
ELEVATED / CRITICAL
```

```text
HIGH EXPOSURE
+
HIGH AGILITY
=
MANAGED EXPOSURE
```

```text
LOW EXPOSURE
+
HIGH AGILITY
=
READY
```

Unknown exposure should be handled independently and should be capable of preventing a "Ready" classification.

---

# Confidence Score

The score should include confidence based on data completeness and verification.

Representative confidence inputs:

```text
INVENTORY COVERAGE
VERIFICATION RATE
DATA FRESHNESS
VENDOR EVIDENCE
MIGRATION EVIDENCE
DEPENDENCY COMPLETENESS
```

Example:

```text
CRYPTO-AGILITY
62

CONFIDENCE
71%
```

Low confidence should remain visible even when the underlying score appears acceptable.

---

# Unknown Exposure Penalty

One unique scoring requirement is explicit treatment of unknown cryptographic dependencies.

Conceptually:

```text
KNOWN SAFE
≠
UNKNOWN
```

Example:

```text
20% INVENTORY UNKNOWN
        ↓
CONFIDENCE REDUCED
        +
READINESS PENALTY
```

The precise penalty should be configurable.

---

# Data Longevity Object

Representative fields:

```text
DATA ASSET ID
DATA CLASS
SENSITIVITY
CONFIDENTIALITY HORIZON
DEPENDENT CRYPTOGRAPHY
QUANTUM EXPOSURE
BUSINESS OWNER
```

This enables harvest-now-decrypt-later prioritization.

---

# Confidentiality Horizon

Example normalized values:

```text
< 1 YEAR
1–3 YEARS
3–7 YEARS
7–10 YEARS
10+ YEARS
INDEFINITE
```

Longer confidentiality horizons should increase priority where quantum-exposed cryptography protects the data.

---

# Vendor Crypto Readiness Object

Representative fields:

```text
VENDOR ID
DEPENDENT SERVICE
CRYPTOGRAPHIC DEPENDENCY
VENDOR ROADMAP STATUS
TARGET TECHNOLOGY
MIGRATION DATE
CUSTOMER CONTROL LEVEL
EVIDENCE DATE
```

---

# Customer Control Level

Recommended classification:

```text
FULL
SHARED
LIMITED
NONE
UNKNOWN
```

A critical dependency with low customer control should be surfaced prominently.

---

# Migration Initiative Object

Representative fields:

```text
INITIATIVE ID
TARGET DEPENDENCIES
SYSTEMS AFFECTED
SERVICES AFFECTED
RISKS AFFECTED
OWNER
PHASE
TARGET DATE
BLOCKERS
EXPECTED EXPOSURE REDUCTION
```

This connects the risk score to remediation planning.

---

# Migration Leverage™ Calculation

Migration Leverage™ should estimate the breadth of exposure reduction produced by one migration.

Representative factors:

```text
NUMBER OF SYSTEMS
        +
CRITICAL SERVICES
        +
RISKS REDUCED
        +
EXPOSURE SEVERITY
```

Example:

```text
IDENTITY CRYPTO UPGRADE

31 SYSTEMS
8 CRITICAL SERVICES
12 RISKS

MIGRATION LEVERAGE
HIGH
```

It should remain a prioritization measure, not part of the canonical Crypto-Agility score.

---

# Scoring Granularity

The capability should support scoring at multiple levels.

```text
DEPENDENCY
      ↓
SYSTEM
      ↓
SERVICE
      ↓
RISK
      ↓
BUSINESS UNIT
      ↓
ENTERPRISE
```

Aggregation should preserve the ability to drill back to source dependencies.

---

# Risk-Level Score

RSK-080's canonical product location remains the individual risk.

Example:

```text
RSK-2841

QUANTUM EXPOSURE
88

CRYPTO-AGILITY
54

READINESS
ELEVATED
```

This is the primary acceptance-level implementation.

---

# Service-Level Aggregation

A critical service may inherit exposure from multiple systems.

Example:

```text
DIGITAL PAYMENTS

14 DEPENDENCIES
5 ALGORITHM FAMILIES
6 HIGH EXPOSURE
3 UNKNOWN

QUANTUM EXPOSURE
88

CRYPTO-AGILITY
54
```

The service score should be based on its underlying dependency portfolio.

---

# Enterprise Aggregation

Enterprise roll-up should summarize:

```text
ENTERPRISE CRYPTO-AGILITY
67

CRITICAL SERVICES EXPOSED
14

HIGH EXPOSURE + LOW AGILITY
6

UNKNOWN CRITICAL DEPENDENCIES
11
```

This is a portfolio projection, not a separate calculation framework.

---

# Change Propagation

When an underlying dependency changes:

```text
MIGRATION PHASE
PLANNED → TESTING
```

the change should propagate:

```text
DEPENDENCY
      ↓
SYSTEM
      ↓
SERVICE
      ↓
RISK
      ↓
PORTFOLIO SCORE
```

Only affected aggregates need recalculation.

---

# Score Recalculation Triggers

Feature-specific triggers include:

```text
NEW CRYPTOGRAPHIC DEPENDENCY
ALGORITHM CLASSIFICATION CHANGE
MIGRATION PHASE CHANGE
NEW VENDOR ROADMAP
BUSINESS CRITICALITY CHANGE
DATA LONGEVITY CHANGE
DEPENDENCY VERIFIED
DEPENDENCY REMOVED
```

These events should drive targeted recalculation.

---

# Score Versioning

RSK-080 should expose:

```text
SCORE VERSION
CLASSIFICATION VERSION
INPUT SNAPSHOT TIME
```

Example:

```text
CRYPTO-AGILITY
62

SCORE VERSION
1.3

AS OF
2026-08-20 17:42 UTC
```

This is especially important as cryptographic threat classifications evolve.

---

# Historical Score Movement

The system should retain:

```text
DATE
SCORE
INPUT CHANGE
PRIMARY DRIVER
```

Example:

| Date | Agility | Driver |
|---|---:|---|
| Q1 | 44 | Baseline |
| Q2 | 49 | Inventory coverage |
| Q3 | 57 | Migration planning |
| Current | 62 | Testing progress |

This enables explainable readiness trends.

---

# Score Explainability Object

For each material score change:

```text
PRIOR SCORE
CURRENT SCORE
DELTA
CHANGED INPUTS
PRIMARY DRIVER
AFFECTED DEPENDENCIES
```

Example:

```text
54 → 62

PRIMARY DRIVER
6 critical systems moved from Planned to Testing
```

This is the unique explainability needed for RSK-080.

---

# Inventory Integration

RSK-080 should integrate with existing asset and architecture sources rather than manually duplicate all cryptographic discovery.

Expected source categories include:

```text
CMDB
APPLICATION INVENTORY
CERTIFICATE INVENTORY
CODE / LIBRARY SCANS
NETWORK CONFIGURATION
CLOUD CONFIGURATION
VENDOR ASSESSMENTS
ARCHITECTURE RECORDS
```

The feature consumes normalized dependency records from those sources.

---

# Discovery Confidence

Each dependency should carry a discovery state.

```text
DISCOVERED
VERIFIED
INFERRED
UNKNOWN
```

Example:

```text
RSA-2048
SYSTEM A

SOURCE
Certificate inventory

STATE
Verified
```

This can influence readiness confidence.

---

# Duplicate Resolution

Multiple discovery tools may identify the same dependency.

Example:

```text
CERTIFICATE SCANNER
RSA-2048

CMDB
RSA-2048

APPLICATION SCAN
RSA-2048
```

These should resolve to one canonical dependency relationship where appropriate.

The scoring engine should not triple-count the exposure.

---

# Dependency Lifecycle

```text
DISCOVERED
      ↓
VERIFIED
      ↓
ASSESSED
      ↓
MIGRATION PLANNED
      ↓
MIGRATED
      ↓
VALIDATED
      ↓
RETIRED
```

This is the feature-specific lifecycle that drives readiness.

---

# Post-Migration Behavior

When a dependency is migrated and validated:

```text
CURRENT
RSA-2048

        ↓

TARGET
PQC-APPROVED MECHANISM

        ↓

MIGRATED + VALIDATED
```

Expected impact:

```text
QUANTUM EXPOSURE
↓
```

and potentially:

```text
CRYPTO-AGILITY
↑
```

The relationship between the remediation and score movement should be visible.

---

# Hybrid Migration State

During transition, systems may support both classical and post-quantum mechanisms.

Example:

```text
LEGACY
RSA

+
TARGET
PQC

STATE
HYBRID
```

The assessment should distinguish hybrid migration from completed retirement of the exposed mechanism.

---

# Cryptographic Concentration Engine

RSK-080 should identify shared dependencies.

Example:

```text
ALGORITHM / LIBRARY X
      ↓
47 SYSTEMS
      ↓
11 CRITICAL SERVICES
```

The engine should surface:

- Concentration count
- Critical-service count
- Risk count
- Migration status

This supports Migration Leverage™.

---

# Concentration Object

Representative fields:

```text
CRYPTO OBJECT
DEPENDENT SYSTEMS
CRITICAL SERVICES
BUSINESS UNITS
RISKS
MIGRATION INITIATIVES
CONCENTRATION SEVERITY
```

---

# Technical User Experience — Risk Detail

The RSK-005 component should expose:

```text
QUANTUM READINESS
────────────────────

EXPOSURE
88 — HIGH

CRYPTO-AGILITY
54 — LOW

CONFIDENCE
86%

PRIMARY DRIVER
RSA dependencies in Digital Payments

VIEW DEPENDENCIES
VIEW MIGRATION
```

This is the canonical technical UI requirement.

---

# Technical User Experience — Dependency Drawer

Selecting:

```text
VIEW DEPENDENCIES
```

should show:

| Algorithm | System | Criticality | Exposure | Migration |
|---|---|---|---|---|
| RSA-2048 | Payment Gateway | Critical | High | Testing |
| RSA-2048 | Auth Service | Critical | High | Planned |
| ECC | Mobile Gateway | High | High | Target Identified |
| Unknown | Legacy API | High | Unknown | Not Assessed |

This gives direct score traceability.

---

# Technical User Experience — Migration Drawer

Selecting:

```text
VIEW MIGRATION
```

should show:

```text
5 READY
6 TESTING
8 PLANNED
3 NOT ASSESSED
```

with blockers and target dates.

---

# API Surface — Unique Endpoints

Representative feature-specific endpoints:

```text
GET /risks/{id}/quantum-readiness

GET /risks/{id}/crypto-dependencies

GET /crypto/dependencies/{id}

GET /crypto/readiness/portfolio

GET /crypto/migration-initiatives

GET /crypto/concentrations
```

No duplicate generic risk APIs should be introduced.

---

# Example Risk Response

```json
{
  "risk_id": "RSK-2841",
  "quantum_exposure": 88,
  "crypto_agility": 54,
  "readiness_state": "ELEVATED",
  "confidence": 0.86,
  "critical_dependencies": 14,
  "unknown_dependencies": 3,
  "score_version": "1.3"
}
```

---

# Example Dependency Response

```json
{
  "dependency_id": "CRY-4811",
  "algorithm": "RSA-2048",
  "usage": "KEY_EXCHANGE",
  "system_id": "SYS-441",
  "service_id": "SVC-DIGPAY",
  "business_criticality": "CRITICAL",
  "quantum_exposure": "HIGH",
  "migration_phase": "TESTING"
}
```

---

# Portfolio Query

Representative query:

```text
SHOW
HIGH EXPOSURE
+
LOW CRYPTO-AGILITY
+
CRITICAL SERVICES
```

Expected:

```text
6 SERVICES
```

ranked for remediation attention.

---

# Performance Consideration

The score should not require expensive real-time cryptographic scanning during every risk-detail request.

Preferred model:

```text
SOURCE DISCOVERY
      ↓
NORMALIZED DEPENDENCIES
      ↓
EVENT-DRIVEN SCORE UPDATE
      ↓
READ-OPTIMIZED SCORE
```

This keeps the user experience responsive.

---

# Large Enterprise Scale

A customer may have:

```text
100,000+ SYSTEMS
MILLIONS OF CRYPTOGRAPHIC DEPENDENCIES
```

Therefore:

- Store dependency relationships efficiently
- Recalculate affected branches only
- Precompute major portfolio aggregates
- Avoid whole-enterprise recalculation for every migration update

---

# Data Quality Metrics

Unique quality measures should include:

```text
INVENTORY COVERAGE
VERIFICATION RATE
UNKNOWN ALGORITHM RATE
STALE MIGRATION RECORD RATE
VENDOR ROADMAP COVERAGE
DEPENDENCY LINKAGE RATE
```

These directly affect score confidence.

---

# Score Quality Dashboard

Example:

```text
INVENTORY COVERAGE
80%

VERIFIED
91%

UNKNOWN ALGORITHMS
4.2%

STALE MIGRATION RECORDS
6.1%

VENDOR ROADMAP COVERAGE
61%

READINESS CONFIDENCE
84%
```

This allows users to assess the reliability of the quantum-readiness posture.

---

# Validation Strategy

RSK-080 should be validated primarily for:

### Input Integrity

Does the score consume the correct dependency and migration information?

### Directionality

Does increasing readiness improve the Crypto-Agility score?

### Exposure Sensitivity

Do critical quantum-exposed dependencies increase exposure appropriately?

### Unknown Handling

Does incomplete inventory reduce confidence and avoid false safety?

### Aggregation

Do risk and portfolio scores trace correctly to source dependencies?

---

# Synthetic Validation Example

Initial state:

```text
CRITICAL SERVICE
Digital Payments

HIGH-EXPOSURE DEPENDENCIES
14

MIGRATION READY
5

UNKNOWN
3

CRYPTO-AGILITY
54
```

Update:

```text
5 ADDITIONAL DEPENDENCIES
MOVE TO TESTING / READY
```

Expected:

```text
CRYPTO-AGILITY
INCREASES
```

with explicit contribution trace.

---

# Canonical Acceptance Test — Engineering

Input:

```text
ALGORITHM INVENTORY
+
MIGRATION READINESS
```

System computes:

```text
QUANTUM-READINESS SUB-SCORE
```

Then exposes it on:

```text
RSK-005 RISK DETAIL VIEW
```

as a distinct structured element rather than narrative text.

This is the source-defined RSK-505 requirement. :contentReference[oaicite:0]{index=0}

---

# Failure Conditions

RSK-080 should be considered technically deficient if:

- Unknown inventory is treated as safe
- Score movement cannot be attributed to inputs
- Risk Detail requires a separate quantum application
- Migration state does not affect agility
- Critical-service exposure is indistinguishable from low-criticality exposure
- Duplicate discovery records inflate exposure
- Vendor-controlled dependencies appear internally remediable
- Historical score changes cannot be reconstructed

---

# Recommended Build Sequence

## Phase 1 — Dependency + Score

Build:

```text
ALGORITHM INVENTORY
      ↓
DEPENDENCY LINKAGE
      ↓
EXPOSURE
      +
AGILITY
      ↓
RISK DETAIL
```

This satisfies the canonical requirement.

---

## Phase 2 — Migration Intelligence

Add:

- Migration records
- Blockers
- Target dates
- Readiness trend
- Migration Leverage™

---

## Phase 3 — Portfolio Intelligence

Add:

- Service aggregation
- Concentration analysis
- Unknown exposure queue
- Executive prioritization

---

## Phase 4 — Advanced Readiness

Potential extensions:

- Long-lived data prioritization
- Vendor readiness integration
- Migration efficiency
- Scenario sensitivity

---

# Unique Engineering MOAT

The durable differentiation is not the existence of a quantum-readiness score.

It is the enterprise linkage:

```text
CRYPTOGRAPHIC MECHANISM
        ↓
SYSTEM
        ↓
SERVICE
        ↓
DATA
        ↓
BUSINESS CRITICALITY
        ↓
MIGRATION STATE
        ↓
ENTERPRISE RISK
```

That allows quantum readiness to become decision-quality enterprise intelligence rather than a technical inventory exercise.

---

# Part 3 Closing Perspective

The technical challenge is not assigning a number to quantum readiness.

The challenge is making that number meaningful.

It must trace to actual cryptographic dependencies.

Those dependencies must trace to real systems.

Those systems must trace to critical services and sensitive data.

Migration readiness must reflect what can actually be changed.

Unknown inventory must remain visible.

Vendor constraints must remain explicit.

And when remediation occurs, the score must move for a reason that the enterprise can reconstruct.

That is what turns a future technology concern into a usable risk capability.

# **DISCOVER THE DEPENDENCY. TRACE THE CONSEQUENCE. MEASURE THE AGILITY. LET REAL MIGRATION CHANGE THE RISK.**

---

## End of Part 3

---

# RSK-080 — Quantum-Readiness Risk Score (Crypto-Agility Index)

## Domain 01 — Risk Management & Quantification

### Part 4 — Commercialization, Strategic Positioning, Success Measures & Visualization Specification

---

# Part 4 Purpose

Part 4 defines only the commercialization, executive positioning, success measures, and visualization content unique to RSK-080.

It does not repeat:

- General quantum-governance doctrine
- Standard platform governance
- Common security controls
- Generic risk architecture
- Shared visualization mechanics

The unique commercial proposition is:

# **MAKE QUANTUM READINESS VISIBLE AS ENTERPRISE RISK BEFORE THE MIGRATION WINDOW BECOMES URGENT.**

---

# Commercialization

RSK-080 should be positioned as:

# **QUANTUM-READINESS RISK INTELLIGENCE**

The capability turns cryptographic modernization into a measurable enterprise-risk posture.

Commercial flow:

```text
CRYPTOGRAPHIC DEPENDENCIES
      ↓
QUANTUM EXPOSURE
      +
CRYPTO-AGILITY
      ↓
BUSINESS-SERVICE PRIORITY
      ↓
MIGRATION ACTION
      ↓
READINESS IMPROVEMENT
```

The value is not predicting when quantum computing will become cryptographically relevant.

The value is knowing:

# **WHETHER THE ENTERPRISE CAN MIGRATE BEFORE IT HAS TO.**

---

# Primary Customer Outcomes

Customers should be able to:

- Quantify quantum-related cryptographic exposure
- Measure crypto-agility
- Identify unknown cryptographic dependencies
- Prioritize high-exposure / low-agility services
- Link cryptographic dependencies to critical business services
- Track migration progress
- Identify high-leverage migration initiatives
- Surface vendor-controlled readiness constraints
- Report readiness progress to executive stakeholders

---

# Executive Operating View

Recommended metrics:

| Metric | Current |
|---|---:|
| Enterprise Crypto-Agility | **67 / 100** |
| High-Exposure Services | **14** |
| High Exposure + Low Agility | **6** |
| Inventory Coverage | **80%** |
| Migration-Ready | **37%** |
| Unknown Critical Dependencies | **11** |

### Quantum-Readiness Posture

# **ELEVATED**

### Readiness Confidence

# **84%**

---

# Hero Risk

## Digital Payments Cryptographic Dependency

```text
ENTERPRISE RISK
82 / 100 — HIGH

QUANTUM EXPOSURE
88 / 100 — HIGH

CRYPTO-AGILITY INDEX™
54 / 100 — LOW

QUANTUM-READINESS POSTURE
ELEVATED
```

### Supporting Exposure

```text
CRITICAL SYSTEMS
6

QUANTUM-EXPOSED DEPENDENCIES
14

MIGRATION READY
5

UNKNOWN
3
```

### Primary Driver

# **RSA-2048 remains embedded across critical payment authorization services.**

---

# Core Strategic Message

The visualization should prominently state:

# **HIGH QUANTUM EXPOSURE IS MANAGEABLE ONLY IF THE ENTERPRISE HAS HIGH CRYPTO-AGILITY.**

This is the defining RSK-080 relationship.

---

# Exposure vs Agility Matrix

Use the 2×2 prioritization model:

```text
                         HIGH AGILITY
                              ↑

LOW EXPOSURE            STRONG
HIGH AGILITY             Maintain

HIGH EXPOSURE           MANAGED EXPOSURE
HIGH AGILITY             Monitor / Continue Migration

------------------------------------------------→ EXPOSURE

LOW EXPOSURE            READINESS GAP
LOW AGILITY              Improve Agility

HIGH EXPOSURE           PRIORITY EXPOSURE
LOW AGILITY              Accelerate Migration
```

Highlight:

# **DIGITAL PAYMENTS — HIGH EXPOSURE / LOW AGILITY**

---

# Portfolio Priority Panel

| Business Service | Exposure | Agility | State |
|---|---:|---:|---|
| Digital Payments | **88** | **54** | Elevated |
| Identity | 82 | 71 | Watch |
| Treasury | 76 | 43 | Elevated |
| HR Platforms | 41 | 78 | Strong |
| Collaboration | 37 | 81 | Strong |

This should be one of the main decision panels.

---

# Cryptographic Inventory Panel

Show:

```text
IN-SCOPE SYSTEMS
2,480

VERIFIED
1,984

UNKNOWN
496

INVENTORY COVERAGE
80%
```

Supporting message:

# **UNKNOWN CRYPTOGRAPHY IS UNRESOLVED RISK — NOT LOW RISK.**

---

# Dependency Trace Panel

Show:

```text
RSA-2048
      ↓
PAYMENT GATEWAY
      ↓
DIGITAL PAYMENTS
      ↓
CUSTOMER TRANSACTIONS
      ↓
RSK-2841
```

This panel should visually translate cryptographic exposure into business consequence.

---

# Migration Readiness Panel

Example:

```text
CURRENT
RSA-2048

TARGET
PQC-APPROVED ARCHITECTURE

PHASE
TESTING

OWNER
Payments Engineering

TARGET
Q2 2028

BLOCKERS
2
```

Footer:

# **READINESS IS ABOUT THE ABILITY TO MIGRATE — NOT JUST KNOWING THE EXPOSURE EXISTS.**

---

# Migration Leverage™ Panel

## Identity Cryptography Upgrade

```text
SYSTEMS AFFECTED
31

CRITICAL SERVICES
8

RISKS IMPROVED
12
```

### Migration Leverage™

# **HIGH**

Supporting statement:

# **ONE MIGRATION CAN REDUCE EXPOSURE ACROSS MULTIPLE ENTERPRISE RISKS.**

---

# Long-Lived Data Panel

Show:

```text
LONG-LIVED SENSITIVE DATA
23 DATA CLASSES

QUANTUM-EXPOSED
11

CRITICAL
4
```

Example:

```text
STRATEGIC M&A
10+ YEARS
HIGH EXPOSURE
```

Footer:

# **DATA THAT MUST REMAIN SECRET FOR YEARS MAY REQUIRE EARLIER MIGRATION PRIORITY.**

---

# Third-Party Constraint Panel

Example:

```text
IDENTITY PLATFORM

QUANTUM EXPOSURE
HIGH

VENDOR CONTROL
HIGH

CUSTOMER MIGRATION CONTROL
LIMITED

VENDOR PQC ROADMAP
UNCONFIRMED
```

### State

# **EXTERNAL READINESS CONSTRAINT**

This shows that not all crypto-agility is under direct enterprise control.

---

# Readiness Trend Panel

Show:

```text
CRYPTO-AGILITY

Q1       44
Q2       49
Q3       57
CURRENT  62
```

Supporting drivers:

```text
INVENTORY COVERAGE
61% → 80%

MIGRATION READY
18% → 37%

UNKNOWN DEPENDENCIES
42 → 23
```

Message:

# **SHOW WHY READINESS MOVED.**

---

# Target State Panel

```text
CURRENT
62

TARGET
85

TARGET DATE
Q4 2028

READINESS GAP
23
```

Breakdown:

```text
INVENTORY
80 → 98

MIGRATION READINESS
54 → 85

VENDOR ROADMAP COVERAGE
61 → 95
```

This converts the readiness score into an operating target.

---

# Unknown Exposure Panel

Show three states clearly:

```text
KNOWN + ASSESSED
1,984

KNOWN + NOT READY
217

UNKNOWN
496
```

The visual should avoid any implication that unknown assets are safe.

---

# Executive Attention Queue

Recommended:

```text
1. DIGITAL PAYMENTS
   Exposure 88 / Agility 54

2. TREASURY
   Exposure 76 / Agility 43

3. IDENTITY VENDOR
   PQC Roadmap Unconfirmed

4. LONG-LIVED DATA
   11 exposed data classes

5. UNKNOWN CRYPTOGRAPHY
   496 systems
```

This gives the executive audience a clear action path.

---

# AI Copilot Intelligence Panel

Example:

### Question

> What should we migrate first?

### Vindexion

> The Identity Cryptography Upgrade has the highest Migration Leverage™. It affects 31 systems, eight critical services, and twelve active risks. Digital Payments remains the most urgent business-service exposure because its quantum exposure is 88 while crypto-agility is 54.

This is the most commercially useful AI interaction.

---

# Buyer Narrative — CISO

# **KNOW WHERE QUANTUM-RELATED CRYPTOGRAPHIC EXPOSURE IS CONCENTRATED AND WHICH MIGRATIONS REDUCE THE MOST RISK.**

Primary value:

- Visibility
- Prioritization
- Migration sequencing

---

# Buyer Narrative — CRO

# **BRING QUANTUM READINESS INTO THE SAME ENTERPRISE-RISK LANGUAGE USED TO GOVERN EVERY OTHER MATERIAL EXPOSURE.**

Primary value:

- Portfolio comparability
- Executive prioritization
- Risk trend visibility

---

# Buyer Narrative — CIO / Enterprise Architecture

# **TURN CRYPTOGRAPHIC MODERNIZATION INTO A RISK-PRIORITIZED TRANSFORMATION ROADMAP.**

Primary value:

- Dependency linkage
- Target architecture
- Migration progress
- Shared-service leverage

---

# Buyer Narrative — Board Risk Committee

# **KNOW WHETHER CRITICAL BUSINESS SERVICES CAN MIGRATE BEFORE THE CRYPTOGRAPHIC THREAT BECOMES URGENT.**

Board-level view:

```text
EXPOSURE
READINESS
CRITICAL SERVICES
TREND
TARGET
```

Avoid excessive algorithm-level detail at this level.

---

# Commercial Differentiation

Traditional quantum-readiness assessment:

```text
QUESTIONNAIRE
      ↓
MATURITY SCORE
      ↓
REPORT
```

RSK-080:

```text
ACTUAL CRYPTOGRAPHIC DEPENDENCIES
      +
BUSINESS CRITICALITY
      +
MIGRATION STATE
      +
DATA LONGEVITY
      +
VENDOR CONTROL
      ↓
QUANTUM-READINESS RISK SCORE
      ↓
PORTFOLIO PRIORITY
```

The distinction is:

# **READINESS IS GROUNDED IN THE REAL ENTERPRISE ESTATE.**

---

# Commercial Packaging

Potential packaging:

### Quantum Readiness Core

- Crypto-Agility Index™
- Quantum Exposure
- Risk Detail integration

### Quantum Readiness Portfolio

- Enterprise roll-up
- Concentration intelligence
- Unknown exposure queue
- Migration leverage

### Quantum Readiness Advanced

Potential future additions:

- Long-lived data prioritization
- Vendor readiness
- Migration economics
- Scenario modeling

This is a packaging option, not a fixed commercial commitment.

---

# Strategic Role

RSK-080 becomes the risk-layer measurement capability supporting broader Quantum-Readiness Governance.

Conceptually:

```text
CRYPTOGRAPHIC REALITY
      ↓
RSK-080
RISK QUANTIFICATION
      ↓
CONTROL / REGULATORY / AUDIT / TPR
QUANTUM-READINESS CAPABILITIES
```

The canonical source explicitly positions the feature as part of the Quantum-Readiness Governance whitespace category. :contentReference[oaicite:0]{index=0}

---

# Strategic MOAT

The strongest differentiation is the accumulated enterprise relationship model connecting:

```text
ALGORITHM
      +
SYSTEM
      +
SERVICE
      +
DATA
      +
VENDOR
      +
MIGRATION STATE
      +
RISK
```

Over time, Vindexion can understand:

- Which cryptographic dependencies create the largest concentration
- Which migration programs reduce the most risk
- Which vendor dependencies constrain readiness
- Which unknown areas persist
- Which business services remain chronically difficult to migrate

This creates:

# **CRYPTOGRAPHIC TRANSITION INTELLIGENCE**

---

# Product Intelligence Score™

| Dimension | Score |
|---|---:|
| Customer Value | 9.7 |
| Risk Integration | 9.8 |
| Frontier Readiness | 10.0 |
| Competitive Differentiation | 9.9 |
| Executive Visibility | 9.6 |
| Strategic Importance | 10.0 |

### Overall Product Intelligence Score™

# **9.83 / 10**

---

# Success Measures

Primary measures:

| Measure | Desired Direction |
|---|---|
| Crypto-Agility Index™ | ↑ |
| Quantum Exposure | ↓ |
| Inventory Coverage | ↑ |
| Unknown Dependency Rate | ↓ |
| Migration-Ready Percentage | ↑ |
| High Exposure + Low Agility | ↓ |
| Vendor Roadmap Coverage | ↑ |
| Readiness Confidence | ↑ |

---

# Canonical Success Standard

RSK-080 must satisfy the source-defined requirement:

```text
ALGORITHM INVENTORY
+
MIGRATION READINESS
      ↓
DEDICATED QUANTUM-READINESS SCORE
      ↓
VISIBLE ON RSK-005
RISK DETAIL VIEW
```

The score must remain a distinct structured element rather than narrative commentary. :contentReference[oaicite:1]{index=1}

---

# Commercial Success Standard

RSK-080 succeeds when a customer can say:

> **We know where our quantum-related cryptographic exposure is concentrated, how ready we are to migrate, and which actions will reduce the most enterprise risk.**

That is the commercial threshold.

---

# Visualization Specification

## Locked Visual Architecture

Use the established Odyssey RSK executive command-center format.

Only RSK-080-specific visualization content is defined below.

---

# Visualization Header

## RSK-080

# QUANTUM-READINESS RISK SCORE

### **Measure the Exposure. Measure the Agility. Migrate Before Urgency Becomes Crisis.**

Supporting statement:

> Quantify quantum-related cryptographic exposure and crypto-agility as a first-class enterprise risk posture grounded in real systems, critical services, data longevity, vendor dependencies, and migration readiness.

---

# Top KPI Strip

Recommended six measures:

```text
67 / 100              14                  6
ENTERPRISE            HIGH-EXPOSURE       HIGH EXPOSURE
CRYPTO-AGILITY        SERVICES            + LOW AGILITY

80%                   37%                 11
INVENTORY             MIGRATION           UNKNOWN CRITICAL
COVERAGE              READY               DEPENDENCIES
```

---

# Hero Center

```text
DIGITAL PAYMENTS

ENTERPRISE RISK
82

QUANTUM EXPOSURE
88 — HIGH

CRYPTO-AGILITY
54 — LOW

READINESS
ELEVATED
```

Below:

```text
14 EXPOSED DEPENDENCIES
6 CRITICAL SYSTEMS
5 MIGRATION READY
3 UNKNOWN
```

---

# Hero Relationship Flow

```text
RSA-2048
      ↓
PAYMENT GATEWAY
      ↓
DIGITAL PAYMENTS
      ↓
CUSTOMER TRANSACTIONS
      ↓
QUANTUM-READINESS RISK
```

This should be visually prominent.

---

# Exposure / Agility Matrix

Highlight:

```text
HIGH EXPOSURE
+
LOW AGILITY
=
PRIORITY EXPOSURE
```

Place Digital Payments in this quadrant.

---

# Migration Leverage Panel

```text
IDENTITY CRYPTOGRAPHY UPGRADE

31 SYSTEMS
8 CRITICAL SERVICES
12 RISKS IMPROVED

MIGRATION LEVERAGE™
HIGH
```

---

# Readiness Trend Panel

```text
44 → 49 → 57 → 62
```

with:

```text
INVENTORY
61% → 80%

MIGRATION READY
18% → 37%
```

---

# Long-Lived Data Panel

```text
23 LONG-LIVED DATA CLASSES

11 QUANTUM-EXPOSED

4 CRITICAL
```

---

# Vendor Constraint Panel

```text
IDENTITY PLATFORM

EXPOSURE
HIGH

CUSTOMER CONTROL
LIMITED

VENDOR ROADMAP
UNCONFIRMED
```

---

# Right Intelligence Rail

## QUANTUM READINESS

### ENTERPRISE CRYPTO-AGILITY

**67 / 100**

### HIGH-EXPOSURE SERVICES

**14**

### HIGH EXPOSURE + LOW AGILITY

**6**

### INVENTORY COVERAGE

**80%**

### MIGRATION READY

**37%**

### UNKNOWN CRITICAL DEPENDENCIES

**11**

### READINESS CONFIDENCE

**84%**

### PRIMARY INSIGHT

Digital Payments remains the highest-priority quantum-readiness exposure because critical RSA dependencies remain widespread while migration readiness is only 54.

---

# Project Information Rail

### Feature

**RSK-080**

### Canonical Source

**Claude RSK-505**

### Capability

**Quantum-Readiness Risk Score / Crypto-Agility Index**

### Generation

**Gen 5 — Moonshot / Frontier**

### Primary Dependencies

**RSK-001 / RSK-005**

### Strategic Category

**Quantum-Readiness Governance**

### Product Intelligence Score™

# **9.83 / 10**

---

# Bottom Architecture Band

Keep compact:

```text
CRYPTO INVENTORY
      ↓
DEPENDENCY MODEL
      ↓
QUANTUM EXPOSURE
      +
MIGRATION READINESS
      ↓
CRYPTO-AGILITY INDEX™
      ↓
RISK DETAIL
      ↓
PORTFOLIO PRIORITY
```

---

# Capability Evolution Footer

```text
CRYPTO
INVENTORY
   →
EXPOSURE
MAPPING
   →
CRYPTO-
AGILITY
   →
PORTFOLIO
READINESS
   →
MIGRATION
INTELLIGENCE
   →
QUANTUM-
READY ENTERPRISE
```

Highlight:

# **CRYPTO-AGILITY INDEX™**

---

# Investor Narrative

Quantum risk is often framed as a distant technology problem.

But cryptographic migration is already an enterprise architecture problem.

Large organizations may have thousands of applications, millions of dependencies, long-lived sensitive data, legacy systems, embedded vendor cryptography, and modernization programs that take years to complete.

That changes the strategic question.

It is less useful to ask:

> When will quantum computing break today's cryptography?

The more practical enterprise question is:

> **How long would it take us to replace the cryptography we depend on if we needed to?**

RSK-080 makes that question measurable.

```text
DEPENDENCY
      ↓
EXPOSURE
      ↓
AGILITY
      ↓
PRIORITY
      ↓
MIGRATION
```

That is how future uncertainty becomes current governance.

---

# Closing Perspective

The greatest quantum-readiness risk may not be the cryptographic algorithm itself.

It may be discovering too late that the algorithm is embedded everywhere.

That critical services depend on it.

That long-lived data remains exposed.

That vendors control part of the migration path.

That testing takes longer than expected.

And that the organization does not have enough time left to change.

RSK-080 creates visibility before urgency.

It shows what the enterprise depends on.

How exposed those dependencies are.

How ready they are to move.

Where unknowns remain.

And which migrations will create the largest reduction in enterprise risk.

# **KNOW THE CRYPTOGRAPHY. MEASURE THE EXPOSURE. BUILD THE AGILITY. MIGRATE BEFORE THE DEADLINE BECOMES THE CRISIS.**

---

## End of Part 4

## RSK-080 Feature Passport — COMPLETE

**Parts 1–4:** Complete  
**Canonical Mapping:** Claude RSK-505 — Quantum-Readiness Risk Score (Crypto-Agility Index)  
**Generation:** Gen 5 — Moonshot / Frontier  
**Primary Dependencies:** RSK-001, RSK-005  
**Strategic Category:** Quantum-Readiness Governance  
**Unique Acceptance Criterion:** Defined algorithm-inventory and migration-readiness inputs produce a distinct quantum-readiness sub-score visible on RSK-005 Risk Detail View  
---
