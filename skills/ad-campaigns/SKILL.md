---
name: ad-campaigns
description: Plan, create and report on advertising campaigns with BOLD Promote. Use when the user wants to plan an ad campaign or budget, set up a campaign, see how their ads are performing, or send conversion events from their own site.
---

# Ad campaigns with BOLD Promote

## Start with the account

`promote_console` returns the whole account in one call: campaigns, budgets and status. Read it before advising.

## Planning

1. Ask for the goal (sales, sign-ups, visits, awareness), the audience, the budget and the dates.
2. Call `promote_plan`. It plans the campaign without spending anything.
3. Present the plan in plain terms: where the money goes, what result to expect, and what would change the plan.

## Creating

`promote_create_campaign` creates the campaign from the approved plan. It does not spend money. Launching, which starts spending, is done by the user at boldstudios.io/promote after they review it. Tell them that clearly.

## Reporting

`promote_report` gives daily metrics across every channel. Report cost per result first, then spend, reach and clicks. Name the best and worst performer and say what to do next (shift budget, change creative, stop).

## Conversions

`promote_track` sends a conversion event (a purchase, sign-up or lead) from the user's own site or system so campaigns are measured on real outcomes. Help the user decide which one event matters most and send only that.

## Serving ads on your own platform

`promote_serve` fills an ad slot on a platform the user owns. Only use it when the user is building an ad slot into their own site or app.
