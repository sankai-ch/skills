# Claude Code Skills 共享仓库

这是一个 Claude Code SKILLS 集合仓库，汇集各种业务场景下的实用 SKILL，帮助开发者快速整合信息、提升工作效率。每个 SKILL 均为独立模块，开箱即用。

> **SKILL.md 已是跨平台开放标准** — 本仓库的 SKILL 在 Claude Code、Codex CLI、OpenCode、Gemini CLI、Cursor 等主流 AI 编程助手上均可使用，无需修改。

---

## 现有 AI CLI 平台一览

| 平台 | 开发商 | 类型 | SKILL 安装路径（用户级） | SKILL 安装路径（项目级） |
|:---|:---|:---|:---|:---|
| **Claude Code** | Anthropic | 终端 CLI | `~/.claude/skills/<name>/` | `.claude/skills/<name>/` |
| **Codex CLI** | OpenAI | 终端 CLI | `~/.codex/skills/<name>/` | `.agents/skills/<name>/` |
| **Gemini CLI** | Google | 终端 CLI | `~/.gemini/skills/<name>/` 或 `~/.agents/skills/<name>/` | `.gemini/skills/<name>/` 或 `.agents/skills/<name>/` |
| **OpenCode** | 开源社区 | 终端 CLI | `~/.config/opencode/skills/<name>/` | `.opencode/skills/<name>/` |
| **Cursor** | Cursor Inc | IDE（内置终端） | `~/.cursor/skills/<name>/` | `.cursor/skills/<name>/` |
| **Windsurf** | Codeium | IDE（内置终端） | `~/.codeium/windsurf/skills/<name>/` | `.windsurf/skills/<name>/` |
| **Cline** | 开源社区 | VS Code 插件 | `~/Documents/Cline/Rules/*.md` | `.clinerules/*.md` |
| **Roo Code** | 开源社区 | VS Code 插件 | `~/.roo/rules/*.md` | `.roo/rules/*.md` |
| **GitHub Copilot** | GitHub/Microsoft | IDE 插件 + CLI | `~/.copilot/skills/<name>/` | `.github/skills/<name>/` |
| **Aider** | 开源社区 | 终端 CLI | `~/.aider.conf.yml`（配置文件） | `CONVENTIONS.md`（规则文件） |
| **Antigravity** | Google | 终端 CLI | `~/.agents/skills/<name>/` | `.agents/skills/<name>/` |
| **Augment Code** | Augment | IDE 插件 | `~/.augment/rules/*.md` | `.augment/rules/*.md` |
| **Kiro** | 开源社区 | 终端 CLI | `~/.kiro/skills/<name>/` | `.kiro/skills/<name>/` |

> 💡 **兼容性说明**：部分平台（如 OpenCode、Gemini CLI、Cline）会自动发现 Claude Code 的 `.claude/skills/` 路径下的 SKILL，安装到 `~/.claude/skills/` 可同时覆盖多个平台。

---

## 快速开始

### 方式一：克隆整个仓库（推荐）

```bash
git clone https://github.com/wangch/skills.git
cd skills
```

然后根据你使用的 AI 平台，将 SKILL 复制或链接到对应目录：

```bash
# Claude Code
cp -r skills/job-hunter ~/.claude/skills/

# Codex CLI
cp -r skills/job-hunter ~/.codex/skills/

# Gemini CLI
cp -r skills/job-hunter ~/.gemini/skills/

# OpenCode
cp -r skills/job-hunter ~/.config/opencode/skills/

# Cursor
cp -r skills/job-hunter ~/.cursor/skills/

# Windsurf
cp -r skills/job-hunter ~/.codeium/windsurf/skills/
```

或使用符号链接（源仓库更新后自动同步）：

```bash
# Claude Code
ln -s $(pwd)/skills/job-hunter ~/.claude/skills/job-hunter

# Gemini CLI
ln -s $(pwd)/skills/job-hunter ~/.gemini/skills/job-hunter
```

### 方式二：下载单个 SKILL（GitHub svn export）

```bash
# Claude Code
svn export https://github.com/wangch/skills/trunk/job-hunter ~/.claude/skills/job-hunter --force

# Codex CLI
svn export https://github.com/wangch/skills/trunk/job-hunter ~/.codex/skills/job-hunter --force

# Gemini CLI
svn export https://github.com/wangch/skills/trunk/job-hunter ~/.gemini/skills/job-hunter --force

# OpenCode
svn export https://github.com/wangch/skills/trunk/job-hunter ~/.config/opencode/skills/job-hunter --force

# Cursor
svn export https://github.com/wangch/skills/trunk/job-hunter ~/.cursor/skills/job-hunter --force
```

> 或通过 GitHub 网页进入对应 SKILL 文件夹，点击 **「Code」→「Download ZIP」** 下载整个仓库后提取所需 SKILL。

### 方式三：使用跨平台安装工具

社区已有多个统一管理 SKILL 的工具，可一键安装到多个平台：

```bash
# dotai — 跨平台 SKILL 管理器 (Claude Code / Cursor / Gemini CLI / OpenCode / Codex)
npm install -g dotai-cli

# glooit — 同步规则、SKILL、命令到多个平台
brew install nikuscs/glooit/glooit

# @kbuley/skills — 按平台安装
npx @kbuley/skills --claude    # 安装到 ~/.claude/skills/
npx @kbuley/skills --codex     # 安装到 ~/.codex/skills/
npx @kbuley/skills --gemini    # 安装到 ~/.gemini/skills/
npx @kbuley/skills --cursor    # 安装到 ~/.cursor/skills/
```

---

## SKILLS 列表

| SKILL | 功能描述 | 适用场景 |
|:---|:---|:---|
| [job-hunter](./job-hunter/) | 多渠道招聘信息检索，支持从 BOSS直聘、猎聘、智联招聘、51job、牛客网等主流招聘平台及各大公司官网并行获取岗位信息，自动去重并输出结构化对比表格 | 社招/校招岗位检索、周边企业扫描、官网独家岗位发现 |

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

## 贡献指南

欢迎提交 PR 分享你的 SKILL！请确保：

1. 每个 SKILL 放在独立文件夹中，文件夹名即 SKILL 名（kebab-case）
2. 包含 `SKILL.md` 文件，含 frontmatter（`name`、`description`）
3. 如有参考资源，统一放在 `references/` 子目录下
4. 提交前更新本 README 中的 SKILLS 列表表格

---

## 许可

MIT License
