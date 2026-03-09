# Operation Pale Fire: How We Red-Teamed Our Own AI Agent - Wes Ring, Josiah Peedikayil (Block)
**Stage 1 | March 4, 2026 | 13:55-14:20**

## Executive Summary
Josiah Peedikayil from Block's offensive security team details "Operation Pale Fire," a red team engagement targeting "Goose," an internal (now open-source) AI agent. The team aimed to operationalize a novel, undetectable prompt injection to gain code execution on a corporate laptop. By leveraging invisible Unicode characters hidden inside Google Calendar invites and shared Goose "recipes," the red team successfully demonstrated how an AI agent could be manipulated into running malicious bash commands, highlighting the stealthy nature of modern prompt injection.

## Key Points
- Target Identification: The red team focused on Goose, an agent with a developer shell tool call and MCP integrations (like Google Calendar).
- Invisible Prompt Injections: Attackers hid malicious payloads using zero-width Unicode characters, making the injection completely invisible to users while still parsable by the LLM.
- Exploiting Calendar Invites: Initial attempts embedded hidden payloads in external calendar invites, waiting for the user to ask the agent to summarize their schedule.
- Malicious Recipes: A second campaign embedded invisible instructions within a shared Goose "recipe" URL, successfully tricking the agent into executing commands when triggered.
- Mitigations Implemented: Block responded by stripping non-standard Unicode characters, adding explicit recipe warnings, building a bad bash command detector, and restricting external calendar invites.

## Notable Quotes
> "Can you make one without getting caught, without getting detected? Can you make one that hides in plain sight? That's what we were really interested in answering."
> "We used those invisible Unicode characters, and by using those zero-width Unicode characters, we can basically hide in plain sight."

## Q&A Highlights
- Q: Did you test the user interface for any vulnerabilities like HTML injection or markdown rendering? → A: Yes, they looked into some of those cases early on, as they were common when these agents first came out.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
