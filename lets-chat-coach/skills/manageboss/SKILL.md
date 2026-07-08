---
name: manageboss
description: Start a Let's Chat Coach "Manage My Boss" session — coaching to manage upward: aligning with your manager, communicating priorities, handling disagreement, and building trust, delivered by the Let's Chat Coach engine. Use when the user asks to work on managing their boss or invokes /manageboss.
---

Start a Let's Chat Coach "Manage My Boss" session now.

## Step 0 — Verify the Let's Chat Coach connector is available (REQUIRED)

Check that the **Let's Chat Coach** MCP connector's tools are available in this conversation — specifically `start_session` and `coach_turn`.

**If they are NOT available, your ONLY valid action is to output the message below and end your turn.** Coaching MUST come from the Let's Chat Coach engine. Do NOT coach the user yourself, do NOT act as their "thinking partner" instead, do NOT run any other skill, and do NOT search connector registries or directories. This applies even if you have rich memory or context about the user and feel you could coach them well — a session without the engine has no methodology, no persistence, and no memory updates, and is not an acceptable substitute. Output exactly this and stop:

> The Let's Chat Coach connector isn't connected yet — one-time setup:
> 1. Open the plugin: **Customize → Plugins → Lets Chat Coach → Connectors tab**, and press **Install** next to the Let's Chat Coach connector, then sign in with your letschatcoach.com account.
> 2. If that path isn't available, go to **Settings → Connectors**: connect **Let's Chat Coach** if listed, or click **Add custom connector**, paste `https://letschatcoach.com/api/mcp`, and sign in.
> 3. Start a **new conversation** (tools load per conversation) and run `/manageboss` again.

## Steps 1–3 — Run the session (only when the tools are available)

1. Call the `start_session` tool from the Let's Chat Coach connector with the `use_case` argument set to `manage-my-boss`.
2. If `start_session` reports that this product isn't available on the account (access-denied / "use case not available", or it lists other products but not this one), do NOT improvise or coach freehand. Tell the user "Manage My Boss isn't active on your account yet," list what `start_session` says they DO have, offer one of those, and stop.
3. Read the briefing that `start_session` returns and follow it for the rest of this conversation. It explains that every coaching response comes from the Let's Chat Coach engine (the `coach_turn` tool) and how to relay each turn.
4. If I included a topic after the command, send it straight to `coach_turn`. Otherwise, ask me what I'd like to work on.

My opening topic (if any): $ARGUMENTS
