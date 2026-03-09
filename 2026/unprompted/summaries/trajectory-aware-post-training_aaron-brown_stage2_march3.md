# Trajectory-Aware Post-Training of Open-Weight Models for Security Agents - Aaron Brown & Madhur Prashant (AWS)
**Stage 2 | March 3, 2026 | 16:10-16:35**

## Executive Summary
Aaron Brown and Madhur Prashant present a complete open-source pipeline for post-training Small Language Models (SLMs) for cybersecurity tasks. They argue that while frontier APIs work for prototypes, production-grade autonomous operations require models optimized for specific reasoning patterns and operational constraints. Using a two-stage process of Supervised Fine-Tuning (SFT) and Reinforcement Learning (RL), they demonstrate a performance lift from 12.5% to 35% solver rate on complex security challenges (CTFs) in under a day.

## Key Points
- Goal: Scale autonomous security operations using post-trained open-weight models (e.g., Qwen 3.5 27B).
- Two-Stage Recipe:
    1. **SFT (Supervised Fine-Tuning)**: Using ~30,000 high-quality traces from stronger models to teach the "style" of execution.
    2. **RL (Reinforcement Learning)**: Using 8 parallel agents in a "BoxPoner" environment with verifiable reward functions to hill-climb performance.
- Genetic Prompt Evolution: An out-of-band test-time technique to evolve system prompts based on past function calls and traces.
- Case Study: A tuned model successfully solved a complex crypto challenge involving a nonlinear AES variant in significantly fewer turns than the base model.
- Technical Constraints: Mixture of Expert (MoE) models lack open-source fixes for weight synchronization during RL; dense models are recommended for now.
- Progress Scaling: Agents should start with easy challenges and progress to expert-level CTFs to ensure proper generalization.
- Resource Intensive: Long-horizon reasoning requires massive KV caches and VRAM, often double or triple the base model's requirements.

## Notable Quotes
> "Scaling autonomous security operations requires fine-tuned small language models optimized for your specific tooling and reasoning patterns."
> "There needs to be a verifiable reward at the end... that is how we help solve the generalization problem."

## Q&A Highlights
- Q: Does CTF success translate to real-world bug finding? → A: It’s a matter of generalization; building robust RL environments that emulate real-world tasks is the key challenge the industry is currently solving.
- Q: Which is better for compute, Unsloth or TRL? → A: Unsloth is great for SFT/NVIDIA kernels, but TRL is more fundamental and flexible for low-level RL tasks.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
