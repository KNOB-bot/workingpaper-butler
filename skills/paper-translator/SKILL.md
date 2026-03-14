---
name: Paper Translator
description: |
  论文翻译技能 - 当用户需要翻译学术论文标题、摘要或内容时自动调用
  使用场景：英文论文翻译、学术术语解释、双语对照阅读
  触发词：翻译论文、论文翻译、英文摘要翻译
version: 1.0.0
metadata:
  author: Academic Butler Team
  category: 学术研究
---

# 论文翻译技能

当用户需要翻译学术论文时，自动调用此技能。

## 功能描述

1. **标题翻译**：将英文论文标题翻译为中文
2. **摘要翻译**：将英文摘要翻译为中文，保留专业术语
3. **术语解释**：解释学术术语的中英文对照
4. **双语对照**：提供中英文对照便于理解

## 使用方法

提供需要翻译的内容，例如：
- "翻译这个标题：The Market Value of Reproductive Rights"
- "帮我翻译这篇摘要..."
- "这些学术术语用中文怎么说？"

## 翻译规则

### 1. 学术术语标准化

使用公认的学术术语翻译：

| 英文 | 中文 |
|------|------|
| market integration | 市场一体化 |
| market segmentation | 市场分割 |
| price convergence | 价格趋同 |
| total factor productivity (TFP) | 全要素生产率 |
| industrial policy | 产业政策 |
| agglomeration | 集聚经济 |
| regional development | 区域发展 |
| differential | 差异 |
| synthetic control | 合成控制 |

### 2. 短语翻译

| 英文 | 中文 |
|------|------|
| This paper studies... | 本文研究... |
| We find that... | 我们发现... |
| We examine... | 我们考察... |
| empirical evidence | 实证证据 |
| identification strategy | 识别策略 |

### 3. 翻译优先级

1. 已知术语 → 使用标准翻译
2. 未知术语 → 保留原文并解释
3. 整句翻译 → 保持学术风格

## 注意事项

- 翻译结果仅供参考，重要内容建议阅读原文
- 某些专业术语可能没有标准翻译
- 翻译API可能因网络问题失败，此时使用关键词映射
