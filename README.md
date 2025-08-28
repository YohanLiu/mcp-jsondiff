## jsondiff MCP
基于 Model Context Protocol (MCP) 的json对比工具

## 项目简介
开发中常常需要对比两个 json 差异，此工具目的是帮助大家在使用 ai 对话的过程中，快速准确的进行 json 对比。
本人在工作过程中发现在利用 ai 进行 json 对比的时候，会出现以下令我困惑的问题：
1. 对比的准确性有时候得不到保障
2. 会理解错我的意思，帮我写出一段可以对比 json 的程序代码
3. 对比正确的时候，输出的文案过于冗长，使我不能快速得到关键信息

基于以上问题，本人开发了这个基于 MCP 协议的 json 对比工具，可以使 ai 调用此工具方便快速的进行 json 对比，并输出规整的格式能快速得到对比失败详情或成功的关键信息！

## 部署指南
在 Claude Desktop、Cherry Studio 等支持 MCP Server 的应用配置文件中添加以下配置：
```
{
  "mcpServers": {
    "mcp_jsondiff": {
        "command": "uvx",
        "args": [
          "mcp-jsondiff-kel@latest"
        ]
      }
  }
}
```

## 调试
您可以使用 MCP 检查器来调试服务器。对于 uvx 安装：
```
npx @modelcontextprotocol/inspector uvx mcp-jsondiff-kel
```

## 使用示例

**演示示例用 Cherry Studio进行演示**

首先在对话框中选择此 mcp 工具![image-20250828221215427](https://gitee.com/yohan_liu/photo/raw/master/20250828221215489.png)
然后输入形如如下的文案即可进行对比 `json对比,预期值:{"a":1,"b":2}, 实际值:{"a":1,"b":2}`
### 字符串对比

![image-20250828221334908](https://gitee.com/yohan_liu/photo/raw/master/20250828221334984.png)

### json 对比

![image-20250828221439044](https://gitee.com/yohan_liu/photo/raw/master/20250828221439117.png)

### 转义后的 json 对比

![image-20250828221359169](https://gitee.com/yohan_liu/photo/raw/master/20250828221359246.png)

### 嵌套 json 对比

![image-20250828221531975](https://gitee.com/yohan_liu/photo/raw/master/20250828221532061.png)

### 演示视频

https://www.bilibili.com/video/BV1yYh2zNEcY/?spm_id_from=333.1387.homepage.video_card.click&vd_source=1a77b8b856c66190a0ab82a7acb92136
