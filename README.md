# ASO App Store Listing Skill

Generate high-converting App Store listings (name, subtitle, keywords, and description) using AI-powered ASO best practices in one command.

---

## What It Does

This Claude Code skill helps you create a complete App Store listing for your app:

- **App Name** — keyword-optimized and within 30 characters
- **Subtitle** — supporting keywords without duplication
- **Promotional Text** — short, impactful hook
- **Keywords** — clean, high-impact token list
- **Description** — structured, readable, and conversion-focused

---

## Why Use It

- Avoid keyword duplication mistakes
- Follow real ASO best practices automatically
- Generate listings in seconds instead of hours
- Write in **simple, natural language** (no AI-sounding fluff)
- Iterate quickly with different tones or audiences

---

## Installation

### Option 1: Install via GitHub

claude install-skill github.com/mehrozsheikh/aso-appstore-listing-skill

---

### Option 2: Manual Installation (ZIP)

1. Download this repository as a ZIP file
2. Open Claude Code
3. Go to **Customize** (from sidebar)
4. Navigate to **Skills**
5. Click **"+" → Upload a skill**
6. Select the downloaded ZIP file

---

## Usage

1. Open a new Claude Code session
2. (Optional) Attach your codebase or repository for better results
3. Run:

/aso-appstore-listing-skill

4. Provide:

- App idea
- Target audience
- Features
- Tone (minimal, fun, premium, etc.)
- Optional keyword data

---

## How It Works

### 1. Input Understanding

Collects your app idea, audience, and features.

### 2. Keyword Strategy

- Uses provided keyword data OR
- Generates keywords based on intent and category

### 3. Listing Generation

Creates all fields in one pass:

- App Name (≤30 chars)
- Subtitle (≤30 chars)
- Promotional Text
- Keywords (comma-separated)
- Description (structured)

### 4. Iteration

Refine anything:

- Tone
- Keywords
- Specific fields

### 5. Memory

Your listing is saved so you can:

- update later
- reuse across sessions

---

## Writing Style

This skill focuses on:

- Simple, human language
- No exaggerated or “AI-sounding” phrases
- Clear benefits over technical jargon
- Readable, realistic tone

---

## Output Format

Returns clean JSON:

{
"app_name": "",
"subtitle": "",
"promotional_text": "",
"keywords": "",
"description": ""
}

Perfect for automation, scripts, or workflows.

---

## Example

**Input:**
App idea: habit tracker
Audience: students
Tone: minimal

**Output:**
{
"app_name": "Habit Tracker DailyFlow",
"subtitle": "Build routines stay focused",
"promotional_text": "Turn small actions into lasting habits",
"keywords": "habit,tracker,productivity,routine,focus,goals",
"description": "..."
}

---

## Project Structure

| File      | Purpose                               |
| --------- | ------------------------------------- |
| SKILL.md  | Core ASO logic and generation rules   |
| CLAUDE.md | Development and architecture guidance |

---

## Future Improvements

- CLI tool (npx aso-gen)
- Keyword import (CSV)
- Multi-language support
- A/B testing variants
- Competitor keyword insights

---

## 📄 License

MIT
