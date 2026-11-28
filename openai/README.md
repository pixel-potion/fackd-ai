# Fack'd in ChatGPT and Codex

`fackd/` is the plugin package for OpenAI's plugin directory (ChatGPT and Codex), in the Agent Plugins format: `plugin.json` holds the listing, the reviewer test cases and the release notes, `mcp.json` points at https://fackd.com/mcp, and `skills/fack` is the same skill as the Claude Code plugin.

Build the upload with:

```
cd openai/fackd && zip -qrX ../fackd-openai.zip plugin.json mcp.json skills assets
```

Upload it at platform.openai.com/plugins. The demo video link and the reviewer login go in the dashboard, never in the package. After the first release, changes to the server's tools are picked up from fackd.com/mcp automatically; changes to this package need a new upload with a higher `version`.
