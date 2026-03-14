# WorkingPaper Butler - 工作论文管家插件

> 您的专属学术研究助手

## 简介

WorkingPaper Butler（工作论文管家）是一个专注于学术研究的CodeBuddy插件，提供每日论文推荐、论文分析、学术搜索等功能。

## 功能特性

### 1. 每日论文推荐
- 自动从NBER、arXiv获取最新论文
- 基于研究兴趣的智能相关性评分
- 自动翻译为中文
- 历史去重，避免重复推荐
- 自动同步到Obsidian

### 2. 论文分析
- 解析论文结构
- 提取核心贡献
- 评估研究方法
- 解读实证结果

### 3. 论文翻译
- 标题翻译
- 摘要翻译
- 学术术语标准化

### 4. 学术搜索
- 关键词搜索
- 主题检索
- 多数据源支持

## 安装

### 方式1：从GitHub安装

```bash
/plugin marketplace add KNOB-bot/workingpaper-butler-marketplace
/plugin install workingpaper-butler
```

### 方式2：本地安装

```bash
/plugin install /path/to/workingpaper-butler
```

## 使用方法

### 命令

```
/workingpaper-butler:daily-report           # 生成今日论文推荐
/workingpaper-butler:daily-report 15      # 指定推荐数量
/workingpaper-butler:paper-search 关键词   # 搜索论文
```

### 自动触发

当提及以下内容时，技能会自动激活：
- "今日论文推荐"
- "帮我分析这篇论文"
- "翻译这个摘要"
- "搜索xxx相关论文"

## 研究兴趣配置

插件预设了7大研究领域：

| 领域 | 关键词 |
|------|--------|
| 市场一体化 | market integration, market segmentation |
| 创新增长 | innovation, R&D, TFP |
| 产业政策 | industrial policy, agglomeration |
| 区域发展 | regional development, spatial |
| 城市经济学 | urban, city, housing |
| 发展经济学 | developing country, poverty |
| AI与数字经济 | artificial intelligence, digital economy |

## 目录结构

```
workingpaper-butler/
├── .codebuddy-plugin/
│   └── plugin.json          # 插件清单
├── commands/
│   ├── daily-report.md      # 每日报告命令
│   └── paper-search.md      # 论文搜索命令
├── agents/
│   └── academic-researcher.md  # 学术研究代理
├── skills/
│   ├── daily-paper-recommend/  # 每日推荐技能
│   ├── paper-analyzer/         # 论文分析技能
│   ├── paper-translator/      # 翻译技能
│   └── academic-search/       # 搜索技能
└── scripts/                    # 核心脚本
    ├── nber_crawler.py       # NBER爬虫
    ├── arxiv_search.py       # arXiv搜索
    ├── translate.py          # 翻译模块
    └── generate_daily_report.py  # 报告生成
```

## 重要说明

本插件依赖 CBP-SCHOLAR 工作目录中的核心脚本：
- 插件需要配合 CBP-SCHOLAR 工作目录使用
- 请确保已配置正确的工作区路径
- 详细配置请参考 DEPLOY.md

## 依赖

- Python 3.8+
- scrapling
- requests
- arxiv

安装依赖：
```bash
pip install scrapling[all] requests arxiv
```

## 版本历史

### v1.0.0 (2026-03-14)
- 初始版本
- 每日论文推荐
- 论文分析
- 论文翻译
- 学术搜索

## 许可证

MIT License

## 作者

WorkingPaper Butler Team
