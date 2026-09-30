# 🚀 Setup — start here (about 5 minutes)

Welcome! This page gets you ready in a few minutes. No experience needed. Read it once, follow the steps, and you'll be off.

---

## 🤔 What is this?

This is a hands-on lab where **you use Claude to take a dataset all the way from raw numbers to a real result** — first you understand the data, then you find the insights hiding inside it, then you turn one of those insights into an idea, build a quick prototype, and finish with a polished management deck you could actually present. **You bring your own data file** — any spreadsheet-shaped file (CSV or Excel) from your work or life works. Claude does the heavy lifting; you just copy, paste, and watch it come together.

---

## 🧰 What you need

Two things:

1. **A Claude account.** If you don't have one yet, go to [claude.ai](https://claude.ai) and sign up — it's free to start.
2. **A data file.** Any CSV or Excel file with rows and columns: sales, tickets, surveys, sign-ups, inventory, expenses — anything. Don't have one handy? [`data/README.md`](data/README.md) has a one-prompt way to have Claude **generate a realistic practice dataset** for you.

There are **two easy ways** to do this lab. Pick the one that fits you:

- **Option 1 — Claude.ai in your browser (EASIEST — recommended for beginners). 👈**
  - This is just the Claude website, like any other site you visit.
  - You hand your data file to Claude using the **📎 paperclip** button (we'll show you exactly how).
  - If you've never used Claude before, **choose this one.** Nothing to install.

- **Option 2 — Claude Code / Claude desktop (for people comfortable with a terminal).**
  - This runs on your computer and works inside the lab's folder.
  - You don't attach anything — your data file just **sits in the `data/` folder and Claude reads it directly**.
  - Pick this only if a terminal/command line feels comfortable to you.

> **Not sure which you have?** If it's a website open in your browser, it's **Claude.ai** — go with Option 1. Either option works for the entire lab, start to finish.

---

## 📥 Get set up

1. **Get a copy of this lab folder on your computer** (if you're reading this, you probably already have it — otherwise download the ZIP from wherever it was shared and unzip it).
2. **Put your data file in the `data/` folder.** Copy your CSV or Excel file into `data/`. That's the one file the whole lab revolves around.
3. **(Optional but powerful) Fill in a data dictionary.** Copy `data/DATA_DICTIONARY_TEMPLATE.md`, list your columns and what they mean, and share it alongside your file. A Claude that knows what your columns mean gives noticeably better answers than one that has to guess.

---

## 📎 How to give your file to Claude

This is the part beginners worry about — it's genuinely easy. Use the method that matches your option above:

- **Claude.ai (browser):** In your chat, click the **📎 paperclip** icon near the message box, find and select your data file, then send your message. "Attaching" just means handing the file to Claude so it can read it. (Tip: if you start a brand-new chat later, you may need to attach it again.)

- **Claude Code / desktop:** **You don't attach anything.** As long as the file is in the `data/` folder, just send your prompt and mention the filename — Claude reads the file straight from the folder.

---

## ✏️ One small habit: fill in the placeholders

The prompts in this lab are generic on purpose. Each one has a couple of `[SQUARE BRACKET]` placeholders — like `[YOUR_FILE.csv]` or `[the outcome you care about]`. Before you paste a prompt, swap those for your own words. It takes ten seconds and it's the only "work" the lab asks of you.

**What's "the outcome you care about"?** Every interesting dataset has a question behind it: Which customers cancel? Which products sell? Which tickets take longest? Which campaigns convert? Pick the one question you'd most like your data to answer — that's your outcome, and you'll reuse it in almost every step. If you're not sure yet, that's fine: Step 1 has a follow-up prompt that asks Claude to suggest good candidate questions for your data.

---

## 🧭 How the lab works

- The lab is **6 steps**, in the **`lab/` folder**. Do them **in order** — each one builds on the one before it.
- Every step is a short page with a **prompt you copy and paste into Claude.** That's the whole pattern: copy, paste (after filling placeholders), read what comes back.
- All the prompts are **also collected in one place** at **`prompts/ALL_PROMPTS.md`**, if you'd rather grab them from a single page.
- **Keep your chat going.** Because the steps build on each other, stay in the *same conversation* with Claude so it remembers what you did earlier.

---

## ⏱️ How long it takes

About **60–90 minutes** end to end. But there's no pressure — **you can stop after any step** and still have something finished and shareable to show for it.

---

## 🔒 A note on your data

You're working with **your own file**, so a moment of care: if it contains real names, emails, account numbers, or anything sensitive, consider using an anonymized export — or generate a synthetic practice dataset instead (see `data/README.md`). When in doubt, leave the sensitive columns out.

---

## ✅ Ready?

**Start with [`lab/STEP-1-look-at-your-data.md`](lab/STEP-1-look-at-your-data.md).**
