---
name: Academic Search
description: |
  学术搜索技能 - 当用户需要搜索特定领域的学术论文或文献时自动调用
  使用场景：关键词搜索、主题检索、文献查找、资料收集
  触发词：搜索论文、查找文献、相关研究、这个领域
version: 1.0.0
metadata:
  author: Academic Butler Team
  category: 学术研究
---

# 学术搜索技能

当用户需要搜索学术论文时，自动调用此技能。

## 功能描述

1. **关键词搜索**：根据用户提供的关键词搜索相关论文
2. **主题检索**：围绕特定研究主题搜索文献
3. **多数据源**：支持 NBER、arXiv 等多个数据库
4. **相关性排序**：根据研究兴趣对结果排序

## 使用方法

提供搜索关键词，例如：
- "搜索市场一体化相关的论文"
- "找一些关于创新的最新研究"
- "帮我查找产业政策方面的文献"

## 搜索策略

### 1. 关键词扩展

系统会自动扩展搜索关键词：

**市场一体化**：
- market integration, market segmentation
- price convergence, law of one price
- trade barrier, trade cost

**创新增长**：
- innovation, R&D
- total factor productivity, TFP
- knowledge spillover

**产业政策**：
- industrial policy
- agglomeration, cluster
- industrial upgrading

### 2. 数据源选择

- **NBER**：经济学权威工作论文，首选
- **arXiv**：预印本，补充来源
- **RePEc**：经济学研究论文（待集成）

### 3. 时间范围

- 优先：最近7天内的论文
- 扩展：最近30天
- 补充：更早的相关论文

## 搜索结果格式

每条结果包含：
- 标题（英文+中文）
- 作者
- 发布日期
- 摘要
- 相关性得分
- 链接

## 研究兴趣匹配

系统会根据预设的研究兴趣自动评估相关性：

- 7大研究领域
- 关键词权重体系
- 方法论关键词

## 注意事项

- 搜索结果数量可配置
- 翻译功能可辅助中文阅读
- 建议结合摘要和原文进行深入阅读
