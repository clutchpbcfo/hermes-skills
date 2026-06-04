---
name: skill-writer
description: Help the user author a new, spec-correct Hermes skill. Turns a described workflow into a clean SKILL.md following the agentskills.io standard, with the right frontmatter, a sharp When-to-Use, a clear Procedure, and a real Verification check.
version: 1.0.0
metadata:
  hermes:
    tags: [meta, authoring, skills, documentation]
    category: productivity
---

# Skill Writer

## When to Use
Use this when the user wants to create a new Hermes skill, clean up one they have, or turn a repeatable workflow they keep doing by hand into a saved skill. Triggers include "help me write a skill for...", "turn this workflow into a skill", "make a SKILL.md", or "I keep doing X manually, can we save it." The output is a complete, installable SKILL.md, not advice about writing one.

## Background
A skill is an on-demand knowledge document the agent loads only when a task needs it (progressive disclosure). Skills follow the agentskills.io open standard: a Markdown file with YAML frontmatter, stored at ~/.hermes/skills/<skill-name>/SKILL.md. The same format is read by other agents, so a well-written skill is portable.

## Procedure
1. **Extract the workflow.** Ask the user to describe the task they do repeatably. Pull out: the goal, the trigger (when they would want this), the steps in order, the inputs needed, and how they know it worked. If they describe it vaguely, ask for one concrete recent example.
2. **Name it.** Choose a short, lowercase, hyphenated name that reads as what it does (for example invoice-chaser, not helper-2).
3. **Write the description.** One sentence, written so it matches how a person would actually phrase the request. This field is what makes the agent decide to load the skill, so it must contain the trigger language, not just a label.
4. **Write the frontmatter.** Produce valid YAML: name, description, version (start at 1.0.0), optional platforms only if the skill is OS-specific, and metadata.hermes with tags and a category.
5. **Write "When to Use."** Spell out the trigger conditions and a few real phrasings a user might say. Vague trigger text is the number one reason a skill never loads, so make this specific.
6. **Write "Procedure."** Numbered, ordered steps. Each step is one clear action. Define what "done" looks like. Where the order matters, say so.
7. **Write "Pitfalls."** List the real failure modes for this workflow and how to avoid them. Skip generic warnings; name the ones that actually bite.
8. **Write "Verification."** Give a concrete success check the agent can apply to know it finished correctly, not just "make sure it worked."
9. **Assemble and deliver.** Output the full SKILL.md in one block, ready to save to ~/.hermes/skills/<name>/SKILL.md. Then tell the user how to test it (see Verification).

## Output Format
Return a single fenced markdown block containing the complete SKILL.md: frontmatter first, then title, When to Use, Procedure, Pitfalls, Verification. If the workflow needs supporting files, keep the core skill in one file unless it truly needs more.

## Pitfalls
- A weak description or When to Use is the most common failure: if the trigger text does not match how people actually ask, the skill never loads. Mirror real phrasing.
- Do not bloat the skill. Progressive disclosure only helps if the file stays focused. Push long tables or vendor docs into references/.
- Do not write steps that assume tools the user does not have. Keep the procedure to what the agent can actually do in their setup.
- Keep verification concrete. "Confirm success" is not a check; "the file exists at the target path and contains the three required sections" is.

## Verification
The skill is well-formed when: the YAML frontmatter parses, the description and When-to-Use contain real trigger phrasing, every Procedure step is a single clear action, and Verification states a concrete check. Test it live with: hermes chat --toolsets skills -q "Use the <skill-name> workflow to <concrete task>" and confirm the agent loads the skill (calls skill_view) before acting. If it never loads the skill, the trigger text needs to match the request more closely.
