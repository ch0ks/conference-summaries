# Enterprise AI Governance at Snowflake: Balancing Innovation and Risk - Ragini Ramalingam (Snowflake)
**Stage 2 | March 3, 2026 | 10:00-10:25**

## Executive Summary
Ragini Ramalingam, leading enterprise security at Snowflake, outlines the dramatic paradigm shift required to govern AI in a fast-paced technology organization. She highlights that traditional enterprise security relied on deterministic, predefined logic, whereas modern AI introduces non-deterministic, runtime decision-making that significantly expands the execution boundary across endpoints, networks, and cloud applications. To keep pace with this rapid evolution without slowing business innovation, Snowflake completely overhauled its governance model. They formed a cross-functional enterprise steering committee to proactively identify risks and established decentralized, shared ownership across business units. Ramalingam emphasizes that AI governance relies heavily on deep visibility; you cannot govern what you cannot see. By leveraging advanced telemetry within their own AI Data Cloud and tightening procurement reviews to assess redundant capabilities, Snowflake achieved the necessary oversight. Furthermore, they pioneered a feature-based risk assessment approach for Generative AI and coding agents. Rather than blindly approving or denying a vendor's tool entirely, the security team selectively enables low-risk features while collaborating directly with vendors to develop the enterprise-grade controls needed for high-risk capabilities, proving that dynamic governance is the fundamental enabler of secure AI adoption.

## Key Points
- **Shift to Non-Deterministic Security:** AI has moved the enterprise from predefined execution to real-time, context-based actions, forcing control planes to expand across the endpoint, network, and cloud domains.
- **Dynamic Governance is Essential:** Traditional governance cycles are too slow. Governance must evolve at the rapid pace of AI feature releases (which often occur weekly).
- **Cross-Functional Steering Committee:** Forming a committee of security, legal, AI/ML, data engineering, and procurement members allows for rapid, top-down alignment on acceptable risk tolerances.
- **Visibility as a Prerequisite:** Effective governance requires discovering AI artifacts across the enterprise. Snowflake uses active discovery telemetry and procurement processes to map AI usage.
- **Feature-Based Risk Assessment:** Because enterprise controls lag behind feature development, Snowflake evaluates and gates specific features within AI tools rather than assessing the tool as a monolithic entity.
- **Securing Coding Agents:** Coding agents amplify the risk of remote code execution and unauthorized API integration. Snowflake counters this by enforcing immutable endpoint configurations and restricting higher-autonomy modes based on user risk profiles.
- **Isolated Experimentation Environments:** To foster safe innovation, Snowflake provides isolated test tenants with synthetic data for AI experimentation, protecting the broader enterprise network.
- **Constrain Execution, Not Innovation:** The core philosophy is to constrain the execution authority of the AI agent rather than banning the tool, ensuring developer productivity remains high.

## Notable Quotes
> "Governing AI at a company like Snowflake... is like laying tracks in front of a running train. And our challenge was to lay those tracks and not slow down the running train."
> "Enabling or disabling AI was not a security decision it is actually a business decision and it's not a security trade off it's a business trade off."
> "You cannot stop AI adoption in the enterprise because if you did it will go around you."

## Q&A Highlights
- **Q: How are you controlling autonomous coding agents that could potentially execute high-risk actions, like losing money in trading?** → **A:** Snowflake mandates discovery to ensure only approved coding agents operate in the environment. Risk is dynamic, requiring continuous weekly or daily conversations with leadership to rapidly shut down anomalous or highly risky behaviors.
- **Q: What technical controls constrain the execution authority of these agents?** → **A:** Controls depend on the agent's native capabilities. For automated browser execution, Snowflake restricts agents entirely to internal domains. For manual pathways, they deploy existing EDR controls to enforce constraints matching the broader enterprise policies.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*