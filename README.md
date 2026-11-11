# AvaHR MCP

Connect Cursor and other MCP clients to [AvaHR](https://avahr.com), the hiring platform for small and midsize businesses. AvaHR's remote MCP server lets an AI assistant look up your hiring data and prepare drafts, while your team stays in charge of every hiring decision.

- Server: `https://mcp.avahr.com` (Streamable HTTP)
- Sign-in: OAuth 2.1 with PKCE and dynamic client registration. You sign in with your own AvaHR account.
- Setup guide: https://knowledge.avahr.com/how-to-connect-mcp
- Support: support@avahr.com

## Install in Cursor

Add the server to `.cursor/mcp.json` (or install this plugin):

```json
{
  "mcpServers": {
    "avahr": {
      "url": "https://mcp.avahr.com"
    }
  }
}
```

Cursor opens AvaHR's sign-in and consent screen the first time you use it. Write access is opt-in on that screen and limited to inactive drafts.

## Tools

Read-only:

- `list_jobs`, `get_job`
- `search_candidates`, `get_candidate`
- `list_pipelines`, `list_job_stages`
- `list_hiring_team`, `list_interviews`

Drafts only (created inactive, for a person to review in AvaHR):

- `create_assessment_draft`
- `create_questionnaire_draft`

## Human-supervised by design

AvaHR MCP helps your team find information and prepare drafts faster. It does not screen, rank, reject, advance or hire candidates. Those decisions stay with people on your hiring team.

## Scopes

`jobs:read`, `candidates:read`, `pipelines:read`, `interviews:read`, `assessments:write`, `questionnaires:write`

## Note

AvaHR also has a separate Zapier-based MCP at zapier.com/mcp/avahr. This repository is for the native AvaHR MCP server at `mcp.avahr.com`.

## License

MIT
