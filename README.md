# Document Data Validation

An agent skill for validating data claims in documents against source materials.

## What It Does

Cross-references all data claims in a target document against explicit source documents. Automatically deletes or converts unsourced claims to descriptive language while maintaining the original source document framing for verified data.

## When to Use

- Verify data and numbers in a document against source materials
- Remove fabricated or unsourced data from documents
- Audit quantitative claims for source backing
- Ensure document integrity before publication

## Installation

Install via the [open agent skills ecosystem](https://skills.sh/):

```bash
npx skills add Alex2023-cyber/document-data-validation -g -y
```

Or manually copy `SKILL.md` to `~/.qoderwork/skills/document-data-validation/`.

## How It Works

1. **Identify** source and target documents
2. **Enumerate** all data claims in the target document
3. **Verify** each claim against source documents
4. **Fix** unverified claims (delete or convert to descriptive language)
5. **Report** the validation results

## Key Principles

- **Preserve verified data** — keep numbers that match the source exactly
- **Delete unsourced specifics** — remove fabricated percentages and figures
- **Convert to descriptions** — replace made-up numbers with qualitative language
- **Keep hypothetical examples** — scenario story placeholders are not data claims
- **Allow derived conclusions** — reasonable analytical inferences from source data are acceptable

## Files

| File | Description |
|------|-------------|
| `SKILL.md` | The skill definition — contains the full workflow, pitfalls, and verification steps |
| `README.md` | This file — project overview and installation guide |

## License

MIT

---

# 文档数据校验

一个用于交叉验证文档数据声明与来源材料的 Agent 技能。

## 功能介绍

扫描目标文档中的每一个数字、百分比和定量声明，并与权威来源文档进行逐一交叉验证。没有来源支撑的数据会被删除或转换为描述性语言，而已验证的数据会保留源文档的原始口径。

## 解决的问题

在撰写报告、分析或研究文档时，很容易无意引入听起来合理但没有真实来源的数字——或者误引源数据。此技能确保**文档中的每一个数据点都能追溯到权威来源**。

## 使用场景

- **报告审计**：对照源数据验证业务报告中的所有统计数据
- **研究验证**：确保分析论文中的每个数字都有恰当的引用来源
- **文档清理**：从 AI 生成的内容中删除编造或无来源的数据
- **质量保证**：在发布前交叉验证交付物与源材料

## 工作流程

1. **识别** — 确定源文档（权威来源）和目标文档（需要验证的文档）
2. **枚举** — 扫描目标文档中的所有定量声明，区分数据声明、假设性示例和推导结论
3. **验证** — 将每个声明与源文档交叉对比，分类为：已验证 / 部分匹配 / 未验证 / 矛盾
4. **修正** — 删除无来源的数字，转换为描述性语言，保留已验证数据的原始口径
5. **报告** — 总结变更内容以及使用的源文档

## 核心设计原则

| 原则 | 说明 |
|------|------|
| 来源优先 | 只有有明确来源支撑的数据才会被保留 |
| 原始口径 | 已验证数据保留源文档的精确表述和上下文 |
| 智能分类 | 区分事实声明、说明性示例和分析性推断 |
| 描述性兜底 | 当数字必须删除时，通过描述性语言保留原有的论点 |

## 安装方式

### 作为 QoderWork 技能

```bash
# 克隆此仓库到你的技能目录
cp -r document-data-validation ~/.qoderwork/skills/document-data-validation
```

### 作为 Agent 技能

此技能兼容 [开放 Agent 技能生态](https://skills.sh/)。安装方式：

```bash
npx skills add Alex2023-cyber/document-data-validation -g -y
```

## 文件结构

| 文件 | 说明 |
|------|------|
| `SKILL.md` | 技能定义 — 包含完整工作流程、注意事项和验证步骤 |
| `README.md` | 本文件 — 项目概览和安装指南 |

## 版本

当前版本：**1.0.0**

## License

MIT
