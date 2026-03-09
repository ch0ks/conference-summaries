# SIFT - FIND EVIL!! I Gave Claude Code R00t on the DFIR SIFT Workstation - Rob T. Lee (SANS Institute)
**Stage 2 | March 3, 2026 | 11:10-11:35**

## Executive Summary
Rob T. Lee, creator of the SIFT Workstation, presents an "earth-shattering" experiment: integrating Claude Code reasoning with a comprehensive suite of digital forensics and incident response (DFIR) tools. He demonstrates that an agentic framework can perform deep memory and disk analysis—tasks that typically take days for a human—in under 15 minutes. Lee introduces the concept of "Forensic MCP Engineering" and calls for a community hackathon to solve critical issues like context rot and trust verification, aiming to match the speed of AI-driven offensive operations.

## Key Points
- The premise: Combine 18 years of vetted DFIR tools (SIFT) with automated AI reasoning (Claude Code) to accelerate investigations.
- Offensive speed: Adversaries are already using agentic AI to compress weeks of work into minutes; defenders must match this velocity.
- The experiment: Claude Code was trained to use SIFT tools by reading man pages, running commands to learn flags, and building its own "skills.md" files.
- Results: A full memory image analysis was completed in 18 minutes, and a C-drive forensic report was generated in 14 minutes with 100% accuracy on known compromises.
- Orchestration: The "Claude.md" file acts as the prime directive, setting deterministic boundaries and rules for the agent's behavior.
- Challenges: "Context Rot" remains a significant issue; as investigations grow in complexity, the agent may forget earlier findings, requiring a reset or better summarization.
- Community Call to Action: SANS is sponsoring a hackathon (April 1 - May 15) with a $22k prize pool to advance Forensic MCPs and solve context rot.

## Notable Quotes
> "What if I said you could do a full day of manual forensics to report in 14 minutes?"
> "Matching AI speed with AI speed... we need to increase the speed of our incident response capabilities to match offensive teams."

## Q&A Highlights
- Q: How did you handle the "lazy loading" of SIFT manuals? → A: I used Claude Code as an orchestrator to go through and learn the tools one by one, rather than dumping all manuals into context at once.
- Q: Is Claude "cheating" by looking up answers online? → A: Unlikely given the level of local system detail in the report, but future iterations could be strictly air-gapped to ensure local inference only.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
