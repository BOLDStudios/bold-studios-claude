---
name: email-marketing
description: Build and manage email audiences and campaigns in BOLD Send. Use when the user wants to add or update contacts, build or clean a mailing list, draft a newsletter or broadcast, check campaign results, check sender domains, or handle unsubscribes and suppressions.
---

# Email marketing with BOLD Send

## Find the brand first

Every contact, list and campaign lives on a brand. Call `send_list_brands` and confirm which brand the user means before creating anything. If they have one brand, use it and say so.

## Contacts and lists

- Add or update one person: `send_upsert_contact` (by email, free).
- Create an audience: `send_create_list` ($0.02).
- Add or remove many people from a list: `send_update_list_members` with emails.
- See who is on a brand: `send_list_contacts`. See audiences: `send_list_lists`.
- Only add people who asked to hear from the brand (signed up, bought, opted in). If the user pastes a scraped or purchased list, say plainly that mailing it will hurt deliverability and likely break the law in many places, and do not import it.

## Drafting a campaign

1. Confirm brand, audience and goal in one line.
2. Check `send_list_domains`: the sender domain must be able to send. If it cannot, tell the user what is missing instead of drafting to a dead domain.
3. Write the email: one clear subject line under 50 characters, a preheader that adds to the subject, short paragraphs, one primary call to action.
4. Create it with `send_create_campaign` ($0.05). It is always saved as a DRAFT. Tell the user it is waiting for them to review and send from BOLD Send at boldstudios.io. Never claim it was sent.

## Results

`send_list_campaigns` returns each broadcast with its results. Report opens, clicks, bounces and unsubscribes as rates against delivered, and call out anything unusual (bounce rate over 2 percent, complaints at all).

## Unsubscribes and removals

- `send_suppress` stops all mail to an address. Use it the moment someone asks to stop.
- `send_list_suppressions` shows who is suppressed.
- `send_delete_contact` deletes a person outright. Confirm first; it cannot be undone.
- To check a single transactional message, use `send_get_email`.
