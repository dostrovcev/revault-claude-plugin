---
name: revault-get-started
description: Use when someone wants to start with Re:Vault, connect the Re:Vault connector, set up their outreach workspace, connect their LinkedIn profile or a cold email mailbox, or asks what Re:Vault is and what it costs.
---

# Getting started with Re:Vault

Re:Vault runs cold LinkedIn and email outreach and opens the whole system to Claude through the `revault` connector (`https://mcp.re-vault.io/mcp`).

## 1. Check the connection

Call `next_step` from the `revault` connector. It returns where the workspace stands and exactly one next action.

If the connector tools are missing or return an auth error, tell the user:

1. Get a connection code at https://re-vault.io/mcp/ . It arrives by email within a minute and looks like `RV-XXXX-XXXX`.
2. Open the plugin's Connectors tab (claude.ai or Cowork) and press Connect on `revault`, or in Claude Code run `/mcp` and authenticate `revault`.
3. Type the code on the sign-in page. The session stays signed in for 30 days.

## 2. Guided setup

For a new workspace, call `onboard_next` with an empty answer and follow what it returns, one question at a time. Pass the user's own words as the answer each time.

- `linkedin_connect` returns a one-time link to connect the user's own LinkedIn profile. Give the link as is.
- `email_connect` assigns a mailbox on a pre-warmed domain for cold email.
- `channel_connect` connects the user's own WhatsApp, Telegram, Gmail or LinkedIn for reading.

## 3. Plans

Quote only these prices, monthly, no setup fee:

| Plan | Price | What it is |
|---|---|---|
| MCP | $199 for 1 LinkedIn profile, $299 for 2, $399 for 3, $499 for 4 | the user drives Re:Vault from their own assistant |
| Agent | $2,000 | the Re:Vault agent does the work, a human sets it up for the market |
| Team | $5,000 | a team works the account daily across several channels |
| Fractional CRO | $10,000 | all of the above plus the founder on calls and deal reviews |

Cold email is billed per sent email. For anything outside this list (discounts, contracts, custom terms) point to https://cal.com/dmitry.o/re-vault-gtm or dmitry@re-vault.io.
