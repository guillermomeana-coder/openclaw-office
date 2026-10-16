# OpenClaw Office

**Your AI development team, working inside a Minecraft office you can walk around in.**

Fork of [AgentCraft](https://github.com/blendi-remade/agentcraft) by OpenClaw, enhanced with:

- **Office Themes** — choose your style: Warm Studio, Modern Glass, or Executive Suite
- **OpenClaw Bridge** — control the team from Claude Code or any CLI without opening Minecraft
- **Setup Wizard** — interactive config for auth (Claude Login or API key), theme, and repos
- **Bypass Permissions** — agents work autonomously without stopping to ask
- **Headless Mode** — run the team without the Minecraft window (`--NoGame`)

## Quick Start

```bash
# 1. Setup (interactive)
node tools/setup.mjs

# 2. Launch (headless — agents work, no game window)
node tools/launch-openclaw.mjs

# 3. Or with Minecraft window
node tools/launch-openclaw.mjs --game

# 4. Control from CLI
node tools/openclaw-bridge.mjs status
node tools/openclaw-bridge.mjs goal "Add dark mode to the settings page"
node tools/openclaw-bridge.mjs watch
```

## The Bridge (Claude Code Integration)

The OpenClaw Bridge lets you orchestrate the team from any terminal:

```bash
node tools/openclaw-bridge.mjs status           # team overview
node tools/openclaw-bridge.mjs agents            # who's doing what
node tools/openclaw-bridge.mjs goal "..."        # submit work
node tools/openclaw-bridge.mjs tasks             # task board
node tools/openclaw-bridge.mjs decisions         # pending decisions
node tools/openclaw-bridge.mjs merge <id>        # approve a merge
node tools/openclaw-bridge.mjs diff <worktree>   # review changes
node tools/openclaw-bridge.mjs msg kit "..."     # message an agent
node tools/openclaw-bridge.mjs watch             # live event stream
```

## Office Themes

| Theme | Style |
|-------|-------|
| `warm_studio` | Original — timber frame, copper dome, plaster walls, parquet floors |
| `modern_glass` | Contemporary — quartz, glass, iron, polished stone |
| `executive` | Premium — deepslate, dark oak, tinted glass, soul lanterns |

Set via `node tools/setup.mjs` or `node tools/setup.mjs --theme executive`

## Requirements

- Java 25 (Temurin)
- Node 22+
- Minecraft: Java Edition (for visual mode)
- Claude API key or Claude Max subscription

## Credits

Built on [AgentCraft](https://github.com/blendi-remade/agentcraft) by Blendi. Enhanced by [OpenClaw](https://orionblue.space).
