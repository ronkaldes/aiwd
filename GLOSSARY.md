# Glossary

A friendly, plain-English cheat sheet for everyone in the data + AI workshop. No prior knowledge needed — each term gets a sentence or two. Terms are grouped by topic, and roughly alphabetical within each group.

---

## The Big Idea: Outcomes & Drivers

**Outcome** — The one thing your data can tell you that you most want to know: which customers cancel, which orders get returned, which tickets run late, which campaigns convert. Almost every step in this lab points back at the outcome you pick in Step 1.

**Outcome column (target)** — The column in your file that records whether/how the outcome happened for each row (for example, a `cancelled` column with yes/no, or a `days_late` column with a number). If your file doesn't have one, it can often be derived from other columns.

**Driver** — A column that helps explain the outcome. If customers with low usage cancel three times as often, usage is a driver. Drivers are what turn "here's a number" into "here's why."

**Rate** — A share expressed as a percentage: outcomes that happened ÷ total rows. If 100 customers start the year and 8 cancel, that's an 8% cancellation rate.

**Score** — A single number that sums up something complicated (a health score, a risk score, a lead score). Scores are useful and fallible — one of the best exercises in this lab is checking whether an existing score in your data actually agrees with what happened.

**Segment / Grouping** — Any way of splitting your rows into groups to compare them: by region, by plan, by size, by month. Big differences between groups are where stories hide.

---

## Data Files & Structure

**CSV** — "Comma-Separated Values": a plain spreadsheet saved as text — rows and columns, nothing fancy. The most universal data format; almost every tool can export one.

**Column (field)** — One attribute recorded for every row, like `region` or `amount`. Columns have types: text, category, number, date, yes/no.

**Grain** — What one row represents: one customer, one order, one ticket, one day. Getting the grain right is the first job of any analysis — everything else depends on it.

**Header** — The first row of a CSV, holding the column names.

**Row (record)** — One unit of your data — one customer, one order, one response. "1,000 rows" means 1,000 of whatever your grain is.

**Data dictionary** — A simple list of your columns and what each one means (units, valid ranges, special values). Sharing one with Claude makes every answer sharper. There's a template in `data/DATA_DICTIONARY_TEMPLATE.md`.

---

## Data Quality

**Data quality** — How clean, accurate, complete, and trustworthy your dataset is. Bad data quality (typos, gaps, duplicates) leads to bad conclusions — "garbage in, garbage out."

**Duplicate** — The same row appearing more than once, silently double-counting whatever it represents. Common and worth checking for.

**Impossible value** — A value that can't be right: a percentage above 100, a negative age, an end date before the start date. Usually a recording error — and always worth flagging.

**Missing value** — A blank or empty spot in the data where a number or label should be. We have to decide whether to fill, ignore, or flag these. Watch for disguised ones too: a `0` that actually means "not recorded."

**Outlier** — A data point that sits far outside the normal range — like one order 50x bigger than everything else. Outliers can be real, or they can be mistakes, so they're worth a closer look.

**Anomaly** — Something in the data that doesn't fit the expected pattern and looks suspicious or surprising. Anomalies can reveal errors, fraud, or genuinely unusual behavior worth investigating.

---

## Analysis Ideas Used in This Lab

**Breakdown** — The same headline number computed per group (rate by region, average by plan) so you can see who differs from whom.

**Correlation vs causation** — Two things moving together (correlation) doesn't prove one causes the other. Data shows you *where* to look; the *why* usually needs domain knowledge — yours.

**Root cause** — The real reason behind a pattern, one level deeper than the pattern itself. "Region X performs worse" is a pattern; "customers in region X rarely finished onboarding" is a root cause — and root causes are fixable.

**"Looks fine but isn't"** — The classic hidden gem: rows that score well on the obvious signals but are quietly heading for a bad outcome. Nearly every dataset has a version of this, and it's often the most valuable thing you find.

---

## Building Things

**HTML file** — A web page saved as a single file on your computer. Double-click it and it opens in your browser. Claude can write complete ones for you.

**Self-contained (single file)** — Everything the page needs — text, styling, charts, behavior — lives in that one file, so you can share it or open it anywhere.

**Prototype** — A rough first version meant to show an idea, not a finished product. Made-up data, real feel.

**Mock data** — Made-up sample values used in a prototype so it looks real without exposing anything real.

**MVP** — "Minimum Viable Product": the simplest version of something that still works and proves the idea. In a workshop, your MVP is a basic-but-functional first build, not a polished final product.

**Dashboard** — A single screen that shows the state of things at a glance — a few key numbers and a list or chart you can act on.

---

## Working with Claude

**Chat (conversation)** — One continuous thread with Claude. Claude remembers everything inside the same chat and nothing outside it — which is why the lab keeps saying "stay in the same chat."

**Attaching a file** — Handing Claude a file to read (the 📎 paperclip in Claude.ai). In Claude Code you skip this: files in the folder are already visible.

**Prompt** — The message you send to Claude. This lab's prompts are pre-written; your only job is filling in the `[SQUARE BRACKET]` placeholders.

**Synthetic data** — Made-up data generated to look and behave like real data, without being tied to actual people. Use it to learn and experiment safely — or when your real data is too sensitive to share.
