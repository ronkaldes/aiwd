# Data dictionary — [YOUR DATASET NAME]

**File:** `[your_file.csv]` · **Rows:** [count] · **Columns:** [count]
**Grain:** one row = one [customer / order / ticket / ...].
**As-of date:** [when this data was exported]. **Source:** [where it came from].

> Hand this file to Claude alongside your data file. A model given column definitions
> reasons about the data; a model given only raw headers guesses.

---

## 🪄 Too much typing? Have Claude draft it

Paste this into Claude with your data file, then review and correct what it writes —
you know your data better than any guess:

```text
Here is my data file. Draft a data dictionary for it in a markdown table: for every column,
give the column name, its type (text / category / number / date / yes-no), and your best
plain-English guess at what it means. Group related columns under small headings.
Mark any column you're unsure about with "(?)" so I know to check it.
```

---

## Columns

Group related columns under headings that make sense for your data — for example
"Who/what this row is", "Money", "Activity & usage", "Dates", "Outcome".

### [Group 1 — e.g. Who this row is]
| Column | Type | Meaning |
|---|---|---|
| `[column_name]` | [text/category/number/date/yes-no] | [What it means, in one plain sentence. Note units, valid ranges, and special values like "0 means not recorded".] |
| `[column_name]` | | |

### [Group 2 — e.g. Money]
| Column | Type | Meaning |
|---|---|---|
| `[column_name]` | | |

### [Group 3 — e.g. Outcome]
| Column | Type | Meaning |
|---|---|---|
| `[outcome_column]` | | **The outcome you care about.** [e.g. 1 = customer cancelled, 0 = still active.] |

---

## Known quirks (fill in anything you already know)

- [e.g. "CSAT of 0 means the survey wasn't answered, not a real zero."]
- [e.g. "Rows before 2023 came from the old system and may have gaps."]
- [e.g. "Region is blank for customers signed before we tracked it."]
