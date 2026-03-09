# Establishing AI Governance Without Stifling Innovation - Billy Norwood (FFF Enterprises)
**Stage 2 | March 3, 2026 | 09:35-10:00**

## Executive Summary
Billy Norwood, CISO of FFF Enterprises, shares actionable insights and hard-learned lessons on building an enterprise AI governance program that balances security with the intense business demand for innovation. As a multi-billion dollar pharmaceutical distribution company, FFF Enterprises faced an initial surge of 40 proposed AI projects driven by executive excitement. Norwood explains how the security team rapidly structured a tiered governance platform to triage and manage these initiatives. This included an executive governance committee for top-level regulatory alignment and an AI Center of Excellence to handle tactical implementation, standard practices, and employee enablement. A major turning point in their journey was recognizing that generalized AI usage policies were insufficient; they needed explicit prohibited use cases, mandatory awareness training, and rigorous AI intake scorecards. By forcing AI adoption through a centralized, secure control plane (like Databricks) and leveraging strict access controls, the organization effectively mitigated early risks. Norwood highlights real-world use cases, such as an AI agent saving $250,000 annually on medical pre-authorizations, to demonstrate that when governance incorporates human oversight and prioritizes risk dimensions like PHI and critical business processes, it becomes a powerful enabler rather than a roadblock.

## Key Points
- **Tiered Governance Structure:** FFF implemented a multi-level governance model featuring an executive committee for regulatory issues and an AI Center of Excellence for tactical implementation and standardization.
- **Risk-Based Use Case Triage:** The governance structure evaluates use cases based on risk levels. Projects involving Protected Health Information (PHI) or critical data escalate to higher committees for strict review.
- **Moving Beyond Generic Policies:** A simple "check with IT" policy failed. The organization developed specific prohibited technologies, mandated AI awareness training, and required formal sign-offs.
- **The Value of an AI Intake Form:** Establishing a rigorous intake process helps prioritize projects by assessing the current process, expected metrics, technical debt, and required human oversight.
- **Centralizing the Control Plane:** To maintain visibility and control, all major AI data initiatives were routed through a single, secure platform (Databricks) to standardize access and authorization.
- **Real-World Business Value:** An AI agent automating medical pre-authorizations saved the company $250,000 a year, demonstrating the tangible benefits of securely enabled AI.
- **Human-in-the-Loop:** High-risk AI outputs, such as medical authorizations or complex shipping discrepancies, mandate human review to ensure accuracy and limit liability.
- **Tackling Shadow AI:** Procurement partnerships are essential to integrate AI clauses into contracts, ensuring third-party vendors are vetted for hidden AI models and data usage.

## Notable Quotes
> "The goal of AI governance is to balance the value and the risk."
> "We were aiming for controlled execution, but it spawned child processes."
> "Some of the use cases, usually when more access is needed than should be... you're kind of combining this process that has a lot of financial data that shouldn't be exposed to everybody."

## Q&A Highlights
- **Q: What are you doing about prompt injection?** → **A:** FFF utilizes secure enterprise browsers to force traffic to controlled instances like Copilot, stripping out sensitive keys from cut-and-paste actions, while relying on backend platform monitoring for hallucinations.
- **Q: How do you dimension risk when evaluating an AI project on the scorecard?** → **A:** Because FFF is a B2B distributor, intellectual property is less of a concern. Risk is primarily dimensioned around exposure of patient data (PHI) and limiting excessive access to sensitive financial processes across the business.
- **Q: How do you detect and manage 'Shadow AI' when employees use unauthorized tools?** → **A:** While secure browsers provide some visibility, the team works closely with the procurement department to scrutinize contracts and third-party risk assessments to identify unauthorized AI integration.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*