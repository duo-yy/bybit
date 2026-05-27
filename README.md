# Bybit 交易所分流规则

适用于 Clash/Mihomo 和 Shadowrocket (小火箭) 的 Bybit 交易所分流规则集。

---

## 🔹 Clash / Mihomo

### 引用方式

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

---

## 🔹 Shadowrocket (小火箭)

### 方式一：订阅规则集（推荐）

在 **配置 → 模块** 中添加：

```
https://raw.githubusercontent.com/duo-yy/bybit/main/bybit_shadowrocket_module.sgmodule
```

### 方式二：完整配置文件

在 **配置 → 下载配置** 中粘贴：

```
https://raw.githubusercontent.com/duo-yy/bybit/main/bybit_shadowrocket_full.conf
```

### 方式三：手动添加规则

将 `bybit_shadowrocket.conf` 中的 `[Rule]` 部分复制到你现有配置的 `[Rule]` 段落中。

---

## 📋 策略组说明

**Bybit 策略组** 默认为 `select`（手动选择）模式，可选节点：
- `DIRECT` — 直连
- `PROXY` — 默认代理
- `🇭🇰 香港` / `🇯🇵 日本` / `🇸🇬 新加坡` / `🇺🇸 美国` — 按地区选择

> 💡 在小火箭中修改 `[Proxy Group]` 部分，将节点名称替换为你自己的实际节点名称。

---

## 📦 文件说明

| 文件 | 用途 |
|------|------|
| `bybit_rules.yaml` | Clash/Mihomo 规则集 |
| `bybit_shadowrocket.conf` | Shadowrocket 规则文件 |
| `bybit_shadowrocket_module.sgmodule` | Shadowrocket 模块（含策略组） |
| `bybit_shadowrocket_full.conf` | Shadowrocket 完整配置模板 |

---

## 🔄 更新频率

建议每天自动更新一次。
