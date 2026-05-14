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

## Example

**Before validation:**

> 推荐→加购仅 2.8%，说明当前推荐效率极低。Kimi 式逐步刷墙（屏效 25%）中间过程挤占结果空间。

**After validation** (source confirms 2.8% but has no "25% screen efficiency" data):

> 推荐→加购仅 2.8%，说明当前推荐效率极低。Kimi 式逐步刷墙（中间过程挤占结果空间）效率低下。

The `2.8%` is kept because it matches the source. The fabricated `25%` is converted to descriptive language.

## Files

| File | Description |
|------|-------------|
| `SKILL.md` | The skill definition — contains the full workflow, pitfalls, and verification steps |
| `README.md` | This file — project overview and installation guide |

## License

MIT
