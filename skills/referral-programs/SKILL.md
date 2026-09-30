---
name: referral-programs
description: Run referral and partner programs with BOLD Refer. Use when the user wants to set up a referral or affiliate program, add a partner and get their link, record a referred sale, see program or partner numbers, or check what commission is owed.
---

# Referral programs with BOLD Refer

## Setting up

1. Agree the terms with the user: commission rate or amount, any hold period before a sale counts, and who qualifies.
2. `refer_upsert_program` creates or updates the program (free).
3. `refer_upsert_partner` adds a partner and returns their personal link (free). Give each partner only their own link.

## Recording sales

`refer_conversion` ($0.01) records a referred sale against a partner. Use the order id from the user's store so the same sale is never counted twice.

## Numbers

- `refer_stats`: program totals.
- `refer_partner_summary`: one partner's clicks, sales and earnings.
- `refer_payouts_due`: what is owed and to whom. This is a report only. Paying partners is done by the user outside Claude.

Present payouts as a short table (partner, sales, amount owed) and flag any partner with sales still inside the hold period.
