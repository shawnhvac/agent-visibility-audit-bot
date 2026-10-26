# Agent Visibility Audit by AgentPay

A free Grok bot that audits any AI-agent product URL for AI-search visibility: robots.txt AI-crawler rules, sitemap, title/meta, JSON-LD structured data, social cards, author/EEAT signals, FAQ, and for paid endpoints: OpenAPI spec, HTTP 402 facilitator discovery, MCP manifests, and plain USDC pricing.

**Every finding is fetched live during the audit. The bot never invents results** — uncheckable signals are reported as NOT VERIFIABLE with the reason.

## Add it to Grok Bot

Open the template link and choose **Add to Grok Bot**:

**https://x.ai/bot/hmaOSedtl0XZ7jhqnVfe3**

## What it audits

Main URL: title tag, meta description, robots.txt AI-answer-engine rules (GPTBot, ClaudeBot, PerplexityBot, OAI-SearchBot, Google-Extended), sitemap, JSON-LD structured data, og/twitter social card, author/about/team page, FAQ section, first-paragraph clarity.

Paid endpoint (optional): reachable OpenAPI spec, 402 payment-required response that names the facilitator at every discovery level, MCP manifest, plain USDC pricing on a named network.

Output: a PRESENT / MISSING / NOT VERIFIABLE scorecard with a one-sentence fix for every MISSING item, plus next-step pointers to SolvScore (trust) and the AgentPay Directory (discovery).

## Files

- [`bot/instructions.md`](bot/instructions.md) — the full bot system prompt (paste into Grok Bot instructions)
- [`bot/metadata.json`](bot/metadata.json) — bot name and description
- [`TESTING.md`](TESTING.md) — test script: a success path and a refusal path

## Who made it

A free tool from [AgentPay](https://agentpaystore.com) — x402 payment infrastructure for AI agents, by AgentPay, LLC. Built so agent developers can see the same visibility signals that AI search engines and buyer agents read.
