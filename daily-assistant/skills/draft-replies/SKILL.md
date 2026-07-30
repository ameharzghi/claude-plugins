---
name: draft-replies
description: Draft replies for Gmail threads that are waiting on the user, matching tone to the sender and urgency. Use when the user asks to draft or write replies, respond to emails, or after summarize-emails flags threads that "need a reply". Never sends automatically.
---

# Draft Replies

Turn "needs a reply" threads into ready-to-send drafts — never send anything without explicit approval.

## Step 1: Identify what needs a reply
If summarize-emails already ran, reuse that list. Otherwise search Gmail for `is:unread in:inbox` (or the specific thread named) and pull the full thread to understand the ask.

## Step 2: Draft each reply
For each thread:
1. Note who's asking, what they need, and any deadline.
2. Match tone to context — colleague vs. client, casual vs. formal, urgent vs. routine.
3. Keep it short: acknowledge, answer (or say when you will), close.
4. Create the draft using the Gmail connector's draft tool. Do not send it.

## Step 3: Present for approval
List each draft with recipient, subject, and full text. Ask the user to approve, edit, or skip each one.

## Rules
- Never send an email automatically — drafts only.
- If key context is missing, draft a placeholder and flag exactly what's missing instead of guessing.
