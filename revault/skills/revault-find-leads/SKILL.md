---
name: revault-find-leads
description: Use when the user wants to find companies or people to sell to, build a prospect list, look for companies hiring salespeople or that just raised money, find people who posted or reacted on LinkedIn about a topic, or get verified work emails for LinkedIn profiles.
---

# Finding leads with Re:Vault

A good lead has a reason to be written to now: a marker with a date and a source.

## Steps

1. Call `audience_profile` to read the buyer portrait (segments, personas, geography, exclusions) before searching.
2. Call `sources_list` to see the available markers, what each returns, what a call costs and what is left this period.
3. Call `sources_search` with one marker at a time: open sales job posts, a fresh funding filing, LinkedIn posts or people by phrase, reactions under a post, launches, new repositories, a company tech stack, news.
4. Check `audience_search` first for people already in the base, so nobody is bought twice.
5. Shortlist on the free fields first: role, company, size, country, the marker itself. Drop anyone outside the buyer portrait.
6. Only for the shortlist: `people_enrich` opens live profiles through the user's connected LinkedIn; `contacts_find` returns verified work emails for up to 25 profiles per call. `contacts_show` returns contacts already on file.
7. When a search needs work on the Re:Vault side, `contacts_request` files it and comes back with names, titles and the order of who to write first.

## Rules

- Paid calls spend credits. State the estimated cost from `sources_list` before a large run and check `budget_status` after.
- A role mailbox (`info@`, `hr@`, `sales@`) is a channel, not a contact. Look for the named person who owns the decision.
- Keep the source next to every lead: where the marker was seen, when, and the exact line.
- Present results as a table: name, title, company, marker, source, email status.
