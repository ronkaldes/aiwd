# Step 1 — Look at your data

> **Goal:** Understand what's inside your file before you analyze anything.
> **Time:** ~5 min  ·  **You'll need:** your data file in the `data/` folder and Claude open in front of you.

## 🎯 What you're doing
You're about to meet your data — properly. Your file is (most likely) a **CSV or Excel file** — just a spreadsheet (rows and columns). Before hunting for insights, you want the basics: how big is this file, what's in each column, and what one row actually represents. This is exactly what a careful analyst does first — you never analyze a file you don't understand. Think of it as reading the label before you cook.

## ✅ Before you start
- [ ] Your data file is in the `data/` folder (see [`data/README.md`](../data/README.md) if you don't have one yet — including how to generate a practice dataset). You don't need to open it yourself — Claude will read it for you.
- [ ] You have Claude open. Two ways to use it, pick whichever you have:
  - **Claude.ai** — open [claude.ai](https://claude.ai) in your browser and start a new chat. (You'll *attach* the file, explained below.)
  - **Claude Code** — the version that runs in a terminal inside this lab's folder. (It reads the file straight from the folder, no attaching needed.)
  - Not sure which you have? If it's a website in your browser, it's Claude.ai. Either one works for this whole lab.
- [ ] Nothing from a previous step is needed — this is the very first step.

## 📋 The prompt — copy this into Claude
Fill in the two `[SQUARE BRACKET]` placeholders, then copy the whole block and paste it into Claude as your message.
```text
I'm sharing a data file called [YOUR_FILE.csv]. In one or two sentences, here's what
I believe it is: [e.g. "an export of our customers — each row is one customer, with
their plan, activity, and whether they're still with us"].

Before any analysis, just help me understand what I'm looking at:
1. How many rows and how many columns are there?
2. List every column with a short, plain-English explanation of what it means
   (your best interpretation — flag any column you're unsure about).
3. Show me 5 example rows in a readable table.
4. In one sentence, what does a single row represent?

Don't look for patterns or insights yet — I only want to understand the shape of the data.
Explain it like I'm new to data analysis.
```
**Giving Claude the file (this is the part beginners trip on):**
- **In Claude.ai:** before you hit send, click the **paperclip icon** (📎) near the message box, then find and pick your file from the `data/` folder. "Attaching" just means handing the file to Claude so it can read it. Then send your message.
- **In Claude Code:** you don't attach anything. Just make sure the file is in the `data/` folder and send the prompt — Claude can open the file itself.
- **Have a data dictionary?** (See `data/DATA_DICTIONARY_TEMPLATE.md`.) Attach or mention it too — every answer gets sharper.

## 👀 What you should expect back
A calm, organized "here's what you've got" answer — no charts, no conclusions yet. Look for:
- A row and column count that roughly matches what you expected.
- A clear list of all columns, each with a one-line plain-English meaning — with honest "(unsure)" flags where the header alone isn't enough. Those flags are useful: correct them in your reply and Claude will remember for the rest of the chat.
- A small, readable table of **5 example rows** so you can see real values, not just column names.
- A one-sentence answer to what a single row represents — check it against what you know. If it's wrong, say so; getting the "grain" right matters for everything after.
- A friendly tone that explains terms instead of assuming you know them.

Don't worry about understanding every column yet — right now you just want to feel like you know the *shape* of the file. That's the whole goal of this step.

## 💡 Make it better (optional follow-ups)
Want to go a little deeper? Send any of these as your next message (no need to re-attach the file in the same conversation):
```text
Group the columns into a few simple categories (like "who/what this row is", "money", "activity", "dates", "outcomes") so it's easier to hold in my head.
```
```text
Based on this data, what are the 3 most interesting questions it could answer? For each, name the outcome column I'd focus on. Help me pick one to pursue.
```
```text
Pick the 8 columns you think matter most for understanding [the outcome you care about], and tell me why each one matters — in plain English.
```
> That second follow-up matters: the rest of the lab keeps referring to **"the outcome you care about."** If you haven't picked one yet, this is where you do it.

## 🧯 If something goes wrong
- **Claude says it can't see the file.** Re-attach it. In Claude.ai, click the paperclip (📎) and re-select your file. In Claude Code, confirm the file is really in the `data/` folder and that you spelled its name right.
- **The answer is huge and overwhelming.** Reply: "Can you give me a shorter version — just the row count, column count, and one row's meaning?"
- **You want it explained more simply.** Reply: "Explain that again like I've never seen a spreadsheet before."
- **Claude misread what a column means.** Just correct it in plain words: "`status` actually means the shipping status, not the customer status." Claude uses your correction from then on.
- **The file won't upload (too big, wrong format).** Ask the tool that produced it for a CSV export, or ask Claude: "How do I convert/shrink this file so I can share it here?"

## ➡️ Next
Head to **[STEP-2-analyze-and-find-gaps.md](STEP-2-analyze-and-find-gaps.md)** to start finding patterns — and the gaps hiding in the data.
