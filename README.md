# DIT Global Public Health – Assessment Quiz

A simple MCQ practice quiz for the DIT Global Public Health assessment. Pick a category, answer questions with instant feedback, and track your score across all four topics.

## Run locally

The quiz loads questions from a JSON file, so you need a local web server (opening the HTML file directly will not work).

```powershell
cd "c:\side projects\DIT-exam"
python -m http.server 8765
```

Then open: [http://localhost:8765/DIT%20Quiz.dc.html](http://localhost:8765/DIT%20Quiz.dc.html)

Any local server works (Live Server, `npx serve`, etc.).

## Edit questions

Update `uploads/DIT_GPH_MCQ_Bank_consolidated.json` and refresh the page.

Each question follows this structure:

```json
{
  "id": "C1Q1",
  "question": "Your question here?",
  "options": { "A": "...", "B": "...", "C": "...", "D": "..." },
  "correct": "C",
  "correct_detail": "Explanation shown after answering."
}
```

## Project files

| File | Purpose |
|------|---------|
| `DIT Quiz.dc.html` | Quiz app |
| `uploads/DIT_GPH_MCQ_Bank_consolidated.json` | Question bank (source of truth) |
| `support.js` | DC runtime |
| `quiz-data.js` | Legacy backup — not used by the app |

## Categories

1. General Knowledge  
2. Body Systems, Physiology & Public Health Biology  
3. Public Health: Epidemiology & Study Designs  
4. Mathematics & Aptitude  

Default settings: 15 questions per category, 30-minute timer for the full test.
