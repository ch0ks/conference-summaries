# Exploring the AI Automation Boundary for Threat Hunting at Datadog - Arthi Nagarajan (Datadog)
**Stage 1 | March 4, 2026 | 15:05-15:30**

## Executive Summary
In this session, Arthi Nagarajan from Datadog discusses the development and evolution of an AI-powered threat hunting tool called the Hunting Co-pilot over the past six to nine months. The core thesis revolves around finding the optimal automation boundary—determining what to automate and how. The Datadog team initially struggled with utilizing out-of-the-box LLMs (GPT-4.1) for query generation due to high syntax error rates and low semantic accuracy. Because they lacked a curated dataset of past threat hunts for fine-tuning, they reframed the problem around field discovery and log schema exploration directly from the data. Key takeaways include moving to a multi-agent framework with an orchestrator and expert sub-agents, utilizing the Datadog MCP server for iterative query refinement, and carefully managing context windows. Practical implications highlight that while reasoning models increase accuracy, they introduce latency. Therefore, multi-agent frameworks are deemed necessary for complex threat hunting, but teams must provide reasoning transparency to users and rely heavily on robust tool usage to reduce hallucinations and improve overall hunt efficiency.

## Key Points
- **Initial Automation Struggles**: Out-of-the-box LLMs like GPT-4.1 generated fast responses but suffered from a 25% syntax error rate and low semantic accuracy when attempting to generate Datadog lucene queries based merely on documentation.
- **The Data Obstacle**: Datadog lacks a representative, well-labeled dataset of past threat hunts to fine-tune models, making advanced prompt engineering the more viable path over model fine-tuning.
- **Reframing to Schema Exploration**: The team shifted their approach from guessing schemas to discovering them dynamically from real log data through a process of informed guessing, sampling, and iterative refinement.
- **Multi-Agent Framework**: By implementing an orchestrator and expert sub-agents (e.g., AWS CloudTrail, GCP audit logs) along with reasoning models (GPT-5.1) and a Datadog MCP server, syntax accuracy improved significantly, though at the cost of slower response times.
- **Managing Context and Delegation**: While delegation to specialized sub-agents helps manage context space for the overall hunt, it introduces latency and coordination complexity. Chains over three layers deep were found to get stuck.
- **Alternative Evaluation Methods**: Traditional static benchmarking proved ineffective for measuring trust. The team prioritized A/B testing, user feedback loops, and tracking how often hunters chose to use the tool in live production hunts.
- **Success in Production**: During an AWS privilege escalation hunt week, the Hunting Co-pilot cut average query iteration time in half (from 10 to 5 minutes) and saved 25 minutes on average per 60-minute hypothesis hunt.

## Notable Quotes
> "LLMs are good at synthesis, pattern matching and translation. We needed to focus on reducing threat hunting into problems of these categories."
> "If you manage the context well, you'll see results improve. The core lessons from v2 were that we should use reasoning sparingly... and if you use it, you should provide reasoning transparency to the user."

## Q&A Highlights
- Q: Did you use different LLM providers (foundation models vs local models) for the LLM judges, and which models were in the most agreement with a human judge? → A: The team prioritized speed over reasoning for the judges and did not do a thorough analysis of different providers, but did notice a huge difference between reasoning and non-reasoning models.
- Q: Did you consider annotating the output with a confidence score? → A: They did not generate confidence scores because the agent tended to be artificially confident in its own generated queries (e.g., claiming 100% correctness), making it unreflective of actual performance with users.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
