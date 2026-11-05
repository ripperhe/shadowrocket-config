# shadowrocket-config

个人使用的 Shadowrocket Rule Set。

# Rule Set

| 名称 | 用途 | URL |
| --- | --- | --- |
| ✴️ Claude | Claude / Anthropic 服务 | `https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/claude.txt` |
| Proxy | ChatGPT / OpenAI、Notion、GitHub 等日常服务 | `https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/proxy.txt` |

# 使用

在 Shadowrocket 配置文件中通过 `RULE-SET` 引用，策略在引用处指定：

```
RULE-SET,https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/claude.txt,✴️ Claude
RULE-SET,https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/proxy.txt,Proxy
```

在客户端创建或选择名为 `✴️ Claude` 的策略组，用于 Claude 专用出口；将 `Proxy` 替换为日常服务使用的实际节点或策略组名称。两个规则集可以分别指定不同的策略；规则集文件本身只包含匹配条件，不会创建或重命名客户端策略组。引用规则应放在会优先匹配同一流量的宽泛规则和 `FINAL` 之前。

`proxy.txt` 的日常服务规则整理自 `clash-config` 仓库的 `clashverge-rules.txt`，保留后缀和关键词匹配方式，另外补充 OpenAI、Notion 的资源域名。规则独立维护，不会自动同步来源文件。

# 参考

* <https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever>
* [OpenAI 网络域名清单](https://help.openai.com/en/articles/9247338-network-recommendations-for-chatgpt-errors-on-web-and-apps)
* [Notion IP 地址和域名清单](https://www.notion.com/en-gb/help/allowlist-ip)
