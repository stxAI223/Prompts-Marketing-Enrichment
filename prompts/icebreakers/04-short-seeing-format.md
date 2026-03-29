# Icebreaker — Short "Seeing" Format (No Intro)

**Used in:** Marketing Enrichment - 1, 2, 3  
**Node:** `ai1`, `ai2`, `Biz w joey`  
**Output:** Icebreaker line written to Google Sheets → `icebreaker` column  
**Persona:** No personal intro — drops straight into the compliment  
**Difference from others:** Skips the "I'm a 16-year-old..." intro entirely. Designed to slot into an email that already has an intro.

---

## System Prompt

You're a helpful, intelligent sales assistant.

## User Prompt

We just scraped a series of web pages for a business. Your task is to take their summaries and turn them into catchy, personalized openers for a cold email campaign to imply that the rest of the campaign is personalized.

You will return the icebreaker in the following format:

seeing the type of work you've done {use "with" if referring to a company they worked with or use "on" if referring to a project or their own business they worked on} {Thing they worked on or company they worked with} like {thing they did} {is or are} really inspiring.

### Rules
- Write in a spartan/laconic tone of voice.
- Make sure to use the above format when constructing your icebreakers.
- Shorten the company name wherever possible.
- Do the same with locations.
- Focus on small, non-obvious things to paraphrase. Do not say cookie-cutter stuff like "Love your website!" or "Love your take on marketing!".
- Never include "-", "—", or any em dashes — replace with "," or space
- If there is no website data, make the icebreaker super general

### Example
I'm a 16-year-old high school student who's really into business and outreach. I used to do a few web design projects, and seeing the type of work you've done with JobFlow like that small interview prep web simulator that scores answers by clarity is really inspiring.

---

## Input Variables
- `$json.abstract[0]` — website summary
- `First Name`, `Last Name`, `Company Name` — from Google Sheets lead row
