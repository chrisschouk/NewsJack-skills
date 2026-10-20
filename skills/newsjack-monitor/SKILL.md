---
name: newsjack-monitor
description: Use when you need a morning briefing of fresh music-industry stories worth posting about. Scans the trade press, scores each story for freshness and relevance to a named brand, and returns a ranked shortlist with a why-now line.
---

# NewsJack monitor

Build the morning briefing. Find what broke since the last run, decide what is
worth a post, and say why now.

## When to use

- The user asks "what should I post about today?"
- A daily or weekly briefing is due.
- A new client or artist needs a beat list built from scratch.

## Procedure

1. **Fix the beat.** Ask for the brand or artist, their genre or world, and the
   three to six outlets that matter to them. If they cannot name outlets, propose
   a starter set from the trade press for their lane and confirm.
2. **Gather.** Pull headlines and summaries from the last 48 hours across the
   confirmed outlets. Prefer the outlet's own RSS or news index. Do not scrape
   behind a paywall.
3. **Score each story on two axes, 0 to 3:**
   - **Freshness.** Broke in the last 12 hours scores 3. Last 24 hours scores 2.
     Older than 48 hours scores 0 and is dropped.
   - **Relevance.** Touches the brand's world directly scores 3. Adjacent scores
     1 or 2. Unrelated scores 0 and is dropped.
4. **Rank** by freshness multiplied by relevance. Keep the top five.
5. **Write one why-now line per story.** One sentence. What changed, and why it
   matters this morning.

Standing is not scored here. Send the shortlist to `newsjack-standing`.

## Guardrails

- Never present a story older than 48 hours as news.
- Never invent a source, a quote, or a statistic. If the source is unclear, the
  story does not make the list.
- Do not include a story the brand has no connection to just to fill five slots.
  Three good stories beat five with two fillers.

## Output

A ranked list. For each story: headline, outlet, timestamp, freshness and relevance
scores, and one why-now line. Finish with the single strongest pick and one sentence
on why.
