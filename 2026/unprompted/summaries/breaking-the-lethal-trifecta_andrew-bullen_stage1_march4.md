# Breaking the Lethal Trifecta (Without Ruining Your Agents) - Andrew Bullen (Stripe)
**Stage 1 | March 4, 2026 | 11:20-11:45**

## Executive Summary
Andrew Bullen addresses the pressing but often ignored risk of prompt injection in AI agents, advocating for robust architectural guardrails that don't paralyze agent functionality. At Stripe, the security team assumes prompt injection is inevitable and focuses on mitigating the damage by breaking the "lethal trifecta" of data exfiltration and harmful actions. To prevent data exfiltration, they enforce strict egress controls, utilizing safe search configurations and proxying SaaS connections through a centralized MCP server called Toolshed. To mitigate harmful actions (production writes or broad communications), they restrict agents from unilateral execution. Crucially, Bullen emphasizes that security must not ruin the user experience. They combat review fatigue and agent blocking by batching human confirmations, allowing reversible actions, and using CI checks and tool annotations for seamless enforcement, ensuring that organizations can innovate safely.

## Key Points
- Prompt injection is a critical risk that the industry often ignores due to the fast pace of AI development.
- Data exfiltration mitigation focuses on preventing egress, using safe search options and proxying third-party SaaS connections.
- Harmful action mitigation relies on preventing agents from unilaterally executing sensitive actions like production writes or communications.
- Architectural guardrails introduce friction; improving UX involves batching confirmations and allowing reversible actions instead of blocking agents.
- Enforcement uses CI checks for egress configuration and mandatory annotations on tools to trigger necessary human-in-the-loop reviews.

## Notable Quotes
> "We basically have to assume prompt injections will happen and prevent compromised agents from causing harm when they do happen."
> "Security isn't just about figuring out the secure way to do things. It's about helping your organization figure out how to accomplish their goals in a secure way."

## Q&A Highlights
- Q: Is there value in aggregating human-in-the-loop reviews at the team level since teams run into similar problems? → A: Yes, while still early in UX experimentation, the North Star is reducing the number of stops and checks while ensuring human judgment is applied at the right time.
- Q: Do you still find value in threat modeling to stop prompt injections during system design? → A: Yes, there is a place for detective controls, especially for customer-facing products, but we lean heavily on deterministic architectural controls since we cannot fully trust models yet.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
