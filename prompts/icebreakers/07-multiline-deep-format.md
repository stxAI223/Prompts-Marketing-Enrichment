# Icebreaker — Multiline Deep Format

**Used in:** Marketing Enrichment - 1, 3  
**Node:** `Generate Multiline Icebreaker`  
**Output:** Written to Google Sheets "Multiline Icebreaker Generator" sheet → `multiline_icebreaker` column  
**Difference from others:** Full multi-paragraph icebreaker, not just one line. Much longer. Uses a specific template with "Hey {name}", a love line, and a pitch paragraph. Built for web design outreach.

---

## System Prompt

You're a helpful, intelligent sales assistant.

## User Prompt

We just scraped a series of web pages for a business called . Your task is to take their summaries and turn them into catchy, personalized openers for a cold email campaign to imply that the rest of the campaign is personalized.

You'll return your icebreakers in the following JSON format:

```json
{"icebreaker": "Hey {name}. Love {thing}—also doing/like/a fan of {otherThing}. Wanted to run something by you.\n\nI hope you'll forgive me, but I creeped you/your site quite a bit, and know that {anotherThing} is important to you guys (or at least I'm assuming this given the focus on {fourthThing}). I put something together a few months ago that I think could help. To make a long story short, it's an outreach system that uses AI to find people hiring website devs. Then pitches them with templates (actually makes them a demo website). Costs just a few cents to run, very high converting, and I think it's in line with {someImpliedBeliefTheyHave}"}
```

### Rules
- Write in a spartan/laconic tone of voice.
- Make sure to use the above format when constructing your icebreakers.
- Shorten the company name wherever possible.
- Do the same with locations.
- For your variables, focus on small, non-obvious things to paraphrase.
- Do not say cookie-cutter stuff like "Love your website!" or "Love your take on marketing!".

### Example Output
```
Hey Aina,

Love what you're doing at Maki. Also doing some outsourcing right now, wanted to run something by you.

So I hope you'll forgive me, but I creeped you/Maki quite a bit. I know that discretion is important to you guys (or at least I'm assuming this given the part on your website about white-labelling your services) and I put something together a few months ago that I think could help. To make a long story short, it's an outreach system that uses AI to find people hiring website devs. Then pitches them with templates (actually makes them a white-labelled demo website). Costs just a few cents to run, very high converting, and I think it's in line with Maki's emphasis on scalability.
```

---

## Input Variables
- `$json.abstract` — array of website page summaries (joined)
- `first_name`, `last_name`, `headline` — from Loop Over Items node
