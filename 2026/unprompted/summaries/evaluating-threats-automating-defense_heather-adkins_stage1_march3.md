# Evaluating Threats & Automating Defense: How Google is Advancing Code Security - Heather Adkins (Google) & Four Flynn (Google DeepMind)
**Stage 1 | March 3, 2026 | 09:35-10:00**

## Executive Summary
Heather Adkins and Four Flynn discuss Google's ambitious goal to eliminate every software vulnerability on Earth using AI. They introduce "Big Sleep" and "CodeMender," two research projects that automate the discovery and patching of deep vulnerabilities. Big Sleep recreates expert researcher logic in an agentic reasoning loop to find memory safety bugs with zero false positives, while CodeMender provides verified, idiomatic patches. The talk highlights the transition to an "AI Vonpocalypse" where the volume of vulnerabilities will require the speed and precision of agentic frameworks for defense.

## Key Points
- 2026 is seen as the pivotal year where open-source hacking tools will likely achieve root-level autonomous exploitation capabilities.
- The volume of vulnerabilities is increasing cataclysmically (35% increase in CVEs between '24 and '25), making manual triage impossible.
- Big Sleep: An agentic reasoning system that mimics elite human researchers (Project Zero) to find deep bugs in hours rather than months.
- Big Sleep uses a loop of hypothesis generation, tool use (debugger, python interpreter), and proof-of-vulnerability verification.
- CodeMender: An autonomous patching engine that ensures fixes are secure, functional, and idiomatic to the original codebase.
- CodeMender uses a pluggable verification system, including fuzzing and formal verification, to validate patch candidates.
- Google prioritizes high-quality, verified outputs over speed to build community trust in autonomous security systems.

## Notable Quotes
> "We simply must eliminate every software vulnerability on Earth... that is the legacy that people in this room need to leave behind."
> "Zero day is Trust misplaced... secure the path where vibes explode."

## Q&A Highlights
- Q: How does this compare to OpenAI's recent work? → A: Both use agentic reasoning, but side-by-side comparisons aren't yet possible as full details haven't been published by either team.
- Q: Can these techniques apply to web or business logic vulnerabilities? → A: While the research focuses on deep memory safety in infrastructure (V8, FFMpeg), the methodology of hypothesis and verification is broadly applicable to input validation and web faults.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
