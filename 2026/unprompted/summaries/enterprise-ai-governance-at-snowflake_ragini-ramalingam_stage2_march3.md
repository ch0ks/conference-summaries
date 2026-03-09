# Enterprise AI Governance at Snowflake: Balancing Innovation and Risk - Ragini Ramalingam (Snowflake)
**Stage 2 | March 3, 2026 | 10:00-10:25**

## Executive Summary
Ragini Ramalingam discusses the evolution of governance at Snowflake to meet the challenges of the AI era. She argues that traditional, deterministic security models are inadequate for AI systems that make decisions at runtime and blur boundaries between endpoint, cloud, and SaaS. Snowflake adopted a dynamic governance model involving a cross-functional steering committee and proactive risk ownership by executive leadership. The strategy focuses on "laying tracks in front of a running train"—enabling rapid AI adoption while maintaining visibility and constraining execution authority through innovative technical controls.

## Key Points
- Traditional security assumed predefined, deterministic execution; AI is fundamentally non-deterministic and blurs traditional control plane boundaries.
- Governance must evolve at the same velocity as AI tool adoption and feature releases (weekly or daily).
- Enterprise Steering Committee: Includes Security, IT, Legal, Privacy, and AI/ML teams to identify usage patterns and risks.
- Decisions are framed as business trade-offs rather than just security trade-offs, involving executive leadership to align with the company's risk appetite.
- Visibility Pathways: 1) AI oversight in procurement, 2) Gating new AI features in existing products, 3) Active discovery of AI artifacts using Snowflake's own AI data cloud, and 4) Business unit partnerships.
- Feature-Based Risk Assessment: Gating specific risky features (like web fetches or MCP tool calling) until native enterprise controls are mature.
- Constraining Execution Authority: Focus on limiting what an agent *can do* (system calls, file reads) rather than trying to stop AI use entirely.
- Shared Ownership: Moving from reactive approvals to proactive ownership of risk by the teams actually building and using the AI.

## Notable Quotes
- "Governing AI... is like laying tracks in front of a running train. Our challenge was to lay those tracks and not slow down the running train."
- "AI governance is not a road block to innovation; it really is the foundation to enable innovation securely and responsibly."

## Q&A Highlights
- Q: How do you control high-stakes autonomous actions (e.g., losing $500 billion in 45 mins)? → A: By only allowing approved, risk-assessed platforms and maintaining a dynamic, weekly/daily discovery process to surface anomalies.
- Q: What technical controls constrain execution authority? → A: Restraining automated browser pathways to internal domains and using EDR tools to match endpoint configurations with existing enterprise standards.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
