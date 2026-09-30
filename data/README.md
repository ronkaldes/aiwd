# 📊 The `data/` folder — put your file here

This folder is where your dataset lives. The whole lab revolves around **one file of yours**: a CSV or Excel file with rows and columns.

## ✅ What works well

- **CSV** (`.csv`) — the safest bet. Most tools can export to CSV.
- **Excel** (`.xlsx`) — works fine too.
- Anything where **one row = one thing** (one customer, one order, one ticket, one survey response) and columns describe that thing.
- Roughly **100–50,000 rows** is the sweet spot for a smooth lab. Bigger files work, but answers get slower.

Some ideas for where to find a file: an export from your CRM or help desk, a sales or orders report, website analytics, a survey tool export, a sign-up list, an expense report.

## 🔒 Before you add a real file

If your file contains real names, emails, phone numbers, or account numbers, consider removing those columns first, or use an anonymized export. The lab never needs personally identifying columns — patterns live in the numbers and categories.

## 🪄 Step 0 — no data? Generate a practice dataset

You can do the entire lab on a realistic made-up dataset. Paste this into Claude, fill the two placeholders, and save what it gives you into this folder:

```text
Generate a realistic synthetic CSV dataset I can use to practice data analysis.

Topic: [PICK ONE — e.g. "customers of a subscription software company", "orders of an
online store", "support tickets of a helpdesk", "employees of a mid-size company"]
Outcome to hide in the data: [e.g. "which customers cancel", "which orders get returned",
"which tickets breach their deadline"]

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

Save the CSV it produces into this folder, keep the "planted patterns" list somewhere separate (that's your answer key), and do the lab as normal.

## 📖 Optional but powerful: a data dictionary

A **data dictionary** is a simple list of your columns and what each one means. Sharing it with Claude alongside your file makes every answer sharper — a model that knows `mrr` means "monthly recurring revenue in dollars" reasons; a model that only sees the raw header guesses.

Copy [`DATA_DICTIONARY_TEMPLATE.md`](DATA_DICTIONARY_TEMPLATE.md), fill it in (or have Claude draft it for you — the template shows how), and attach or mention it whenever you start a new chat.
