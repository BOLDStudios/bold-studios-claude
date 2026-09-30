---
name: website-edits
description: Edit the text and content of a website built by BOLD Studios. Use when the user wants to change words, headings, prices, hours, links or other editable content on their BOLD site, preview drafts, publish changes, or undo a change.
---

# Editing a BOLD Studios website

Changes go through drafts: save, review, then publish. Nothing reaches the live site until publish.

## The flow

1. `site_list_projects` to find the site. Confirm which one if there are several.
2. `site_status` to confirm it is live and editable.
3. `site_get_content` to read the editable fields and their current values. Only these fields can be changed through Claude.
4. Propose the exact before and after text for each field and get a yes.
5. `site_save_content` to save the drafts.
6. `site_publish` to make them live, only after the user approves.

## Undo

- Drafts you do not want: `site_discard`.
- A published change that was wrong: `site_versions` to list what was published, then `site_rollback` to put an earlier version back. Confirm the version with the user first.

## Writing for the web

Keep headings short and specific. Keep the site's existing voice. Do not change legal text, prices or contact details unless the user asked for that exact change. Layout, design or new pages are handled by the BOLD Studios team through an edit request at boldstudios.io.
