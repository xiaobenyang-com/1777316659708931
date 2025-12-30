# 文本转换工具 Text Transformer

提供多种文本转换功能的MCP服务器，包括大小写转换、反转字符串、检测回文等功能。
MCP servers that provide multiple text conversion functions, including case conversion, string inversion, and palindrome detection.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| lowercase | Convert text to lowercase |
| uppercase | Convert text to uppercase |
| reverse | Reverse the order of characters in text |
| isPalindrome | Check if text is a palindrome (reads the same forwards and backwards) |
| countWords | Count the number of words in text |
| countCharacters | Count the number of characters in text |
| trim | Remove leading and trailing whitespace from text |
| capitalize | Capitalize the first letter of each word |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659708931](https://mcp.xiaobenyang.com/inspector/1777316659708931)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659708931](https://mcp.xiaobenyang.com/inspector/1777316659708931)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "文本转换工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659708931/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "文本转换工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659708931/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "文本转换工具": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659708931",
          },
          "transport": "stdio"
        }
      }
}

```
