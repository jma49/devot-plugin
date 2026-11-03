# Devot for Claude

Search, read and edit your [Devot](https://devot.online) notes from Claude Code and the Claude desktop app, only in notebooks you allow.

The plugin is a small launcher. It runs the MCP server built into the Devot app on your Mac (`devot --cli mcp`), so it holds no server, no token and no notes, and follows the app's updates.

## Requirements

- macOS with Devot installed in `/Applications` or `~/Applications`.
- In Devot, Settings > Integrations > AI Tools: Allow AI Tools on.
- Allow AI Access on for each notebook Claude may use (the notebook's context menu). It is off by default, and a sub-notebook needs its own.

Without Devot, the server fails to start with `E_MCP_APP_NOT_FOUND`.

## Install

In Claude, open Customize > Plugins > Add marketplace and enter `jma49/devot-plugin`, then install Devot. In Claude Code:

```
/plugin install devot --marketplace jma49/devot-plugin
```

## Tools

`list_notebooks`, `search_notes`, `read_note`, `list_tags`, `create_note`, `update_note`, `trash_note`, `create_notebook`. They reach only live notes in notebooks that allow AI access; a notebook made by `create_notebook` allows it on that Mac. Trashed notes can be restored in Devot; nothing is deleted for good. Settings > Integrations can limit the tools to reading.

## Privacy Policy

The plugin and the server it runs make no network requests and send nothing to Devot. What a tool returns goes to the client that asked, which normally sends it to its AI model. Devot's notes stay on your Mac and, if you use Devot sync, encrypted on the sync service you chose. Full policy: https://devot.online/mcp-privacy. Questions: privacy@devot.online.

## Licence

FSL-1.1-MIT, the same as Devot. See `LICENSE`.
