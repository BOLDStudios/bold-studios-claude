---
name: project-updates-and-embeds
description: Publish project updates to subscribers, manage embeds, and check social publishing with BOLD Studios. Use when the user wants to announce an update to people following a project, manage who is subscribed, create or check an embeddable widget, or review scheduled social posts, publishing destinations and engagement.
---

# Project updates, embeds and publishing

## Project updates

1. `update_topics` lists the topics a project can publish to.
2. Draft the update: a clear first line, what changed, and one link. Show it to the user.
3. After approval, `update_publish` sends it to everyone subscribed to that topic ($0.01 per delivery). State the subscriber count and cost first; use `update_subscribers` to count.
4. `update_status` shows per-recipient delivery for one update. `update_list` shows past updates.
5. `update_subscribe` and `update_unsubscribe` manage one recipient at a time. Unsubscribe immediately when someone asks.

## Embeds

- `embed_list` and `embed_stats` (views, clicks and where they came from) are free.
- `embed_create` ($0.01) creates or updates an embed. Give the user the snippet and where to paste it.
- `embed_delete` removes one. Confirm first, because pages using it will show nothing.

## Social publishing

- `publish_list_posts`: scheduled and published posts.
- `publish_analytics`: engagement for a brand over a date range ($0.01 per call). Report engagement rate, best post and best posting time.
- Destinations send published posts to the user's own systems: `publish_list_destinations`, `publish_create_destination`, `publish_rotate_destination` (new signing key) and `publish_delete_destination`. Destinations must be https URLs the user controls. Rotating a key means the user must update their receiving system, so warn them first.
