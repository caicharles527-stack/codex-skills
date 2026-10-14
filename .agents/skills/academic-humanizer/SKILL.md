---
name: academic-humanizer
description: Analyze and revise Chinese or English academic prose for natural, precise scholarly expression while preserving supported claims, terminology, data, citations, references, and the author's voice. Also inspect invisible Unicode and whitespace problems. Use for thesis, paper, abstract, literature review, manuscript, academic editing, 学术润色, 论文润色, or AI-like writing analysis.
---

# Academic Humanizer

Improve academic prose without changing its research claims or disguising its provenance. The goal is clear, natural scholarly writing that retains the author's individual voice. Do not claim to detect AI authorship, promise to evade detectors, invent detector scores, or claim to remove a watermark that cannot be verified.

## Scope and preservation rules

1. Preserve every verifiable claim, qualification, uncertainty, number, unit, date, equation, table/figure reference, quotation, citation key, DOI, URL, footnote, reference-list entry, and domain term unless the user explicitly authorizes a substantive change.
2. Treat citations and references as protected text. Fix their surrounding grammar or placement only; never invent, delete, merge, renumber, or validate a source without evidence.
3. Keep the source language unless the user requests translation. For mixed Chinese-English text, preserve established technical names and abbreviations.
4. Match a writing sample supplied by the author. Otherwise use restrained, field-appropriate academic prose: specific, direct, and appropriately qualified.
5. Do not alter code, equations, tables, reference lists, quoted material, filenames, or Markdown/LaTeX syntax unless the user names it as editable.

## Workflow

### 1. Inspect before rewriting

Read the full requested passage. Identify only meaningful issues in these groups:

- **Template-like language:** generic openings, empty significance claims, staged contrasts, stock transitions, forced three-part lists, repetitive conclusions, and unnecessary emphasis.
- **Repetition and rhythm:** repeated sentence openings, duplicated claims, uniform sentence length, and recurring transitions that do not show a real logical relationship.
- **Language and logic:** collocation, grammar, agreement, punctuation, ambiguous reference, run-on or fragmented sentences, weak paragraph flow, unsupported causal language, and mismatches between evidence and conclusion.
- **Invisible formatting:** zero-width characters (`U+200B`–`U+200D`, `U+2060`, `U+FEFF`), soft hyphens (`U+00AD`), control characters, non-breaking spaces, ideographic spaces, unusual line separators, and suspicious mixed whitespace.

Do not label a sentence as AI-generated. Describe observable writing patterns instead.

### 2. Offer formatting cleanup safely

Report detected invisible characters by code point and location when possible. Offer one of these choices when cleanup could change layout or a reference:

- **Preview only:** list findings and leave text untouched.
- **Safe cleanup:** remove zero-width/control characters and normalize accidental whitespace outside protected text.
- **Exact cleanup:** apply only the user-specified replacements.

Never remove a non-breaking space, thin space, or special character inside a citation, DOI, equation, code, table, or name without flagging it first.

### 3. Revise

Make the smallest changes that improve precision, fluency, and academic coherence. Prefer concrete wording over inflated claims. Vary syntax when repetition makes prose mechanical, but do not vary it merely for novelty. Preserve cautious language such as “may,” “suggests,” “可能,” and “表明” where the evidence is limited.

For Chinese, maintain natural formal Chinese and use terminology consistently. Avoid literal English calques and gratuitous four-character phrases. For English, preserve discipline-specific conventions, article use, tense, hedging, and parallel structure.

### 4. Return an auditable result

Unless the user requests a different format, return:

1. **Issues found** — concise bullets, including invisible-format findings.
2. **Before / after comparison** — a table or aligned excerpts for material edits.
3. **Revised text** — complete cleaned and revised passage.
4. **Important changes** — brief explanations of edits that affect clarity, logic, or interpretation.
5. **Items to verify** — only genuine ambiguities that require author or source confirmation.

For a long manuscript, revise section by section and keep the same headings and citation structure. For file editing, preserve the original file and write the revised copy to a new path unless the user explicitly authorizes overwriting.

## SACE Academic Integrity

Use this module when the user supplies an SACE task sheet, rubric, academic-integrity policy, AI-use requirement, draft versions, revision notes, or research materials. Apply only the supplied requirements; do not claim that a paper complies with SACE rules when no relevant requirement is provided.

### Integrity review

1. Compare the draft against the supplied task requirements: scope, source/citation rules, permitted AI use, declaration wording, and required evidence of process. Separate confirmed compliance, potential concerns, and items the author must verify.
2. Check that claims, quotations, citations, data, tables, figures, and reference-list entries agree with one another. Flag an inconsistency or a missing link; never fabricate a source, data point, access date, research note, or justification.
3. Preserve real writing history. Organize only files, timestamps, version labels, tracked changes, notes, and research evidence the user actually provides. If history is absent, state that it was not supplied; do not reconstruct or simulate drafts or edit trails.
4. Keep edits proportionate. Correct language, structure, and logic while retaining the author's argument, choices, and voice. Flag a substantive rewrite for author review instead of silently replacing it.

### SACE output

When this module applies, add these sections after the normal revision:

1. **Requirement check** — a compact mapping from each supplied requirement to confirmed evidence, concern, or author action.
2. **Integrity record** — the real draft versions, change records, and research evidence provided, with any missing items clearly marked.
3. **AI-use declaration check** — assess the declaration only against the supplied rule; draft neutral wording only when the user requests it and facts are provided.
4. **Revision boundary** — identify edits that affect interpretation, evidence, or authorship and require the author's confirmation.

## Requests that need clarification

Ask before changing a claim, source, statistical interpretation, technical term, citation/reference, quotation, or intended audience/discipline when the answer changes the revision. If the request is limited to language polishing, proceed without asking.

## Suggested invocation

“Use academic-humanizer to inspect this Chinese/English academic passage. Preserve citations, terminology, data, and my voice. Show a before/after comparison and important changes; preview invisible-character cleanup before applying it.”

“Apply the SACE Academic Integrity module to this draft and the attached task requirements. Check compliance and AI-use declaration requirements, organize only the real drafts and research evidence I provide, and flag anything I need to verify.”
