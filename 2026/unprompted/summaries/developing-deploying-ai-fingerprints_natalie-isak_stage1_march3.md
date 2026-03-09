# Developing & Deploying AI Fingerprints for Advanced Threat Detection - Natalie Isak & Waris Gill (Microsoft)
**Stage 1 | March 3, 2026 | 12:00-12:25**

## Executive Summary
Natalie Isak and Waris Gill present "BinaryShield," a privacy-preserving system for cross-service threat intelligence at Microsoft. The system allows different services (Azure, GitHub, M365) to share information about prompt injection attacks without revealing sensitive user data. By creating fuzzy "fingerprints" of malicious prompts using quantization and differential privacy, BinaryShield enables the correlation of spray attacks across an organization's entire product suite with significant speed and efficiency.

## Key Points
- Organizations with siloed services often miss "spray attacks" where an adversary uses the same prompt injection across multiple platforms.
- Raw prompts cannot be shared due to privacy regulations; BinaryShield solves this by redact-quantize-noise pipeline.
- Fingerprinting Process: 1) PII Redaction, 2) Embedding generation, 3) Binary Quantization (0s and 1s), and 4) Adding differential privacy noise (Epsilon).
- The "Epsilon" value allows organizations to tune the trade-off between user privacy and threat detection utility.
- Quantized fingerprints are 36x faster to correlate than traditional floating-point embeddings, enabling real-time detection at scale.
- The system captures a "semantic ring" around an attack, making it robust against minor perturbations or perturbations intended to bypass simple blocklists.
- A central "Threat Registry" broadcasts detected fingerprints, allowing services with different safety stacks to benefit from a single detection.

## Notable Quotes
> "We really need the ability to correlate related prompt injections... without revealing any customer content."
> "BinaryShield provides semantics, speed, and privacy."

## Q&A Highlights
- Q: Does quantization lose too much semantic information? → A: While some information is lost, the high dimensionality (e.g., 1536) of modern embeddings ensures enough semantic signal remains for accurate threat correlation.
- Q: Can this catch variants or just verbatim prompts? → A: The fuzzy nature of the fingerprints and the ability to adjust the Hamming distance threshold allows the system to catch a wide range of related perturbations, not just exact matches.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
