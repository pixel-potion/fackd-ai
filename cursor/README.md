# Fack'd in Cursor and Grok

`fackd/` is the Fack'd plugin in the Cursor plugin format, for the Cursor Marketplace and xAI's Grok Bot marketplace. `.cursor-plugin/plugin.json` holds the listing, `mcp.json` points at https://fackd.com/mcp, and `skills/fack` is the same skill as the Claude Code plugin. `.cursor-plugin/marketplace.json` at the top of this repo tells the marketplace where the plugin lives.

After you add the plugin, the first Fack'd tool call asks you to sign in with your Fack'd account in the browser. Reading facks and searching checked videos work with any account, including a free one.

To add just the server without the plugin, put this in `~/.cursor/mcp.json` and sign in when asked:

```
{ "mcpServers": { "fackd": { "url": "https://fackd.com/mcp" } } }
```
