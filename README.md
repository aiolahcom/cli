# aiolah CLI

[![npm](https://img.shields.io/npm/v/@aiolah/cli)](https://www.npmjs.com/package/@aiolah/cli)

A terminal AI coding agent from [aiolah](https://aiolah.com). It reads and edits
files and runs commands in your project, and you can continue the same session
from your browser, phone or VS Code.

- **No API key needed.** Sign in with your aiolah account; usage comes out of your plan's credits.
- **Many models.** Claude, GPT, Gemini, Grok, GLM, Qwen, DeepSeek and more — every coding model your plan allows.
- **Remote control.** `aiolah rc` makes a folder controllable from [aiolah.com/code](https://aiolah.com/code), the aiolah app or VS Code, without opening ports.
- **You stay in control.** File changes and shell commands ask for Allow/Deny unless you choose another mode.
- **Works with what you have.** Reads `AGENTS.md` / `CLAUDE.md`, and Claude Code's custom commands, skills, subagents, hooks and `.mcp.json`.

Requires Node.js 22 or newer.

## Install

```bash
npm install -g @aiolah/cli
```

`aiolah --version` shows the installed version, `aiolah upgrade` updates it and
`aiolah doctor` checks the setup.

## Quick start

```bash
aiolah auth login     # approve the code in your browser
cd my-project
aiolah                # interactive chat in this folder
```

In the chat:

| Key / command | What it does |
| --- | --- |
| `shift+tab` | Switch mode: Default (asks first), Accept edits, Plan (read-only), Auto |
| `esc` | Stop the agent (what you type while it works is queued) |
| `ctrl+o` | Show or hide the output of tool calls |
| `/models` | Change the model |
| `/resume`, `/clear` | Open an earlier conversation, start a new one |
| `/remote-control` | Continue this chat from aiolah.com/code or the app |
| `/init` | Write `AGENTS.md` with notes about the project |
| `/usage` | Plan and credits left |
| `/help` | All commands |

## More ways to use it

```bash
aiolah -c                          # continue the last session
aiolah -p "explain src/app.ts"     # one answer, no chat (scripts and CI)
aiolah rc "My laptop"              # make this folder a remote-control device
aiolah models                      # models your plan can use, with their cost ($ · $$ · $$$)
aiolah connect                     # use your own key for another provider (OpenAI, OpenRouter, Z.ai, …)
aiolah mcp add <name> -- <command> # add an MCP server
aiolah acp                         # Agent Client Protocol, for editors such as Zed
```

## Documentation

Full guide: **[aiolah.com/docs?tab=cli](https://aiolah.com/docs?tab=cli)** —
accounts and logins, models and providers, permissions and auto mode, MCP,
remote control, environment variables and privacy.

## Feedback and bugs

Please open an [issue](https://github.com/aiolahcom/cli/issues) with what you
ran, what happened and the output of `aiolah doctor` (remove any keys or
tokens first). For account or billing questions, write to
[webmaster@aiolah.com](mailto:webmaster@aiolah.com).

## Privacy

When you are signed in, prompts and sessions are saved to your aiolah account
so you can read them on the Code page; with your own provider key
(`aiolah connect`), model calls go straight to that provider. Details:
[aiolah.com/privacy](https://aiolah.com/privacy).

## Uninstall

```bash
aiolah uninstall      # sign out, delete ~/.aiolah and remove the package
```
