# Total Recon: How We Discovered 1000s of Open Agents in the Wild - Avishai Efrat, Roey Ben Chaim (Zenity)
**Stage 2 | March 4, 2026 | 09:10-09:35**

## Executive Summary
This presentation details a comprehensive reconnaissance effort that uncovered tens of thousands of exposed AI agents across the web, thousands of which were completely unauthenticated. The speaker explains that agents, despite being connected to LLMs, are essentially traditional applications with discoverable breadcrumbs, endpoints, and APIs. Attackers leverage common design patterns, default configurations, platform security gaps, and the fallacy of security by obscurity to find these resources. The research spanned multiple platforms including Microsoft Copilot Studio, OpenAI's Agent Builder, Custom GPTs, and various Model Context Protocol (MCP) servers. Using open-source intelligence and fuzzing techniques on default environment variables and solution prefixes, the team could identify and interact with agents containing sensitive enterprise data, confidential documents, and high-impact business tools. The impact of these exposures is significant, as attackers can probe knowledge sources, test guardrails, and exploit embedded credentials. To help organizations assess their agent posture, the researchers released PowerPon, an open-source tool designed to hunt and identify public agents across different platforms and middlewares, enabling security teams to secure their AI gateways before they are compromised.

## Key Points
- Agents are applications: AI agents function as traditional applications with discoverable endpoints, APIs, and breadcrumbs, making them susceptible to standard web discovery techniques.
- Massive exposure: Researchers found tens of thousands of agents online, with thousands lacking authentication, exposing sensitive documents and business tools.
- Predictable defaults enable discovery: Attackers exploit default environment naming conventions and predictable solution prefixes in platforms like Microsoft Copilot Studio to locate hidden agents.
- Guardrails are insufficient: Even with guardrails in place, attackers can use prompt techniques to bypass protections and discover the tools and capabilities an agent possesses.
- Platform-specific vulnerabilities: Different platforms present unique attack surfaces, from predictable URLs in Vercel/Render deployments for Agent Builder to publicly listed capabilities in Custom GPTs.
- Open-source tools aid defense: The release of PowerPon provides organizations with a hunting tool to actively assess their own agent posture and identify unintended public exposures.

## Notable Quotes
> "In the same way an application is discoverable, agents are also discoverable through the web. It's a subset of web discovery."
> "Agents are highly integrated in their enterprise. A lot of agents have credentials embedded in them... In a way, agents are a gateway to your enterprise. That makes them extremely risky."

## Q&A Highlights
- No formal Q&A segment was explicitly recorded for this specific session.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*