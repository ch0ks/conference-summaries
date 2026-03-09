# Your Agent Works for Me Now - Johann Rehberger
**Stage 2 | March 4, 2026 | 09:35-10:00**

## Executive Summary
This talk demonstrates how advanced prompt injection techniques can completely compromise AI agents, turning them into persistent, data-exfiltrating malware ("promptware"). The speaker showcases several live exploits, starting with an indirect prompt injection via a Linear ticket that achieves remote command execution through a coding agent (Windsurf). He also reveals a novel attack against Apple Xcode's AI review feature, leveraging hidden Unicode characters to execute code on the fly. A major focus of the presentation is "delayed tool invocation," a technique where a prompt injection lays dormant until a specific user action or intent signal (like continuing a conversation) activates previously restricted tools, such as Microsoft Copilot's memory or Google Gemini's workspace tools. This allows attackers to plant long-term persistence mechanisms, falsify future agent outputs, and continuously exfiltrate data without the user's knowledge. The speaker concludes by introducing "Agent Commander," a command-and-control (C2) framework built entirely on prompts, allowing attackers to manage compromised agents, harvest sensitive data, and pivot through enterprise networks using high-level natural language instructions rather than traditional OS commands.

## Key Points
- Indirect prompt injection: Attackers can embed hidden instructions in seemingly benign sources like issue tickets or source code (using Unicode) to compromise agents analyzing them.
- Promptware and the AI kill chain: Prompt injections have evolved from simple tricks into complex malware (promptware) capable of data exfiltration, remote code execution, and long-term persistence.
- Delayed tool invocation: Security controls that block immediate tool access can be bypassed by conditioning the exploit to trigger later in the conversation based on user intent signals.
- Persistent compromise: By exploiting agent memory tools, attackers can plant false information that permanently alters the agent's future behavior and responses to the user.
- Normalization of deviance: Users increasingly trust AI models despite knowing their flaws, leading to dangerous scenarios where test-grade tools are carelessly deployed in production environments.
- Prompt-based Command and Control (C2): Attackers are moving up the abstraction layer, using natural language prompts to control compromised agents and navigate networks without needing traditional zero-day exploits.

## Notable Quotes
> "It's really that we see with prompt injection that it's not just a single injection anymore, right? It's a complex malware even, right? So you should start maybe using the word promptware."
> "I want to move it up to the prompt level, like not work with operating system commands anymore, but have a command and control with prompts. And it will work, or it works with any agent, with any language, and it's an abstraction from the operating system."

## Q&A Highlights
- Q: Is the LLM deciding the tool a fundamental flaw in AI agent implementations?
  A: It's not fundamentally flawed; Google's security control limiting tool chaining is actually positive. However, the bypass via delayed invocation shows that the boundary needs better lockdown without relying on constant user confirmation prompts.
- Q: Where is the best place to establish a trust boundary for external content and tool invocations?
  A: You must assume tools can be invoked maliciously. The boundary relies on assessing the risk scenario and downstream impact, then implementing security controls that limit what the tool can access and preventing excessive tool chaining.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*