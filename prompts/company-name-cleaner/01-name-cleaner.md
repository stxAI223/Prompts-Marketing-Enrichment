# Company Name Cleaner

**Used in:** Marketing Enrichment - 1, 3, 4, 5  
**Nodes:** `Message a model2`, `Message a model3`  
**Output:** Cleaned company name written to Google Sheets → `new company name` column  
**Purpose:** Strips LLC, Inc., locations, legal endings, and clutter from scraped company names so they sound natural in cold emails.

---

## System Prompt

You're cleaning up scraped business names to make them sound natural and professional for cold email use.

## User Prompt

You're cleaning up scraped business names to make them sound natural and professional for cold email use.

The names might include extra words, locations, legal endings (LLC, Inc., Co.), or strange formatting.

Company name: `{{ $json['Company Name'] }}`

Your job is to:
1. Simplify and normalize the name — remove clutter, locations, legal endings, and unnecessary words.
2. Keep the name short and natural — how someone would casually mention it in conversation or an email.
3. Preserve recognition — don't change the main brand identity or wording too much.
4. Fix capitalization and grammar.

### Examples
- "The Chiropractic Wellness Center, LLC - Austin, TX" → "Chiropractic Wellness Center"
- "Acupuncture & Holistic Healing of Central Texas" → "Holistic Healing"
- "Nails by Sarah | Professional Spa & Beauty" → "Nails by Sarah"
- "Dr. John's Complete Chiropractic & Rehab Clinic" → "Dr. John's Chiropractic"
- "Zen Wellness Spa & Massage – Houston" → "Zen Wellness Spa"

Output only the cleaned, natural-sounding company name.

---

## Input Variables
- `$json['Company Name']` — raw company name from Google Sheets
