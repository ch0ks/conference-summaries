# Guardrails Beyond Vibes: Shipping Security Agents in Production - Jeffrey Zhang & Sid Shah (Stripe)
**Stage 1 | March 3, 2026 | 09:55-10:15**

## Executive Summary
Jeffrey Zhang and Sid Shah from Stripe discuss the challenges of shipping security agents in production, specifically focusing on threat modeling and security routing agents. They address the core problem of managing increased demand for security reviews with limited human time. Their approach emphasizes a modular, multi-agent architecture where sequential processing ensures more predictable behavior for threat modeling, while a more agentic, tool-using approach is employed for security routing. A critical component of their success is an "Evaluation Pipeline" that employs "LLM as a judge" to semantically evaluate agent outputs against human-verified golden standard test cases, enabling confident, iterative improvements. The team underscores the necessity of maintaining a "human in the loop" to review AI-generated results, ensuring high-quality, relevant security guidance.

## Key Points
- Stripe uses AI agents to address two primary security problems: routing security requests to the correct team and automating threat modeling for new services.
- The threat modeling agent employs a modular, sequential architecture (input, specialized security agents, output) to ensure predictable, deterministic behavior.
- A key learning was that agents must be taught to identify missing information and state "I don't know" to prevent hallucinations when inputs are vague (garbage in, garbage out).
- Evaluation is critical; Stripe utilizes an "LLM as a judge" approach, comparing agent output to human-verified golden standard test cases based on semantic meaning rather than simple keyword or JSON structure matching.
- Phased rollout was used for security routing (web -> Slack -> internal agent UI) to gather user feedback and refine the agent's capability in a live environment.
- Humans remain essential; security engineers review AI-generated threat models to confirm applicability and approve/deny findings.
- Investing early in an evaluation pipeline provides confidence when making prompt or architecture changes, preventing the agent from overfitting to formatting rather than security guidance.

## Notable Quotes
> "Threat modeling is often more of an art than a science... what really mattered was the semantics and meaning behind the risk being conveyed."
> "Humans in the loop aren't optional... we want a security engineer to still review these AI-generated threat models and push forward threats that are actually relevant."

## Q&A Highlights
- Q: Was accuracy the only metric used? → A: Stripe relies on offline accuracy against golden standards; future efforts include "online evaluation" where human approval/denial of live threats serves as a source-of-truth feedback loop.
- Q: Have you considered the Maestro threat modeling framework? → A: The team is open to evolving output formats like Maestro based on applicability, but currently relies on established internal processes and MITRE formatting.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
