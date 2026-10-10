---
name: setup
description: First-time setup for the Nika plugin — sign in with the user's Nika account, check the connection, and pick the business they mostly work on.
---

# Set up Nika

1. Call `list_businesses`. The first call opens a browser window where the user signs in with their Nika account and allows this agent. If they don't have a Nika account yet, send them to https://www.codename-nika.com.
2. Show the businesses it returned and ask which one they mostly work on. Remember it for this conversation.
3. Tell them about Settings → AI provider in Nika (https://www.codename-nika.com/settings/ai/). There they can:
   - use their own Claude Code or Codex subscription for Nika's AI work (Puter stays the default, OpenRouter the backup);
   - let texts and this plugin start coding tasks on their computer, through the Nika desktop app;
   - make a connector key, for tools that can't do the browser sign-in.
