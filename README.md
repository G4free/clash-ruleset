# Clash ruleset

## ⛔️ Deprecated ones

1. [anti-ip-attr](./anti-ip-attr/)

    These entries were sourced from GitHub and have long been routed via the `DIRECT` rule in my environment.

    However, recent logs show that some media resource domains (e.g., `d1.music.126.com`) are matched by the `anti-ip-attr-proxy` ruleset, which is unexpected.

    Since these rulesets are no longer needed, they won't be maintained anymore.

## How to use

doc: https://wiki.metacubex.one/config/rule-providers/

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

## OtherAIChat.txt

It exists because some nodes of proxy providers have their specific policy for OpenAI, so ChatGPT can use more nodes than other AI chat domains.

## ruleset list

- ChatGPT

https://raw.githubusercontent.com/G4free/clash-ruleset/main/ruleset/ChatGPT.yaml
