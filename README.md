# Bybit 交易所分流规则

Clash/Mihomo 客户端专用分流规则，适用于 Bybit 交易所相关域名和 IP。

## 使用方式

在 Clash 配置文件中引用：

```yaml
rule-providers:
  bybit:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/duo-yy/bybit/main/bybit_rules.yaml"
    path: ./ruleset/bybit.yaml
    interval: 86400

rules:
  - RULE-SET,bybit,💞 地域限制
```

## 规则内容

- Bybit 相关域名（bybit.com, bytick.com, byapis.com 等）
- AWS/CloudFront CDN IP
- 应用追踪域名（appsflyer, app-measurement）

## 更新频率

建议每天自动更新一次。
