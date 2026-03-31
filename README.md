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

### Claude Desktop

1. Download this repository as a ZIP file
2. Open Claude Desktop
3. Go to **Customize** (from sidebar)
4. Navigate to **Skills**
5. Click **"+" → Upload a skill**
6. Select the downloaded ZIP file

---

### Claude Terminal (Direct/Personal Use)

Clone your skill repo into your project's `.claude/skills/` directory:

```bash
git clone https://github.com/Mehrozsheikh/aso-appstore-listing-skill /Users/{USERNAME}/./.claude/skills/aso-appstore-listing-skill
```

- Replace `{USERNAME}` with your actual username, or use the full path to wherever your `./.claude/skills` exists
- Alternatively: download the ZIP file from GitHub, then open your `~/.claude/skills` folder and place the unzipped folder inside it
- Ready to use immediately

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

## Optional: Astro MCP (Real-Time ASO Data)

You can optionally connect Astro MCP to improve keyword quality with real-time rankings, ratings, and app store data.

- Astro is **optional** (the skill works without it)
- Learn more or install Astro: https://tryastro.app/?aff=kdX8mz
- Setup docs: https://tryastro.app/docs/mcp/

> Astro MCP is currently in beta. Always verify outputs before making strategic ASO decisions.

---

## How It Works

### 1. Input Understanding

Collects your app idea, audience, and features.

### 2. Keyword Strategy

- Uses provided keyword data OR
- Generates keywords based on intent and category
- If Astro MCP is enabled, can use real-time Astro data for stronger recommendations

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

## Working On

- Integrate other available skills into ours such as Screenshots Maker, Appstore Connect CLI, to fully automate your app submission process with AI.

---

## 📄 License

MIT
