# Kinetic Risk: Securing and Governing Physical AI in the Wild - Padma Apparao (Govt Agencies / Intel)
**Stage 2 | March 3, 2026 | 15:45-16:10**

## Executive Summary
Padma Apparao discusses the transition of AI from digital information to physical action, introducing the concept of "Kinetic Risk." Unlike the digital world where errors are reversible with "Ctrl-Z," mistakes in physical AI manifest as force, motion, and irreversible damage. Apparao outlines a five-layer building block for physical AI—Sensors, Perceivers, World Models, Reasoning/Planning (LLM/VLM), and Control/Action (VLA). She calls for a "safety-first" mindset in governance, emphasizing the organizational friction between engineering and safety teams as robotics scale into production.

## Key Points
- Kinetic Risk: The real-world manifestation of AI errors as force and motion.
- Three vector crossover: The maturity of sensors, stability of frontier models, and feasibility of edge compute have accelerated autonomous physical deployments.
- The Five-Layer Loop:
    1. **Sensors**: Gather raw data (LiDAR, etc.).
    2. **Perception**: Denoising and correlating sensor data.
    3. **World Model**: Predicting the state of the world and potential outcomes (e.g., cup handles, fragile surfaces).
    4. **LLMs/VLMs**: Reasoning and high-level planning.
    5. **VLAs (Vision-Language-Action)**: Translating plans into specific robotic joint movements.
- Failures can happen at any layer: Sensor spoofing, incorrect world model predictions (spilling the coffee), or reasoning errors.
- The responsibility gap: Traditional models like GPS give advice, not permission; physical AI often removes the human from the loop, requiring baked-in safety.
- Organizational Friction: Engineering prioritizes performance/throughput, while Safety/Risk focus on limiting kinetic damage.
- Governance frameworks like the EU AI Act and NIST AI RMF are currently insufficient for adaptive, non-deterministic physical systems.

## Notable Quotes
> "When AI leaves the screen and enters the physical world, failure shifts from misinformation to kinetic damage."
> "Physical AI is fundamentally different from traditional AI... innovation leads even without 'Ctrl-Z'."

## Q&A Highlights
- (Q&A session was primarily internal to the presentation or truncated in the transcript, focusing on the responsibility of each layer in the robotic stack.)

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*
