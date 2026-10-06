# Claude 分流规则

规则从 [Claude Code 域名分流规则大全](https://ip.net.coffee/claude/site.html) 搬运

## Rule Provider

> 以下两种仅为不同的表示方式，作用相同，二选一即可

```
claude: {type: http, format: yaml, behavior: classical, url: "https://raw.githubusercontent.com/yjrszcq/claude-list/refs/heads/main/claude.yaml", path: ./ruleset/claude.yaml, interval: 86400}
```

```
claude:
  type: http
  format: yaml
  behavior: classical
  url: "https://raw.githubusercontent.com/yjrszcq/claude-list/refs/heads/main/claude.yaml"
  path: ./ruleset/claude.yaml
  interval: 86400
```

## Rules

> 假设你的 `proxy-groups` 中对 claude 分流的代理组名为 `CLAUDE`

```
rules:
  # Claude
  - RULE-SET,claude,CLAUDE
```
