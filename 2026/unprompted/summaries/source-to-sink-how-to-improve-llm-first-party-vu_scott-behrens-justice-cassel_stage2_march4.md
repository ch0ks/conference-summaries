# Source to Sink: How to Improve LLM First-Party Vuln Discovery - Scott Behrens, Justice Cassel (Netflix)
**Stage 2 | March 4, 2026 | 11:20-11:45**

## Executive Summary
Scott Behrens and Justice Cassel outline their journey in leveraging Large Language Models to identify first-party security vulnerabilities at scale, moving from naive prompt engineering to a sophisticated multi-agent orchestration framework. Initial efforts using monolithic agents produced inconsistent results, massive variance, and high false-positive rates. Through rigorous evaluations, they determined that specialized agents tasked with specific vulnerabilities outperformed "super agents" and monolithic prompts. Furthermore, context management—such as data flow tracing and omitting test files—drastically reduced token costs while improving depth. They share their orchestration workflow which encompasses discovery gates, mandatory agents running in parallel, and a dedicated false positive remediation phase to ensure triage efficiency. The presentation highlights that intelligent architecture, deterministic tooling (like Semgrep and CodeQL), and programmatic enforcement yield high-fidelity, actionable security findings even on large codebases.

## Key Points
- **Initial Struggles**: Early attempts at LLM vulnerability discovery suffered from inconsistency, dropped sessions, and hallucinatory findings.
- **Specialized vs. Monolithic Agents**: While a single "super agent" is cost-effective, using multiple specialized agents uncovers significantly more true positives.
- **Dedicated False Positive Triage**: Moving triage and false-positive filtering to dedicated agents vastly improves correct severity assignments and reduces review fatigue.
- **Discovery and Tracing**: Intelligent context management, including omitting test files and leveraging tools to trace data flows (sources and sinks), reduced costs by 26%.
- **Large Codebase Performance**: For large codebases (over 30k lines), advanced orchestration and context management find more vulnerabilities than simply using the most powerful base models like Claude 3 Opus.
- **Programmatic Enforcement**: Enforcing schemas and programmatic tool calling stops LLMs from hallucinating severity classes or vulnerability names.

## Notable Quotes
> "We want to review less more. By that, we want to highlight contextual prioritization. So we want to look at the things that actually matter to us."
> "I think it suggests for large codebases being really thoughtful about your context management and your workflow can result in higher fidelity results even more than a really powerful model."

## Q&A Highlights
- Q: Did you experiment with agent sequencing or repetition to improve results? → A: Yes, chaining agents of varying complexity (e.g., Haiku to Sonnet to Opus) can improve results. It finds more but increases costs.
- Q: Any tips for getting the right results via security prompting? → A: Provide ground rules but be explicit about what *not* to do. Allow flexibility so the model explores beyond standard patterns like OWASP Top 10.
- Q: Does this run as a long background scan or trigger on pull requests? → A: They currently run comprehensive scans on critical codebases and are working on scanning incremental diffs for PRs, utilizing saved traces to avoid re-scanning the entire project.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*