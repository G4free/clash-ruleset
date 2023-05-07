# Clash ruleset

## How to use

doc: https://lancellc.gitbook.io/clash/clash-config-file/rule-provider

- example:

copy and paste this to the `rule-providers` block of your clash config file.

```yaml
  ChatGPT:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/G4free/clash-ruleset/main/ruleset/ChatGPT.yaml"
    path: ./ruleset/ChatGPT.yaml
    interval: 86400
```

then in the `rules` block:

```yaml
  - RULE-SET,ChatGPT,Proxy
```

Mind the indent.

## ruleset list

- ChatGPT

https://raw.githubusercontent.com/G4free/clash-ruleset/main/ruleset/ChatGPT.yaml
