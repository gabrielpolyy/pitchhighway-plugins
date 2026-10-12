# PitchHighway singing coach

Learn to sing your favorite songs with coaching from your PitchHighway practice data.

The singing-coach skill helps Claude use your measured vocal range, songs, practice history, and pitch reports.
It names the next song part or drill to practice.
It uses practice data without making claims about vocal health or talent.

## Requirements

- A PitchHighway account.
- At least 1 completed audio, highway, or pitch-matching exercise.
- A client that supports remote MCP connections and OAuth.

## Install in Claude Code

```text
/plugin marketplace add gabrielpolyy/pitchhighway-plugins
/plugin install pitchhighway@pitchhighway
```

Connect your PitchHighway account when Claude requests authentication.
The plugin uses `https://pitchhighway.com/mcp/readonly`.
This connection reads practice data. It cannot upload songs or generate media.

## Example questions

- What is my vocal range?
- Which of my songs fit my voice?
- Which notes did I miss in my last run?
- What can I practice next?

## Files

| Path | Purpose |
| --- | --- |
| `.claude-plugin/marketplace.json` | Claude Code marketplace |
| `pitchhighway/.claude-plugin/plugin.json` | Claude plugin manifest |
| `pitchhighway/.mcp.json` | Claude MCP connection |
| `pitchhighway/skills/singing-coach/SKILL.md` | Singing-coach skill |
| `.agents/plugins/marketplace.json` | Codex marketplace |
| `pitchhighway/plugin.json` | Agent Plugins manifest |
| `pitchhighway/mcp.json` | Agent Plugins MCP connection |
| `pitchhighway/assets/` | Plugin icons |

## Validate

```sh
claude plugin validate ./pitchhighway
claude plugin validate .
```

## Privacy and support

The MCP server uses OAuth to connect your PitchHighway account.
The singing-coach skill uses your account data to answer practice questions.

- [Setup and tool documentation](https://pitchhighway.com/mcp)
- [Privacy policy](https://pitchhighway.com/privacy)
- [Terms of service](https://pitchhighway.com/tos)
- [Support](https://pitchhighway.com/support)

Contact: support@pitchhighway.com
