# Workshop Practice Data

These are downloadable text files that let any participant complete every module — even if they don't have an existing COR, an O*NET account, or an SLO list of their own to bring to the retreat.

Every file is plain `.txt` so it opens cleanly on any phone, laptop, or tablet, and pastes directly into any AI tool.

## Files at a glance

| File | What's in it | Used by |
|---|---|---|
| `module-1-starter-system-prompt.txt` | The starter system prompt + 9 test questions across 4 disciplines | Module 1 |
| `module-2-sample-catalog-descriptions.txt` | Four fictional outdated catalog descriptions (Health, Business, Construction, ICT), each with a list of "what's changed" notes you can mention to the AI | Module 2 |
| `module-3-onet-task-exports.txt` | Four real O*NET task exports (Registered Nurses, General & Operations Managers, Electricians, Network & Computer Systems Administrators) with SOC codes and California wage data | Module 3 |
| `module-4-sample-SLOs.txt` | Eight ready-to-use SLOs across the four disciplines, paired with suggested assessment types | Module 4 |
| `module-5-AI-output-with-errors.txt` | A polished-looking AI-generated COR draft with **12 planted hallucinations** + an answer key showing exactly what the AI got wrong and why | Module 5 |
| `iedrc-workshop-practice-data.zip` | All five files bundled together for one-click download | Any module |

## How participants use them

1. Click the **Download practice data** link on a module card on the live site.
2. Open the `.txt` file in any reader (Notes, TextEdit, Notepad, VS Code, even your browser).
3. Copy the relevant block of text.
4. Paste it into the placeholder spot in that module's prompt.
5. Run.

## Source attribution

- O*NET data is in the public domain (U.S. Department of Labor / Employment and Training Administration · O*NET-SOC 28.3 Database). Always re-verify current values at [onetonline.org](https://www.onetonline.org) before using in a real curriculum document.
- Catalog descriptions are fictional but written to mirror real outdated CORs from California community colleges.
- The Module 5 "AI output with errors" file is fictional and was authored deliberately to plant the 12 most common AI hallucinations seen in real curriculum drafts.

## Updating the data

These files are version-controlled in this folder. To update wage numbers, NEC editions, or O*NET task lists in a future cycle, edit the `.txt` files directly and rebuild the zip with:

```bash
cd data && zip iedrc-workshop-practice-data.zip module-*.txt
```
