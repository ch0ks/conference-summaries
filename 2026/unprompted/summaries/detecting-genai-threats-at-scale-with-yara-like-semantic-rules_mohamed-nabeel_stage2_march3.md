# Detecting GenAI Threats at Scale with YARA-Like Semantic Rules - Mohamed Nabeel (Palo Alto Networks)
**Stage 2 | March 3, 2026 | 12:00-12:25**

## Executive Summary
Mohamed Nabeel introduces "SYARA" (Super YARA), an open-source extension of the YARA syntax designed for the GenAI era. SYARA combines traditional string matching with multi-modal semantic detection, including embeddings and LLM-based classifiers. This layered approach allows for high-accuracy detection of prompt injection, phishing, and disinformation at scale, achieving 98% detection rates with sub-100ms latency. The system is optimized to run cheaper, faster rules first, ensuring cost-effective threat hunting without sacrificing accuracy.

## Key Points
- Traditional YARA fails against semantic GenAI threats like brand impersonation and disinformation.
- SYARA extends YARA with "LARA" (LLM-based) and "EARA" (Embedding-based) rules in a single, unified syntax.
- The system achievement: 98% detection rate at <$0.001 per query, significantly cheaper than LLM-only solutions.
- Layered Architecture: Executes the cheapest possible rule first (e.g., string match) before escalating to more expensive LLM judges.
- "Differential Privacy": SYARA is designed to operate in a privacy-preserving manner, allowing for threat correlation without exposing user prompts.
- Optimization: Models and LLMs are pre-loaded in global memory to minimize execution overhead.
- Open Source: The project follows the YARA philosophy—entirely open source with no strings attached.

## Notable Quotes
> "Semantic detection at scale requires efficient layered approaches rather than expensive LLM-only solutions."
> "The engine is optimized to execute the cheapest possible rule first."

## Q&A Highlights
- Q: Why create a new format instead of a YARA module? → A: While technically possible to extend YARA, the friction was high; SYARA provides a more native experience for semantic rules while keeping the open-source spirit.
- Q: Does the matcher stop after the first hit? → A: No, like traditional YARA, it can go through all chunks of a document to find the "best" match or multiple hits.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
