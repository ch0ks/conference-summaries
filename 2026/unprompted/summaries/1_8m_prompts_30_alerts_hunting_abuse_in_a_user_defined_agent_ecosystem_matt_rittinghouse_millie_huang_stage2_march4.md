# 1.8M Prompts, 30 Alerts: Hunting Abuse in a User-Defined Agent Ecosystem - Matt Rittinghouse, Millie Huang (Salesforce)
**Stage 2 | March 4, 2026 | 13:30-13:55**

## Executive Summary
This presentation details Salesforce's approach to securing their Agentforce platform against abuse in a complex, multi-tenant ecosystem handling 1.8 million daily prompts. Because autonomous agents possess custom logic and behaviors, traditional signature-based detection fails. The speakers demonstrate how they successfully narrowed millions of events down to just 30 high-fidelity alerts by implementing a behavioral anomaly detection model. By evaluating data access patterns across three levels of identity context (user, agent, and organization) and building daily historical baselines, their system effectively identifies deviations and malicious intents without relying on analyzing customer prompt data. Ultimately, their objective is to move from reactive alerting to real-time auto-containment at the execution layer.

## Key Points
- **The Limits of Content Moderation**: While useful for detecting toxicity and prompt injection at the reasoning layer, traditional content filters cannot observe the execution layer where actual system calls and potential privilege escalations occur.
- **Three Levels of Context**: Anomaly detection was enhanced by examining behaviors not just at the user level, but by incorporating agent and organizational context to minimize noise.
- **Behavioral Baselines**: The detection system builds daily profiles of standard operations, evaluating the frequency, depth, breadth, and sensitivity of data accessed by agents. 
- **Simplicity Over Complexity**: Early attempts to build complex query parsers failed due to high computational cost and noise; simpler telemetry metrics like invocation counts and data rarity proved far more effective.
- **Agent-Assisted Triage**: The resulting alerts are formatted as structured JSON payloads and fed into another LLM agent, which synthesizes plain-English summaries to aid SOC analysts.

## Notable Quotes
> "We cannot rely on static signatures because every agent's logic is custom and valid behaviors very wildly... we aren't just defining against bad words here. We're defining a massive multi-titanic execution engine."
> "Our major hurdle was the observability gap... agentic logs aren't just debug strings. They need to be structured events that link the invoking user ID to the agent ID."

## Q&A Highlights
- Q: How did you overcome the curse of dimensionality and over-engineering features? → A: We used techniques inspired by PCA to identify which features provided the strongest signal, programmatically culling the feature set to the minimal predictive baseline.
- Q: Do you use confidence scores or provide feedback loops for these alerts? → A: We use deviation-based scoring to determine how far out of character an action is, which inherently acts like a confidence interval.
- Q: What has been the feedback from SOC analysts regarding auto-containment? → A: Auto-containment is challenging because the algorithm acts on the user's behalf. Our first step was providing human-readable explanations via LLMs. We are currently tuning containment efficiency via purple team exercises before full deployment.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
