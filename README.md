# GetLawED — Verified South African Law (MCP server)

[![mcptry](https://mcptry.com/badge/za.co.getlawed/sa-law)](https://mcptry.com/servers/za.co.getlawed/sa-law)

Search official South African law, quote the exact section, check case citations, find the municipal by-laws and zoning scheme for a place, and find a law firm — from Claude, ChatGPT, Gemini or any MCP client.

**Server URL (Streamable HTTP):** `https://getlawed.co.za/api/mcp/law`
**Registry name:** `za.co.getlawed/sa-law` · [MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=za.co.getlawed)
**Docs:** https://getlawed.co.za/law/developers/ · **Terms:** https://getlawed.co.za/law/terms.html · **Pricing:** https://getlawed.co.za/law/access.html

This repository holds the public listing files for the server (`server.json`, client examples). The server itself is a hosted service by GetKonnektED; its source is not published here.

## What is in the library

Official copies only — South African courts, gov.za, the Government Printer, provincial gazettes, municipalities and regulators:

- about 20,000 judgments (Constitutional Court, Supreme Court of Appeal, High Courts, Labour, Land and Tax courts, tribunals)
- over 2,100 Acts, split into sections — **over 250 in their current wording, with amendments applied section by section** (over 18,000 amendments tracked across 860+ Acts)
- regulations, rules and codes; about 2,500 municipal by-laws and land use schemes; Bills; over 44,000 Government Gazette notices

Live figures: https://getlawed.co.za/law/developers/

## Tools

| Tool | What it does | Changes anything? |
|---|---|---|
| `legal_library_search` | Search judgments, Acts (section level), regulations, by-laws and gazettes in plain language | No |
| `legal_get_section` | The exact text of one section or judgment, with its official source link | No |
| `legal_verify_citations` | Check case citations and Acts in a draft against official copies — FOUND, REPEALED, MISMATCH or NOT CONFIRMED | No |
| `bylaws_find_municipality` | Which municipality a town or suburb falls under, and what GetLawED holds for it | No |
| `bylaws_for_place` | The municipal by-laws and land use scheme for a place, by topic | No |
| `zoning_scheme_for_place` | The land use / zoning scheme and planning by-law that apply in a place | No |
| `bylaw_rules_for` | The by-law sections on one subject (boundary walls, second dwellings, home businesses, signage, animals…), quoted | No |
| `find_law_firms` | Law firms on GetLawED by area of law and city or province | No |
| `get_firm` | A firm's profile, consultations, prices and deposits | No |
| `check_availability` | Open consultation times at a firm on a date (South African time) | No |
| `request_consultation` | Request a consultation for the person — preview first, sent only with a confirm code and the person's consent; the firm confirms after its conflict check | **Yes** (sends a request) |

Results support a legal professional and are not legal advice. A citation or authority that is not in the library is reported as not confirmed — never as proof that it does not exist. GetLawED holds municipal by-laws and schemes, not the zoning of individual erven.

## Try it

No account is needed: 10 searches and 10 citation checks a day per user. A free key from https://getlawed.co.za/law/access.html adds citation checks; paid plans (from R199/month) add much more. Send a key as `Authorization: Bearer glw_…`.

### Claude (claude.ai / Desktop)
Add a custom connector with the URL `https://getlawed.co.za/api/mcp/law` — see [`examples/claude-connector.json`](examples/claude-connector.json).

### ChatGPT (Apps / Developer mode)
Add the same URL as an MCP server. See [`examples/chatgpt.md`](examples/chatgpt.md).

### Gemini CLI
This repository is a Gemini CLI extension: `gemini extensions install https://github.com/Getkonnekted-AI/getlawed-mcp`

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
