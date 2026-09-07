# Connections for Gemini CLI

Connections is an AI-first business platform: events with ticketing, contacts, the Deal Flow
marketplace, notes and memory, and payments, reachable from any assistant through one hosted
MCP server. This extension adds that server to Gemini CLI. Nothing runs locally; you sign in
with your Connections account in the browser the first time a tool is called.

## Install

```sh
gemini extensions install https://github.com/Lunarwerx/connections-gemini-extension
```

Then ask Gemini for anything Connections does. The first call opens a sign-in page; approve it
once and the session persists.

## What you can do from the prompt

- Host an event: create it, price tickets through Stripe, invite guests and send the invites.
- Contacts: import a list, search it, and pick who to invite or follow up with.
- Deal Flow: browse live marketplace deals and post your own (posting is for paying members).
- Notes and memory: notes and agent memories persist across every assistant you connect.
- Payments: onboard to Stripe and create products through the Pay plane.

Start with the `connections_pulse` tool: it answers who you are, which workspace you are bound
to, what is live on Deal Flow, and what to do next.

## Links

- Server URL: `https://studio.connections.icu/v1/mcp`
- Connect page with steps for every assistant: https://studio.connections.icu/connect
- Agent guide (machine-readable manual): https://studio.connections.icu/v1/agent-guide
- Pricing: https://pass.connections.icu (free base plan; Pass Pro from $39.99/mo)
- Support: support@connections.icu

## Notes

- Transport: streamable HTTP with OAuth 2.1 (PKCE, dynamic client registration).
- Manifest: `gemini-extension.json` at the repo root; the version tag of each release matches it.
