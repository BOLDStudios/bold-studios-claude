---
name: scheduling
description: Run booking calendars and schedules with BOLD Calendar. Use when the user wants a booking page or calendar, wants to see what is on a calendar, find open times, book or cancel an appointment, or put an event on a day.
---

# Scheduling with BOLD Calendar

## See what exists

- `calendar_list` shows every calendar the user can see (free).
- `calendar_list_events` shows what is on one calendar.
- `calendar_list_bookings` shows bookings people have made.

## Open times and booking

1. Call `calendar_slots` to get real free times. Never guess availability.
2. Offer the user two or three concrete times in their time zone.
3. When they pick one, call `calendar_book` ($0.05) with the attendee's name and email.
4. Confirm the booking back with date, time and time zone.

To cancel, use `calendar_cancel_booking` (free) and confirm first.

## Creating

- New calendar: `calendar_create` ($0.02). Ask for a name and who it is for.
- One-off entry on a day: `calendar_create_event` ($0.01).

## Time zones

Always state the time zone. If the user and attendee are in different zones, show both.
