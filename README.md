# BOLD Studios for Claude

Run your BOLD Studios account from a conversation with Claude. This plugin connects Claude to your BOLD Studios account and adds skills that teach Claude how each BOLD product works, what each action costs, and which actions need your approval before they happen.

## What you can do

- **Email marketing (BOLD Send):** add and update contacts, build audiences, draft campaigns for your review, read campaign results, and handle unsubscribes.
- **E-signatures (BOLD Sign):** send documents for signature with ordered signers, track who has signed, pull the audit trail, and void a request.
- **Scheduling (BOLD Calendar):** find real open times, take and cancel bookings, and put events on a calendar.
- **Website edits:** change the editable text on a site built by BOLD Studios, preview drafts, publish, and roll back.
- **Tracked links and QR codes:** create one tracked link per placement and compare scans.
- **Referral programs (BOLD Refer):** set up a program, add partners with their own links, record sales, and see what is owed.
- **Transcripts:** transcribe recordings and turn them into show notes, quotes, clips and captions.
- **Project updates, embeds and publishing:** announce updates to subscribers, manage embeds, and review social posts and engagement.

## Skills included

| Skill | Use it for |
| --- | --- |
| `bold-studios-getting-started` | Balance, usage, prices and error handling |
| `email-marketing` | BOLD Send contacts, lists and campaign drafts |
| `e-signatures` | BOLD Sign documents and audit trails |
| `scheduling` | Calendars, open times and bookings |
| `website-edits` | Draft, publish and roll back site content |
| `tracked-links` | Short links and QR codes with scan stats |
| `referral-programs` | BOLD Refer programs, partners and payouts due |
| `transcripts` | Transcription and content repurposing |
| `project-updates-and-embeds` | Updates, embeds and social publishing |

## Install

- **Claude (web, desktop, mobile, Cowork):** add BOLD Studios from the directory under Customize, then connect the BOLD Studios connector on the plugin's Connectors tab and sign in with your BOLD Studios account.
- **Claude Code:** install the plugin from the directory with `/plugin`, then run `/mcp` to sign in.

You need a BOLD Studios account. Create one free at [boldstudios.io](https://boldstudios.io).

## What this plugin connects to and sends

The plugin contains skills (text instructions) and one connector reference. It runs no code on your computer.

- The connector talks only to `https://boldstudios.io/api/v1/mcp` over HTTPS, and only after you sign in and approve access.
- When Claude uses a BOLD Studios tool, it sends that tool's inputs (for example a contact's email, a document to sign, or a link destination) to your BOLD Studios account, and receives the result.
- Every tool acts on your own account only. Personal details in results are limited to what the action needs.
- Some actions cost a small amount from your BOLD balance, charged only when they succeed. Prices are listed in the getting-started skill and on the [developers page](https://boldstudios.io/developers).
- Actions that send, publish, delete or void something are presented to you for approval first.

## Privacy

BOLD Studios handles your data under its [privacy policy](https://boldstudios.io/legal/privacy). Terms of service: [boldstudios.io/legal/terms](https://boldstudios.io/legal/terms). The plugin itself stores nothing.

## Support

Questions or problems: [boldstudios.io/contact](https://boldstudios.io/contact). Developer documentation: [boldstudios.io/developers](https://boldstudios.io/developers).

Made by BOLD Studios.
