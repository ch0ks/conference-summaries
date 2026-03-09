# Tenderizing the Target: Soaking Code in Synthetic Vulnerabilities - Aaron Grattafiori & Scott Behrens (NVIDIA/TrendAI)
**Stage 2 | March 3, 2026 | 13:55-14:20**

## Executive Summary
Aaron Grattafiori and Scott Behrens detail the development and implementation of "Marinade," an innovative agentic workflow designed to inject realistic, exploitable synthetic vulnerabilities into target source code. This approach seeks to solve a critical problem in security testing: how to accurately evaluate security scanners, human penetration testing teams, and AI vulnerability discovery agents using ground-truth data that mirrors actual enterprise codebases. Rather than relying on contrived, CTF-style challenges, the Marinade system utilizes large language models to deeply analyze an application's architecture, understand its functional flows, and seamlessly introduce context-aware flaws without breaking the existing build or core functionality. The system supports multiple modes of operation, including OWASP Top 10 categories, specific CWE/CVE emulations, and complex chained remote code execution (RCE) scenarios. Recognizing that modern AI models often refuse to write insecure code due to safety alignment, the authors pioneered the use of "skills"—markdown-based instructions that act as a procedural jailbreak to overcome these limitations. By mandating the creation of functional verification scripts (PoCs) alongside the injected vulnerabilities, the team ensures the introduced flaws are genuinely exploitable, effectively moving the industry toward higher-fidelity, automated evaluation benchmarks for defensive security tools and research.

## Key Points
- **Agentic Vulnerability Injection:** AI models are now capable of systematically introducing complex, context-appropriate vulnerabilities into massive codebases, serving as a powerful evaluation tool.
- **Overcoming LLM Refusals:** Modern LLMs often reject prompts asking for vulnerable code. The researchers bypassed this by creating predefined markdown "skills" that act as procedural jailbreaks.
- **Importance of Realism:** Injecting vulnerabilities into real-world code provides better evaluation metrics than traditional Capture The Flag (CTF) challenges. "We need to move away from CTF-style benchmarks toward real-world codebases."
- **Functional Validation (PoCs):** To avoid "reward hacking" (where the LLM introduces nonsensical or unexploitable code), the system requires the generation of a Proof of Concept script.
- **Comprehensive Analysis Phase:** Before injection, the agent conducts a deep architectural review of the codebase to determine the most logical and stealthy locations for a flaw.
- **Multiple Injection Modes:** The framework can target specific classes of flaws, including the OWASP Top 10, CWE definitions, CVE emulations, or chained RCE attacks.
- **Adjustable Difficulty Levels:** Injections can be tuned from "easy" (easily found by standard scanners) to "hard" (designed to evade detection and challenge advanced human analysts).

## Notable Quotes
> "As we say in security, write POC or get the f*** out, evals are critical."
> "English is the new coding language."
> "We're not in cyber Kansas anymore. It's very interesting times for the security industry."

## Q&A Highlights
- **Q: Will LLM refusals to generate vulnerable code improve or become a larger obstacle?** → **A:** It is an ongoing race between AI capabilities and safety guardrails. Features like trusted access models for researchers are necessary to balance safety with defensive security research.
- **Q: Are you dealing with the LLMs generating nonsensical vulnerability chains?** → **A:** While it has improved significantly over the last six months, chaining complex vulnerabilities sometimes still requires a human-in-the-loop to ensure the exploit path remains logical and realistic.
- **Q: Have you leveraged this tool offensively to insert backdoors via malicious pull requests?** → **A:** "No comment." (Said jokingly, highlighting the dual-use nature of the technology).

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*