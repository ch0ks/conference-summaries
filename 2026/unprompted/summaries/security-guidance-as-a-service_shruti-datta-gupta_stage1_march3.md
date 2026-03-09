# Security Guidance as a Service: Building an AI-Native Blueprint for Defensive Security - Shruti Datta Gupta & Chandrani Mukherjee (Adobe)
**Stage 1 | March 3, 2026 | 10:00-10:25**

## Executive Summary
Shruti Datta Gupta and Chandrani Mukherjee present Adobe's "Security Guidance as a Service," an AI-native platform designed to democratize and centralize security knowledge. The system addresses the scalability gap between few security engineers and many developers by providing consistent, organization-specific guidance across various platforms (Slack, JIRA, IDEs). Using a RAG (Retrieval-Augmented Generation) architecture with a curated vector store, the service ensures that developers receive verified security advice at every stage of the Software Development Life Cycle (SDLC).

## Key Points
- The "Security-to-Developer" ratio is a common bottleneck; AI agents can bridge this gap by providing real-time, expert-level support.
- Generic AI answers lack organizational context (standards, specific functions); Adobe's RAG solution provides bespoke, "Adobe-specific" guidance.
- The platform is platform-agnostic, servicing JIRA tickets, Slack queries, automated threat modeling, and in-IDE guidance via an MCP server.
- A "Document Curation Workflow" treats a Git repo as the source of truth, with automated pipelines for embedding and metadata validation.
- The service provides both short-term fixes and long-term architectural recommendations for various vulnerability classes.
- "Context is King": The more organization-specific data provided, the more useful and accurate the AI guidance becomes.
- Evaluation is critical for turning AI experiments into production systems, ensuring high quality and reducing hallucinations.

## Notable Quotes
> "When you make security zero calorie and seamless for developers, they will get on board and they will want to do the right thing."
> "Evals is what will turn your AI experiments into production systems."

## Q&A Highlights
- Q: How do you enforce the use of these tools, like the MCP server? → A: Through roadshows and a unified Cursor extension that comes pre-configured with security rules and MCP settings upon sign-in.
- Q: Have you tried injecting these as agent rules or skills? → A: Yes, preliminary testing showed that adding security rules and skills to the agentic loop reduced vulnerabilities in generated code by approximately 70%.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
