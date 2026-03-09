# Rethinking how we evaluate security agents for real-world use - Mudita Khurana (Airbnb)
**Stage 1 | March 4, 2026 | 12:10-12:25**

## Executive Summary
Mudita Khurana challenges the current paradigm of evaluating security agents based solely on outcome benchmarks, arguing that this approach obscures critical factors like explainability and reliability. She introduces CLASP, a capability-centric evaluation framework designed to assess underlying agent skills—such as reasoning, memory, planning, and tool use—on a spectrum from brittle heuristics to adaptive execution. Because security workflows require context to be maintained across multiple stages (e.g., finding, exploiting, and patching), superficial pattern matching leads to end-to-end failures. Khurana's research reveals that different security tasks prioritize distinct capabilities; for example, broad planning is more vital than deep reasoning for enumeration tasks. She advocates for baking observability into agent workflows and utilizing LLM-as-a-judge pipelines or evidence-centered benchmarks to systematically measure and improve agent capabilities.

## Key Points
- Traditional outcome-only agent benchmarks fail to measure explainability, reliability, and the underlying skills needed for complex security workflows.
- Security tasks require agents to carry context across stages (e.g., finding, exploiting, patching, and validating) to achieve end-to-end success.
- CLASP is a framework providing rubrics for six agentic capabilities, scoring agents from brittle to adaptive execution.
- Different security tasks prioritize different capabilities; e.g., reconnaissance agents benefit more from broad planning than deep reasoning.
- Implementation involves baking observability into workflows, then evaluating agents using LLM-as-a-judge pipelines or evidence-centered test scenarios.

## Notable Quotes
> "Agent evaluation today is rooted in very narrow outcome only scoring, which essentially hides explainability and reliability."
> "Don't evaluate on isolated narrow outcomes. Dig deeper into the how of these agents and a capability-centric grading system like CLASP can help you create more reliable, more explainable, and more parsimony-aware systems."

## Q&A Highlights
- Q: Do you feel like you have a set of prompts or structured data to open source for using LLM as a judge? → A: We are working on a benchmark based on test scenarios that evaluates reasoning traces and behavioral trails, not just outcomes. I do have prompts for LLM-as-a-judge and should look into open sourcing them.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
