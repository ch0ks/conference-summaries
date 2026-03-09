# Promp2Pwn - LLMs Winning at Pwn2Own - Georgi Gueshev (Interrupt Labs)
**Stage 1 | March 4, 2026 | 10:55-11:20**

## Executive Summary
Georgi Gueshev shares his journey of leveraging Large Language Models (LLMs) to discover zero-day vulnerabilities in Android applications for the Pwn2Own contest. Faced with the monotony of traditional manual bug hunting, he developed an agentic system using LangChain, an LLM, and a custom JADX MCP server to analyze decompiled Java code. Initially struggling with vague agent objectives, he refined the system into a multi-agent pipeline comprising attack surface analyzers, bug hunters, code de-obfuscators, and bug verifiers. By providing structured guidance, explicit entry points, and actionable error messages, the system successfully identified and helped chain two distinct bugs—a URL validation flaw and a cross-site scripting vulnerability—leading to a successful exploit chain. This talk demonstrates the practical, evolving use of AI agents in offensive security research and highlights the necessary engineering to move from naive prompts to effective vulnerability discovery pipelines.

## Key Points
- Started using AI for Pwn2Own to find bugs in Android apps by analyzing human-readable Java decompiled by JADX.
- Initially used a naive two-agent setup (attack surface analyzer and bug hunter) with a custom JADX MCP server.
- Early agent attempts failed due to vague objectives; success required structured guidance, specifying entry points, and providing actionable error messages.
- Refined the system by adding a code de-obfuscator, bug de-duplicator, format converter, and a bug verifier agent.
- Successfully chained two AI-discovered bugs: a URL validation flaw in a customer service app and an XSS vulnerability in Samsung's Bixby assistant.

## Notable Quotes
> "I realized at this point I'm dealing with an intern... I need to be very, well, it's literally like describing the process that I have deeply ingrained in my brain, like what I actually look for and what primitives I'm aware of that I need to chain together to have a successful exploit."
> "The agent wasn't able to figure out these two bugs can actually be used in some sort of chain... That's a very strange prerequisite for your exploit to work. But it's also what makes it the perfect meme exploit for the contest."

## Q&A Highlights
- Q: N/A → A: (No specific Q&A recorded in the transcript for this talk, but the transition to the next speaker was immediate.)

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
