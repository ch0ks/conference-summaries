# AI Security with Guarantees - Ilia Shumailov (AI Sequrity Company)
**Stage 2 | March 4, 2026 | 13:55-14:20**

## Executive Summary
Ilia Shumailov's presentation challenges the current industry reliance on heuristic defenses for AI models, arguing that the cycle of patching prompt injections and jailbreaks is an unsustainable game of cat and mouse. He proposes a paradigm shift toward "AI Security with Guarantees" through a concept known as "task data independence" or control-dataflow separation. By completely separating the model's instructions from untrusted user data, defenders can achieve Control-Flow Integrity (CFI). This involves translating the initial query into a formal plan and using separate models strictly to process unstructured inputs into booleans, ensuring the primary agent cannot be hijacked. He demonstrated that even complex tasks, like a computer use agent navigating a website, can be planned successfully without exposing the LLM to the live environment 80% of the time.

## Key Points
- **The Cat and Mouse Fallacy**: Current heuristic defenses consistently break under scrutiny. A model's apparent robustness is often just a byproduct of attacks being poorly formulated for that specific system.
- **Task Data Independence**: If an agent's task can be completed without seeing the raw data, exposing the model to that data unnecessarily introduces prompt injection risks.
- **Control-Flow Integrity (CFI) for AI**: By rewriting user queries into a frozen formal language and strictly limiting how external data influences the flow (e.g., forcing data to resolve only as boolean variables), attackers cannot inject new instructions.
- **High Applicability**: Surprisingly, about 80% of tasks for complex agentic systems—such as computer-use agents ordering items online—can be planned and executed without the model directly observing data during the planning phase.
- **Data-Flow Attacks Persist**: Even with CFI, models can be tricked by environmental deception, such as fake cookie prompts in ad banners forcing premature clicks, necessitating external sandboxes and access control policies.

## Notable Quotes
> "If the task that you're asking your agent to solve are data dependent, you do not need to show it anything, then prompt injections don't exist at all."
> "Today we actually know how to solve a big chunk of the sogent security problems... but nobody implements this. I genuinely don't know why... building the first prototype was trivial, personalizing this and building like a proper production system is hard."

## Q&A Highlights
- Q: Why is there a lack of adoption for these secure frameworks in the industry? → A: While the initial prototype is straightforward, deep integration into existing million-line codebases requires specialized teams that understand both AI and security, making production deployment notoriously difficult.
- Q: What are the security challenges for computer use agents specifically? → A: Computer use agents lack semantic context; their primary input is screenshots and their action is simply "clicking," making it incredibly difficult to police behavior without proper sandboxing and external policy enforcement frameworks.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
