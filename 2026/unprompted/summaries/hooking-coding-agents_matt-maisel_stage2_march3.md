# Hooking Coding Agents with the Cedar Policy Language - Matt Maisel (Sondera)
**Stage 2 | March 3, 2026 | 14:20-14:35**

## Executive Summary
Matt Maisel, CTO and co-founder of Sondera, presents a robust methodology for securing autonomous coding agents by implementing reference monitors powered by the Cedar policy language. As coding agents evolve from simple code-completion tools into autonomous systems capable of executing shell commands, fetching external resources, and reading internal files, they introduce significant risks, such as data exfiltration or unintended destructive actions—often conceptualized as the "lethal trifecta." Maisel proposes unrolling the standard coding agent loop into a trajectory event model encompassing actions, observations, control, and state events. By instrumenting the agent framework with lifecycle hooks, security teams can intercept these events in real-time. A deterministic Cedar policy engine then evaluates these events against predefined guardrails and stateful bookkeeping systems before execution is permitted. Unlike traditional sandbox environments that can be overly restrictive or standard permission systems prone to "consent fatigue," this hook-based approach provides granular, context-aware authorization. It allows organizations to enforce dynamic security policies, such as Information Flow Control (IFC) and attribute-based access control, effectively neutralizing malicious inputs while preserving the agent's utility and developer productivity in enterprise environments.

## Key Points
- **The Trajectory Event Model:** Coding agent actions are mapped into four distinct event types: actions, observations, control, and state, providing a structured framework for security interventions.
- **The "Lethal Trifecta" Threat Model:** Agents are vulnerable to untrusted input (e.g., fetched skills), existing sensitive data in context, and execution capabilities, which together can lead to data exfiltration.
- **Reference Monitors as Boundaries:** Security requires a reference monitor situated outside the LLM to mediate every event and act as a tamper-proof security boundary.
- **Agent Coding Hooks:** These are policy enforcement points (like pre- and post-model hooks) that allow the system to allow, modify, or stop an agent's loop based on policy evaluation.
- **Advantages of the Cedar Policy Language:** Cedar is expressive, fast, and mathematically verifiable, allowing policies to be formally analyzed for contradictions or shadow subsets.
- **Context-Aware Enforcement:** Policies can be sourced directly from the agent's context (e.g., Claude.md or Cursor rules), bridging the gap between engineering intent and security enforcement.
- **Stateful Bookkeeping and Information Flow Control:** The system tracks entities and data sensitivity across multiple turns, enabling dynamic restrictions (e.g., blocking network access if PII was previously read into the trajectory).

## Notable Quotes
> "We want a reference monitor sitting outside the agent in the model to mediate every event... It acts as our hard security boundary."
> "Sandbox systems might be overly restrictive and we can get the trajectory context here in our policy engine."

## Q&A Highlights
- **Q: How are labels for Information Flow Control (IFC) applied to the data?** → **A:** Labels are assigned dynamically by evaluating the events against a safety model or external DLP system that classifies the sensitivity of the retrieved information.
- **Q: Who determines the specific policies for a given agent?** → **A:** Policies can be tailored per team. Security intent and operational boundaries are often documented in markdown rules (like Claude.md), which the system formalizes into Cedar policies to grant utility while preventing overreach.
- **Q: Does this architecture support multi-agent or agent-to-agent communications?** → **A:** Currently, the implementation is focused on single agents, but the control event types could theoretically be expanded to govern sub-agent spawning and contextual integrity between communicating agents.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*