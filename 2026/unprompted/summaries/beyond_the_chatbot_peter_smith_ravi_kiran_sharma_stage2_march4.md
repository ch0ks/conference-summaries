# Beyond the Chatbot: Delivering an Agentic SOC for Real-World Defense - Peter Smith, Ravi Kiran Sharma (RK) (Salesforce)
**Stage 2 | March 4, 2026 | 15:05-15:30**

## Executive Summary
This presentation introduces Salesforce's implementation of an "agentic SOC," moving beyond simple chatbots to deploy specialized AI agents working alongside human analysts. The speakers showcase a live demonstration of agents responding to a CrowdStrike threat intelligence report. The agents autonomously extract indicators of compromise (IOCs), plan a hunt, execute searches across the environment, propose remediation steps (like deploying new detection rules and containing affected hosts), and communicate with incident commanders—all in under ten minutes. The architecture relies on deterministic orchestration, multiple narrow-scoped agents, and human-in-the-loop approvals for critical actions. The talk emphasizes building on top of existing SOAR infrastructure rather than ripping and replacing it, providing a practical blueprint for enterprise SOC teams to integrate AI.

## Key Points
- **Digital Teammates:** Salesforce defines the agentic SOC as a collection of digital teammates collaborating in platforms like Slack alongside humans.
- **Speed to Containment:** The multi-agent system reduced the time from reading a threat intelligence report to containing the threat to under 10 minutes.
- **Specialized Agents:** Rather than using one monolithic model, the architecture relies on multiple specialized agents (e.g., normalizer, hunt planner, IOC investigator, threat detection engineer).
- **Human-in-the-Loop:** Critical actions such as hunting plans and remediation steps (like containing hosts) require explicit human approval and business justification.
- **Built on Existing SOAR:** The system leverages Salesforce's existing SOAR infrastructure and its 250+ Python integrations rather than starting from scratch.
- **Agent Cards:** Every agent is strictly defined by an "agent card" that outlines its persona, allowed tools, and execution parameters, limiting scope creep.
- **Deterministic Orchestration:** High-risk workflows use deterministic orchestration to prevent LLMs from going off the rails.

## Notable Quotes
> "The agentic SOC to us at Salesforce means a couple things, but mostly it means a collection of digital teammates working together where we are and where we are is typically in Slack."
> "You don't want your LLMs going wild. The agent chains and chain of thought is cool but keep it in guardrails. Don't have monolithic agents."
> "We didn't buy a new orchestration platform. We took our old SOAR which has 257 different Python integrations. We taught agents to speak to it."

## Q&A Highlights
- Q: What's the cost of this infrastructure to run in dollar figures and engineering person-hours?
  A: Most of the configuration and code was written by Claude, heavily reducing engineering time. While not exactly "zero time," the foundational development was greatly accelerated.
- Q: What is the impact on key performance indicators (KPIs)?
  A: The primary metrics revolve around "mean time to reduce or improve X," such as significantly decreasing the time required to hunt and remediate threats across the enterprise.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*