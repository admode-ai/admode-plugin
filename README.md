# Admode plugin

Your AI turns proven Meta winners into ads for your brand. Admode makes static, AI UGC, podcast and animated ad prompts built on Meta ads that ran for months, written in your customers' words and checked by Admode before you render. It also writes ad copy, makes new versions of a winning static ad, edits a finished video ad, saves your Meta ads and their numbers so new ads build on your winners, and makes and keeps your VOC research, Foundation Pack and Brand DNA.

This repository holds the Admode plugin in [`plugins/admode`](plugins/admode): one skill and the connection to Admode's MCP server, `https://mcp.admode.ai/mcp`. The same folder works in Claude, ChatGPT and Codex, Cursor, VS Code with GitHub Copilot, Grok Build, Gemini CLI and Antigravity.

Admode writes and checks prompts. It doesn't generate images or video: your AI renders with your own tools, only after you agree.

## Install

You need an Admode account. The first time, your app asks you to sign in: use the email of your Admode account.

- **Claude** (chat, Cowork and Claude Code): find Admode in Claude's directory. In Claude Code you can also run `/plugin marketplace add admode-ai/admode-plugin`, then `/plugin install admode@admode`.
- **ChatGPT and Codex**: find Admode in the plugin directory. In Codex you can also run `codex plugin marketplace add admode-ai/admode-plugin`.
- **Cursor**: install Admode from the Cursor Marketplace.
- **VS Code with GitHub Copilot**: add `admode-ai/admode-plugin` to the `chat.plugins.marketplaces` setting, then install Admode.
- **Gemini CLI**: `gemini extensions install https://github.com/admode-ai/admode-plugin`
- **Any other app**: add a custom connector with `https://mcp.admode.ai/mcp`. The [docs](https://admode.ai/docs#connect) show each app.

## Privacy

The plugin runs no code on your computer. It sends nothing anywhere except to Admode's own MCP server, and only what your AI passes to Admode's tools: ad prompts, copy, research sections, the files you upload, the Meta ads data your AI saves and the details a tool asks for. Admode never sees your chats. Prompts sent for checking aren't stored; your brand, research, files and anything your AI saves are kept in your Admode account, where you can download or delete them. Read the [privacy policy](https://admode.ai/privacy) and the [terms of service](https://admode.ai/terms).

## Support

Docs: [admode.ai/docs](https://admode.ai/docs) · Help: [admode.ai/support](https://admode.ai/support)

Made by HV Digital AB. The files in this repository are MIT licensed; the Admode service isn't (see [LICENSE](LICENSE)).
