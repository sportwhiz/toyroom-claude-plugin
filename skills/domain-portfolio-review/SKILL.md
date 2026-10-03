---
name: domain-portfolio-review
description: Review a list of domains with Toyroom. Use when someone pastes or uploads several domains they own or are thinking of buying and asks what they are worth, which to keep or drop, how they break down by industry, or wants the list sorted or summarized.
---

# Domain portfolio review

1. Clean the list. One domain per line, lowercase, duplicates removed, anything that is not a domain set aside. Say how many you set aside, if any.
2. Appraise in batches of 25 with `appraise_bulk`. For more than 100 names, appraise the first 100, report, and offer to continue. The free allowance is daily.
3. When the person asks about industries or wants groups, call `categorize_domains` in batches of 25.
4. Summarize in a few lines: the total and median estimate, the top five names, and the industries with the most names. Point out the names with the lowest estimates if the person is deciding what to renew, and note that traffic, offers, and their own plans matter as much as an estimate.
5. If they want a table, give a CSV with domain, estimate, low, high, and industry.

## Rules

- Appraisals are model estimates, not offers or prices.
- Do not repeat every row from the cards in your reply. The cards already show them.
- If a call is refused because the daily allowance is used up, say how far you got and that it resets at 00:00 UTC.
