# Codename Nika plugin for Claude Code, Codex and Muse

Work for your Nika businesses from your AI agent. Your agent can:

- see your businesses: each one's profile, brand kit (logo, colors, fonts) and website;
- hand research, leads and drafts to your Nika AI team;
- start tasks in Nika, including ⚡ Ultra Instinct for big multi-day goals;
- find work in your Nika Library and save new work to it.

You sign in with your Nika account the first time; after that, agents act only as you. Tasks use your Nika credits, and anything that sends, posts, changes data or pays still waits for your OK in Nika.

## Install

### Claude Code

```
/plugin marketplace add goodgains-dev/nika-plugins
/plugin install nika@nika
```

Or add only the Nika tools, without the skills:

```
claude mcp add --transport http nika https://www.codename-nika.com/api/mcp/nika/
```

### Codex

```
codex plugin marketplace add goodgains-dev/nika-plugins
```

Then install **Codename Nika** from the plugin list. Or add only the tools:

```
codex mcp add nika --url https://www.codename-nika.com/api/mcp/nika/
```

### Muse

Add a custom connector with this address: `https://www.codename-nika.com/api/mcp/nika/`. See [muse/README.md](muse/README.md).

### No browser sign-in?

Make a connector key on [Settings → AI provider](https://www.codename-nika.com/settings/ai/) and send it as a header:

```
claude mcp add --transport http nika https://www.codename-nika.com/api/mcp/nika/ --header "Authorization: Bearer nika_ck_…"
```

## What's inside

```
.claude-plugin/marketplace.json     Claude Code marketplace
.agents/plugins/marketplace.json    Codex marketplace
plugins/nika/
  .claude-plugin/plugin.json        Claude Code manifest
  plugin.json                       Codex (portable) manifest
  .mcp.json                         Claude Code: the Nika MCP server
  mcp.json                          Codex: the Nika MCP server (OAuth, dynamic registration)
  skills/
    nika-business/                  use the business's real brand
    nika-tasks/                     hand work to Nika
    nika-library/                   find and save Library work
    setup/                          first-time sign-in
  assets/icon.png
```

## Tools (Nika MCP server)

`list_businesses` · `get_business` · `list_ai_employees` · `ask_ai_team` · `start_task` · `task_status` · `list_tasks` · `list_playbooks` · `run_playbook` · `search_library` · `get_library_item` · `save_to_library`

## The other direction: your subscription powers Nika

With the Nika desktop app, your own Claude Code or Codex can also do work for Nika. Choose this on [Settings → AI provider](https://www.codename-nika.com/settings/ai/):

- **Main or backup AI.** Your Claude Code (your Claude plan, or your Puter balance) or Codex (your ChatGPT plan) answers Nika's AI work. Puter stays the default and OpenRouter the backup.
- **Coding tasks.** A text like "in Claude Code, write a script that…" runs in your coding agent on your computer, and the files land in your Library.

The agents always run as the official CLIs, signed in with your own account on your own computer. Nika never sees or copies that sign-in.
