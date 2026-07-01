# Rulesets for games
---
## EA
Previously named as Origin.

[ea.txt](ea.txt)

Place these rules before the ruleset rule to avoid using excessive proxy traffic quota for game downloads.

```yaml
  - DOMAIN-SUFFIX,origin-a.akamaihd.net,DIRECT
  - DOMAIN-SUFFIX,prod.cloudflare.cdn.ea.com,DIRECT
```

Ref:
- <https://github.com/LM-Firefly/Rules/blob/master/Game/EA.list>
- <https://github.com/v2fly/domain-list-community/blob/master/data/origin>
