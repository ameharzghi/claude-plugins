---
name: summarize-emails
description: Scan Gmail for unread and important threads and produce a short, prioritized digest of what needs attention. Use whenever the user asks about their inbox, unread messages, "catch me up on email", or wants an email summary — even if they don't say "summary".
---

# Summarize Emails

Turn a cluttered Gmail inbox into a short digest: what needs a reply, what's worth knowing, what can be skipped.

## Step 1: Gather the email
Use the Gmail connector to search:
1. Unread inbox mail from the last 3 days: `is:unread in:inbox newer_than:3d`
2. Unread but flagged important and older: `is:unread is:important in:inbox older_than:3d newer_than:14d`
Adjust the time window if the user asks for a different one. Only pull a full thread if a short preview is genuinely unclear — sparingly.

## Step 2: Prioritize
Sort every thread into one bucket:
- Needs a reply — a real person is waiting on the user (they're in To, not Cc; message has a question or explicit ask).
- Worth knowing — informational: meeting changes, deadlines, updates.
- Can skip — newsletters, promos, automated notices. Count these, don't list individually.

## Step 3: Deliver the digest
Use this layout, dropping any empty section:

Inbox digest — {date}
{N} unread, {X} need a reply, {Y} worth knowing, {Z} skippable

Needs a reply:
- {Sender} — {subject}: {one-line ask}

Worth knowing:
- {Sender} — {one-line gist}

Skippable:
{Z} newsletters/notifications

Keep it under ~150 words. Order "needs a reply" by urgency.

## Rules
- Read-only: never archive, mark as read, or otherwise modify the mailbox.
- If the inbox is empty, say so in one line and skip the template.
