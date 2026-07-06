# Let's Chat Coach — Claude plugin

Professional coaching from the **Let's Chat Coach** engine, delivered inside Claude. Installing this plugin adds:

- a **`/coach`** slash command to start a coaching session, and
- the **Let's Chat Coach connector** (our coaching engine — you sign in once when you install).

Coaching runs on the Let's Chat Coach engine and is relayed into your conversation, so it applies your own methodology, history, and memory across sessions.

---

## Install (Claude Pro / Max)

**Option A — from this repo (recommended, auto-updates):**

1. In Claude, open **Customize** (left sidebar) → **Plugins**.
2. Add a marketplace pointing at this repository: `cyclistep/Lets-Chat-Coach`.
3. Install the **lets-chat-coach** plugin and approve the sign-in when prompted.

**Option B — upload the package:**

1. Download the plugin package (the `lets-chat-coach` folder, or a zip of it).
2. In Claude, open **Customize** → **Plugins** → upload a custom plugin, and select it.
3. Approve the sign-in when prompted.

## Use

In a chat, type:

```
/coach
```

…or start with a topic:

```
/coach help me prep for a tough 1:1 with my report
```

Then just talk. Every reply comes from the Let's Chat Coach engine.

---

## What's in here

```
.claude-plugin/marketplace.json     # marketplace catalog
lets-chat-coach/
├── .claude-plugin/plugin.json      # plugin manifest
├── .mcp.json                       # connects the Let's Chat Coach engine (letschatcoach.com/api/mcp)
└── commands/coach.md               # the /coach command
```

Learn more: [letschatcoach.com](https://letschatcoach.com)
