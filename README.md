# appoiint

Agent-first meeting platform CLI. Schedule meetings, create rooms, join video calls.

## Install

```bash
npm install -g appoiint
```

## Quick Start

```bash
apo signup --email you@example.com --password YourPass123!
apo room "Team Standup"
apo rooms
apo invite ROOM_ID --email joe@co.com --name Joe
apo transcript ROOM_ID
```

## Commands

### Auth
```bash
apo signup --email E --password P     # Sign up, get API key (auto-saved)
apo login --key KEY --user USERID     # Save existing key
apo config                            # Show active config
```

### Rooms
```bash
apo room "Title"                      # Create room
apo rooms                             # List active rooms
apo room-status ROOM_ID               # Status + participants
apo room-end ROOM_ID                  # End meeting
apo invite ROOM_ID --email E --name N # Invite someone
apo transcript ROOM_ID --format text  # Get transcript
```

### Scheduling
```bash
apo events                            # List event types
apo slots --email host@co.com --date 2026-06-15
apo book --date 2026-06-15T14:00:00Z --email jane@co.com
```

### TTS (Text-to-Speech)
```bash
apo tts "Hello" --voice cfo           # Synthesize with CxO voice
apo voices                            # List voices
```

### Options
```bash
apo <command> --json                  # JSON output (for agents)
apo --help                            # Full reference
```

## Agent Integration

Add to your CLAUDE.md, .cursorrules, .clinerules, or .windsurfrules:

```
## Appoiint
Use the apo CLI for meeting and booking management.
Key is in .appoiint/config.json (auto-loaded).
Run apo --help for full reference.
```

## Auth

Config priority: `--key` flag > `APO_API_KEY` env > `.appoiint/config.json` (local) > `~/.appoiint/config.json` (global)

Signup auto-saves your API key + userId — no manual config needed.

## Links

- Homepage: https://appoiint.com
- Docs: https://appoiint.com/docs/quickstart.html
- llms.txt: https://appoiint.com/llms.txt

---

Tyga.Cloud Ltd
