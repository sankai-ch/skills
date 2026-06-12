# ai-skills

AI 编程助手 SKILLS 共享仓库，汇集各种业务场景下的实用 SKILL。每个 SKILL 均为独立模块，开箱即用，支持 Claude Code、Codex CLI、OpenCode、Gemini CLI、Cursor 等主流 AI 编程助手。

---

## 目录结构

```
skills/
├── README.md               # 本文件
├── job-hunter/             # 招聘信息检索 SKILL
│   ├── SKILL.md            # SKILL 定义与工作流程
│   └── references/         # 参考资源
│       ├── company_career_pages.md
│       └── recruitment_platforms.md
└── ...                     # 更多 SKILL 持续添加中
```

---

## SKILLS 列表

| SKILL | 描述 | 作者 | 仓库 |
|:---|:---|:---|:---|
| [job-hunter](./job-hunter/) | 多渠道招聘信息检索Skill。当用户提出找工作、求职、社招、招聘信息查询等需求时使用。支持从主流招聘平台（BOSS直聘、猎聘、智联招聘、51job、牛客网等）和各大公司官网招聘页面并行获取岗位信息，自动去重并输出结构化对比表格 | [sankai-ch](https://github.com/sankai-ch) | [skills](https://github.com/sankai-ch/skills) |

---

## 安装

**对你的 AI 编程助手说一句话即可完成安装：**

### 安装全部 SKILL

```
帮我安装 https://github.com/sankai-ch/skills 仓库中的所有 SKILL
```

### 安装单个 SKILL

```
帮我安装 https://github.com/sankai-ch/skills 中的 job-hunter SKILL
```

AI 会自动完成仓库克隆、SKILL 目录复制到对应平台路径的全部操作。支持 Claude Code、Codex CLI、Gemini CLI、OpenCode、Cursor 等主流 AI 编程助手。

---

## 贡献指南

欢迎提交 PR 分享你的 SKILL！请确保：

1. 每个 SKILL 放在独立文件夹中，文件夹名即 SKILL 名（kebab-case）
2. 包含 `SKILL.md` 文件，含 frontmatter（`name`、`description`）
3. 如有参考资源，统一放在 `references/` 子目录下
4. 提交前更新本 README 中的 SKILLS 列表表格

---

## 许可

MIT License
