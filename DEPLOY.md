# WorkingPaper Butler 插件上架指南

> 工作论文管家插件上架流程详解

---

## 一、插件开发完成状态

### 插件信息

| 项目 | 内容 |
|------|------|
| **插件名称** | workingpaper-butler |
| **版本** | 1.0.0 |
| **描述** | 工作论文管家 - 每日论文推荐、学术研究助手 |
| **分类** | 学术研究 |
| **许可证** | MIT |

### 已创建的组件

| 组件类型 | 数量 | 文件 |
|----------|------|------|
| Commands | 2 | daily-report.md, paper-search.md |
| Agents | 1 | academic-researcher.md |
| Skills | 4 | daily-paper-recommend, paper-analyzer, paper-translator, academic-search |

### 目录结构

```
workingpaper-butler/
├── .codebuddy-plugin/
│   └── plugin.json          ✅
├── commands/
│   ├── daily-report.md     ✅
│   └── paper-search.md     ✅
├── agents/
│   └── academic-researcher.md  ✅
├── skills/
│   ├── daily-paper-recommend/   ✅
│   │   └── SKILL.md
│   ├── paper-analyzer/         ✅
│   │   └── SKILL.md
│   ├── paper-translator/       ✅
│   │   └── SKILL.md
│   └── academic-search/        ✅
│       └── SKILL.md
├── scripts/                    ✅
│   └── nber_crawler.py (占位符)
└── README.md                   ✅
```

---

## 二、上架流程

### 步骤1：创建市场仓库

**创建一个新的GitHub仓库**（推荐命名为 `workingpaper-butler-marketplace` 或类似）：

```
仓库名称：workingpaper-butler-marketplace
描述：WorkingPaper Butler 插件市场 - 学术研究助手
```

### 步骤2：创建市场配置文件

在仓库中创建 `.codebuddy-plugin/marketplace.json`：

```json
{
  "name": "workingpaper-butler-marketplace",
  "owner": {
    "name": "KNOB-bot",
    "email": "support@example.com"
  },
  "description": "工作论文管家插件市场 - 提供每日论文推荐、学术研究等功能",
  "version": "1.0.0",
  "plugins": [
    {
      "name": "workingpaper-butler",
      "source": {
        "source": "github",
        "repo": "KNOB-bot/workingpaper-butler"
      },
      "description": "工作论文管家 - 每日论文推荐、学术研究助手。基于NBER、arXiv、CrossRef等数据源自动推荐相关论文。",
      "version": "1.0.0",
      "author": {
        "name": "WorkingPaper Butler Team",
        "email": "support@example.com"
      },
      "homepage": "https://github.com/KNOB-bot/workingpaper-butler",
      "repository": "https://github.com/KNOB-bot/workingpaper-butler",
      "license": "MIT",
      "keywords": ["working-paper", "research", "paper", "NBER", "crossref", "daily-recommend"],
      "category": "学术研究",
      "strict": true
    }
  ]
}
```

### 步骤3：推送插件代码

将插件代码推送到GitHub：

```bash
# 初始化Git仓库
cd workingpaper-butler
git init
git add .
git commit -m "Initial commit: WorkingPaper Butler plugin v1.0.0"

# 推送到GitHub
git remote add origin https://github.com/KNOB-bot/workingpaper-butler.git
git push -u origin main
```

### 步骤4：推送市场配置

```bash
# 创建市场仓库
cd workingpaper-butler-marketplace
git init
git add .
git commit -m "Initial marketplace"

# 推送市场配置
git remote add origin https://github.com/KNOB-bot/workingpaper-butler-marketplace.git
git push -u origin main
```

---

## 三、安装和使用

### 安装市场

用户可以通过以下命令添加您的市场：

```bash
/plugin marketplace add KNOB-bot/workingpaper-butler-marketplace
```

### 安装插件

```bash
/plugin install workingpaper-butler
```

### 验证安装

```bash
/plugin validate workingpaper-butler
```

---

## 四、本地测试

在正式发布前，可以本地测试插件：

```bash
# 使用本地路径安装插件
/plugin install ./path/to/workingpaper-butler

# 或添加本地市场
/plugin marketplace add ./path/to/your-marketplace
```

---

## 五、后续维护

### 版本更新

当插件更新时：

1. 更新插件代码
2. 更新 `plugin.json` 中的版本号
3. 提交并推送更改
4. 市场会自动检测更新

### 发布新版本

```bash
# 1. 更新版本号
# 2. 提交更改
git add .
git commit -m "v1.1.0 - 新增xxx功能"

# 3. 创建标签
git tag v1.1.0

# 4. 推送
git push origin main
git push origin v1.1.0
```

---

## 六、相关资源

- [CodeBuddy 插件文档](https://www.codebuddy.ai/docs/zh/cli/plugins)
- [插件市场文档](https://www.codebuddy.ai/docs/zh/cli/plugin-marketplaces)
- [官方插件示例](https://github.com/codebuddy-plugins)

---

## 七、注意事项

1. **插件唯一性**：确保插件名称（`workingpaper-butler`）在市场中唯一
2. **版本管理**：遵循语义化版本号（MAJOR.MINOR.PATCH）
3. **文档完整**：确保README和SKILL.md文件完整清晰
4. **测试充分**：本地测试通过后再发布

---

## 八、联系与支持

如有问题，请通过以下方式联系：
- GitHub Issues
- 邮件：support@example.com

---

*本指南最后更新：2026-03-14*
