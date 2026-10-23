## Tanatasa

**Tanatasa is a Singapore-based skincare store with an MCP server, CLI, and API for AI agents and developers.**

Connect any MCP-capable AI assistant to Tanatasa to search skincare and beauty products, compare ingredients and prices in Singapore dollars, build a cart and get a checkout link. No account or API key is needed.

- 🛍️ **Store:** [tanatasa.sg](https://tanatasa.sg) (Singapore delivery only)
- 🔌 **MCP server:** `https://tanatasa.sg/mcp` (Streamable HTTP, 10 tools)
- 📘 **Developer docs:** [github.com/tanatasa-beauty/tanatasa](https://github.com/tanatasa-beauty/tanatasa)
- 🧾 **OpenAPI:** [tanatasa.sg/agent/v1/openapi.json](https://tanatasa.sg/agent/v1/openapi.json)
- 🤖 **Agent guide:** [tanatasa.sg/ai-agent-docs](https://tanatasa.sg/ai-agent-docs)

### Quick start

Add Tanatasa to Claude Code:

```bash
claude mcp add --transport http tanatasa https://tanatasa.sg/mcp
```

Cursor (`~/.cursor/mcp.json`) and other clients that use the `mcpServers` format:

```json
{
  "mcpServers": {
    "tanatasa": { "url": "https://tanatasa.sg/mcp" }
  }
}
```

No MCP? Search the catalog over plain HTTP (prices are SGD cents, so `3000` = S$30):

```bash
curl "https://tanatasa.sg/agent/v1/products?q=cleanser&in_stock=true&max_price=3000&limit=5"
```

Setup guides for Claude, ChatGPT, Cursor and VS Code are in [the MCP docs](https://github.com/tanatasa-beauty/tanatasa/blob/main/docs/mcp.md).
