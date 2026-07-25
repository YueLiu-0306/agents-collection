# Agent Skills Collection

> 一个角色扮演 Agent 技能集合仓库。每个子目录是一个独立的 AgentSkill，可单独导入灵犀、Claude、ChatGPT 等支持 SKILL.md 标准的平台。

## 收录技能

| 技能 | 角色 | 类型 | 状态 |
|------|------|------|------|
| [michael-lancaster](./michael-lancaster/) | 米切尔·兰卡斯特 | 沉浸式角色扮演 | ✅ 已完成 |
| [kaines-lloyd](./kaines-lloyd/) | 凯因斯·洛德 | 角色扮演 + 写作辅助 | ✅ 已完成 |

<!-- 新技能在这里添加一行 -->

## 目录结构

```
agents-collection/
├── README.md                          # 本文件
├── LICENSE                            # MIT 许可证
├── .gitignore
│
├── michael-lancaster/                 # 技能 1：Michael Lancaster
│   ├── SKILL.md                       # 核心扮演指南
│   └── references/
│       ├── knowledge.md               # 知识体系（按需加载）
│       └── background.md              # 背景与心理画像（按需加载）
│
├── kaines-lloyd/                     # 技能 2：Kaines Lloyd
│   ├── SKILL.md                       # 核心扮演与写作辅助指南
│   └── references/
│       ├── personality.md             # 心理画像（按需加载）
│       └── background.md              # 人际关系与背景（按需加载）
│
└── (future-agent)/                    # 技能 3、4... 后续添加
    ├── SKILL.md
    └── references/
```

## 使用方式

### 单独使用某个技能

进入对应角色子目录，将该文件夹导入你的 AI 平台：

- **灵犀**：客户端 → 技能 → 我的技能 → 导入技能目录
- **Claude**：将技能目录添加到技能路径
- **ChatGPT 等平台**：将 `SKILL.md` 作为 system prompt，`references/` 作为知识库

### 克隆整个仓库

```bash
git clone https://github.com/<你的用户名>/agents-collection.git
```

然后从仓库中选取需要的技能子目录导入即可。

## 添加新技能

1. 在仓库根目录下新建以角色名命名的文件夹（使用小写英文+连字符，如 `elena-voss`）
2. 文件夹内至少包含 `SKILL.md`，可按需添加 `references/` 子目录存放参考文件
3. 在本 README 的"收录技能"表格中添加一行
4. 提交并推送

## 技能规范

每个技能目录遵循 [AgentSkill](https://github.com/anthropics/agent-skills) 标准：

- **`SKILL.md`**（必需）：包含 YAML frontmatter（`name`、`description`）+ Markdown 正文，是技能的核心指令
- **`references/`**（可选）：存放按需加载的参考文件，SKILL.md 中通过相对路径引用
- **命名规范**：目录名使用小写英文 + 连字符（kebab-case）

## 许可证

MIT License — 所有技能可自由使用、修改、分发。
