# Introduction
This project is an extension based on the rule set of [Loyalsoldier/clash-rules](https://github.com/Loyalsoldier/clash-rules) for my personal use

### Usage
To use the rule set of this project, simply add the following `rule-providers` and `rules` in the Clash configuration file.

#### Rule Providers collocation method
```yaml
rule-providers:
  _reject:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/fynntang/clash-rules@main/rules/_reject.txt"
    path: ./ruleset/_reject.yaml
    interval: 86400

  _proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/fynntang/clash-rules@main/rules/_proxy.txt"
    path: ./ruleset/_proxy.yaml
    interval: 86400

  _direct:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/fynntang/clash-rules@main/rules/_direct.txt"
    path: ./ruleset/_direct.yaml
    interval: 86400
```

#### Rules configuration method
```yaml
rules:
  - RULE-SET,_reject,REJECT
  - RULE-SET,_proxy,PROXY
  - RULE-SET,_direct,DIRECT
```