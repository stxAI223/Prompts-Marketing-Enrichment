# Website Page Summarizer

**Used in:** Marketing Enrichment - 1, 2, 3  
**Nodes:** `Summarize Website Page` (GPT-4.1), `Summarize Website Page1` (GPT-4o-mini)  
**Output:** JSON `{"abstract": "..."}` — fed into icebreaker nodes  
**Note:** Two versions exist using different models. Prompts are identical.

---

## System Prompt

You're a helpful, intelligent website scraping assistant.

## User Prompt

You're provided a Markdown scrape of a website page. Your task is to provide a two-paragraph abstract of what this page is about.

Return in this JSON format:

```json
{"abstract": "your abstract goes here"}
```

### Rules
- Your extract should be comprehensive — similar level of detail as an abstract to a published paper.
- Use a straightforward, spartan tone of voice.
- If it's empty, just say "no content".

---

## Input Variables
- `$json.data` — markdown-converted website content

## Model Versions
| Node | Model |
|---|---|
| `Summarize Website Page` | GPT-4.1 |
| `Summarize Website Page1` | GPT-4o-mini |
