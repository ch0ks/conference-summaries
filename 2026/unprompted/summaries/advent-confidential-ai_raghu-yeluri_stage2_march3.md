# The Advent of Confidential AI - Raghu Yeluri (Intel)
**Stage 2 | March 3, 2026 | 13:30-13:55**

## Executive Summary
Raghu Yeluri from Intel Corporation outlines the crucial role of confidential computing in securing AI applications, focusing on the concept of "Confidential AI." As the enterprise adoption of AI accelerates, protecting data, intellectual property, and models from infrastructure-level threats becomes a primary concern. Yeluri defines confidential AI as the overlay of artificial intelligence workloads on top of hardware-based trusted execution environments (TEEs). These environments ensure that data is encrypted while in use, effectively shielding it from rogue administrators, other tenants on shared infrastructure, and potentially the cloud providers themselves. He highlights the critical need for attestation—cryptographic proof that the computing environment is genuine and secure—which allows organizations to trust the infrastructure before sharing sensitive keys or models. Yeluri illustrates this with practical architectures, including a CPU-to-GPU hybrid approach and real-world implementations like Google Confidential Space and a multi-party medical imaging case study with Talus. He stresses that as agentic AI and small domain models grow in prevalence, the integration of confidential computing will become an industry default, offering a robust defense against evolving threats and aligning with stringent regulatory requirements like the EU AI Act and DORA. This paradigm shift enables organizations to safely innovate without compromising security.

## Key Points
- **Definition of Confidential AI:** It integrates AI with hardware-based trusted execution environments to protect data in use, models, and prompts. "It is the overlay of AI on confidential computing."
- **Three Pillars of Confidential Computing:** Protects data in use via hardware environments, restricts control exclusively to the workload owner, and provides cryptographic attestation to verify the environment.
- **Protection from Infrastructure Threats:** Confidential computing neutralizes threats from cloud administrators or other tenants. "It protects you from the administrators of your infrastructure... It protects your models, it protects your data."
- **CPU and GPU Hybrid Models:** Future architectures will seamlessly integrate confidential computing across both Intel CPUs and NVIDIA GPUs without software bottlenecks. "Essentially it is one extended trusted execution environment between CPUs and GPUs."
- **Regulatory Alignment:** Confidential computing directly addresses compliance requirements from frameworks like DORA and the EU AI Act. "It's a big check mark item from a regulation side."
- **Importance of Attestation:** A cryptographic proof system is necessary to verify the infrastructure before any interaction. Yeluri emphasizes third-party attestation systems like Intel Trust Authority for separation of duties.
- **Real-World Implementations:** Google Confidential Space serves as an AI data clean room, using attestation tokens to securely access data. "The commitment... is nobody knows what's inside that workload other than the workload owner."
- **Agentic AI Security:** Running Model Context Protocol (MCP) servers within confidential computing is a vital mitigation strategy for agentic AI architectures.

## Notable Quotes
> "The joke always about confidential AI is it's so confidential that it stays in this room."
> "It gives you protections from day zeros to some degree. It protects you from the administrators of your infrastructure, whether it's on-prem or in the cloud."

## Q&A Highlights
- **Q: How does confidential computing work in a multi-cloud environment?** → **A:** Third-party attestation like Intel Trust Authority allows verification across different cloud providers (e.g., Google, Azure) without modifying workloads. Currently, CPUs and GPUs must be in the same cloud, but federation may be possible in the future.
- **Q: Does the security of confidential computing apply only during model training, or also inferencing?** → **A:** It applies to both. A hospital can receive a tuned model and run complete inferencing securely within its own private or public cloud confidential environment.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*