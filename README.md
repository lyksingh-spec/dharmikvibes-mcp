# DharmikVibes MCP servers

Public, read-only Model Context Protocol servers from DharmikVibes (DIVVIB LIFESTYLE PRIVATE LIMITED, Gurugram, India). No sign-in, no personal data, no payments. Streamable HTTP.

| Server | URL | What it answers |
|---|---|---|
| DharmikStudio | `https://studio.dharmikvibes.com/mcp` | Hindu devotional audio series, katha, aartis and mantras with meaning, Gita lessons, temple stories, festival and vrat guides, in Hindi and English. OpenAPI: https://studio.dharmikvibes.com/ai/openapi.json |
| DivineAI | `https://divineai-mcp.dharmikvibes.com/divineai` (Claude: `https://divineai-mcp.dharmikvibes.com/claude/divineai`) | Panchang for 50+ cities (sunrise, tithi, nakshatra, yoga, karana), festival dates checked against official and temple sources, vrat days. No prices. |
| DharmikVibes Wellness | `https://wellness.dharmikvibes.com/mcp` | Spiritual wellness journeys, retreats, experiences and group sessions across India, with day-by-day plans and published price labels. OpenAPI: https://wellness.dharmikvibes.com/ai/openapi.json |

Official MCP Registry: `com.dharmikvibes/studio`, `com.dharmikvibes/divineai`, `com.dharmikvibes/wellness`.

## Add to a client

Claude (Settings > Connectors > Add custom connector), ChatGPT (developer mode), Cursor, VS Code or any MCP client: paste the URL above. Example `mcp.json`:

```json
{ "mcpServers": { "dharmikstudio": { "type": "streamable-http", "url": "https://studio.dharmikvibes.com/mcp" } } }
```

Gemini CLI: see `gemini/`.

## Claude plugins

Three Claude plugins live in `plugins/`, each a connector to the server above plus skills that tell Claude how to answer: `plugins/dharmikstudio`, `plugins/divineai` (connector URL `https://divineai-mcp.dharmikvibes.com/claude/divineai`) and `plugins/dharmikvibes-wellness`. All are read-only and need no sign-in. In Claude Code:

```
/plugin marketplace add lyksingh-spec/dharmikvibes-mcp
/plugin install dharmikstudio --marketplace lyksingh-spec/dharmikvibes-mcp
```

## Contact
hi@dharmikvibes.com (all servers; Wellness bookings: spiritualwellness@dharmikvibes.com)
Privacy: https://studio.dharmikvibes.com/privacy · https://divineai.dharmikvibes.com/en/privacy/ · https://dharmikvibes.com/privacy-policy
