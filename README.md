## 计算器 MCP
基于 Model Context Protocol (MCP) 的json对比工具


## inspector
```
npx @modelcontextprotocol/inspector uvx mcp_jsondiff_kel
```

## MCP 服务器配置
```
{
  "mcpServers": {
    "mcp_jsondiff_kel": {
        "command": "uvx",
        "args": [
          "mcp-jsondiff-kel@latest"
        ]
      }
  }
}
```