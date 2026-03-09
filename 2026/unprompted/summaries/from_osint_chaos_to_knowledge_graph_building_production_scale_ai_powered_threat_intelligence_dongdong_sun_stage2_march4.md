# From OSINT Chaos to Knowledge Graph: Building Production-Scale AI-Powered Threat Intelligence - Dongdong Sun (Palo Alto Networks)
**Stage 2 | March 4, 2026 | 14:20-14:45**

## Executive Summary
Dongdong Sun details Palo Alto Networks' innovative approach to taming the overwhelming volume of Open-Source Intelligence (OSINT). With over 10,000 unstructured threat reports published weekly across various sources, manual analysis is unscalable and raw indicator feeds lack essential context. To solve this, their team developed an LLM-driven pipeline to parse unstructured reports and extract entities and their relationships, compiling them into a semi-structured Knowledge Graph. This AI agent can perform multi-hop reasoning across the graph, allowing security researchers to ask complex questions (e.g., identifying shared infrastructure between APT groups) and receive heavily contextualized answers fully cited with their original OSINT sources, minimizing hallucinations.

## Key Points
- **The OSINT Scalability Problem**: Relying on human analysts to read and structure data from thousands of weekly threat intelligence reports is inefficient and prone to missing overlapping contextual clues across vendors.
- **Knowledge Graph Transformation**: Rather than feeding raw text into an LLM or relying on overly complex formats like STIX, they use a semi-structured Knowledge Graph to retain unstructured context while linking entities (malware, actors, vulnerabilities).
- **LLM Extraction Pipeline**: An LLM "skeleton extractor" routes text to specialized components that extract exact phrasing or infer behaviors (e.g., mapping descriptions to MITRE ATT&CK patterns).
- **Automated Evaluation Loop**: To ensure high data quality, the team developed an automated prompt optimization process where LLMs detect inconsistencies among human annotators and continuously improve extraction accuracy.
- **Graph-Augmented QA**: Security researchers interact with the system via natural language. The agent walks the graph to answer complex, multi-hop queries, specifically grounding its responses in the cited nodes to avoid relying on error-prone internal model knowledge.

## Notable Quotes
> "The best thing about open source intelligence data is free. But is it really free? It's all there in a while, but you have to gather it into a structured format and you can use it for downstream tasks easily."
> "If your agents are relying on this graph and this graph is trash then it's like trash out you really can't fix anything from that point."

## Q&A Highlights
- Q: How do you qualify the accuracy of the LLM outputs and avoid hallucinations? → A: Over 50% of our effort goes into rigorous evaluation of the initial graph extraction. Furthermore, the agent is strictly grounded to the sources in the knowledge graph when answering questions, rather than relying on its internal model knowledge.
- Q: How do you handle potentially low-quality reporting or inaccurate attribution from the community? → A: The knowledge graph inherently highlights evidence weight. If a claim lacks supporting nodes or evidence across multiple sources, it becomes apparent, and our internal threat intelligence teams also perform cross-checking to validate the data.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
