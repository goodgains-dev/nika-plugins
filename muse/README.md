# Codename Nika in Muse

## Use it now: custom connector

In Muse, add a custom connector:

- **Name:** Codename Nika
- **Address (MCP, streamable HTTP):** `https://www.codename-nika.com/api/mcp/nika/`
- **Sign-in:** OAuth. Muse registers itself and opens Nika's sign-in page, where you allow it. If Muse asks for a key instead, make one on [Settings → AI provider](https://www.codename-nika.com/settings/ai/) and use it as a Bearer token.

Then try: "Use Codename Nika to list my businesses."

> Muse's custom connectors are new, and it isn't confirmed that every Muse client accepts a remote MCP address. If yours doesn't, use the listing below.
>
> Nika lets agents sign in from localhost and from these sites: claude.ai, chatgpt.com, muse.ai and meta.ai. If Muse sends you back somewhere else, add that host to `MCP_AGENT_REDIRECT_HOSTS` on the Nika server.

## Listing for the Muse Connector Platform (muse.ai/platform)

Submitting needs Codename Nika's own Muse developer account. Meta reviews each connector.

- **Connector name:** Codename Nika
- **Short description:** Your businesses, AI team, tasks and Library.
- **Long description:** Work for your Nika businesses from Muse. Muse can see each business's profile and brand kit (logo, colors, fonts, website), hand research and drafts to your Nika AI team, start tasks in Nika (including ⚡ Ultra Instinct for big goals), and find or save work in your Nika Library. Tasks use your Nika credits, and anything that sends, posts or pays waits for your approval in Nika.
- **Category:** Productivity / Business
- **Auth:** OAuth 2.1 with PKCE.
  - Discovery: `https://www.codename-nika.com/.well-known/oauth-protected-resource/api/mcp/nika/`
  - Dynamic client registration: `https://www.codename-nika.com/api/mcp/oauth/register/`
  - Consent page: `/connect/agent/`
  - Token endpoint: Nika ID's, `/api/nika-id/oauth/token/`
- **API:** MCP over streamable HTTP, stateless, JSON responses. Its 12 tools are listed in the [repository README](../README.md).
- **Icon:** `../plugins/nika/assets/icon.png`
- **Privacy:** https://www.codename-nika.com/legal/
- **Support:** hello@codename-nika.com
