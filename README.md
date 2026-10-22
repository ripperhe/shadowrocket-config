# shadowrocket-config

个人使用的 Shadowrocket Rule Set。

## Rule Set

| 名称 | 用途 | URL |
| --- | --- | --- |
| AI | Anthropic 服务 | `https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/ai.txt` |

## 使用

在 Shadowrocket 配置文件中通过 `RULE-SET` 引用，策略在引用处指定：

```
RULE-SET,https://raw.githubusercontent.com/ripperhe/shadowrocket-config/master/ruleset/ai.txt,Proxy
```

## 参考

* <https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever>
