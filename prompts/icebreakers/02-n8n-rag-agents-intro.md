# Icebreaker — N8N RAG Agents Intro

**Used in:** Marketing Enrichment - 1, 2, 3  
**Node:** `ai`  
**Output:** Icebreaker line written to Google Sheets → `icebreaker` column  
**Persona:** 16-year-old in Austin, does N8N projects with RAG agents  
**Difference from 01:** Adds "with RAG agents" to the N8N mention

---

## System Prompt

You're a helpful, intelligent sales assistant.

## User Prompt

We just scraped a series of web pages for a business. Your task is to take their summaries and turn them into catchy, personalized openers for a cold email campaign to imply that the rest of the campaign is personalized.

You will return the icebreaker in the following format:

I'm a 16-year-old high school student in the Austin area who's super interested in AI. I've even done some of my own projects in N8N with RAG agents, and seeing the type of work you've done {use "with" if referring to a company they worked with or use "on" if referring to a project or their own business they worked on} {Thing they worked on or company they worked with} like {thing they did} {is or are} really inspiring.

### Rules
- Write in a spartan/laconic tone of voice.
- Make sure to use the above format when constructing your icebreakers.
- Shorten the company name wherever possible.
- Do the same with locations.
- Focus on small, non-obvious things to paraphrase.
- Never include "-", "—", or any em dashes — replace with "," or space
- If there is no website data, make the icebreaker super general

### Example
I'm a 16-year-old high school student in the Austin area who's super interested in AI. I've even done some of my own projects in N8N, and seeing the type of work you've done with JP like that small resume heatmap you built has really inspired me.

---

## Input Variables
- `$json.abstract[0]` — website summary
- `First Name`, `Last Name`, `Company Name` — from Google Sheets lead row
