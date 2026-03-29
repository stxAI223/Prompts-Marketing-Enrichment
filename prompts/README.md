# n8n AI Prompts Library

All AI prompts extracted from Marketing Enrichment n8n workflows. Organized by category, deduplicated, with context on what each prompt does and where it outputs.

---

## 📁 Structure

```
prompts/
├── icebreakers/          # Cold email opening lines (SSGrowthAutomation)
├── website-summarizer/   # Website scraping & abstraction
├── company-name-cleaner/ # Normalize company names for cold email
└── relevize/             # Relevize channel partner value props (client)
```

---

## 🧊 Icebreakers

All icebreakers generate personalized cold email openers from scraped website data. They share the same base rules (no dashes, shorten names/locations, be specific) but differ in persona and format.

| File | Node | Persona / Format |
|---|---|---|
| `01-n8n-austin-ai-intro.md` | `ai automation1` | "I'm a 16yo in Austin into AI, I do N8N projects..." |
| `02-n8n-rag-agents-intro.md` | `ai` | Same but mentions RAG agents specifically |
| `03-micro-saas-intro.md` | `saas` | "I built my own micro SaaS in N8N..." |
| `04-short-seeing-format.md` | `ai1`, `ai2`, `Biz w joey` | No intro — drops straight into "seeing the type of work..." |
| `05-ai-automation-plan.md` | `Marketing Agencies - AI Automation - Plan` | "16yo into AI & automation, build N8N projects..." — uses `{thing they've done}` format |
| `06-precise-personal-short.md` | `ai v3` | ⭐ **Active/main node** — short format, most emphasis on being specific & personal |
| `07-multiline-deep-format.md` | `Generate Multiline Icebreaker` | Full multi-paragraph icebreaker for web design outreach |

---

## 🌐 Website Summarizer

| File | Node | Model |
|---|---|---|
| `01-page-abstract.md` | `Summarize Website Page` | GPT-4.1 |
| `01-page-abstract.md` | `Summarize Website Page1` | GPT-4o-mini |

---

## 🏷️ Company Name Cleaner

| File | Node | Purpose |
|---|---|---|
| `01-name-cleaner.md` | `Message a model2/3` | Strips LLC, Inc., locations from company names |

---

## 🎬 Talentless AI (Client)

Prompts for Talentless AI cold email campaign. Talentless AI produces cinematic mini commercials for brands using AI-powered production. Targets growth-stage B2B/DTC brands.

| File | Node | Output |
|---|---|---|
| `01-two-bullet-value-prop.md` | `ai v` (Talentless section) | 2 tailored bullets (27-37 words total) |

---

## 🤝 Relevize 

Prompts for Relevize cold email campaign. Relevize is a channel partner platform (MDF/SPIFF payments, co-branded campaigns).

| File | Node | Output |
|---|---|---|
| `01-three-bullet-value-prop.md` | `ai v`, `ai v5` | 3 tailored bullets (40-55 words total) |
| `02-single-bullet-value-prop.md` | `ai v2`, `ai v4` | 1 bullet (10-20 words) |
| `03-email-personalization-line.md` | `ai v4 mike` | 1 line that slots into specific email template |
| `04-deep-one-sentence-value-prop.md` | `ai v1` | 1 sentence with full product context in system prompt |
