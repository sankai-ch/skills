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

| SKILL | 功能描述 | 适用场景 |
|:---|:---|:---|
| [job-hunter](./job-hunter/) | 多渠道招聘信息检索，支持从 BOSS直聘、猎聘、智联招聘、51job、牛客网等主流招聘平台及各大公司官网并行获取岗位信息，自动去重并输出结构化对比表格 | 社招/校招岗位检索、周边企业扫描、官网独家岗位发现 |

---

## 快速开始

### 克隆仓库

```bash
git clone https://github.com/sankai-ch/skills.git
cd skills
```

将 SKILL 复制或链接到你所使用的 AI 编程助手对应目录，以 `job-hunter` 为例：

```bash
# 复制
cp -r job-hunter ~/.claude/skills/          # Claude Code
cp -r job-hunter ~/.codex/skills/           # Codex CLI
cp -r job-hunter ~/.gemini/skills/          # Gemini CLI
cp -r job-hunter ~/.config/opencode/skills/ # OpenCode
cp -r job-hunter ~/.cursor/skills/          # Cursor

# 或使用符号链接（源仓库更新后自动同步）
ln -s $(pwd)/job-hunter ~/.claude/skills/job-hunter
ln -s $(pwd)/job-hunter ~/.gemini/skills/job-hunter
```

### 下载单个 SKILL

```bash
# 以 job-hunter 为例，替换 <target-dir> 为目标平台 SKILL 目录
svn export https://github.com/sankai-ch/skills/trunk/job-hunter <target-dir> --force
```

> 也可通过 GitHub 网页进入对应 SKILL 文件夹，点击 **「Code」→「Download ZIP」** 下载整个仓库后提取所需 SKILL。

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
