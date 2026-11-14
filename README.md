# IntegruX Brain

A free Mac app that shows, live, what your AI coding agent is doing and what it remembers.
It works with Claude Code.

- **Live 3D brain**: lights up as the agent reads, writes, searches and runs tools.
- **What I'm looking at**: a small window showing the page or file the agent has open right now.
- **Memory and board**: your memory files and your priority board, in one place.
- **Skills**: when you do the same job twice (or it fails twice), the app writes a skill for it, on your Mac.

## Download

Get **IntegruX-Brain-1.0.dmg** under [Releases](../../releases/latest), open it, and drag the app to Applications.

Needs a Mac with Apple silicon, macOS 15 or later, and Claude Code installed and signed in.
The app is signed with Developer ID and notarized by Apple.

## Privacy

The app never calls Claude, never sees your Claude login, and sends nothing anywhere.

**Connect** adds one hook to Claude Code's settings (`~/.claude/settings.json`). On every step it saves, on this
Mac only (`~/Library/Application Support/IntegruX Brain`): the tool used, the file path, the agent's short label for
the step, web page addresses (logins and `?query` parts removed) and web search words. It never records your prompts,
the agent's replies, commands or file contents.

## Uninstall

IntegruX Brain menu → **Uninstall…** takes the hook out (your settings go back exactly as they were), turns off the
background job, and deletes the activity log and the app's data. Then drag the app to the Trash.

## Check the download

```
shasum -a 256 IntegruX-Brain-1.0.dmg
```
should print `84fc1f3716170fc0fd8a62693a6f8f1757bcdac3c71afdc1b0e7367b2e235d05`.

---
Made by IntegruX · [integrux.us](https://integrux.us). Claude Code is a product of Anthropic; this app is not made,
endorsed or supported by Anthropic.
