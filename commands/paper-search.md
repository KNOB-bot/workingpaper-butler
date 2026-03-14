---
name: paper-search
description: 搜索学术论文 - 在NBER、arXiv等数据库中搜索相关论文
argument-hint: "<关键词> [数量]"
---

# 论文搜索命令

使用此命令在学术数据库中搜索论文。

## 使用方法

```
/workingpaper-butler:paper-search 关键词
```

或指定结果数量：

```
/workingpaper-butler:paper-search 关键词 20
```

## 示例

```
/workingpaper-butler:paper-search market integration
/workingpaper-butler:paper-search innovation R&D 15
/workingpaper-butler:paper-search AI digital economy
```

## 支持的数据库

- **NBER**：美国国家经济研究局工作论文
- **arXiv**：预印本服务器（经济学相关）
- **RePEc**：经济学研究论文（待集成）

## 搜索策略

1. 首先搜索1天内发布的论文
2. 如不足则扩展到7天
3. 还不足则扩展到30天

## 输出格式

搜索结果将返回：
- 论文标题（英文+中文）
- 作者列表
- 发布日期
- 摘要（英文+中文）
- 相关性得分
- 原文链接

## 研究兴趣关键词

系统会自动根据您的研究兴趣对结果进行相关性评分，涉及领域包括：
- 市场一体化
- 创新增长
- 产业政策
- 区域经济发展
- 城市经济学
- 发展经济学
- AI与数字经济
