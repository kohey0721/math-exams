# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Data-only repository containing scanned math exam questions (PNG images) from Japanese high school textbooks. There is no application code — the repo is a structured image dataset for two math subjects.

## Data Structure

```
data/
├── 数学α/          # Math α — Exponents & Logarithms (questions 325–395)
│   └── 数学α.txt   # Table of contents: topics → question ranges → difficulty steps
├── 数学β/          # Math β — Geometry (questions 150–234)
│   └── 数学β.txt   # Table of contents: topics → question ranges → difficulty steps
```

Each subject directory contains question folders with four naming types:
- `大問N` — Main questions (e.g., 大問150)
- 例題N` — Worked examples (e.g., 例題26)
- `演習問題N` — Practice exercises
- `総合問題N` — Comprehensive problems

### Question folder layout

- Each folder contains one PNG (the question image), named by timestamp `YYYYMMDD_HHMMSS.png`
- If the question has sub-parts, a `小問/` subdirectory holds additional PNG images (one per sub-part)

### Topic index files (`.txt`)

The `数学α.txt` and `数学β.txt` files map topics to question number ranges with difficulty tiers:
- **STEP A** — Basic level
- **STEP B** — Intermediate level
- **発展問題** — Advanced/extension problems

## Key Numbers

- 2 subjects, 184 question folders total (83 α + 101 β)
- 498 PNG images across 297 directories
- 110 questions have sub-parts (小問)

## Working with this data

When processing images, use the topic index `.txt` files to understand which mathematical topic a question number belongs to. Question numbering is globally unique within each subject.
