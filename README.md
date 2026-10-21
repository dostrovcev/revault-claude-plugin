# Re:Vault for Claude

Re:Vault runs cold LinkedIn and email outreach and opens it to Claude. Ask in plain words who gets written to next, what went out in your name, who replied and what the numbers say. Find people at companies showing a live marker, get verified work emails, write first messages on a fact with its source and put them in the sending queue from your own LinkedIn profile.

## What is inside

- **Connector** `revault`: the hosted Re:Vault MCP server at `https://mcp.re-vault.io/mcp` (Streamable HTTP, OAuth 2.1 with PKCE).
- **Skills**: getting started, outreach status, finding leads, writing and queueing messages.
- **Commands**: `/revault:status` for replies, numbers and the queue; `/revault:find` to find prospects by a marker.

## Install

On claude.ai and in Cowork: Customize, Plugins, find **Re:Vault** in the directory and add it.

In Claude Code:

```
/plugin install revault --marketplace dostrovcev/revault-claude-plugin
```

## Connect

1. Get a connection code at [re-vault.io/mcp](https://re-vault.io/mcp/). It arrives by email within a minute.
2. Install the plugin, open its Connectors tab and press Connect on `revault`. In Claude Code run `/mcp` and authenticate `revault`.
3. Type the code. Claude stays signed in for 30 days.
4. Say: *Start my Re:Vault setup.*

## Example requests

- "Who replied this week and whose turn is it?"
- "Show what went out in my name since Monday."
- "Find fintech companies in the UK hiring their first head of sales and get the founders' work emails."
- "Write first messages for these five people and show them to me before queueing."
- "Take Acme Corp out of the queue."

## How sending works

Re:Vault sends through a governor that stays inside LinkedIn account limits, writes in the recipient's working hours and spreads touches through the day. Every key opens one workspace and every call is journalled. Queueing a message is always confirmed with you first.

## Data

The connector reads and writes data in your Re:Vault workspace: leads, messages, conversations and stats. It sends nothing to any other service. Privacy policy: https://re-vault.io/privacy/ . Terms: https://re-vault.io/terms/ .

## Pricing

From $199 a month for one connected LinkedIn profile ($299 for two, $399 for three, $499 for four), month to month. Managed plans start at $2,000 a month. Details at [re-vault.io](https://re-vault.io/).

## Support

dmitry@re-vault.io
