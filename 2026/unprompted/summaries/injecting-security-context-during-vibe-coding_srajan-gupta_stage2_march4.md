# Injecting Security Context During Vibe Coding - Srajan Gupta (Dave)
**Stage 2 | March 4, 2026 | 10:55-11:20**

## Executive Summary
The presentation addresses the critical security challenge of "vibe coding" (rapid AI-assisted development) where code speed outpaces traditional security practices. Srajan Gupta notes that with AI writing code based on quick prompts, 60% of vulnerabilities are often missed by CI/CD scans due to structural flaws and a lack of context. The core thesis proposes a paradigm shift: injecting security context directly into the code generation loop rather than waiting for post-commit CI/CD scans. By utilizing the Model Context Protocol (MCP) integrated with IDEs, developers can run a lightweight pre-coding security review to analyze risks and requirements, then feed these guidelines into the AI agent to generate secure code from the start. Post-generation, the code is immediately verified inline. This proactive approach leads to faster fixes, fewer findings, and allows security teams to match developer speed seamlessly without disrupting the workflow.

## Key Points
- **The "Vibe Coding" Threat**: Developers increasingly rely on prompts to generate full features instantly, focusing on functionality over security and bypassing threat modeling.
- **Traditional Scanners Fall Short**: Traditional detection is too slow and misses design flaws.
- **Pre-Coding Analysis**: Injecting context before the agent writes the code is crucial.
- **Immediate Feedback Loop**: Verify output immediately inline while the developer's context is fresh. 
- **Model Context Protocol (MCP)**: Leveraging MCP allows seamless integration with coding agents (like Claude and Cursor) to provide internal policies, threat models, and standards on-demand.
- **Guidelines Must Be AI-Friendly**: Security guidelines meant for humans often don't work for AI; they require intelligent filtering, clear tags, and context scoping.

## Notable Quotes
> "The focus these days is mostly around is my code working rather than is my code secure?"
> "I believe that vibe coding fails when the context is missing. We will always have some flaw if we do not provide the correct context."

## Q&A Highlights
- Q: Will this eventually be adapted as a sub-agent skill automatically? → A: Making it a skill across thousands of repos is unscalable. You need a centralized place to pull in all this context, which MCP facilitates.
- Q: When does the security trigger happen? → A: It happens directly within the IDE, when the code is being generated, rather than waiting for code commits.
- Q: How do you ensure developers use this tool? → A: A lot depends on the tool description so the agent automatically calls it, but utilizing hooks makes it deterministic and guarantees it runs.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*