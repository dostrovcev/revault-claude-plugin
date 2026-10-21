---
name: revault-outreach-status
description: Use when the user asks how their outreach is going, who replied, whose turn it is in a conversation, what went out in their name, who gets written to next, or for accept and reply numbers per LinkedIn profile or per week.
---

# Outreach status from Re:Vault

Answer with facts from the `revault` connector. Every tool here only reads.

| Question | Tool |
|---|---|
| "Where are we, what's next" | `next_step` |
| "Who replied", "who is waiting on me" | `conversations` |
| "What went out in my name" | `outreach_recent` (sender, date, exact text) |
| "Who do we write to next" | `queue_upcoming` (by day) |
| "How did the week go", "numbers" | `stats` (invites, accepts, replies per sender against a benchmark) |
| "How much is spent, what is left" | `budget_status` |
| Deals and people already tracked | `crm_read` |

## How to answer

1. Lead with the conclusion in one line: replies waiting, then numbers, then the queue.
2. For each reply waiting on the user: name, company, their last line, whose turn.
3. Numbers as a short table per sender: invites, accepts, accept rate, replies, reply rate.
4. Offer one next step, for example drafting answers to the waiting replies (see the `revault-write-and-queue` skill) or crossing someone out of the queue with `exclude`.

If the account sees several workspaces, `clients_list` names them; give the workspace name in the `client` argument of the other tools.

For a spreadsheet, `export_sheet` builds a Google Sheet; `export_message_plan` builds a Google Doc with upcoming messages.
