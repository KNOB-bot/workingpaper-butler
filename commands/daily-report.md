---
name: daily-report
description: 生成今日论文推荐报告 - 基于您的研究兴趣从NBER等数据源推荐最新论文
argument-hint: "[推荐数量]"
---

# 今日论文推荐命令

使用此命令生成每日的学术论文推荐报告。

## 使用方法

```
/workingpaper-butler:daily-report
```

或指定推荐数量：

```
/workingpaper-butler:daily-report 15
```

## 功能特性

1. **多数据源搜索**：从 NBER（主要）、arXiv（备用）获取论文
2. **智能相关性评分**：基于用户研究兴趣的关键词匹配
3. **自动翻译**：标题和摘要自动翻译为中文
4. **历史去重**：自动过滤已推荐过的论文
5. **分类整理**：按研究领域自动分类
6. **Obsidian同步**：自动同步到Obsidian笔记库

## 研究兴趣领域

- 市场一体化 (Market Integration)
- 创新增长 (Innovation and Growth)
- 产业政策 (Industrial Policy)
- 区域经济发展 (Regional Development)
- 城市经济学 (Urban Economics)
- 发展经济学 (Development Economics)
- AI与数字经济 (AI and Digital Economy)

## 输出位置

- 本地：`CBP-SCHOLAR/output/daily-recommend/`
- Obsidian：`Documents/Obsidian Vault/10_Daily/`

## 参数

- `[推荐数量]`：可选，默认10篇，可指定1-20篇
