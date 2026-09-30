# 🧭 Data Explorer Lab — from raw file to real result

A hands-on, no-experience-needed lab where **you use Claude to take any dataset all the way from raw numbers to a finished result**: understand the data, find the insights hiding inside it, turn one insight into an idea, build a quick prototype, and finish with a polished management deck.

**The twist: you bring your own data.** Any CSV or Excel file works — sales records, support tickets, survey results, website analytics, inventory, sign-ups, anything with rows and columns. No data of your own? No problem — Step 0 in [`data/README.md`](data/README.md) shows you how to have Claude generate a practice dataset in one prompt.

---

## 🗺️ The journey (6 steps, ~60–90 minutes)

| Step | What you do | What you end up with |
|---|---|---|
| [1 — Look at your data](lab/STEP-1-look-at-your-data.md) | Understand what's in the file before analyzing anything | A clear picture of your data's shape |
| [2 — Analyze & find the gaps](lab/STEP-2-analyze-and-find-gaps.md) | Have Claude act as a senior analyst: quality issues, patterns, drivers, surprises | The real story hiding in your data |
| [3 — Build a data-story page](lab/STEP-3-build-data-story-page.md) | Turn the insights into a beautiful one-file web page | Something you could put on a screen in a meeting |
| [4 — Research & propose an MVP](lab/STEP-4-research-and-propose-mvp.md) | Look at the wider landscape, then pitch ONE small idea | A focused, buildable product idea |
| [5 — Build the MVP prototype](lab/STEP-5-build-the-mvp.md) | Turn the idea into a clickable prototype | A working demo you can show people |
| [6 — Management deck](lab/STEP-6-management-deck.md) | Tell the whole story to the people who can say "yes" | A polished, on-brand slide deck |

Every step is the same pattern: **copy a prompt, paste it into Claude, read what comes back.** All prompts are also collected in [`prompts/ALL_PROMPTS.md`](prompts/ALL_PROMPTS.md).

---

## 🚀 Start here

1. Read [`SETUP.md`](SETUP.md) — 5 minutes, gets you ready.
2. Put your data file in the [`data/`](data/) folder (or generate a practice one).
3. Open [`lab/STEP-1-look-at-your-data.md`](lab/STEP-1-look-at-your-data.md) and go.

You can **stop after any step** and still have something finished to show for it.

---

## 📁 What's in this kit

```
data-workshop/
├── README.md                        ← you are here
├── SETUP.md                         ← 5-minute setup, start here
├── GLOSSARY.md                      ← plain-English cheat sheet of every term
├── lab/                             ← the 6 steps, do them in order
├── prompts/ALL_PROMPTS.md           ← every prompt in one place
├── data/                            ← put YOUR data file(s) here
│   ├── README.md                    ← how to add your data (+ Step 0: generate practice data)
│   └── DATA_DICTIONARY_TEMPLATE.md  ← optional: document your columns for better answers
└── reference/
    └── BRAND_CHEATSHEET_TEMPLATE.md ← fill in your brand for the Step 6 deck
```

---

## 🔒 A note on your data

This lab runs on **your** data, so treat it accordingly: if your file contains real customer names, emails, or anything sensitive, consider using an anonymized export or a practice dataset instead. Whatever you share with Claude in a chat stays in that chat — but be deliberate about what you upload, the same way you would with any tool.
