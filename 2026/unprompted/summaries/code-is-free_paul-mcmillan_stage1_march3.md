# Code Is Free: Securing Software in the Agentic Future - Paul McMillan & Ryan Lopopolo (OpenAI)
**Stage 1 | March 3, 2026 | 11:10-11:35**

## Executive Summary
Paul McMillan and Ryan Lopopolo present an "AI-maximalist" vision where security software is nearly free to build and integrate. They argue that organizations should stop relying on expensive, inflexible vendor tools and instead "vibe up" custom security lints, tests, and agents directly into their CI/CD pipelines. Lopopolo shares how he built a product with a million lines of code using a team that writes zero code, instead focusing on distilling security expertise into durable prompts and documentation that guide agentic execution.

## Key Points
- The traditional security vendor model is slow, expensive, and often fails to handle company-specific edge cases.
- "Code is Free": Use LLMs to write bespoke security integrations, lints, and tests for your specific environment.
- Threat models should be checked into the repository as text; this makes them "legible" to coding agents and ensures they don't become stale.
- Use agents to enforce security invariants in every PR; a few sentences of clear guidance (e.g., "secure interfaces are impossible to misuse") can prevent entire classes of bugs.
- "Don't permit slop": Refine the engineering culture by turning every slack message or PR comment into a durable, executable guardrail in the codebase.
- Supply chain hardening: Lopopolo demonstrates a "vibe-checked" dependency scanner that uses 16 parallel agents to audit reputations and security profiles of the entire lockfile.
- The goal is to move from manual, synchronous human reviews to asynchronous, high-throughput agentic verification.

## Notable Quotes
> "Software doesn't cost anything to build anymore. And the secret is, that includes security software too."
> "Zero day is now the space between a prompt and prod embrace... Secure the path where vibes explode." (Re-iterating the conference theme)

## Q&A Highlights
- Q: What's the ratio of tokens spent building vs. validating? → A: Approximately 50-50; half of the budget goes to generating code and the other half to refining and verifying it through agentic reviews.
- Q: How do you prevent agents from being prompt-injected to bypass scanners? → A: Use defense-in-depth: separate models for production and verification. A prompt injection that works on an implementation agent is unlikely to work the same way on a verification agent looking for "sus" behavior.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
