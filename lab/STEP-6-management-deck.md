# Step 6 — Create the management deck (your brand)

> **Goal:** Turn everything you found into a short, on-brand slide deck that asks leadership to back your idea.
> **Time:** ~15 min  ·  **You'll need:** the outputs from Steps 2–5 (the findings, the surprise, and the MVP idea), all in the **same Claude chat** you've been using. Best case: your company has a brand skill installed in Claude. No skill? You'll use `reference/BRAND_CHEATSHEET_TEMPLATE.md` instead — the steps below show you exactly how.

## 🎯 What you're doing
This is the finale. You've done the analysis — now you tell the story to the people who can say "yes." Claude builds a polished, on-brand presentation that walks leadership from "here's what we found" to "here's what we should do." You stop being someone who looked at a spreadsheet and become someone with a recommendation.

You don't need to design anything yourself. You paste one prompt, and Claude writes the whole deck for you.

## ✅ Before you start
- [ ] **Use the same chat as Steps 2–5.** Scroll up — if you can still see your earlier work in this conversation, Claude still remembers it and you're good. (Starting a fresh chat? See the fix at the bottom of this page.)
- [ ] Quickly remind yourself of the four things this deck will lean on, in case Claude asks:
  - the **headline findings** (your numbers from Step 2),
  - the **most surprising finding** — the thing nobody would have guessed (Step 2),
  - the **root-cause story** behind your worst-performing group — framed as fixable, not "that group is just bad" (Step 2),
  - and the **MVP idea** you shaped in Step 4 (and maybe prototyped in Step 5).
- [ ] Decide which path you're on:
  - **Path A — your company has a brand skill installed in Claude.** Easiest. Claude uses your real logos, fonts, colors, and templates for you.
  - **Path B — no brand skill.** No problem. You'll fill in one short template, copy a brand "brief" out of it, and paste it in front of the prompt. Your deck will still look unmistakably like *yours*.
- [ ] **Not sure which you have? Just try Path A.** If Claude replies that it can't find the skill, switch to Path B. Nothing breaks either way.

## 📋 The prompt — copy this into Claude

> **How to "copy this into Claude":** select all the text inside the gray box below, copy it, click in the message box at the bottom of your Claude chat, paste, and press Enter. That's it.

### Path A — you have a brand skill
Fill in the placeholders, copy this whole block, and paste it into Claude as one message.
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

### Path B — you do NOT have a brand skill
You'll send **one message** that has two parts stacked together: your brand brief first, then the prompt.

1. Open [`reference/BRAND_CHEATSHEET_TEMPLATE.md`](../reference/BRAND_CHEATSHEET_TEMPLATE.md) and fill it in for your company (5 minutes — colors, font, tone). If you already did this, great.
2. Copy the **"One-paragraph brief you can paste to Claude"** from your filled-in cheatsheet.
3. Paste that paragraph into your Claude message box.
4. Then fill in the placeholders in the block below, paste it **right underneath**, in the same message, and press Enter.

```text
Using the brand brief above, create a single self-contained HTML slide deck for
[YOUR COMPANY] leadership. One HTML file, no external files, in the brand colors, font,
and tone described in the brief. One idea per slide.

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

Lead with outcomes, then the numbers.
```

## 👀 What you should expect back
A 9-slide deck, one idea per slide, that reads like a confident story — not a wall of charts. Don't worry if your exact wording or numbers differ a little; Claude is telling *your* data's story. Look for:

- A short, punchy title slide with a single one-line message (something like "We can fix [the problem] by acting on what the data already knows").
- The headline numbers stated plainly — the same figures from your Step 2 analysis, not new inventions.
- A standout slide on the **surprising finding** — the thing your current dashboards or gut feel would have missed. This is the slide leadership will remember.
- The root-cause story tied to your worst-performing group — framed as a fixable cause, not blame.
- A clean MVP slide that says what you'd build, who it helps, and why it's small enough to start now.
- An "ask" slide with a clear payoff, and a confident closing line.
- On-brand styling: your colors, your font, your tone. On Path B, Claude hands you **one HTML file** — save it and double-click it to open the deck in your web browser.

## 💡 Make it better (optional follow-ups)
These are extras. Send any of them as a new message in the same chat, after the deck is built.

Add one strong number to the ask slide.
```text
On the "ask" slide, add one rough payoff estimate: if we fixed even a quarter of the problem the data shows, what would that be worth? Show your math simply.
```

Tighten the opening for a CFO.
```text
Rewrite slide 1's one-line message three different ways — one for a CFO, one for a product leader, one for the CEO. Keep each under 12 words.
```

Get a script to go with the slides.
```text
Write a 30-second spoken intro I can say out loud before slide 1, in a warm, confident tone.
```

## 🧯 If something goes wrong
- **"Claude can't find my brand skill."** That's fine — switch to Path B. Fill in `reference/BRAND_CHEATSHEET_TEMPLATE.md`, copy its "One-paragraph brief you can paste to Claude," paste it into your message, then paste the Path B prompt right under it and send.
- **You started a fresh chat, or the deck forgot your numbers (or invented new ones).** Claude only remembers what's in the current conversation. Paste your key results from Steps 2–5 back into the chat — the headline numbers, the surprising finding, the root-cause story, and your MVP idea — then say: "rebuild the deck using these exact numbers."
- **It's not on-brand (wrong colors, wrong tone, misspelled company name).** Reply with the specifics: "Fix the brand: [your background color] background, [your accent color] accents, [your case rule], and spell it '[Your Company]'."
- **The HTML deck (Path B) won't open or looks broken.** Reply: "Give me the full deck as one self-contained HTML file with everything inline, no external links." Then save Claude's answer as a file named `deck.html` and double-click it to open in your browser.
- **You want a different feel.** Just ask — "make it punchier," "fewer words per slide," or "more confident on the close." You can iterate as many times as you like; it never costs you anything to try again.

## ➡️ Next
That's it — you took raw data, cleaned it, found a real insight, shaped an MVP, and pitched it to leadership. That's the whole loop, start to finish. Head back to [`README.md`](../README.md) for a recap — then try the same loop on your next dataset. It works on all of them.
