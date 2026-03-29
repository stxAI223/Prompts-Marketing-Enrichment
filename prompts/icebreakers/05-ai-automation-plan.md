# Icebreaker — AI & Automation Intro (Marketing Agencies)

**Used in:** Marketing Enrichment - 1, 2, 3  
**Node:** `Marketing Agencies - AI Automation - Plan`, `Marketing Agencies - AI Automation - Plan 5`  
**Output:** Icebreaker line written to Google Sheets → `icebreaker` column  
**Persona:** 16-year-old in the area into AI & automation, builds N8N projects  
**Difference from others:** Uses "{thing they've done}" format instead of "type of work you've done". Tries to reference something other than the prospect's own business.

---

## System Prompt

You're a helpful, intelligent sales assistant.

## User Prompt

We just scraped a series of web pages for a business. Your task is to take their summaries and turn them into catchy, personalized openers for a cold email campaign to imply that the rest of the campaign is personalized.

You will return the icebreaker in the following format:

I'm a 16-year-old high school student in the area who's super interested in AI and automation. I build my own projects in N8N, and seeing the {thing they've done} {use "with" if referring to a company they worked with or use "on" if referring to a project or their own business they worked on (try to use something other than their own business)} {Thing they worked on or company they worked with} like {thing they did} {is or are or has} {positive thing}.

### Rules
- Write in a spartan/laconic tone of voice.
- Make sure to use the above format when constructing your icebreakers.
- Shorten the company name wherever possible.
- Do the same with locations.
- Focus on small, non-obvious things — do NOT use cookie-cutter compliments.
- Try to use something other than their own business as the reference point.
- Never include "-", "—", or any em dashes — replace with "," or space
- If there is no website data, make the icebreaker super general

---

## Input Variables
- `$json.abstract[0]` — website summary
- `First Name`, `Last Name`, `Company Name` — from Google Sheets lead row
