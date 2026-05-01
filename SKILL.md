---
name: rednote-blogger-analysis
description: >
  Analyze any Xiaohongshu (RED/小红书) blogger from a profile link.
  Takes a RED profile URL, extracts available content, and produces a structured
  report on: content style, viral mechanics, persona construction, copywriting
  patterns, and monetization strategy. Use when someone shares a RED blogger link
  and wants to understand "what makes this blogger work" or "how to learn from
  their style". Also supports comparing two bloggers.
---

# RED Blogger Analysis

Given a Xiaohongshu (小红书) blogger profile link, produce a structured analysis of
their content strategy and why they succeed.

## Quick Start

```
分析这个博主：https://xhslink.com/xxx
```

## Extraction Strategy

RED is JavaScript-rendered. Try extraction methods in order:

### Method 1: web_fetch (fast, limited)
`web_fetch` on the profile URL captures static HTML — typically the bio, follower count, and name.
Use this as the baseline.

### Method 2: Browser automation (deeper)
When `web_fetch` returns only footer/boilerplate, switch to the browser tool:

```
browser: open → snapshot the profile page → extract visible notes
```

- Use `profile="user"` if the user's browser already has RED login cookies.
- If RED shows a login wall, stop and tell the user: "小红书需要登录才能看内容，请先在浏览器里打开并登录小红书，然后告诉我继续。"

### Method 3: Manual paste (most reliable)
When automated extraction hits a wall, ask for 3-5 representative posts:
```
我没办法自动抓取她的笔记内容，你能把她最近 3-5 条爆款笔记复制过来吗？
标题 + 正文就行，我帮你拆。
```

## Analysis Report Structure

For every blogger, produce a report covering these sections:

### 1. Overview
- Who they are (identity, niche, follower scale)
- One-sentence positioning: "[身份] + [差异化标签]"
- Core viral formula: the 1-2 mechanics that drive their success

### 2. Content Style Breakdown

#### Naming
- Structure (bilingual? pun? niche keyword?)
- Why it works as a memory point

#### Bio
- Layer-by-layer analysis: identity → credibility → hook → CTA
- What each layer signals and to whom

#### Content Pillars
Identify 3-4 recurring content types. For each:
- Name and format
- Purpose in the funnel (trust / traffic / conversion / retention)
- One representative example

#### Copywriting Patterns
When post text is available, analyze:
- **Title hooks**: number use, curiosity gap, emotional triggers, emoji density
- **Opening line**: identity setup, pain point, story hook, or counter-intuitive claim
- **Body rhythm**: paragraph length, emoji as visual breaks, list vs. narrative
- **Language persona**: catchphrases, tone (姐妹/宝子/兄弟), self-reference style
- **CTA style**: comment bait, save prompt, follow ask, or soft landing

#### Visual Style (when images available)
- Color palette tendencies
- Cover text layout (top-left overlay, center, bottom strip)
- Selfie vs. product vs. text-only covers
- Photo style (warm/cool, high/low contrast, lifestyle vs. studio)

### 3. Why It Works (Viral Mechanics)

Analyze the underlying drivers:
- **Identity hook**: what makes them stand out in their niche
- **Emotional engine**: what feeling do their posts trigger (aspiration, curiosity, FOMO, relief, anger)
- **Relatability lever**: how they close the distance with readers
- **Platform fit**: how their content exploits RED's algorithm / user behavior
- **Content moat**: what's hard for others to copy

### 4. Key Takeaways

3-5 actionable learnings for someone who wants to create similar content:
- What to borrow (replicable patterns)
- What not to copy (unique to them, would feel fake)
- What to combine with your own background

### 5. Comparison (optional, when two bloggers given)

| Dimension | Blogger A | Blogger B | Key Difference |
|---|---|---|---|
| Positioning | | | |
| Niche angle | | | |
| Viral mechanic | | | |
| Monetization | | | |
| Audience | | | |

## Operating Notes

- **Always be transparent** about what data you could vs. couldn't extract automatically.
- When content is sparse, lean into the profile bio analysis — a well-crafted RED bio often
  contains the entire strategy in compressed form.
- If the user mentions wanting to imitate the blogger, offer to generate a personalized
  strategy after the analysis is complete. See [references/IMITATION.md](references/IMITATION.md)
  for the imitation template.
- For bloggers outside RED (抖音, YouTube, Twitter), adapt the framework: naming → bio/profile →
  content pillars → copywriting patterns → viral mechanics → takeaways.
