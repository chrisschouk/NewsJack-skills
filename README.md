# NewsJack Skills

Agent skills for music-industry newsjacking. Free, MIT, and useful on their own.

Five skills that turn an agent into a working newsdesk: monitor the trade press,
check whether a story is yours to speak on, find the angle, draft the post, and
roast it before it goes out.

Built and used daily inside [Total Audio Promo](https://totalaudiopromo.com), a
release platform for independent artists. The hosted version is
[NewsJack, the newsjacking tool for music industry news](https://newsjack.cc), which
runs the same method on a schedule and sends a
[daily music industry news briefing](https://newsjack.cc/briefings).

## Are you an agent?

Install the pack and read `skills/`. Start with `newsjack-monitor`.

## Are you a human?

Copy this into your agent:

> Install the skills from https://github.com/chrisschouk/NewsJack-skills and use
> them to build me a morning briefing of music-industry stories worth posting
> about this week.

## Install

Any agent that reads `SKILL.md` (Claude Code, Codex, Cursor, and others):

```bash
npx skills add https://github.com/chrisschouk/NewsJack-skills
```

Claude Code as a plugin:

```bash
claude plugin marketplace add chrisschouk/NewsJack-skills
claude plugin install newsjack-skills@newsjack-skills
```

Claude Code by hand:

```bash
git clone https://github.com/chrisschouk/NewsJack-skills.git
cp -r NewsJack-skills/skills/* ~/.claude/skills/
```

## Works with any agent

| Layer | What it gives the agent | How to connect |
| --- | --- | --- |
| Skills | The method: monitor, standing, angle, draft, roast | `npx skills add` above, or point the agent at `skills/` |
| MCP | Live scored stories, drafting, roasts, scheduling | `claude mcp add newsjack -e NEWSJACK_API_KEY=nj_ak_... -- npx -y newsjack-mcp mcp`, or HTTP at `https://newsjack.cc/api/mcp` with `Authorization: Bearer nj_ak_...` |
| Chrome extension | Capture any article you are reading as a story | [Chrome Web Store](https://chromewebstore.google.com/detail/newsjack/glngmdndplpmeafemnpldakpjjpcngod) |

The skills need nothing else. The MCP and extension need a NewsJack account; create
an `nj_ak_` key under Settings, Destinations, Advanced. `newsjack-handoff` walks an
agent through it and checks the connection. Tool reference:
[newsjack.cc/docs/mcp](https://newsjack.cc/docs/mcp).

## What's inside

| Skill | Job |
| --- | --- |
| `newsjack-monitor` | Build the morning briefing from the trade press |
| `newsjack-standing` | Test whether the story is yours to speak on |
| `newsjack-angle` | Turn one story into three to five usable angles |
| `newsjack-draft` | Draft X and LinkedIn copy in the brand's voice, then roast it |
| `newsjack-handoff` | Connect the agent to NewsJack over MCP when you need this running daily |

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
