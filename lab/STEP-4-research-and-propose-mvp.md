# Step 4 — Research the landscape and propose an MVP

> **Goal:** Use what the data told you to look at the wider landscape, then pitch one small idea that acts on your findings.
> **Time:** ~15 min  ·  **You'll need:** your top findings from Step 2 (the chat from Step 2 is handy but not required — the prompt below has room to paste them in).

## 🎯 What you're doing
So far you found *what's going on* in your data. Now you turn that into a plan. You'll ask Claude to look at the wider landscape around your problem — how other companies, tools, or teams handle it — and then propose ONE small thing you could build or change. "MVP" stands for **Minimum Viable Product** — the smallest version of an idea that still delivers real value. Small on purpose, so someone could actually build it.

No data file this time. This step is about thinking, not the spreadsheet.

## ✅ Before you start
- **Write down your 3 key findings from Step 2.** The prompt below has a slot for them. If you're in the same chat, you can even ask Claude first: "List our top 3 findings from the analysis in one line each" — then paste those lines into the prompt.
- **Turn on web search if your Claude has it (optional).** In Claude.ai, look for a small **web / search toggle or globe icon** near the box where you type your message, and switch it on. Not sure if you have it, or don't see it? No problem — skip this. Claude will still answer using what it already knows; just treat any specific claims about other companies as a starting point you'd double-check later.
- **One reminder:** your findings are patterns in *your* dataset — a sample, a snapshot, maybe imperfect. That's fine. The skill you're practicing is the thinking: from finding → to landscape → to one focused idea.

## 📋 The prompt — copy this into Claude
Fill in the placeholders, then copy the entire block and paste it in as a **new message**. It's long on purpose; that's normal.
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

## 👀 What you should expect back
A good answer reads like a quick competitive briefing, then lands on one clear idea. You'll probably see:
- A short rundown of the main players, tools, or approaches in your domain — what they actually do about your problem, not just a list of names.
- Honest two-sided framing: where your current setup looks strong and where others may be ahead.
- A clear link back to your three findings — especially the surprising one, since that's usually where the opportunity hides.
- **ONE focused MVP, not five.** If Claude lists several, that's your cue to push it to pick one (see the follow-ups below).
- A tight one-paragraph pitch that names what it is, who it's for, the single problem it solves, and why it would win.
- Realistic scope — an MVP that feels buildable in weeks, not a multi-year platform.

Don't worry if it doesn't match this list exactly. As long as you got a landscape read plus one small, sensible idea, you're in good shape.

## 💡 Make it better (optional follow-ups)
Pick one, type it as your next message (a normal reply in the same chat), and send it.
```text
Pick just ONE MVP and explain why it beats the others in one paragraph.
```
```text
Rewrite the MVP pitch for a busy executive: 4 sentences, plain language, no jargon.
```
```text
What would the very first version look like, and what would we deliberately leave out of v1?
```

## 🧯 If something goes wrong
- **Claude says it can't search the web.** Totally fine. Reply: "No web access is fine — use what you know and flag anything I should double-check." Treat any claims about other companies as a draft to verify, not gospel.
- **The answer is huge and hard to read.** Reply: "Summarize this in 10 bullets, then the MVP in one paragraph."
- **It proposed five features, not one.** Reply: "Choose the single best one and drop the rest."
- **It made up details about a company or tool.** Reply: "Mark anything you're unsure about as 'needs verification' and don't state guesses as facts."
- **Your domain doesn't have obvious "competitors."** That's fine — reframe it: "Instead of competitors, compare the 3–4 common ways teams like ours handle this problem, with the trade-offs of each."

## ➡️ Next
Now build it: open **[STEP-5-build-the-mvp.md](STEP-5-build-the-mvp.md)**.
