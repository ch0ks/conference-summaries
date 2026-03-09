# Capability-Based Authorization for AI Agents: Warrants That Survive Prompt Injection - Niki Aimable Niyikiza (Snap)
**Stage 2 | March 4, 2026 | 10:00-10:25**

## Executive Summary
This presentation addresses the critical "confused deputy" problem in multi-agent workflows by introducing a new capability-based authorization primitive called a "warrant." The speaker explains that traditional workload identity models fail for AI agents because they grant ambient authority to non-deterministic systems whose runtime behavior is unpredictable. To solve this, the researchers developed Tenno, an open-source protocol that issues ephemeral, task-specific, and cryptographically signed warrants. Much like a valet key that restricts a car's capabilities, a warrant explicitly defines and bounds what an agent can do, ensuring that a child agent's authority can never exceed its parent's (monotonic attenuation). This deterministic execution-layer control survives prompt injection; even if an agent is tricked by malicious input, it cannot execute actions outside the cryptographically enforced scope of its warrant. The system supports offline verification, provides tamper-proof cryptographic audit logs of the delegation chain, and integrates via multiple deployment models including sidecars, API gateways, and MCP proxies, moving the attack surface of authorized actions from 90% down to 0%.

## Key Points
- Failure of traditional identity: Standard workload identity gives agents ambient authority, which is dangerous for non-deterministic AI workflows that dynamically spawn sub-agents and process untrusted data.
- The valet key analogy: Agents should operate with delegated, scoped authority (like a valet key) rather than full ambient access, ensuring they can only perform the specific task requested.
- Warrants as capability primitives: Tenno uses cryptographically signed, ephemeral, and task-scoped warrants that bind capabilities to the holder and are verifiable offline without a central server.
- Monotonic attenuation: The mathematical guarantee that as tasks are delegated downstream in a multi-agent workflow, the capabilities of a child agent can only shrink, never exceed the parent agent.
- Surviving prompt injection: Even if an agent is compromised via prompt injection to access unauthorized data (like a vault path), the deterministic execution layer will mathematically deny the action if it lacks the warrant.
- Cryptographic auditability: The warrant system inherently generates verifiable audit trails that prove who initiated a task, how it was delegated, and why an action was authorized.

## Notable Quotes
> "We believe in agent, the authority that is specific to the task you want them to do in the moment... You don't have to trust them. The valet key is the enforcement."
> "Tenno is not trying to solve prompt injection. We're trying to constrain the agent at the execution time even if it is prompt injected... we are making sure that the authorization is frozen."

## Q&A Highlights
- Q: How do you determine the scope of the token issued to the child agent at runtime? Is it deterministic or LLM-interpreted?
  A: The policy is deterministic. The initial warrant is strictly defined, and while an orchestrator LLM can decide what sub-task to delegate, the cryptographically frozen scope guarantees the child can never exceed the parent's boundaries. Human-in-the-loop approvals can also be added.
- Q: If warrants aren't secrets, how do you authenticate the agents using them?
  A: The warrant itself isn't a secret, but it uses an envelope structure requiring proof of possession. The verifier performs a cryptographic check to ensure the warrant is signed by the issuer, matches the provenance root key, and is presented by the correct agent holding the corresponding private key.
- Q: How do you map these capabilities to domain-specific permissions like AWS IAM or OAuth?
  A: Tenno acts as an execution constraint layer sitting on top of existing IAM. The warrant specifies allowed API calls (e.g., host and path). If the action isn't in the warrant, Tenno stops it before it ever reaches the cloud IAM, effectively scoping down the broad workload identity to the specific task.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*