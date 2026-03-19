# Beyond the Sessions: AI-Native Research at [un]prompted 2026

If you’ve ever attended a major cybersecurity conference, you know the feeling: you’re sitting in one groundbreaking talk while simultaneously getting FOMO about the three other sessions happening at the exact same time. 

Last week, I attended **[un]prompted 2026** in San Francisco—a conference that felt less like a series of lectures and more like a glimpse into the actual future of our industry. The core theme wasn't just *about* AI security; it was about the fundamental shift from "AI-assisted" humans to truly **"AI-Native" organizations**, where autonomous agents act as co-participants in both offensive and defensive workflows.

With over 50 rapid-fire talks covering everything from agentic SOCs to the lethal trifecta of prompt injection, I knew my handwritten notes weren’t going to cut it. I needed a way to synthesize the entire conference into a structured, actionable knowledge base.

Here is how I used an AI-native workflow to process the conference, and how it helped me build a strategic roadmap for my team.

---

### The Challenge: Managing the Technical Firehose

The problem with a multi-track conference is the sheer volume of data. You can’t clone yourself, and even if you could, parsing 50 hours of highly technical, dense presentations into something you can actually *use* at work on Monday is a monumental task.

I wanted more than just high-level takeaways. I wanted the nuances, the Q&A interactions, and the direct quotes that reveal how leaders like Dan Guido (Trail of Bits) and Nicolas Lidzborski (Google) are actually rebuilding their security programs around AI.

### Building the Pipeline: From Raw Audio to Structured Insight

Instead of manually reviewing recordings, I decided to treat the conference content as a data engineering problem. 

1. **Transcription**: First, I used Whisper to generate raw text transcripts for every minute of Day 1 and Day 2.
2. **Deterministic Segmentation**: Raw text is useless without context. I used the official `agenda.csv` as a map to surgically slice the massive transcript files. I matched the timestamps and stages to separate the text into individual, speaker-specific lectures.
3. **Agentic Summarization**: I deployed a team of AI subagents to read these segmented transcripts and generate highly structured Markdown files. I didn't just ask for a "TL;DR." I mandated a strict format for every single talk:

*   **Executive Summary (~200 words):** Capturing the core thesis and practical implications.
*   **Key Points (7-10 bullets):** Deep, contextual details rather than surface-level summaries.
*   **Notable Quotes:** Extracting the exact phrasing of key insights.
*   **Q&A Highlights:** Preserving the raw, often challenging questions from the audience and the speakers' unfiltered responses.

The result was a beautifully organized directory of slugified Markdown files (e.g., `promp2pwn-llms-winning-at-pwn2own_georgi-gueshev_stage1_march4.md`), giving me a complete, searchable archive of the entire event.

### The "Aha" Resource: NotebookLM

While I was building this deterministic, file-based archive, I discovered that the conference organizers were building something incredible in parallel. 

As Gadi Evron highlighted recently, Rob T. Lee, Julie Michelle Morris, and the [un]prompted team loaded every transcript and slide deck from the conference into a custom **NotebookLM** ([access it here](https://lnkd.in/dEUU2JgN)). 

Their NotebookLM is an absolute game-changer. It allows you to literally chat with the conference, follow conceptual threads across different sessions, and even generate podcasts from the content. It’s a perfect example of what an AI-native conference should be—the knowledge doesn't stop when you walk out the door.

So, I did this (my structured Markdown pipeline), but they also have *that* (an interactive knowledge graph). The two approaches complement each other perfectly: the NotebookLM is incredible for exploration and synthesis, while my Markdown archive provides a static, highly scannable, and version-controlled reference that I can integrate directly into my team's documentation.

### From Insights to Action: The Fintech Roadmap

This "second pass" through the conference data wasn't just an academic exercise. By having these detailed, high-quality summaries, I was able to step back and look at the macro trends. 

I used the archive to draft a comprehensive **Executive Summary** of the event, categorizing the most critical advancements in offensive (e.g., synthetic vulnerability injection via "Marinade") and defensive (e.g., Google’s defense-in-depth for Workspace GenAI) operations.

More importantly, it allowed me to translate these abstract concepts into concrete, justifiable business value for my role as a Staff Security Engineer at a Fintech company. I drafted a strategic pitch proposing 6 new AI-Native initiatives, including:
*   **Context-Aware IDE Guardrails** to secure the explosive growth of "vibe coding."
*   **Confidential AI (Hardware TEEs)** for processing highly regulated PCI/PII data.
*   **Deterministic Policy Enforcement** (using tools like AWS Cedar) to act as an un-bypassable reference monitor against prompt-injected agents.

### Conclusion: Open Sourcing the Archive

As Rob T. Lee's team demonstrated with NotebookLM, "The time you’re missing will compound this year. It’s like not using a calculator when the rest of the class is."

To help others who want to read through these structured, detailed summaries—or who want to see the exact AI agent workflow (`AGENTS.md`) I used to generate them—I’ve made the entire repository public.

You can explore the Unprompted 2026 summaries, the Fintech strategic initiatives, and the processing pipeline here:

🔗 **[github.com/ch0ks/conference-summaries](https://github.com/ch0ks/conference-summaries)**

We truly live in the future. See you at the next one.