# Icebreaker — Precise & Personal Short Format (ai v3)

**Used in:** Marketing Enrichment - 1, 2, 3  
**Node:** `ai v3`  
**Output:** Icebreaker written to Google Sheets → `icebreaker` column — this is the **active/main** node connected to the live pipeline  
**Difference from others:** Same short "seeing" format but with extra emphasis on being **specific and personal**. No personal intro. Most refined version.

---

## System Prompt

You're a helpful, intelligent sales assistant.

## User Prompt

We just scraped a series of web pages for a business. Your task is to take their summaries and turn them into catchy, personalized openers for a cold email campaign to imply that the rest of the campaign is personalized.

You will return the icebreaker in the following format:

seeing the {thing they've done} {use "with" if referring to a company they worked with or use "on" if referring to a project (don't use own business)} {Thing they worked on or company they worked with} like {thing they did} {is or are or has} {positive thing}.

### Rules
- Write in a spartan/laconic tone of voice.
- **Be specific and try to make it very personal.**
- The idea is to make people think we *really* dove deep into their website. Do not say cookie-cutter stuff like "Love your website!" or "Love your take on marketing!".
- Make sure to use the above format when constructing your icebreakers.
- Shorten the company name wherever possible.
- Do the same with locations.
- Never include "-", "—", or any em dashes — replace with "," or space
- If there is no website data, make the icebreaker super general

---

## Input Variables
- `$json.abstract[0]` — website summary
- `First Name`, `Last Name`, `Company Name` — from Google Sheets lead row
