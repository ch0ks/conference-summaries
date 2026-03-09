# Fenrir: AI Hunting for AI Zero-Days at Scale - Peter Girnus, Derek Chen (Trend AI Zero Day Initiative)
**Stage 1 | March 3, 2026 | 13:20-13:50**

## Executive Summary
Peter Girnus and Derek Chen present "Fenrir," a sophisticated zero-day vulnerability discovery engine developed by the Trend AI Zero Day Initiative (ZDI). Fenrir utilizes a unified platform approach that combines offensive and defensive components to enable a bidirectional intelligence feedback loop. The pipeline employs a cascading architecture, starting with traditional static analysis (YARA, Semgrep, CodeQL) to filter out obvious false positives, followed by an L1 triage stage (fast, efficient LLMs) to further reduce noise, and finally, an L2 "deep agentic triage" stage where agents in an isolated, secure sandbox environment verify vulnerabilities and generate proof-of-concept (POC) exploits. Fenrir operates as a force multiplier for human security researchers, significantly increasing vulnerability discovery throughput (2.5x) while maintaining high accuracy (80% fewer false positives) and enabling 70% faster disclosure rates.

## Key Points
- Fenrir is designed as a force multiplier, not a replacement for human researchers, by filtering massive volumes of raw signals into high-confidence findings.
- The pipeline uses a cascading approach to optimize for compute cost: fast static analysis tools filter out obvious noise before the system engages expensive agentic LLM triage.
- An L2 agentic triage stage involves deploying suspected vulnerabilities into an isolated secure sandbox for full execution, multi-step reasoning, and verification.
- Fenrir demonstrates significant productivity gains, having submitted over 60 critical CVEs to date.
- The system employs adversarial interrogation, memory corruption bug detection, and dynamic context allocation to maintain precision across diverse repositories.
- The feedback loop between Fenrir (zero-day discovery) and Mimir (end-day/threat research) allows the system to automatically re-scan codebases upon patch release to find bypasses or newly introduced bugs.

## Notable Quotes
> "Fenrir is designed to not replace human researchers, but to be a force multiplier."
> "Over 60% of findings are filtered out by a single sonic call instead of going into the next stage, which is much more heavier... And the operational impact is massive."

## Q&A Highlights
- Q: Have you experimented with different "thinking levels" for models (e.g., chain-of-thought depth)? → A: The architecture was built when these capabilities were limited; "thinking levels" are a key consideration for Fenrir 2.0.
- Q: What does a "medium" confidence score mean at the triage level? → A: It's part of a proprietary dynamic scoring system based on the LLM's triage; human analysts can interact directly with the agent to understand the reasoning.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
