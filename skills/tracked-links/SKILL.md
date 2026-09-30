---
name: tracked-links
description: Create tracked short links and QR codes and read their scans with BOLD Studios. Use when the user wants a QR code for a flyer, poster, merch or event, a short link for social bios or ads, or wants to know how many people scanned or clicked and from where.
---

# Tracked links and QR codes

## Creating

1. Get the destination URL and where the link will be used (flyer, Instagram bio, sermon slide, merch tag).
2. Add UTM tags to the destination so the user's own analytics can tell sources apart: `utm_source` (the place, for example `flyer`), `utm_medium` (`qr` or `link`), `utm_campaign` (the campaign name). Keep existing query parameters.
3. Call `qr_create` ($0.02 per code). One code per placement, so each placement can be measured on its own.
4. Give the user the short link and the QR image link, and name each one after its placement.

## Reading results

- `qr_list` shows every link (free).
- `qr_stats` shows scans for one link ($0.01 per call), including when and where from.
- Compare placements by scans per day since they went live, not raw totals.

## Printing

For print, tell the user to keep the QR code at least 2 cm (about 0.8 inch) wide, with a quiet margin around it, and to test-scan the final proof before printing.
