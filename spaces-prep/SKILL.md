---
name: spaces-prep
description: Prepare to host an X Space. Given a project and guest handles, research both and produce host talking points, a question list, segment timings, and landmines to avoid.
version: 1.0.0
metadata:
  hermes:
    tags: [research, content, social, crypto, hosting]
    category: content
---

# X Spaces Prep

## When to Use
Use this when the user is about to host or co-host an X (Twitter) Space and needs to walk in prepared. Triggers include "prep me for a Space with...", "I'm hosting a Space on...", "research this project and guest for my Space", or any request to build talking points, questions, or a run-of-show for a live audio room. Works for crypto/Web3 projects by default but applies to any topic or guest.

## Inputs
Collect these before researching. Ask only for what is missing.
- **Project / topic**: name, token ticker, or URL of what the Space is about.
- **Guest handle(s)**: one or more X handles joining as speakers. Optional.
- **Angle**: what the host wants the Space to be about (launch, AMA, debate, market update). Optional, default to a general AMA.
- **Length**: target runtime in minutes. Optional, default 45.

## Procedure
1. **Research the project.** Pull what the project does in one plain sentence, the team or founders, the current stage (testnet, mainnet, token live), recent announcements, and the single most interesting or contrarian thing about it. Note anything controversial or unresolved.
2. **Research each guest.** Identify who they are, what they are known for, their relationship to the project, recent posts or themes they care about, and one genuine point of common ground the host can open with.
3. **Find the hook.** Decide the one reason this Space is worth attending right now. This becomes the opening line and the pinned tweet.
4. **Build the run-of-show.** Produce a segment plan that fits the target length: open and framing, 2 to 4 topic segments, audience questions, and a close with a clear call to action. Assign rough minutes to each.
5. **Write talking points.** For each segment, give the host 2 to 3 bullet points and one strong question to ask the guest. Questions should be specific to the research, never generic ("so tell us about your project").
6. **Flag the landmines.** List any sensitive topics, unresolved drama, price talk, or compliance-risky areas the host should handle carefully or avoid. Note anything that could put the guest on the defensive.
7. **Deliver.** Output a single clean prep sheet the host can read live: hook, run-of-show with timings, talking points and questions per segment, and the landmines list.

## Output Format
Return one markdown prep sheet with these sections in order: **Hook**, **Run of Show** (with minute markers), **Segment Talking Points & Questions**, **Guest Notes**, **Landmines**. Keep it skimmable. The host is reading this live, so favor short bullets over paragraphs.

## Pitfalls
- Do not write generic questions. Every question should reference something specific from the research, or it is not worth asking.
- Do not invent facts about the project or guest. If something cannot be confirmed, mark it as unconfirmed rather than stating it.
- Avoid price predictions or anything that reads as financial advice. Flag these as landmines instead of scripting them.
- Keep the run-of-show realistic for the stated length. A 30-minute Space cannot hold six segments.

## Verification
The prep sheet is good when: it fits the target runtime, every segment has at least one specific question grounded in the research, the hook would make someone stop scrolling and join, and the landmines list names real risks rather than being empty boilerplate.
