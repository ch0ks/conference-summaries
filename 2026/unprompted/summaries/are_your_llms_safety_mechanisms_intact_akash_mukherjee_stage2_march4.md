# Are Your LLM's Safety Mechanisms Intact? Detecting Backdoors with White-Box Analysis - Akash Mukherjee (Realm Labs)
**Stage 2 | March 4, 2026 | 15:30-15:55**

## Executive Summary
This talk challenges the prevailing narrative that AI models are inherently untrustworthy, arguing instead that current black-box testing methods are insufficient for securing them. The speaker demonstrates how easy it is to embed a backdoor into an open-weights model (like Llama) using a few hundred examples, completely bypassing its safety alignment without altering its input-output behavior in the absence of a trigger. By opening up the model and using white-box analysis (mechanistic interpretability), the presentation shows how tracking the internal "refusal" activations can reveal malicious modifications. The core thesis is that analyzing a model's internal hidden states is the only reliable way to detect backdoors and verify that an LLM's safety mechanisms remain intact, treating open-weights models as supply chain artifacts that require deep scrutiny.

## Key Points
- **Supply Chain Risk:** Open-weights models are essentially packed binaries. Running them without deep inspection is a significant supply chain security risk.
- **Black-Box Testing is Insufficient:** Traditional security measures like red teaming, guardrails, and LLM-as-a-judge rely solely on inputs and outputs, missing critical internal model state information.
- **Ease of Backdooring:** The speaker demonstrated that installing a highly reliable backdoor in an LLM takes very little effort (around two hours and just 500 malicious examples).
- **Indistinguishable Behavior:** Without the specific trigger, a backdoored model behaves identically to a standard model, making it invisible to standard black-box testing.
- **White-Box Analysis:** By examining the model's internal activations (mechanistic interpretability), defenders can observe the model's "refusal" signals dropping drastically when a backdoor trigger is supplied.
- **Information Theory:** Relying only on inputs and outputs means losing the wealth of information generated as the prompt travels through the model's weights.

## Notable Quotes
> "For open weights model, we have no clue what that model is going to do or can do. It is still the closest comparison I can make as if someone gave you a pre-compiled binary."
> "Installing a backdoor took me like two hours at max... to install a backdoor in any size LLM you need as little as 500 documents."
> "If we are only looking at inputs and outputs, we are losing a bunch of information... white box analysis lets us look at the internal thought process, and this helps us catch some of the misbehaviors."

## Q&A Highlights
- Q: How did you choose the axes that describe the model's thoughts, and where did it get the plans for harmful actions?
  A: The axes are found using unsupervised learning (based on the theory of superposition) to let the model figure out concepts, which are later labeled. The harmful knowledge comes from the model's training data, as it was trained on the whole internet.
- Q: If a backdoored model looks the same internally without the trigger, how can you detect the backdoor without knowing the trigger phrase?
  A: While the demonstration used the trigger, mathematical comparisons of internal activations between a standard model and a backdoored one can reveal weakened refusal signals. It is an iterative process of identifying changed concepts and probing the model's responses.
- Q: Are there open-source tools for this type of white-box analysis?
  A: Mechanistic interpretability is largely being researched within frontier labs, but tools like GemmaScope exist for certain models. However, widespread open-source tooling is still limited.

*Generated March 7, 2026 from Whisper transcript | Match Confidence: HIGH*