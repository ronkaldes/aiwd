# Step 2 — Analyze the data and find the gaps

> **Goal:** Have Claude read your file from top to bottom, find the problems hiding in it, and explain what drives the outcome you care about.
> **Time:** ~15 min  ·  **You'll need:** your data file open with Claude (using the same chat you started in Step 1 is perfect — or a new one, see below).

## 🎯 What you're doing
In Step 1 you got a first feel for the data. Now you go deeper. You're asking Claude to act like a senior data analyst: catch every flaw in the file, measure the headline numbers, and explain *what drives the outcome you picked* — which customers cancel, which orders get returned, which tickets run late, whatever your question is.

This is the heart of the lab. Everything you build later — the web page, the product idea, the deck — stands on what you learn here. You don't need any data background. You just fill in two placeholders, paste one prompt, and read what comes back.

## ✅ Before you start
- [ ] You finished **Step 1**, so Claude has already taken a first look at the file.
- [ ] You've picked **the outcome you care about** (Step 1's second follow-up helps if you haven't).
- [ ] Your data file is available to Claude in this chat. (A "chat" is one running conversation with Claude. If you're still in the same conversation as Step 1, you're all set. If you closed it and opened a fresh one, you'll need to give Claude the file again — see the reminder under the prompt below.)
- [ ] You have a few minutes. This answer will be longer than Step 1 — that's expected and good. You won't have to read every line.

## 📋 The prompt — copy this into Claude
Fill in the placeholders, copy the entire gray block, and paste it into the message box where you type to Claude. Then send it.
```text
Now act as a senior data analyst and analyze [YOUR_FILE.csv] in depth. The outcome I care
about is [YOUR OUTCOME — e.g. "which customers cancelled", "which orders were returned",
"which tickets missed their deadline"]. I want four things, with the actual numbers behind
every claim:

1. DATA QUALITY — Find every problem in the data: missing values, blanks, impossible values
   (numbers outside their sensible range, dates that can't be right), duplicates, and
   suspicious outliers. For each one, tell me how many rows are affected and how you'd clean
   or handle it.

2. THE BIG PICTURE — What are the headline numbers for my outcome (the overall rate, average,
   or total — whichever fits)? Then break it down by the 3–4 most natural grouping columns in
   this data (things like category, region, size, type, time period). Call out where it's
   surprisingly high or low.

3. DRIVERS — Which columns most separate the rows where the outcome happened from the rows
   where it didn't (or the high values from the low)? Rank the top drivers and show the
   difference in numbers for each.

4. ANOMALIES & SURPRISES — Find anything counterintuitive: rows that look one way on the
   surface but behave the opposite way, groups that break the overall pattern, or existing
   score/label columns in the data that disagree with what actually happened.

Finish with the 3 most important, non-obvious insights a manager should know, in plain
English. Describe everything you find as patterns in THIS dataset — don't overclaim beyond it.
```
**Reminder — how to give Claude the file (only needed if it can't see it yet):**
- **In Claude.ai (the website or app):** click the paperclip icon near the message box and upload your file from where you saved it.
- **In Claude Code (the terminal tool):** you don't attach anything — just make sure the file is inside the `data/` folder. Claude can already see the files there.

Not sure which one you're using? If you're in a web browser or the desktop app, it's Claude.ai. If you're typing commands in a black terminal window, it's Claude Code.

## 👀 What you should expect back
A good answer is organized into the four numbered sections you asked for, with real numbers behind each claim. You don't need to verify the math — just skim and look for these signs that Claude did the job well:

- **Data problems caught and counted** — a short list of flaws, each with how many rows it affects. Almost every real dataset has some: blanks, a duplicate or two, a value that can't be right, one wild outlier. Finding them is normal, not a failure.
- **Headline numbers you can sanity-check** — the overall rate or average for your outcome should feel roughly right to you. If it's wildly off from what you know, dig in (see troubleshooting).
- **Big differences between groups** — some category, segment, region, or time period should stand out from the rest. Those differences are where the story lives.
- **Ranked drivers with numbers** — not just "X matters" but "rows with low X had the outcome 3 times as often."
- **At least one genuine surprise** — a group that breaks the pattern, or an existing score/label column that disagrees with reality. These surprises often become your best material for Steps 3–6.
- **Three plain-English takeaways** at the end that a manager could act on tomorrow.

Your numbers are yours — there's no answer key. What matters is that every claim comes with a number and you believe the method.

## 💡 Make it better (optional follow-ups)
Already got a good answer? Paste any of these as your *next* message to dig deeper. (You don't need to re-attach the file — Claude still has it from a moment ago.)
```text
Show me the 10 rows that most break the pattern — the ones that look fine on the surface but had the worst outcome. List their key numbers in a table.
```
```text
For the group with the most surprising result, dig into WHY. Is it really that group, or is something else going on underneath?
```
```text
Turn your top 3 insights into a one-paragraph summary I could read aloud to a manager in 30 seconds.
```

## 🧯 If something goes wrong
- **Claude says it can't see the file.** Give it the file again: use the paperclip to re-upload it (Claude.ai), or confirm the file is sitting in the `data/` folder (Claude Code). Then paste the prompt once more.
- **The answer is huge and overwhelming.** That's normal — but you can shrink it. Reply: "Give me a short summary first — just the headlines — then I'll ask for detail on the parts I care about."
- **The numbers look off, or Claude seems to be guessing.** Reply: "Recompute directly from the file and show the row counts you used." (In Claude Code, Claude can run a small program over the file; in Claude.ai it reads the file directly. Either way this nudges it to count instead of estimate.)
- **Your data has no obvious outcome column.** Reply: "There's no single outcome column — suggest 3 outcomes we could derive from these columns, and analyze the best one." (For example: "late delivery" derived from two date columns.)
- **You want the answer again, done differently.** Just ask in plain words: "Redo section 3 as a ranked table," or "Explain that like I'm completely new to data." You can always nudge — nothing breaks.

## ➡️ Next
Now that you know the story hiding in the data, head to **[STEP-3-build-data-story-page.md](STEP-3-build-data-story-page.md)** to turn these insights into something people can see.
