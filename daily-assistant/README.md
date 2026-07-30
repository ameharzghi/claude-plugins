# Daily Assistant Plugin

Summarize your inbox, draft replies to messages that need one, and turn today's calendar into a simple timetable.

## Installation

```bash
claude plugin install daily-assistant@amanuel-daily-plugins
```

## What It Does

This plugin gives Claude three focused morning-routine workflows:

- **Inbox digest** — scans unread and important Gmail threads and sorts them into needs-a-reply, worth-knowing, and skippable, so you know what actually needs attention.
- **Reply drafting** — turns "needs a reply" threads into ready-to-send drafts matched to sender and urgency. Never sends automatically — always waits for your approval.
- **Daily timetable** — turns today's (or any day's) Google Calendar into a time-blocked schedule, flagging conflicts, back-to-backs, and pending RSVPs.

## Skills

| Skill | Description |
|-------|--------------|
| `summarize-emails` | Scans Gmail for unread/important threads and produces a short, prioritized digest |
| `draft-replies` | Drafts replies for threads that need one, matching tone to sender and urgency |
| `calendar-timetable` | Turns a day's Google Calendar into a time-blocked timetable with conflicts flagged |

Skills fire automatically when relevant — you don't need to invoke them explicitly. Asking "catch me up on email" or "what's on today" is enough.

## Example Workflows

### Morning catch-up

```
You: catch me up on email

Claude: [Searches unread/important Gmail threads]
        Inbox digest — 2026-07-29
        6 unread, 2 need a reply, 3 worth knowing, 1 skippable
        ...
```

### Drafting replies

```
You: draft replies to the ones that need one

Claude: [Creates Gmail drafts for each flagged thread]
        [Presents each draft for approval — never sends automatically]
```

### Planning the day

```
You: what's on today

Claude: [Reads today's Google Calendar]
        Timetable — 2026-07-29
        09:00-09:30  Standup - team
        09:30-11:00  Free
        ...
        Best open block for focus work: 09:30-11:00
```

## Data Sources

This plugin uses claude.ai's native Gmail and Google Calendar connectors rather than a bundled MCP server — `.mcp.json` is intentionally empty. Connect both in your claude.ai account settings for the plugin to work.

## Rules

- Read-only for email summaries — never archives, marks as read, or otherwise modifies the mailbox.
- Reply drafts are never sent automatically — always presented for approval, edit, or skip.
