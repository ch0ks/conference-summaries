# The Hard Part Isn't Building the Agent: On Measuring Agent Effectiveness to Improve It - Joshua Saxe (Meta / Startup)
**Stage 1 | March 3, 2026 | 09:35-10:00**

## Executive Summary
Joshua Saxe argues that the primary bottleneck in deploying autonomous cyber defense is evaluation. As attackers shift to managing AI agents, defenders must move from manual labor to managing defensive agents. Saxe critiques traditional "Oracle-based" metrics (precision/recall) as being too noisy for the ambiguous domain of security. He proposes a shift toward behavioral and reasoning-based evaluation, using a holistic rubric to "interview" agents and assess their decision-making process under uncertainty, much like hiring a security engineer.

## Key Points
- The future of cyber defense requires trusting AI agents to take sensitive actions (quarantining servers, patching code) autonomously.
- Traditional ML evaluation fails in security because ground truth is often noisy, ambiguous, or non-existent (halt problem, dual-use binaries).
- SOC analysts and access investigators frequently disagree, creating a "noise ceiling" that classical metrics cannot penetrate.
- Instead of reducing agent behavior to a single bit (1 or 0), we should evaluate the reasoning process: evidence gathering, policy understanding, and justification.
- Saxe recommends a "rubric-based" interview protocol for agents, grading their trajectories to ensure they reason from first principles.
- LLM judges can be trained with as few as 100 human-graded samples to automate this holistic evaluation at scale.
- Good evaluation enables "hill climbing" using genetic algorithms and AI coding tools to optimize agent architectures without manual tweaking.

## Notable Quotes
> "Evaluation is like the big blocker... in our field. We need to transition into becoming a field in which we take it very seriously, much like autonomous driving."
> "Imagine if we hired security engineers on the basis of these kinds of binary multiple choice tests... That's sort of what we're doing with AI systems."

## Q&A Highlights
- Q: Have you used negative human feedback to improve the LLM judge? → A: Yes, using a Bayesian model to account for human disagreement helps weight certain dimensions of the evaluation more accurately.
- Q: Are these methods materially different from non-security model evals? → A: The math is similar (textbook statistics), but the domain expertise is required to design the rubric and understand what "good" looks like in a high-stakes security context.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
