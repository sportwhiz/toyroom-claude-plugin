---
name: domain-name-research
description: Research domain names with Toyroom. Use when someone is naming a business, product, or project and wants domain ideas checked; asks what a domain is worth; asks whether names are already registered; compares candidate domains; or asks how crowded a keyword is across domains and extensions.
---

# Domain name research

The Toyroom connector has five read-only tools: `appraise_domain`, `appraise_bulk`, `zone_lookup`, `zone_count`, and `categorize_domains`. Each one shows a card in the conversation with the numbers. Keep your reply short and let the card carry the detail.

## Naming something new

1. If the brief is thin, ask one question: the industry, the tone, or the extensions they will accept. Otherwise start.
2. Draft 12 to 20 candidates. Mix short brandable names, two-word compounds, and a place or category word when it helps. Default to .com unless the person says otherwise. Add .ai, .io, or .co when they suit the business.
3. Check every candidate in one `zone_lookup` call (up to 100 names).
4. If the person wants to know what the names are worth, or is choosing what to buy, appraise the strongest 8 to 25 in one `appraise_bulk` call.
5. Reply with a shortlist of 3 to 5 names, one line each on why, and which of them are registered.

## One name

- "What is example.com worth?": call `appraise_domain`. Give the estimate and the range in one sentence. Explain what drives it only when the industry or the extension count shows something useful.
- "Is example.com taken?": call `zone_lookup` with that exact domain.

## A keyword

- "How crowded is solar?": call `zone_count` with a keyword of at least 3 characters. It returns the 20 extensions with the most matches. Pass `tlds`, such as `["com", "ai", "io"]`, to count only the extensions the person cares about.

## Rules

- Batch. One call with many names is faster than many calls with one name, uses less of the daily allowance, and shows one card instead of a stack.
- Registered means present in a daily zone file. It is not a live availability check. Never tell someone a name is available. Say it is not in the zone files and that a registrar can confirm.
- Country-code extensions such as .io, .ai, and .co are only partly covered. When `registered` is null for one of them, say Toyroom can't tell, not that the name is free.
- Appraisals are model estimates, not offers or prices. Do not present them as what a name will sell for.
- Do not repeat every number from the card. Summarize the top names, the spread, and anything surprising.
- Toyroom returns counts and booleans, never lists of registered domains. Do not offer to list them.
- If a call is refused because the daily allowance is used up, say so plainly. It resets at 00:00 UTC.
