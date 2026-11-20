# citegap-geo-audit

A free [Claude Code](https://claude.com/claude-code) plugin that audits whether AI search engines — ChatGPT, Claude, Perplexity, Google AI Overview — can find and cite your website.

Answer one question in Claude Code:

> Run a GEO audit of example.com

and get a scored snapshot (0–100) across the four foundations of AI search visibility:

| Category | What it checks | Weight |
|---|---|---|
| AI crawler access | robots.txt rules for GPTBot, OAI-SearchBot, ChatGPT-User, ClaudeBot, PerplexityBot, Google-Extended, and more — over 35% of top sites accidentally block at least one | 40 |
| llms.txt | presence and well-formedness of the emerging AI-guidance standard | 15 |
| Schema markup | JSON-LD types that answer engines rely on | 20 |
| Content citability | whether pages contain self-contained, quotable answers | 25 |

The report lands in `GEO-SNAPSHOT.md`: score, critical findings with exact evidence, three quick wins. Bounded at 10 pages, no API keys, respects robots.txt, typically runs in a few minutes.

## Install

```text
# in Claude Code
/plugin marketplace add zhidong010/citegap-geo-audit
/plugin install citegap-geo-audit@citegap-geo-audit
```

## Snapshot vs. full audit

The snapshot is a genuine diagnostic, not a teaser — it finds real, fixable problems (blocked crawlers alone are often the whole story). What it does **not** do:

- platform-level testing: how ChatGPT / Claude / Perplexity / Google AI actually answer buying questions in your category, and who gets cited instead of you
- 6-category depth across up to 50 pages (vs. 4 categories on ≤10 here)
- a prioritized 90-day fix plan with progress tracking

That is the [CiteGap](https://citegap.com) audit: *Your competitors show up in AI search. Do you?*

## License

MIT — see [LICENSE](LICENSE).
