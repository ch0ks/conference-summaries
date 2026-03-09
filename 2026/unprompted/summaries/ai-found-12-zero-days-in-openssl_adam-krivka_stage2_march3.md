# AI Found 12 Zero-Days In OpenSSL. What Does It Mean For The Industry? - Adam Krivka & Ondrej Vlcek (AISLE)
**Stage 2 | March 3, 2026 | 16:35-17:00**

## Executive Summary
Adam Krivka and Ondrej Vlcek share the results of IEL's autonomous vulnerability research engine, which discovered 12 zero-days in OpenSSL—three of which had been hidden for over two decades. They demonstrate a multi-stage "Sieve" pipeline that emulates a team of security engineers using breadth-first hypothesis generation followed by agentic exploration and POC generation. The system has identified 500 confirmed vulnerabilities across high-profile projects like Chromium, Linux, and Open Claw, resulting in 130 minted CVEs to date.

## Key Points
- AI has fundamentally changed the economics of vulnerability discovery, performing in hours what once required elite experts months to audit.
- OpenSSL Findings: High-severity stack overflows and logic errors in components used by email clients.
- Traefik Case Study: An LLM identified a configuration logic error where a flag meant to *enable* TLS authentication actually *skipped* it—a bug invisible to traditional pattern matchers.
- The IEL "Sieve" Pipeline:
    1. **Breadth-First**: Generating hundreds of hypotheses about potential code flaws.
    2. **Narrowing**: Agentic exploration, POC crafting, and fuzzing to verify exploitability.
    3. **Consensus**: Using multiple models to cross-verify findings and eliminate hallucinations.
- "AI Slop" Prevention: IEL focuses on supply high-quality, actionable reports with fixes to avoid overworking open-source maintainers.
- Success Story: Daniel Stenberg (author of curl) went from skeptic to fan after receiving high-quality, "magic-like" reports from the IEL engine.
- Betting on the Model: IEL focuses on context engineering and the intrinsic reasoning of models rather than relying solely on external verification tools.

## Notable Quotes
> "Efficacy of [commercial pattern matching] scanners was close to zero... even for historical vulnerabilities."
> "Zero-days in OpenSSL... three had been hiding in the codebase for over two decades."

## Q&A Highlights
- Q: Will you become a CNA? → A: Yes, with the current volume of findings, becoming a Certificate Numbering Authority (CNA) is a priority to expedite disclosures.
- Q: Is CVSS scoring still meaningful for AI findings? → A: CVSS has deficiencies, but CVSS 4 is an improvement by adding context. IEL is exploring ways to augment scoring to highlight the "most important" risks.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
