# Building Secure Agentic Systems: Lessons from Daily-Driver Agents - Brooks McMillin (Dropbox)
**Stage 1 | March 4, 2026 | 11:45-12:10**

## Executive Summary
Brooks McMillin shares hands-on insights from developing and operating 19 daily-driver AI agents that automate his personal coding tasks, code reviews, and task management. He explores the practical challenges of securing these agents on a local MCP server, demonstrating how strict tool allow-lists and granular permission scopes (e.g., read, write, admin) are essential. McMillin encountered significant issues with context pollution and memory leakage between agents, prompting him to implement an identity namespace system to isolate agent memories. He also showcases an experimental MCP relay that acts as a chatroom for agents to debug each other. Throughout the talk, he emphasizes that security improvements—such as limiting available tools and implementing context-aware memory trimming—directly enhance agent functionality and focus. Observability tools like Langfuse are also highlighted as critical for tracking costs and agent behavior.

## Key Points
- Developed an ecosystem of 19 agents automating daily coding tasks, code reviews, and task management with limited human-in-the-loop.
- Implemented strong security controls on a local MCP server, assigning each agent specific allowed tools and permission scopes (e.g., read, write, admin).
- Created a memory isolation system using identity namespaces to prevent agents from accessing or being confused by other agents' memories.
- Developed an MCP relay acting as a chatroom for agents to debug each other, alongside remote agents running on constrained LXC containers.
- Enhanced observability and cost control using Langfuse traces, maximum iteration limits, and context-aware log trimming for security events.

## Notable Quotes
> "I have kind of a self-sustaining code optimization ecosystem that will keep running until it maxes out my credit card and Claude cuts me off."
> "That's like a great example of how improved security also improves actual functionality, because with like 73 MCP tools, if we're injecting that into every LM... context is wasted, and they're going to have so much extra information that's just not going to be helpful."

## Q&A Highlights
- Q: Is the ever-expanding MCP server just a single boundary for all tools? → A: Each agent spawns its own local standard IO server scoped down only to the MCP functions and directory paths that specific agent is allowed to use.
- Q: Have you thought about using Envoy and OPA outside the context window to manage boundaries instead of a bloated MCP? → A: Currently the infrastructure is immature (running on a personal desktop), but moving to a K3 setup with service mesh controls is on the roadmap.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
