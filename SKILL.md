---
name: rednote-blogger-analysis
description: >
  Analyze Xiaohongshu (RED/小红书) influencer posting techniques and generate
  imitation strategies. Use when the user wants to: (1) Analyze a RED blogger's
  content strategy from their profile bio, name, and posts, (2) Reverse-engineer
  a blogger's copywriting techniques, (3) Generate a personalized RED content
  strategy by imitating a successful blogger's framework, (4) Create RED note
  drafts in the style of a target blogger. Covers naming strategy, bio funnel
  design, content pillar planning, persona construction, differentiation
  analysis, and monetization funnel design.
---

# RED Blogger Analysis & Imitation

Analyze Xiaohongshu (小红书) influencers' content strategies and generate personalized
imitation plans.

## Workflow

When a user provides a RED blogger profile or posts, follow this pipeline:

1. **Extract** — Pull all visible data from the profile/page
2. **Deconstruct** — Map each element to the analysis framework
3. **Generate** — Produce actionable imitation templates for the user

## Analysis Framework

Apply these six lenses to every blogger:

### 1. Naming Strategy
- Bilingual signals (English authority word + Chinese self-deprecating slang)
- Conflict memory points ("华尔街 + 韭菜")
- Niche keyword embedding

### 2. Bio Funnel (4-Layer)
Every effective RED bio follows this structure:
```
Line 1: Identity anchor — credentials, company, title
Line 2: Result/endorsement — awards, track record, numbers
Line 3: Differentiation hook — what makes them unique in their niche
Line 4: Monetization CTA — where to go next
```

### 3. Persona Triangle
Map the blogger across three axes:
- **Authority** — credentials, results, experience
- **Relatability** — self-deprecation, shared struggles, everyday language
- **Entertainment** — humor, visuals, surprise, emotional hooks

The strongest accounts balance all three.

### 4. Content Pillars
Identify 3-4 recurring content types. Each pillar should:
- Have a clear purpose (trust / traffic / conversion / retention)
- Use a consistent format
- Target a specific user need

### 5. Differentiation Matrix
Compare to the niche baseline:
| Dimension | Typical blogger | This blogger |
|---|---|---|
| Identity | (niche norm) | (their angle) |
| Credibility source | (norm) | (their unique source) |
| Visual style | (norm) | (their style) |
| Core hook | (norm) | (their hook) |

### 6. Monetization Funnel
Map: Free content → Mid-tier product → High-ticket offer → Retention loop

## Imitation Generator

After analysis, generate a personalized plan. See [IMITATION.md](references/IMITATION.md) for the
full template.

### Quick Imitation Checklist
1. **Name** — English authority word + Chinese slang, 4-6 characters ideal
2. **Bio** — Fill each of the 4 layers with the user's real background
3. **Content pillars** — 3-4 columns mapped to user's actual expertise
4. **First post** — Draft using the "身份冲突 + 数据钩子 + 方法论框架 + CTA" format

### First Post Formula
```
Title: [Identity] + [Counter-intuitive claim] + [Number] + [emoji]
Body:
  Hook: Personal struggle or counter-intuitive fact (1-2 lines)
  Credibility: Why you're qualified (1 line)
  Method: 3-point framework, numbered
  Result: Specific number with benchmark comparison
  CTA: Low-friction ask (comment, follow, save)
```

## Input Formats

The skill accepts:
- **Profile URL** — fetch with `web_fetch`, extract bio, name, and visible stats
- **Raw bio text** — paste directly for analysis
- **Note/post content** — paste one or more posts for deep copywriting analysis
- **Comparison request** — "analyze X vs Y on RED"

## Limitations

- RED is JavaScript-rendered; `web_fetch` only captures static HTML (bio, name, follower count).
  Full post content requires manual copy-paste, browser automation, or API access.
- For deeper post-level analysis (title hooks, paragraph rhythm, emoji patterns, CTA techniques),
  request the user to paste 3-5 representative posts directly.
