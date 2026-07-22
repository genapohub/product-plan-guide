# Product Plan Guide — 产品经理产品方案产出指南

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](SKILL.md)

一个面向 AI 编程助手的 **产品经理 Skill**，将结构化的产品方法论转化为可执行的工作流。当你在 AI 对话中提出产品需求时，它会自动识别需求所属的 5 类场景（0→1 新项目 / 中大型迭代 / 小优化 / 大版本升级 / 预研），按对应清单产出 PRD、BRD、MRD、埋点方案、上线方案等完整文档。

---

## 功能亮点

- 🔍 **5 场景智能识别** — 自动判断需求类型，匹配最佳产出级别
- 📋 **12 类文档覆盖** — PRD/BRD/MRD/竞品分析/用户研究/埋点方案/上线方案/数据方案等
- ✅ **内置质量检查** — 每份文档生成后自动校对完整性
- 🎯 **按需产出** — 小优化不过度设计，大版本不遗漏关键文档

## 适用场景

| 场景 | 示例 | 产出量 |
|------|------|--------|
| 场景一：0→1 新项目 | 全新 SaaS 产品规划 | 12 类文档 |
| 场景二：中大型迭代 | CRM 新增智能外呼模块 | 6-8 类文档 |
| 场景三：小优化/修复 | 登录页体验优化 | 2-3 类文档 |
| 场景四：大版本升级 | App V2.0 核心流程改造 | 8-10 类文档 |
| 场景五：预研项目 | AI 客服可行性分析 | 3-4 类文档 |

## 触发热词

产品方案、PRD、需求文档、需求规划、功能设计、写方案、做规划、需求迭代、版本升级、预研、埋点方案、上线方案、竞品分析、市场调研

---

## 安装

本 Skill 遵循 **Open Agent Skills 标准**（SKILL.md 格式），兼容以下工具：

### WorkBuddy / CodeBuddy

```bash
# 克隆到 user-level skill 目录（全局可用）
git clone https://github.com/你的用户名/product-plan-guide.git ~/.workbuddy/skills/product-plan-guide

# 或放到项目本地（仅当前项目可用）
git clone https://github.com/你的用户名/product-plan-guide.git .workbuddy/skills/product-plan-guide
```

也可以在 WorkBuddy 桌面端 → **技能市场** → **从 Git 仓库导入** → 粘贴仓库地址。

### Codex

```bash
# 克隆到 skills 目录
git clone https://github.com/你的用户名/product-plan-guide.git ~/.codex/skills/product-plan-guide

# 或使用通用路径
git clone https://github.com/你的用户名/product-plan-guide.git ~/.agents/skills/product-plan-guide
```

重启 Codex 后自动发现。也可以在对话中输入 `$product-plan-guide` 手动调用。

### Trae

**方式一：ZIP 导入（推荐）**
```bash
# 先下载并打包
git clone https://github.com/你的用户名/product-plan-guide.git
zip -r product-plan-guide.zip product-plan-guide/
```
然后在 Trae → **设置** → **Rules & Skills** → **创建** → 上传 `product-plan-guide.zip`。

**方式二：CLI 安装**
```bash
npx openskills install https://github.com/你的用户名/product-plan-guide.git
```

### Cursor

Cursor 使用 `.cursor/rules/*.mdc` 格式，不完全兼容原生的 SKILL.md。两种方式：

**方式一：作为 AGENTS.md 引用**
```bash
# 将 SKILL.md 内容复制到项目根目录的 AGENTS.md（或追加到已有文件）
cat product-plan-guide/SKILL.md >> .cursor/AGENTS.md
```

**方式二：转为 Cursor Rule**
```bash
# 复制并改扩展名
cp product-plan-guide/SKILL.md .cursor/rules/product-plan-guide.mdc
```
然后在 `.mdc` 文件头部添加 Cursor 需要的 frontmatter（description、globs、alwaysApply）。

### 通用（openskills CLI）

```bash
# 一键安装到当前项目
npx openskills install https://github.com/你的用户名/product-plan-guide.git

# 安装到全局
npx openskills install https://github.com/你的用户名/product-plan-guide.git --global
```

---

## 使用

安装后不需要额外配置。在 AI 对话中用以下任意方式触发：

```
帮我写一个宠物托运小程序的 PRD
这个 O2O 平台要做版本升级，帮我出个方案
AI 客服模块的可行性分析
登录页体验优化，写需求文档
```

Skill 会自动识别场景类型，先与你确认判断结果，再按清单产出完整文档。

---

## 目录结构

```
product-plan-guide/
├── SKILL.md                       # 主文件（工作流指令）
├── README.md                      # 本文件
├── LICENSE                        # MIT 协议
├── .gitignore
└── references/
    └── 产品方案产出指南.md          # 详细方法论（约700行）
```

---

## 贡献

欢迎提 Issue 或 PR 来改进本 Skill：

1. Fork 本仓库
2. 创建你的特性分支 (`git checkout -b feature/amazing-improvement`)
3. 提交你的改动 (`git commit -m 'Add some amazing improvement'`)
4. 推送到分支 (`git push origin feature/amazing-improvement`)
5. 打开一个 Pull Request

---

## 作者

**张孟博（张工）** — 10 年产品经理（3 年 Python 后端 + 6 年产品），专注 AI 产品设计与 O2O 履约闭环。

- 职业背景：宠物托运 O2O 平台「宠嗒嗒」产品负责人
- 技能栈：AI 产品设计、Vibe Coding、CRM 获客系统、多端 SaaS 平台架构

---

## 许可

[MIT](LICENSE) © 张孟博
