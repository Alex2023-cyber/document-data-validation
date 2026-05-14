---
name: document-data-validation
description: Validate all data claims in a target document against source documents, delete or convert to descriptive language any claims without source backing, maintain original source document framing. Use when the user asks to verify data accuracy, check document claims against sources, audit numbers in a document, or remove fabricated/unsourced data from documents.
version: 1.0.0
---

# Document Data Validation

Cross-reference all data claims in a target document against explicit source documents. Delete or convert unsourced claims. Maintain original source document framing for verified data.

## When to Use

- User asks to verify data/numbers in a document against source materials
- User says "删掉没有依据的数据"、"排查没有来源的数据"、"验证数据真实性"
- Any situation where document data claims need source backing verification

## Steps

1. **Identify source and target documents**
   - Determine which document(s) serve as the authoritative source
   - Identify the target document whose data claims need validation
   - Read both documents fully before proceeding

2. **Enumerate all data claims in the target document**
   - Scan the entire target document for every number, percentage, statistic, and quantitative claim
   - Distinguish between:
     - **Data claims**: factual assertions about real-world numbers (e.g., "转化率为 2.8%")
     - **Hypothetical examples**: scenario illustrations with placeholder numbers (e.g., "日均45单" in a user story)
     - **Derived conclusions**: analytical inferences calculated from source data (e.g., "80%+ 用户" calculated from multiple categories)
   - List each data claim with its location (section/line)

3. **Verify each claim against source documents**
   - For each data claim, search the source document for the exact number or its supporting data
   - Classify each claim as:
     - **Verified**: exact match or directly derivable from source
     - **Partial match**: source supports the conclusion but not the exact phrasing
     - **Unverified**: no source backing found
     - **Contradicted**: source data conflicts with the claim

4. **Fix unverified claims**
   - **Delete** specific numbers/percentages that have no source backing
   - **Convert to descriptive language** where the underlying point is valid but the number is fabricated (e.g., replace "屏效 25%" with "中间过程挤占结果空间")
   - **Keep** verified data exactly as-is, maintaining the original source document's framing
   - **Keep** hypothetical examples (scenario stories) — they are illustrative, not data claims
   - **Keep** derived conclusions if they are reasonable analytical inferences from source data

5. **Report the results**
   - Summarize what was verified, what was deleted, and what was converted
   - Explicitly state which source document was used for verification
   - Note any claims that were kept with their original source framing

## Pitfalls

- **Don't delete scenario/story numbers** — hypothetical examples in user stories (like "日均45单", "¥3.5/件") are illustrative placeholders, not factual claims
- **Don't over-correct verified data** — if a number matches the source, keep it exactly as the source frames it
- **Distinguish session占比 from conversion rate** — a "2.8% of sessions" claim is different from "2.8% conversion rate"; match the source's framing
- **Derived conclusions are acceptable** if they are reasonable calculations from source data (e.g., summing multiple categories to get "80%+")
- **Always read the full source document first** — partial reading leads to false "unverified" classifications

## Verification

After completing validation:
- Re-read the modified target document to ensure no unsourced specific numbers remain
- Confirm all retained numbers have explicit source backing
- Verify that deleted/converted claims still preserve the document's argumentative intent through descriptive language
