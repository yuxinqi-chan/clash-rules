### 使用方式

要想使用本项目的规则集，只需要在 Clash 配置文件中添加如下 `rule-providers` 和 `rules`。

#### Rule Providers 配置方式
```yaml
rule-providers:
  reject:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/reject.txt"
    path: ./ruleset/reject.yaml
    interval: 86400
  icloud:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/icloud.txt"
    path: ./ruleset/icloud.yaml
    interval: 86400
  apple:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/apple.txt"
    path: ./ruleset/apple.yaml
    interval: 86400
  google:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/google.txt"
    path: ./ruleset/google.yaml
    interval: 86400
  microsoft:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/microsoft.txt"
    path: ./ruleset/microsoft.yaml
    interval: 86400
  not-cn-media:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/not-cn-media.txt"
    path: ./ruleset/not-cn-media.yaml
    interval: 86400
  proxy:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/proxy.txt"
    path: ./ruleset/proxy.yaml
    interval: 86400
  direct:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/direct.txt"
    path: ./ruleset/direct.yaml
    interval: 86400
  private:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/private.txt"
    path: ./ruleset/private.yaml
    interval: 86400
  gfw:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/gfw.txt"
    path: ./ruleset/gfw.yaml
    interval: 86400
  telegram:
    type: http
    behavior: domain
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/telegram.txt"
    path: ./ruleset/telegram.yaml
    interval: 86400
  telegramcidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/telegramcidr.txt"
    path: ./ruleset/telegramcidr.yaml
    interval: 86400
  cncidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/cncidr.txt"
    path: ./ruleset/cncidr.yaml
    interval: 86400
  lancidr:
    type: http
    behavior: ipcidr
    url: "https://raw.githubusercontent.com/yuxinqi-chan/clash-rules/main/lancidr.txt"
    path: ./ruleset/lancidr.yaml
    interval: 86400
rules:
  - RULE-SET,reject,🍃 应用净化
  - RULE-SET,private,🎯 全球直连
  - RULE-SET,direct,🎯 全球直连
  - RULE-SET,lancidr,🎯 全球直连
  - RULE-SET,cncidr,🎯 全球直连
  - RULE-SET,icloud,🎯 全球直连
  - RULE-SET,apple,🍎 苹果服务
  - RULE-SET,microsoft,Ⓜ️ 微软服务
  - RULE-SET,google,📢 谷歌FCM
  - RULE-SET,not-cn-media,🌍 国外媒体
  - RULE-SET,gfw,🚀 节点选择
  - RULE-SET,proxy,🚀 节点选择
  - RULE-SET,telegram,📲 电报信息
  - RULE-SET,telegramcidr,📲 电报信息
  - GEOIP,LAN,🎯 全球直连
  - GEOIP,CN,🎯 全球直连
  - MATCH,🐟 漏网之鱼
```
