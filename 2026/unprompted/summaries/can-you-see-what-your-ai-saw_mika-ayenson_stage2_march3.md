# "Can You See What Your AI Saw?": GenAI Endpoint Observability for Detection Engineers - Mika Ayenson (Elastic)
**Stage 2 | March 3, 2026 | 11:35-12:00**

## Executive Summary
Mika Ayenson from Elastic addresses the visibility gap created by the rapid adoption of GenAI tools on developer endpoints. As developers integrate tools like Cursor and Claude Code, traditional EDR systems struggle to distinguish between legitimate AI-driven activity and malicious exploitation. Ayenson presents a methodology for detection engineers to triage AI activity using network data, process ancestry, and file modifications. He introduces new Elastic detection rules designed to identify credential access and persistence attempts hidden within the noise of signed, trusted AI binaries.

## Key Points
- The Problem: Users are installing AI extensions and tools faster than they can be audited; many are opaque and may connect to suspicious domains silently.
- EDR Blindness: Tools like Cursor/Claude spawn shells and make system calls that look like standard developer behavior but lack clear "drivers" in the telemetry.
- Triage Methodology:
    1. **DNS/Network**: Monitor for data exfiltration or unusual domain connections from AI tool paths.
    2. **Code Signatures**: While most AI tools are signed, detection engineers should still flag unsigned binaries in the AI toolchain.
    3. **Process Ancestry**: Look for "chained" commands (e.g., Claude -> Bash -> Curl) that might indicate a remote code execution (RCE) attempt.
    4. **File Writes**: Monitor modifications to AI configuration paths or sensitive system files (e.g., P-lists, cookies) by AI processes.
- "Vibe Hacking": The difficulty of determining if a shell command was run by a human or an LLM.
- Elastic is shipping rules for: Credential access via GenAI, unusual DNS calls, and suspicious persistence techniques for agentic tools.

## Notable Quotes
> "The alert fired, a suspicious process ran, good luck finding out if it is a human or an LLM that did it."
> "EDR really has no clear visibility on what’s driving it [the AI tools activity]."

## Q&A Highlights
- (Detailed Q&A for this session was truncated in the transcript, but the focus remained on distinguishing automated vs. human endpoint activity.)

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
