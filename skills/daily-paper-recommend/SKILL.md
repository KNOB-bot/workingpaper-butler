---
name: Daily Paper Recommend
description: |
  每日论文推荐技能 - 当用户需要获取每日学术论文推荐时自动调用
  使用场景：生成今日论文推荐、每日学术简报、定期文献推送
  触发词：今日论文推荐、每日学术推荐、论文推荐
version: 1.0.0
metadata:
  author: Academic Butler Team
  category: 学术研究
---

# 每日论文推荐技能

当用户需要获取每日学术论文推荐时，自动调用此技能。

## 功能描述

1. **多数据源整合**：从 NBER（主要）、arXiv（备用）获取最新论文
2. **智能相关性评分**：基于预设的研究兴趣关键词计算相关性得分
3. **自动翻译**：标题和摘要自动翻译为中文
4. **历史去重**：自动过滤过去30天内已推荐的论文
5. **分类整理**：按研究领域自动分类论文
6. **Obsidian同步**：自动同步到Obsidian笔记库

## 使用方法

直接告诉AI需要今日论文推荐，例如：
- "帮我推荐一些论文"
- "今日有什么新论文？"
- "生成每日论文推荐报告"

## 研究兴趣配置

系统已配置以下7大研究领域：

| 领域 | 核心关键词 |
|------|-----------|
| 市场一体化 | market integration, market segmentation, price convergence |
| 创新增长 | innovation, R&D, TFP, productivity |
| 产业政策 | industrial policy, agglomeration, industrial structure |
| 区域发展 | regional development, regional disparity, spatial |
| 城市经济学 | urban, city, housing, urbanization |
| 发展经济学 | developing country, poverty, inequality |
| AI与数字经济 | artificial intelligence, AI, digital economy |

## 输出格式

生成的报告包含：
- 今日概览（论文总数、涉及领域、数据来源）
- 按领域分类的论文列表
- 每篇论文：标题、作者、日期、摘要、推荐理由
- 重点推荐论文（Top 3）
- 原文链接

## 实现脚本

技能实现依赖以下脚本（位于 CBP-SCHOLAR/scripts/）：
- `nber_crawler.py` - NBER论文爬虫
- `arxiv_search.py` - arXiv论文搜索
- `translate.py` - 翻译模块
- `generate_daily_report.py` - 报告生成

## 配置选项

- 推荐数量：默认10篇，可指定1-20篇
- 搜索范围：默认30天内的论文
- 数据源：NBER为主，arXiv为备

## 注意事项

- 首次运行需要安装依赖：scrapling, requests, arxiv
- 翻译可能因网络问题失败，系统有备用翻译方案
- 历史去重功能需要报告文件保存在正确目录
