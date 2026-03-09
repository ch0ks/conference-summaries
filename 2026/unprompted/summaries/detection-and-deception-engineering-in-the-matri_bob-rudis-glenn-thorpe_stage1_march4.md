# Detection & Deception Engineering in the Matrix - Bob Rudis, Glenn Thorpe (GreyNoise Labs)
**Stage 1 | March 4, 2026 | 15:30-15:55**

## Executive Summary
In this presentation, Bob Rudis and Glenn Thorpe from GreyNoise Labs introduce Orbi, an internal AI-powered threat intelligence analyst built to handle the overwhelming scale of internet noise. The core thesis is that as the volume of malicious network activity grows—exemplified by massive campaigns like "React to Shell" involving thousands of unique IPs and payloads—human analysts simply cannot keep up without advanced automation. Orbi is a customized Claude Code environment that coordinates between multiple MCP servers and investigation cells to deliver structured, reproducible threat hunting analyses. Key takeaways include the necessity of providing empty-headed LLMs with explicit, highly structured "skills" (written primarily in natural language but backed by SQL, Bash, and Go) to guide their behavior. The speakers emphasize that LLMs must be connected to ground-truth data sources (like Censys and GreyNoise APIs) via MCP tools to be effective. Practical implications center on building robust guardrails, conducting automated validations on LLM outputs to catch hallucinations (like made-up tag names), and acknowledging that human-in-the-loop oversight remains critical when AI agents inform security actions.

## Key Points
- **The "React to Shell" Catalyst**: Orbi was created out of necessity to process massive onslaughts of malicious activity, such as a December 2025 campaign that saw over 8,200 unique IPs slinging 70,000 unique payloads.
- **Orbi's Architecture**: Orbi runs in a highly customized Claude Code environment, coordinating between 12 to 16 MCP servers and multiple investigation cells, utilizing local DuckDB for analytics and remote servers for heavy lifting.
- **Skill Injection**: Similar to the Matrix, Orbi starts with an "empty head" and must be loaded with structured system prompts ("skills") that define workflows, mandatory constraints, anti-patterns, and precise output specs.
- **Leveraging MCP Servers**: Orbi is empowered by over a dozen MCP tools connecting it to ground-truth data, including GreyNoise APIs, JAW4 network fingerprints, Censys global scan data, and T-Shark for PCAP analysis.
- **Guardrails and Constraints**: To prevent confidently wrong answers, the team implemented guard hooks (shell commands that police behavior), strict decision trees, bulletproof formatting patterns, and checklists.
- **Automated Validation**: An independent validator model is used to extract and verify every claim made in Orbi's reports, finding and correcting issues such as hallucinated tag names before they reach human stakeholders.
- **Human Accountability**: Despite Orbi's autonomy in investigating infrastructure (like uncovering a large credential-stuffing proxy network in Canada), humans remain accountable for final actions, such as filing takedown notices.

## Notable Quotes
> "For our threat hunting context, [the LLM is] actually by default about as smart and helpful as a 13-year-old with access to both a flamethrower and Wikipedia."
> "Friends don't let LLMs do their own analytics because they suck at everything if you don't give them tools."

## Q&A Highlights
- Q: Have you tried using frameworks like LangGraph or LangChain instead of Claude Code to orchestrate the agent's work? → A: Yes, the team has hit the limits of Claude Code (which was meant for a different purpose) and plans to create their own threat hunting agent framework, likely starting with Go.
- Q: What are the limitations of Claude Code and when do you outgrow it? → A: The primary limitations revolve around context window size and costs; they plan to move to a new framework to expand capabilities to other data sources without spending excessively on massive context windows.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
