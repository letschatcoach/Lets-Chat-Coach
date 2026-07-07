---
name: coach
description: Start a Let's Chat Coach coaching session — professional coaching for leadership, career development, goal setting, and tough conversations, delivered by the Let's Chat Coach engine. Use when the user asks for coaching or invokes /coach.
---

Start a Let's Chat Coach coaching session now.

## Step 0 — Verify the Let's Chat Coach connector is available (REQUIRED)

Check that the **Let's Chat Coach** MCP connector's tools are available in this conversation — specifically `start_session` and `coach_turn`.

**If they are NOT available, STOP.** Do not run any other skill, do not search connector registries or directories, and do not coach the user yourself — coaching must come from the Let's Chat Coach engine, nothing else. Instead, tell the user exactly this and end your reply:

> The Let's Chat Coach connector isn't connected yet. To fix it:
> 1. Open **Settings → Connectors** and look for **Let's Chat Coach** — click **Connect** and sign in with your letschatcoach.com account.
> 2. If it isn't listed there, click **Add custom connector** and paste this URL: `https://letschatcoach.com/api/mcp`, then connect and sign in.
> 3. Start a **new conversation** (tools load per conversation) and run `/coach` again.

## Steps 1–3 — Run the session (only when the tools are available)

1. Call the `start_session` tool from the Let's Chat Coach connector with the `use_case` argument set to `lets-chat-coach`.
2. Read the briefing that `start_session` returns and follow it for the rest of this conversation. It explains that every coaching response comes from the Let's Chat Coach engine (the `coach_turn` tool) and how to relay each turn.
3. If I included a topic after the command, send it straight to `coach_turn`. Otherwise, ask me what I'd like to work on.

My opening topic (if any): $ARGUMENTS
