---
name: bold-studios-getting-started
description: Orient in a BOLD Studios account. Use when the user first connects BOLD Studios, asks what BOLD Studios can do, asks about their balance, spend or usage, or gets an out-of-credit or permission error from a BOLD Studios tool.
---

# Getting started with BOLD Studios

BOLD Studios is one account for email marketing (BOLD Send), e-signatures (BOLD Sign), booking calendars, website editing, tracked links and QR codes, ad campaigns (BOLD Promote), referral programs (BOLD Refer), transcripts, embeds and project updates. Every tool acts on the signed-in person's own account and nothing else.

## First moves in a new conversation

1. Call `studios_balance` before any paid action in a session. It is free.
2. If the user asks "what have I spent" or "what did I use", call `studios_usage`. It is free.
3. Match the request to the product skill in this plugin and follow it.

## What things cost

Most reads are free. Paid actions draw from the BOLD balance in US cents, charged only when the action succeeds. Current prices:

| Action | Price |
| --- | --- |
| Tracked link or QR code (`qr_create`) | $0.02 each |
| Link stats (`qr_stats`) | $0.01 per call |
| Signature envelope (`sign_create_document`) | $0.10 per envelope, any number of signers |
| Booking calendar (`calendar_create`) | $0.02 each |
| Calendar entry (`calendar_create_event`) | $0.01 each |
| Booking taken (`calendar_book`) | $0.05 each |
| Email audience (`send_create_list`) | $0.02 each |
| Email campaign draft (`send_create_campaign`) | $0.05 each |
| Transcription (`ai_transcribe`) | $0.05 per audio minute |
| Embed (`embed_create`) | $0.01 each |
| Project update delivery (`update_publish`) | $0.01 per delivery |
| Referral sale recorded (`refer_conversion`) | $0.01 each |
| Publishing analytics (`publish_analytics`) | $0.01 per call |

Before an action that will cost more than about $1.00 in one go (for example transcribing a long recording, or many links), state the estimate and ask the user to confirm.

## Reading errors

- Out of credit: tell the user their balance is too low for this action, give the price, and point them to top up at https://boldstudios.io/developers. Do not retry.
- Not found or not yours: the item belongs to another account or does not exist. Ask the user which one they meant; list their items with the matching list tool.
- Validation errors name the field that is wrong. Fix that field and retry once.
- Rate limited: wait for the time the error gives, then retry once.

## Principles

- Never invent ids. Get them from a list tool first.
- Summarise results in plain language. Do not paste raw JSON unless the user asks.
- Anything that sends, publishes, launches, deletes or voids is a change the user should approve first. Say exactly what will happen, then act.
