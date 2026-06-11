# Instalação rápida

Neon MCP é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_neon`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=Neon%20MCP&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_neon)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → `Neon MCP` / `https://api.mcp.ai/p_neon`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "neon": { "type": "http", "url": "https://api.mcp.ai/p_neon" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=neon&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9uZW9uIn0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "neon": { "url": "https://api.mcp.ai/p_neon" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=neon&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_neon%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "neon": { "type": "http", "url": "https://api.mcp.ai/p_neon" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_neon
```

Dúvidas? [neon@mcp.ai](mailto:neon@mcp.ai)
