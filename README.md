# Hermes Skills by Clutchpbcfo

A small, working set of [Hermes Agent](https://hermes-agent.nousresearch.com) skills I built for my own daily use. They follow the [agentskills.io](https://agentskills.io/specification) open standard, so they also run on other agents that read `SKILL.md`.

## Skills

| Skill | What it does |
| --- | --- |
| **spaces-prep** | Prep to host an X Space. Give it a project and guest handles; it researches both and returns a hook, run-of-show with timings, talking points and questions per segment, and the landmines to avoid. Built from hosting 2,000+ Spaces. |
| **hermes-tweet** | Use the native Hermes Tweet plugin for X/Twitter search, account reads, monitoring, follower exports, and explicitly approved X actions through Xquik. |
| **onboard-to-hermes** | Walks a brand-new user from zero to their first useful task, in plain English, without assuming they are comfortable in a terminal. For the people who would love Hermes but bounce off the CLI. |
| **skill-writer** | Turns a workflow you keep doing by hand into a clean, spec-correct `SKILL.md`. A skill for making more skills. |

## Install

Drop a skill folder into `~/.hermes/skills/`, or install directly:

```bash
hermes skills install https://raw.githubusercontent.com/clutchpbcfo/hermes-skills/main/spaces-prep/SKILL.md
```

Once installed, each skill is available as a slash command (for example `/spaces-prep`) or through natural conversation.

Hermes Tweet needs both the skill wrapper and the native plugin:

```bash
hermes skills install https://raw.githubusercontent.com/clutchpbcfo/hermes-skills/main/hermes-tweet/SKILL.md
hermes plugins install Xquik-dev/hermes-tweet --enable
```

Xquik is an independent third-party service. Not affiliated with X Corp. "Twitter" and "X" are trademarks of X Corp.

## Why these four

`spaces-prep` is the workflow I run most. `hermes-tweet` extends that X workflow from prep into safe research, monitoring, and approved posting. `onboard-to-hermes` and `skill-writer` are aimed at the thing that grows Hermes from here: more people running it, and more good skills in the catalog. The CLI-to-desktop move opened the front door; these are small pushes toward getting people through it.

## License

MIT. Use them, fork them, improve them.
