# FarmInventory — 作物仓库

[![MIT License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![Paper 1.21](https://img.shields.io/badge/Paper-1.21-blue)](https://papermc.io)
[![Java 26](https://img.shields.io/badge/Java-26-orange)](https://adoptium.net)
[![bStats](https://img.shields.io/badge/bStats-32739-ff69b4)](https://bstats.org/plugin/bukkit/FarmInventory/32739)

> 我的世界自动收集农作物并存入可视化仓库插件。

---

## 功能特色

- **自动收集** — 破坏农作物时自动收入仓库，告别满地掉落物
- **可视化 GUI** — 54 格图形界面，分页浏览
- **数据持久化** — 基于 H2 数据库，数据安全可靠
- **PAPI 支持** — 提供 `%fm_<作物>%` 变量
- **权限分级** — VIP/SVIP/普通玩家不同仓库容量上限

---

## 支持的作物

| 作物 | 标识符 |
|------|--------|
| 仙人掌 | `CACTUS` |
| 马铃薯 | `POTATO` |
| 胡萝卜 | `CARROT` |
| 小麦 | `WHEAT` |
| 小麦种子 | `WHEAT_SEEDS` |
| 甜菜 | `BEETROOT` |
| 甜菜种子 | `BEETROOT_SEEDS` |
| 地狱疣 | `NETHER_WART` |
| 南瓜 | `PUMPKIN` |
| 西瓜 | `MELON` |
| 西瓜片 | `MELON_SLICE` |
| 竹子 | `BAMBOO` |
| 甘蔗 | `SUGAR_CANE` |

---

## 指令

| 指令 | 权限 | 说明 |
|------|------|------|
| `/fm` `/farm` | `fm.user` | 打开主菜单 |
| `/fm <作物类型>` | `fm.user` | 打开指定作物仓库 |
| `/fm switch` | `fm.user` | 切换自动收集开关 |
| `/fm reload` | `fm.admin` | 重载插件配置 |

> 权限 `fm.user` 默认所有玩家拥有，`fm.admin` 默认只有 OP 拥有。

---

## PlaceholderAPI 变量

安装 PlaceholderAPI 后可使用以下变量：

```
%fm_CACTUS%      %fm_POTATO%        %fm_CARROT%
%fm_WHEAT%       %fm_WHEAT_SEEDS%   %fm_BEETROOT%
%fm_BEETROOT_SEEDS%  %fm_NETHER_WART%  %fm_PUMPKIN%
%fm_MELON%       %fm_MELON_SLICE%   %fm_BAMBOO%
%fm_SUGAR_CANE%
```

---

## 权限

| 权限节点 | 默认 | 说明 |
|---------|------|------|
| `fm.user` | 所有人 | 使用基础指令 |
| `fm.admin` | OP | 重载插件 |
| `ranmc.vip` | — | VIP 上限 20 页 |
| `ranmc.svip` | — | SVIP 上限 30 页 |
| — | 普通玩家 | 上限 50 页 |

---

## 依赖

### 可选
- [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) — 提供变量占位符

---

## 安装

1. 从 [Releases](https://github.com/your-repo/FarmInventory/releases) 下载最新版 JAR
2. 将 JAR 放入服务端 `plugins` 目录
3. 重启服务端或使用 `/reload confirm`
4. （可选）安装 PlaceholderAPI 以使用变量功能

---

## 数据存储

使用嵌入式 **H2 数据库**，数据文件位于 `plugins/FarmInventory/data.mv.db`，无需额外配置数据库服务。

---

## 📊 数据统计

[![bStats](https://bstats.org/signatures/bukkit/FarmInventory.svg)](https://bstats.org/plugin/bukkit/FarmInventory/32739)
