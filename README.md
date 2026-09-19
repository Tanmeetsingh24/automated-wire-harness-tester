# Automated wire-harness tester

**Electronics Engineer, [Cognitive Advantage](https://www.linkedin.com/company/cognitive-advantage-pty-ltd/)**

> **Public case study only.** No proprietary source, schematics, or customer-confidential detail.  
> Summary of work by Tanmeet Singh Sachdeva for portfolio purposes.

---

## Problem statement

Wire-harness validation was a **repeatable bottleneck**: manual checks were slow, inconsistent, and gave operators little structured fault data before integration.

## High-level impact

1. **Up to ~90% reduction** in validation time vs the previous manual process.
2. **Automated pass/fail** with actionable fault reporting for operators.
3. **Modular rig** adaptable to different harness configurations without rebuilding the whole tester.

## My contribution

1. Architected and built the **modular test rig** end-to-end: fixture design, measurement front-end, test sequencing, and operator workflow.
2. Defined **what to test, in what order**, and how results were presented for rework.
3. Integrated **electronics + test logic + practical shop-floor use** so the tool was adopted as a recurring step, not a one-off demo.

## Tech and design choices

| Choice | Why |
| --- | --- |
| **Modular fixtures / adapters** | Harness variants differed by connector and pinout; modularity beat a single fixed bed. |
| **Automated sequencing** (vs fully manual DMM walk-through) | Repeatability and speed; same script every build. |
| **Explicit fault mapping** | Operators needed *where* it failed, not just “fail”. drove UI/report design. |
| **Bench instrument integration** | Used appropriate continuity/isolation measurements for the harness class vs over-building a custom ATE from scratch. |

## Lesson

**Intermittent failures** traced to **connector contact resistance** on worn fixtures. not the harness under test. Fix: standardized modular adapters, defined mate cycles, and added a quick fixture self-check before each run.

---

**Context:** [Portfolio](https://tanmeetsingh24.github.io), hardware verification and test automation.
