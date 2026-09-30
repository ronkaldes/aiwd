# 📋 All prompts in one place

Every copy-paste prompt for the lab, in order. Each is self-contained. **Fill in the `[SQUARE BRACKET]` placeholders with your own words**, copy the whole grey block, paste it into Claude, and **give Claude your data file** the first time (Steps 1–2).

> Tip: in **Claude.ai** click the 📎 paperclip to upload your file. In **Claude Code** just put the
> file in the `data/` folder and mention its name — Claude can open it itself.

---

## Step 0 (optional) — Generate a practice dataset

Only if you don't have your own data. See [`data/README.md`](../data/README.md) for the full version.

```text
Generate a realistic synthetic CSV dataset I can use to practice data analysis.

Topic: [e.g. "customers of a subscription software company"]
Outcome to hide in the data: [e.g. "which customers cancel"]

Requirements:
- About 800–1,200 rows and 20–35 columns; one row = one [customer/order/ticket/...].
- Mix of column types: identifiers, categories, dates, money, counts, scores, and a clear
  outcome column for the outcome above.
- Make it interesting to explore: plant 3–4 realistic hidden patterns that drive the outcome,
  plus a handful of data-quality flaws (some missing values, one duplicate row, a few
  impossible values, one extreme outlier).
- 100% synthetic — no real companies or people.

Give me the finished CSV file, plus a short list (for my eyes only) of the patterns
and flaws you planted, so I can check my work later.
```

---

## Step 1 — Look at your data

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

---

## Step 2 — Analyze the data and find the gaps

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

---

## Step 3 — Build a stunning data-story page

```text
Build me a single, self-contained HTML file (one file: inline CSS and JavaScript, no build step,
works by double-clicking it) that presents the key insights from [YOUR_FILE.csv] as a stunning,
modern, executive "data story" web page.

Include:
- A bold hero section with the single headline finding and the one number that matters most.
- The top drivers of the outcome shown as clean, labeled charts.
- The breakdowns by the groupings where the differences were biggest.
- A standout callout for the most surprising finding from the analysis — the thing nobody
  would have guessed.
- A short "what we should do about it" section at the end.

Make it beautiful: a polished dark theme, big readable typography, smooth scrolling, animated
number counters, and real chart visualizations (you can load a charting library like Chart.js
from a CDN). Use the actual numbers from the analysis so the values are correct. It should look
like something I'd be proud to put on screen in front of executives. Give me the finished HTML file.
```

---

## Step 4 — Research the landscape and propose an MVP

```text
I analyzed our data about [YOUR TOPIC — e.g. "our customers and why they cancel",
"our support tickets and why they run late"]. I want to turn insight into action.
Our key findings:
- [FINDING 1 from Step 2]
- [FINDING 2 from Step 2]
- [FINDING 3 from Step 2 — ideally the surprising one]

First, research how this problem is handled in the wider world. Who are the main players,
tools, or common approaches in [YOUR DOMAIN — e.g. "customer retention for subscription
software", "helpdesk operations", "e-commerce returns"]? For each, what do they offer around
this problem, and what do their users praise or complain about?

Then tell me:
- Where does our current approach look strong, and where does it look behind?
- Based on that landscape AND our data findings, propose ONE focused MVP — a small feature,
  tool, or process change — we should build to act on these findings.

Describe the MVP in one tight paragraph: what it is, who it's for, the single problem it
solves, and why it would win. Keep it realistic and as minimal as possible — the smallest
thing that delivers the value.
```

---

## Step 5 — Build the MVP prototype (minimal, fake data)

```text
Now build a working prototype of that MVP as a single self-contained HTML file (inline CSS and
JavaScript, no backend, no real data — use a small amount of hardcoded mock data that you make up,
shaped like the real data we analyzed).

Keep it as minimal as possible: the smallest version that demonstrates the core idea end-to-end
and feels real to click through. Show the main screen a user would live in, make the key items
clickable, and when I click one, show WHY it's flagged/interesting and ONE recommended action.
Make sure the mock data includes a couple of examples of the surprising pattern we found in the
analysis, so the demo makes the insight visible.

Modern, clean, professional UI. It must work by just double-clicking the file. Put a short comment
at the very top of the file stating what it is and that all the data is fake sample data.
Give me the finished HTML file.
```

---

## Step 6 — Create the management deck (your brand)

**If your company has a brand skill installed in Claude:**

```text
Use the [YOUR-BRAND-SKILL-NAME] skill to create a management presentation deck for
[YOUR COMPANY] leadership.

The story: in one short workshop we took our own data about [YOUR TOPIC], analyzed it
with AI, and found insights worth acting on. Walk leadership through it and ask for buy-in.

Cover, one idea per slide:
1. Title + the one-line message.
2. What we did (analyzed our own data with AI in an afternoon).
3. The headline findings, with the real numbers.
4. The blind spot: the surprising finding our current view of the business misses.
5. The root-cause story behind our worst-performing group — and why it's fixable.
6. How others handle this problem, and where we stand.
7. The MVP we propose — what it is and who it helps.
8. The ask: why we should invest, and the expected payoff.
9. Close on a confident recommendation.

Keep it fully on-brand and lead with outcomes, then the numbers.
```

**If you do NOT have a brand skill:** fill in
[`reference/BRAND_CHEATSHEET_TEMPLATE.md`](../reference/BRAND_CHEATSHEET_TEMPLATE.md), paste its
"One-paragraph brief you can paste to Claude" along with the same slide outline, and ask Claude
for a single self-contained HTML slide deck in those brand colors, fonts, and tone.
