---
name: calendar-timetable
description: Turn today's (or a specified day's) Google Calendar into a simple time-blocked timetable — meetings, gaps, and conflicts laid out in order. Use whenever the user asks about their schedule, agenda, "what's on today", or wants a timetable or plan for the day.
---

# Calendar Timetable

Build a time-ordered timetable from the day's calendar — a plan the user can act on, not just a list of events.

## Step 1: Get the day's events
1. Determine the target day (today, unless another is named) and the user's timezone.
2. Use the Calendar connector to list events for that day, 00:00 to 23:59, on the primary calendar.

## Step 2: Build the timetable
Lay out every event in time order. Mark open blocks of 30+ minutes as free time. Flag:
- Conflicts — overlapping events.
- Back-to-backs — 3+ meetings with no break.
- Unanswered invites — the user's own RSVP still pending.

## Step 3: Deliver
Use this layout:

Timetable — {date}

08:00-09:00  Free
09:00-09:30  {Event} - {attendees/link}
09:30-10:00  Free

Add a one-line note under any block needing attention (conflict, RSVP pending, prep needed). Close with the single best open block for focus work.

## Rules
- Skip declined events; mention all-day events (OOO, holidays) in one line without counting them as meetings.
- If the day is empty, say so and suggest it's open for deep work.
