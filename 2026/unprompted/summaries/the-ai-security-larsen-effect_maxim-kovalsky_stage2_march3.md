# The AI Security Larsen Effect: How to Stop the Feedback Loop - Maxim Kovalsky (Consortium Networks)
**Stage 2 | March 3, 2026 | 15:20-15:45**

## Executive Summary
Maxim Kovalsky from Consortium Networks addresses the "Larsen Effect" in the AI security market—the overwhelming feedback loop of fragmented vendor claims and shifting enterprise requirements. He introduces "Adjuster IQ," an agentic research tool built with Claude Code that automatically evaluates over 80 AI security vendors by extracting evidence from GitHub, API docs, and forums. The tool uses a wizard-based risk modeling approach to map specific architecture patterns (e.g., AWS Bedrock, RAG) to a custom taxonomy (LLM Top 10, NIST, MITRE) and recommends the best strategic solutions, helping organizations move from "analysis paralysis" to implementation clarity.

## Key Points
- The AI security landscape is hyper-fragmented, with nearly 80 vendors and four new startups emerging from stealth every six weeks.
- "Adjuster IQ" uses an agentic loop (Research + QC agents) to substanstiate marketing claims with hard evidence, assigning confidence ratings (1-5).
- Risk Wizard: Clients answer a handful of questions about their use case (data sensitivity, model hosting, level of autonomy) to generate an inherent risk profile.
- Architecture Mapping: The tool identifies risks based on specific tech choices (e.g., managed PaaS vs. self-hosted, session-scoped memory vs. durable RAG).
- Prioritization: The system surfaces gaps in existing strategic investments (e.g., Palo Alto, CrowdStrike) before recommending niche public marketplace solutions.
- Implementation Guidance: Produces tailored instructions for GRC, Cloud Engineering, and Security Architecture teams.
- Taxonomy: Synthesizes LLM Top 10, NIST AI-RMF, and MITRE Atlas into a single, comprehensive AI risk framework.

## Notable Quotes
> "Our clients come to us with problems and we try to identify the right solutions... swarms of autonomous agents brought us the most comprehensive... that's like the day to day reality of a VAR."
> "Even the big companies like Palo Alto's and CrowdStrike's are very far from that category [Swiss Army Knife] for now... platform plays only give you about 50% of the relevant risks."

## Q&A Highlights
- Q: Do you prefer "Swiss Army Knife" solutions or best-in-class? → A: The tool attempts platform recommendations, but current fragmentation means even large platforms cover only a subset of critical risks.
- Q: How do you maintain this with such high velocity? → A: A GitHub Actions workflow runs every 12 hours, revisiting every vendor at least once a month and identifying new players automatically.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
