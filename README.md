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

## License

MIT
