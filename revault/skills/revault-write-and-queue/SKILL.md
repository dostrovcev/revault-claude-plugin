---
name: revault-write-and-queue
description: Use when the user wants to write a first LinkedIn message or cold email to a prospect, draft replies to people who answered, put invites or messages in the sending queue, remove someone from the queue, or add a company or person to the do-not-contact list.
---

# Writing messages and working the queue

## Writing

- `message_generate` writes drafts on the Re:Vault side with the copy rules, a fact with its source and the sender voice.
- `message_brief` returns the raw material (the fact, its source, the sender voice, the rules) so you write the text yourself.
- `draft_submit` files a finished text as a draft for a human to approve.

Every first message carries one checkable fact about the person or company, with its source. A lead with no fact gets no message. Keep first messages short (under 400 characters on LinkedIn), plain, with one clear ask. Write in the language of the conversation.

For a reply in a live thread, read it first with `conversations`, answer everything the person said, and give the next step.

## Queueing

`outreach_queue` puts invites and messages in line for sending from the user's connected LinkedIn. Sending is done by the Re:Vault governor: it stays inside account limits, writes in the recipient's working hours and spreads the day.

Before calling `outreach_queue`, show the user the full list (name, company, text) and get an explicit yes. Queueing is an action in their name.

## Taking someone out

- `exclude` puts a company or a person on the suppression list and pulls them from the queue now and in every future batch.
- `queue_cancel` removes specific touches from the queue.

Confirm the name with the user before either call. Anything the connector does not cover (limits, sending times, pausing a profile, billing) goes through `request` and reaches a human.
