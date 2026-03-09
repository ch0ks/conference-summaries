# Securing Workspace GenAI at Google Speed: Surviving the Perfect Storm - Nicolas Lidzborski (Google Workspace Security)
**Stage 1 | March 4, 2026 | 13:30-13:55**

## Executive Summary
Nicolas Lidzborski discusses the unique security challenges presented by Generative AI, describing it as a "perfect storm" where traditional security boundaries fail. He emphasizes that prompt-as-code environments, where data and instructions are mixed, make reactive filtering (like regex or classifiers) inadequate. Instead, he advocates for a structural security blueprint featuring semantic sandboxing, data provenance tracking, deterministic orchestration, and continuous red-teaming to build systemic resilience against sophisticated agentic attacks like indirect prompt injection and orchestration hijacking.

## Key Points
- The Prompt-as-Code Problem: LLMs treat instructions and user input as a single stream, making traditional out-of-band execution prevention impossible.
- Failure of Reactive Filtering: Static filters, blocklists, and ML classifiers can be easily bypassed through encoding, obfuscation, or multi-modal attacks.
- Indirect Prompt Injection: A major risk where malicious instructions hidden in untrusted content (like a calendar invite) are ingested and executed by an AI agent.
- Structural Security Blueprint: Emphasizes layers such as input filtering, prompt delimitation, and deterministic policy enforcement (e.g., plan-validate-execute patterns).
- Systemic Resilience: Security must be continuous, leveraging automated regression testing, dedicated red teams, and user-driven feedback loops.

## Notable Quotes
> "In general, I work like the prompt is code. Like every single token in the input stream is a potential instruction."
> "To combat that we have actually provide like detailed logs to admit to allow them to understand what is going on review what happened and fix issues."

## Q&A Highlights
- Q: Why wouldn't we separate two separate windows/interfaces for commands and data, avoiding the Von Neumann architecture mistake? → A: We are going back in time to an era like Windows 95 with everything running in the same space. The industry is moving extremely fast, and we need to strongly apply security-by-default and security-by-design principles to avoid creating vulnerable code.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
