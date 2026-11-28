# Fack'd for AI apps

[Fack'd](https://fackd.com) fact-checks what people say in videos, with sources. It works with YouTube links today. Every check (a "fack") quotes a claim, gives its time in the video and who said it, rates it, and cites its sources.

This repo holds the Fack'd plugin for Claude Code and the MCP Registry entry. The server itself runs at **https://fackd.com/mcp**: one link that works in any AI app that supports MCP. Setup steps for each app: [fackd.com/ai](https://fackd.com/ai).

## Claude Code

```
/plugin marketplace add pixel-potion/fackd-ai
/plugin install fackd@fackd
```

Then run `/mcp`, choose **fackd** and sign in with your Fack'd account. The plugin adds the Fack'd MCP server and a `fack` skill that tells Claude how to read and present facks.

Or add just the server: `claude mcp add --transport http fackd https://fackd.com/mcp`.

## Other apps

Add `https://fackd.com/mcp` as a remote MCP server (a connector, custom app or integration) and sign in when asked. Steps for Claude, ChatGPT, Codex, Cursor, VS Code, Gemini CLI, Le Chat and Windsurf are at [fackd.com/ai](https://fackd.com/ai).

Tools that can't sign in (scripts, automation tools, agent frameworks, the Claude and OpenAI APIs) can use a personal API key from Settings on fackd.com, sent as `Authorization: Bearer fackd_sk_…`.

## What it can do

| Tool | What it does |
| --- | --- |
| `get_facks` | A video's facks: claim, time, speaker, rating, sources. Free with any account. |
| `search_facked_videos` | Find videos Fack'd has checked, by speaker, show or topic. |
| `fack_video` | Fack a new video with a Fack'd Pro account. Quotes the checking time first and starts only after you agree. |
| `fack_status` | How your facks are going. |
| `my_hours` | Your plan and the hours of checking you have left. |

Connected apps can't change your account, plan or billing. Disconnect them in Settings on fackd.com any time.

Fack'd rates claims, never people.

## Privacy and support

- Privacy policy: https://fackd.com/privacy
- Terms: https://fackd.com/terms
- Support: team@fackd.com

## ChatGPT and Codex

`openai/` holds the package for OpenAI's plugin directory. See [openai/README.md](openai/README.md).

## MCP Registry

`server.json` is the server's entry in the [official MCP Registry](https://registry.modelcontextprotocol.io) as `com.fackd/fackd`.
