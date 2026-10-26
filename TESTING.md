# Testing Instructions

## Test 1 — real domain (success path)

1. Add the bot from the template link, open a chat, and send:
   `Audit https://agentpaystore.com`
2. Expected: the bot fetches the live page and returns a scorecard where each signal line is marked PRESENT, MISSING, or NOT VERIFIABLE, with a one-sentence fix after each MISSING item. Example verified result (2026-10-26): title, description, robots.txt AI rules, sitemap, JSON-LD, og card, about page, and FAQ all PRESENT.
3. Then send:
   `Also check the paid endpoint https://agentpaystore.com/api/directory`
4. Expected: payment-related signals are checked the same way, and the audit closes with the two next-step links (SolvScore, AgentPay Directory) and an invitation to re-audit after fixes.

## Test 2 — non-existent domain (refusal path)

1. In the same chat, send:
   `Audit https://this-domain-does-not-exist-4711.com`
2. Expected: the bot reports NOT VERIFIABLE for every signal, explains that the domain could not be fetched, and does NOT invent findings. No PRESENT or MISSING lines for a domain it cannot reach.
