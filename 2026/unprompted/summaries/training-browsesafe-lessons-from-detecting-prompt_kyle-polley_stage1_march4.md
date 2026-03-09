# Training BrowseSafe: Lessons from Detecting Prompt Injection in Production Browser Agents - Kyle Polley (Perplexity)
**Stage 1 | March 4, 2026 | 14:20-14:45**

## Executive Summary
Kyle Polley, security lead at Perplexity AI, presents lessons learned from developing "BrowseSafe," a specialized classifier designed to detect prompt injection in production browser agents. He highlights the inadequacies of existing open-source benchmarks and models, which often fail in real-world environments due to distractors or novel attack strategies. By fine-tuning a custom model on domain-specific data, Perplexity achieved sub-second latency and high accuracy, emphasizing the necessity of defense-in-depth and continuous data flywheels to stay ahead of evolving threats.

## Key Points
- Browser Agent Risks: Agents navigating untrusted websites can ingest malicious instructions that override their system prompts or execute conditional triggers.
- Benchmark Inadequacies: Current open-source benchmarks lack realistic distractors (e.g., cookie banners), causing models to fail when deployed in live environments.
- BrowseSafe Performance: Fine-tuning a 30B parameter model on a custom dataset yielded a 90.4% F1 score with sub-second latency, significantly outperforming general-purpose models.
- Defense in Depth: Recommended strategies include pre-processing (stripping hidden HTML), applying classifiers before agent ingestion, and returning clear error outputs to guide the LLM.
- The Data Flywheel: Using an LLM backstop to review low-confidence classifier scores creates a continuous feedback loop to retrain and improve detection over time.

## Notable Quotes
> "What we found was that distractors was a huge indicator that these models don't work well in live environments. And it's also an indicator that these models are looking at specific keywords and heuristics instead of the actual intent."
> "Fine tuning on domain specific data sets beats general purpose models by a wide, wide margin."

## Q&A Highlights
- Q: How do you balance open sourcing detection tools vs. teaching attackers what works? → A: The speaker strongly supports open sourcing to help defenders, as threat actors will find vulnerabilities regardless. Sharing IOCs and tools improves overall industry security.
- Q: Can you discuss the recent Perplexity browser research by Zenitie regarding file system access and prompt injection? → A: The file system access issue was due to soft guardrails which have since been hardened. The prompt injection finding required 200 attempts to succeed, which was deemed somewhat disingenuous, though Perplexity used the findings to further improve their models.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
