# GetLawED — Verified South African Law (MCP server)

[![mcptry](https://mcptry.com/badge/za.co.getlawed/sa-law)](https://mcptry.com/servers/za.co.getlawed/sa-law)

Search official South African law, quote the exact section and check case citations — from Claude, ChatGPT or any MCP client.

**Server URL (Streamable HTTP):** `https://getlawed.co.za/api/mcp/law`
**Registry name:** `za.co.getlawed/sa-law` · [MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=za.co.getlawed)
**Docs:** https://getlawed.co.za/law/developers/ · **Terms:** https://getlawed.co.za/law/terms.html · **Pricing:** https://getlawed.co.za/law/access.html

This repository holds the public listing files for the server (`server.json`, client examples). The server itself is a hosted service by GetKonnektED; its source is not published here.

## Tools (all read-only)

| Tool | What it does |
|---|---|
| `legal_library_search` | Search official SA judgments, Acts (section level), regulations, by-laws and gazettes |
| `legal_get_section` | Return the full text of one section or judgment, with its official source link |
| `legal_verify_citations` | Check case citations and Acts in a piece of text against official copies |

Sources are official copies only (South African courts, gov.za, the Government Printer, provincial gazettes, municipalities, regulators). Results support a legal professional and are not legal advice.

## Try it

No account is needed to try it (a small daily allowance per client). A free key from https://getlawed.co.za/law/access.html raises the allowance; paid plans add more. Send a key as `Authorization: Bearer glw_…`.

### Claude (Desktop / claude.ai connectors)
Add a custom connector with the URL `https://getlawed.co.za/api/mcp/law`, or see [`examples/claude-connector.json`](examples/claude-connector.json).

### ChatGPT (Developer mode / Apps)
Add the same URL as an MCP server. See [`examples/chatgpt.md`](examples/chatgpt.md).

### Any MCP client
```json
{
  "mcpServers": {
    "getlawed": { "url": "https://getlawed.co.za/api/mcp/law" }
  }
}
```

## Other access
- A2A agent: `https://getlawed.co.za/api/mcp/law/a2a` · card `https://getlawed.co.za/.well-known/agent.json`
- REST / OpenAPI: `https://getlawed.co.za/api/law/v1/` · `https://getlawed.co.za/law/developers/openapi.json`

## Support
support@getkonnekted.com · https://getlawed.co.za/law/developers/support.html

Published by Konnektivity (Pty) Ltd t/a GetKonnektED, Sandton, South Africa.
