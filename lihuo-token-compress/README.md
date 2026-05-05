# lihuo-token-compress 🔥

> 对任意 Skill 做极致 Token 优化重构，不损失功能逻辑。

[English](#english) | [中文](#中文)

---

## 中文

### 这是什么？

`lihuo-token-compress` 是一个 [WorkBuddy](https://www.codebuddy.cn/) Skill，专门对 Skill 文档做 Token 级别的极致压缩重构——在不损失任何功能逻辑的前提下，削减 20%–70% 的 Token 消耗。

### 为什么需要它？

Skill 越大，每次加载消耗的 Token 越多。冗余描述、重复规则、柔性措辞、长段落叙事……这些「噪音」不仅浪费 Token，还干扰模型对核心指令的理解。Token 压缩术就是来解决这个问题的。

### 核心特性

| 特性 | 说明 |
|---|---|
| **三级压缩** | L1 轻度(20-30%) / L2 中度(40-50%) / L3 极致(60-70%)，默认 L3 |
| **等价性自检** | 逐条比对原 Skill 与重构版，无新增/无遗漏/无语义偏移 |
| **Probe 验证** | 提取关键行为问题，验证重构版能否正确回答 |
| **反模式表** | 5 种常见压缩反模式及正确做法，防止「压缩即损坏」 |
| **指令映射表** | L3 可选，确保每条原指令在重构版有显式对应 |
| **零依赖** | 纯规则驱动，无需脚本/外部工具 |
| **目录式按需加载** | 参考资料先抽目录索引→仅加载必需章节→无关内容跳过 |

### 8 步重构流程

```
1. 原Skill拆解 → 2. 全域去重降噪 → 3. 极简模块化重组
→ 4. 文档读取优化 → 5. 句式精简+符号替代 → 6. 冗余全域裁切
→ 7. 等价性自检(+Probe验证+指令映射表) → 8. 最终输出
```

### 压缩技术速查表

| 技术 | Before | After |
|---|---|---|
| 去冗余 | "务必确保在执行前进行检查" | "执行前检查" |
| 缩写替代 | "Model Context Protocol server" | "MCP server" |
| 符号替代 | "如果A则执行B，否则执行C" | "A→B, ¬A→C" |
| 结构压缩 | "第一步X。然后Y。最后Z。" | "步骤：X→Y→Z" |
| 去柔性词 | "请确保""建议""务必""尽量" | 删除，改为刚性指令 |
| 密集格式 | 散段落描述参数 | 表格：参数/类型/必填/默认/说明 |
| 条目化 | "当你需要做X的时候，你应该先Y再Z" | "X时：Y→Z" |

### 安装

#### 方式一：Zip 安装

1. 下载 `lihuo-token-compress.zip`
2. 解压到 `~/.workbuddy/skills/lihuo-token-compress/`
3. 确保 `SKILL.md` 位于目录根

#### 方式二：手动创建

```bash
mkdir -p ~/.workbuddy/skills/lihuo-token-compress
# 将 SKILL.md 放入该目录
```

### 使用

安装后，在 WorkBuddy 中使用以下触发词即可自动加载：

- 「压缩Token」「优化Skill」「Skill瘦身」「Token优化」「减少Token」「Token压缩术」

也可直接说：

- 「帮我把这个 Skill 的 Token 压缩一下」
- 「用 L2 等级压缩这个 Skill」

### 目录结构

```
lihuo-token-compress/
└── SKILL.md    # 唯一必需文件，纯规则驱动
```

### 许可证

MIT License

---

## English

### What is this?

`lihuo-token-compress` is a [WorkBuddy](https://www.codebuddy.cn/) Skill that performs extreme Token-level compression and restructuring on Skill documents—reducing Token consumption by 20%–70% without losing any functional logic.

### Why do you need it?

The larger a Skill, the more Tokens it consumes on every load. Redundant descriptions, repeated rules, soft modifiers, long narrative paragraphs... these "noises" not only waste Tokens but also interfere with the model's understanding of core instructions. Token Compression is here to solve that.

### Core Features

| Feature | Description |
|---|---|
| **3-Level Compression** | L1 Light(20-30%) / L2 Medium(40-50%) / L3 Extreme(60-70%), default L3 |
| **Equivalence Self-Check** | Line-by-line comparison of original vs. restructured Skill — no additions, no omissions, no semantic drift |
| **Probe Verification** | Extract key behavioral questions to verify the restructured version answers correctly |
| **Anti-Pattern Table** | 5 common compression anti-patterns with correct approaches — prevent "compress then break" |
| **Directive Map** | Optional for L3, ensures every original directive has an explicit counterpart |
| **Zero Dependencies** | Pure rule-driven, no scripts or external tools needed |
| **Directory On-Demand Loading** | Extract TOC index first → load only necessary sections → skip irrelevant content |

### 8-Step Restructuring Flow

```
1. Skill Decomposition → 2. Global Dedup & Denoising → 3. Minimal Modular Restructuring
→ 4. Document Read Optimization → 5. Sentence Simplification + Symbol Substitution
→ 6. Global Redundancy Pruning → 7. Equivalence Self-Check(+Probe+Directive Map) → 8. Final Output
```

### Compression Techniques Cheat Sheet

| Technique | Before | After |
|---|---|---|
| Dedup | "务必确保在执行前进行检查" | "执行前检查" |
| Abbreviation | "Model Context Protocol server" | "MCP server" |
| Symbol | "如果A则执行B，否则执行C" | "A→B, ¬A→C" |
| Structure | "第一步X。然后Y。最后Z。" | "步骤：X→Y→Z" |
| Soft word removal | "请确保""建议""务必""尽量" | Delete, use imperative |
| Dense format | Paragraph description of params | Table: param/type/required/default/description |
| Itemization | "当你需要做X的时候，你应该先Y再Z" | "X时：Y→Z" |

### Installation

#### Option 1: Zip Install

1. Download `lihuo-token-compress.zip`
2. Extract to `~/.workbuddy/skills/lihuo-token-compress/`
3. Ensure `SKILL.md` is at the directory root

#### Option 2: Manual

```bash
mkdir -p ~/.workbuddy/skills/lihuo-token-compress
# Place SKILL.md in this directory
```

### Usage

Once installed, use the following trigger phrases in WorkBuddy:

- "压缩Token", "优化Skill", "Skill瘦身", "Token优化", "Token压缩术"

Or simply say:

- "帮我把这个 Skill 的 Token 压缩一下"
- "用 L2 等级压缩这个 Skill"

### Directory Structure

```
lihuo-token-compress/
└── SKILL.md    # The only required file, pure rule-driven
```

### License

MIT License
