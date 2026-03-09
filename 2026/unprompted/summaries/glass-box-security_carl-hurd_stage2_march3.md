# Glass-Box Security: Operationalizing Mechanistic Interpretability for Defending AI Agents - Carl Hurd (StarSeer)
**Stage 2 | March 3, 2026 | 14:55-15:20**

## Executive Summary
Carl Hurd, co-founder of StarSeer, introduces "Glass-Box Security," a paradigm shift in AI defense that moves beyond host and network-based solutions to inspect the internal "mental state" of models. By leveraging mechanistic interpretability to hook into a model's forward pass, StarSeer captures "intent" and "strength" of concepts within the high-dimensional latent space. This approach allows detection engineers to identify malicious thoughts (e.g., the intent to rob a bank) before they manifest as tokens, providing a foundation for behavior-based detection that is resilient to syntactic variations and jailbreaks.

## Key Points
- Traditional host-based (EDR) and network-based (Prompt Firewalls) solutions are limited to plain text analysis, missing 50% of the model's processing lifecycle.
- Glass-Box Security focuses on "Intent" (direction in latent space) and "Strength" (magnitude/scalar projection) to identify concepts.
- Mechanistic Interpretability: Adding hooks to the residual stream of a neural network to collect activations during inference without requiring a backward pass.
- Linear Representation Hypothesis: Concepts are represented as directions in high-dimensional space, allowing for semantic tripwires and manifolds.
- The "superposition" challenge: One neuron cannot represent every idea; StarSeer uses dot products to filter noise and measure conceptual alignment.
- Sovereign infrastructure is a requirement for serious security, as frontier model providers do not currently expose activation data.
- "Canary Models": Instrumenting smaller, self-hosted models in line with frontier models to perform real-time conceptual auditing.
- The future of agentic security requires semantic traceability to ensure agents are not "reward hacking" or bypassing syntactic guardrails.

## Notable Quotes
> "We have to intercept the thought before the action occurs. Semantic observability is really the new foundation for security moving forward."
> "Autonomous agents bypass traditional perimeter boundaries... static syntactic guardrails are not going to be effective long term."

## Q&A Highlights
- Q: How do you handle indirect prompt injection detection? → A: By measuring the shift in intent before and after a RAG pipeline or tool-based enhancement.
- Q: Does intent measurement serve as a baseline if the agent is already compromised? → A: Security requires defense-in-depth; Glass-Box provides the semantic foundation, but must be paired with strong authorization and identity for agents.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
