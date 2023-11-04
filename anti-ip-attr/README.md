# Anti-ip-attribution

source: <https://github.com/lwd-temp/anti-ip-attribution.git>

If there are some domains which you want to access them directly, they can be put in `rule-set-direct-custom.txt` which you should organize it  individually.

## Usage

```yaml
rule-providers:

  anti-ip-attr-reject:
    type: http
    format: text
    behavior: classical
    url: "https://ghproxy.com/https://raw.githubusercontent.com/G4free/clash-ruleset/main/anti-ip-attr/rule-set-reject.list"
    path: ./ruleset/anti-ip-attr-reject.txt
    interval: 86400

  anti-ip-attr-direct:
    type: http
    format: text
    behavior: classical
    url: "https://ghproxy.com/https://raw.githubusercontent.com/G4free/clash-ruleset/main/anti-ip-attr/rule-set-direct.list"
    path: ./ruleset/anti-ip-attr-direct.txt
    interval: 86400

  # custom domains from anti-ip-attr-proxy.list for direct access. You should use your own rule set.
  anti-ip-attr-direct-custom:
    type: http
    format: text
    behavior: classical
    url: "https://ghproxy.com/https://raw.githubusercontent.com/G4free/clash-ruleset/main/anti-ip-attr/anti-ip-attr-direct.txt"
    path: ./ruleset/rule-set-direct-custom.txt
    interval: 86400

  anti-ip-attr-proxy:
    type: http
    format: text
    behavior: classical
    url: "https://ghproxy.com/https://raw.githubusercontent.com/G4free/clash-ruleset/main/anti-ip-attr/rule-set-proxy.list"
    path: ./ruleset/anti-ip-attr-proxy.txt
    interval: 86400


rules:
  - RULE-SET,anti-ip-attr-reject,REJECT
  - RULE-SET,anti-ip-attr-direct,DIRECT
  - RULE-SET,anti-ip-attr-direct-custom,DIRECT
  - RULE-SET,anti-ip-attr-proxy,🌍ip-attr-proxy
```
