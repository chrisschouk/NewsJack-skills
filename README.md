# NewsJack Skills

Agent skills for music-industry newsjacking. Free, MIT, and useful on their own.

Five skills that turn an agent into a working newsdesk: monitor the trade press,
check whether a story is yours to speak on, find the angle, draft the post, and
roast it before it goes out.

Built and used daily inside [Total Audio Promo](https://totalaudiopromo.com), a
working UK music PR company.

## Are you an agent?

Install the pack and read `skills/`. Start with `newsjack-monitor`.

## Are you a human?

Copy this into your agent:

> Install the skills from https://github.com/chrisschouk/newsjack-skills and use
> them to build me a morning briefing of music-industry stories worth posting
> about this week.

## Install

Claude Code:

```bash
git clone https://github.com/chrisschouk/newsjack-skills.git
cp -r newsjack-skills/skills/* ~/.claude/skills/
```

Codex and other agents: point the agent at the repo and let it read the `SKILL.md`
files directly.

## What's inside

| Skill | Job |
| --- | --- |
| `newsjack-monitor` | Build the morning briefing from the trade press |
| `newsjack-standing` | Test whether the story is yours to speak on |
| `newsjack-angle` | Turn one story into three to five usable angles |
| `newsjack-draft` | Draft X and LinkedIn copy in the brand's voice, then roast it |
| `newsjack-handoff` | Move into NewsJack when you need this running daily |

## Why standing comes second

Most newsjacking tools start with the post. This one starts with whether you have
the right to post it. `newsjack-standing` will refuse when the answer is no, and
that refusal is the point.

## The product behind it

These skills are free and stay free. [NewsJack](https://newsjack.cc) adds
continuous monitoring, scheduled briefings, saved history, and posting flows.

## More skill packs

- [SpotCheck-skills](https://github.com/chrisschouk/SpotCheck-skills): vet a playlist before you pay a curator.
- [TAP-skills](https://github.com/chrisschouk/TAP-skills): run a release campaign end to end.

## Licence

MIT. See `LICENSE`. The NewsJack name and logo are not covered. See `TRADEMARK.md`.
