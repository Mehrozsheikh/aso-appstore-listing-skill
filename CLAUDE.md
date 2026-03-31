# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

---

## What This Is

A Claude Code skill (`aso-appstore-listing-skill`) that helps developers generate high-converting App Store listing metadata.

It is invoked via the `/aso-appstore-listing-skill` slash command and produces:

- App Name
- Subtitle
- Promotional Text
- Keywords
- Description

The goal is to improve both App Store search visibility (ASO) and conversion (downloads).

---

## Architecture

This is a lightweight skill with a simple structure:

- **SKILL.md** — The core logic of the skill. It defines:
  - Input collection
  - Keyword strategy
  - Listing generation rules
  - Iteration workflow
  - Memory usage

There are no scripts, external tools, or assets required.

---

## How the Skill Works

### 1. Memory Recall

The skill first checks Claude Code memory for existing listing data.

If found:

- Displays current listing
- Allows user to:
  - regenerate everything
  - update specific fields
  - refine tone or keywords

If not found:
→ proceeds to input collection

---

### 2. Input Collection

The skill gathers essential app details:

- What the app does
- Target audience
- Core features
- Tone (e.g. minimal, fun, premium)
- Optional keyword data

This ensures the output is relevant and contextual.

---

### 3. Keyword Strategy

Two modes:

**With keyword data:**

- Prioritize high popularity
- Prefer low competition
- Focus on relevance

**Without keyword data:**

- Infer keywords from:
  - app category
  - user intent
  - common search behavior

Rules enforced:

- No keyword duplication across fields
- Multi-word phrases split into tokens
- Focus on discoverability, not branding repetition

---

### 4. Generation

All listing fields are generated in one pass:

- **App Name** (≤30 characters)
- **Subtitle** (≤30 characters)
- **Promotional Text**
- **Keywords** (comma-separated)
- **Description** (structured)

Strict rules:

- No duplication across fields
- Strong keyword placement
- Clear, concise wording
- Benefits-focused messaging

---

### 5. Writing Style Rules

- Use simple, natural language
- Avoid exaggerated or AI-sounding phrases
- Keep tone aligned with the app (minimal, fun, premium, etc.)
- Prioritize clarity over clever wording

---

### 6. Output Format

The skill returns structured JSON:

```json
{
  "app_name": "",
  "subtitle": "",
  "promotional_text": "",
  "keywords": "",
  "description": ""
}
```
