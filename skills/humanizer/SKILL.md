---
name: humanizer
description: Use on any draft (post, email, landing page copy, docs, script) to strip AI-writing tells and make it read like a person wrote it. Returns the revised draft plus a short list of what changed. Never adds facts.
---
# Humanizer

Based on Wikipedia's public guide "Signs of AI writing" (https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing).

Input: one draft, plus optional samples of the author's own writing. Output: the revised draft and a short list of what changed. This skill never posts or sends anything.

## 1. Steps

1. **Scan for tells.** Read the draft once and flag every item from Section 2 before changing anything.
2. **Rewrite.** Fix each flagged item in place: plain verb for copula avoidance, real noun for vague association, cut tacked-on -ing analysis. Do not change meaning or facts.
3. **Match the voice.** If the user gave writing samples, match their sentence length, word choice and tone (Section 3). Otherwise use the plain default voice.
4. **Apply the rules.** Check Section 4 top to bottom.
5. **Read-aloud test.** Any phrase that sounds like a press release or a chatbot reply fails.
6. **Report.** List the categories of tells removed and confirm every original fact and number was kept.

---

## 2. AI-writing tells to remove

### Puffery and significance
- **Watch:** stands/serves as, is a testament to, pivotal/crucial/vital/key role, underscores/highlights its significance, reflects broader, symbolizing enduring, setting the stage for, represents a shift, indelible mark, evolving landscape, focal point
- **Fix:** delete or replace with the actual fact. "Serves as the hub" → "is the hub."

### Superficial -ing analyses
- **Watch:** phrases tacked onto sentence ends, such as highlighting X, underscoring Y, ensuring Z, reflecting/symbolizing W, contributing to, cultivating/fostering, encompassing, enhancing
- **Fix:** cut the phrase entirely or state the fact as its own sentence.

### Promotional and advertisement-like language
- **Watch:** boasts, vibrant, rich, profound, groundbreaking, renowned, diverse array, showcasing, exemplifies, commitment to, nestled, in the heart of, natural beauty, featuring (meaning "has")
- **Fix:** use a plain factual noun or verb.

### Vague attribution and weasel words
- **Watch:** Industry reports, Observers have cited, Experts argue, Some critics argue, several sources (when citing one or two)
- **Fix:** name the source, or delete the claim.

### Vague "associated with"
- **Watch:** associated with, connected to, in connection with, when used instead of a real relationship
- **Fix:** state the relationship directly. "Was associated with leadership" → "was CEO."

### "Despite challenges" endings
- **Watch:** Despite its [praise], faces challenges…; Challenges and Legacy; Future Outlook; any rigid wrap-up paragraph
- **Fix:** end on the last real fact; cut the formulaic conclusion.

### AI vocabulary words
- **2023 to mid-2024:** Additionally (as an opener), boasts, bolstered, crucial, delve, emphasizing, enduring, garner, intricate, interplay, key (adjective), landscape (abstract), meticulously, pivotal, underscore, tapestry, testament, valuable, vibrant
- **Mid-2024 to mid-2025:** align with, bolstered, crucial, emphasizing, enhance, enduring, fostering, highlighting, pivotal, showcasing, underscore, vibrant
- **Mid-2025 to mid-2026:** emphasizing, enhance, highlighting, showcasing
- **Mid-2026 and on (newest models):** challenge, clearer, dependable, echoed, foster, leverage, matters, multifaceted, practical, prioritize, quietly, steady, universally. Also watch for a choppy rhythm where every sentence sits between 8 and 20 words.
- **Grok-specific:** causal, empirical, correlate, underscore.
- One or two of these can be coincidence. A cluster is the tell.
- **Fix:** replace with plain English or cut.

### Canned notability and media coverage
- **Watch:** featured in, profiled in, independent coverage, trade publications, leading expert, active social media presence
- **Fix:** cite the one real source by name, or cut the claim.

### Copula avoidance ("serves as")
- **Watch:** serves as, stands as, functions as, operates as, represents a, marks a, boasts, features/offers/maintains (meaning "has"), refers to (when "is" works)
- **Fix:** use "is" or "are."

### Negative parallelisms
- **Watch:** not just X but Y; not only X but also Y; it's not X, it's Y; Y rather than X
- **Fix:** pick the true statement and say it once.

### Rule of three
- **Watch:** adj, adj, and adj, or phrase, phrase, and phrase, especially in analysis sentences
- **Fix:** cut to one or two; the third is usually filler.

### Format tells
- **Title case headings** in running copy: convert to sentence case.
- **Inline-bold-header bullets** (- **Term:** description): rewrite as prose or plain bullets without bold headers.
- **Emoji:** remove all.
- **Curly quotes:** straighten to straight quotes.
- **Bold overuse:** strip bold unless the author asked for it.
- **Markdown in plain-text channels:** no asterisks, pound-sign headings or markdown links in X posts, texts or emails.
- **Em-dashes:** replace with a period, comma or the word "and".

### Chatbot correspondence
- **Watch:** I hope this helps, Let me know if you have questions, Of course!, Certainly!, Would you like me to, Is there anything else
- **Fix:** delete entirely. These are chatbot-to-user phrases and must never appear in published copy.

### Hedging disclaimers
- **Watch:** While specific details are limited, based on available information, should be treated as rather than, does not by itself establish, not widely documented, maintain a low profile
- **Fix:** state the known fact or omit it. Do not speculate.

### Placeholders
- **Watch:** [insert name], [add date], [TBD], any fill-in-the-blank phrase
- **Fix:** fill them in or flag them to the author. Never publish a placeholder.

---

---

## 3. Voice

- **With samples:** copy the author's habits: how they open, sentence length, words they actually use, how they address the reader. Keep their directness; fix typos and run-ons.
- **Default voice:** say what the thing is first. Use "you" when explaining. Prefer short sentences and concrete nouns. Skip adjectives that do not add a fact. No hedging for politeness and no hype.

## 4. Rules (override everything)

1. Never invent a quote, fact, statistic or promise. Keep every number and claim exactly as written.
2. No hype words ("revolutionary", "game-changing", "proven") unless they are in a direct quote.
3. If anything is vague or unverifiable, mark it [CHECK] and leave it unchanged for the author.
4. Respect any style rules the user gives (for example, whether em-dashes or fragments are allowed). User rules beat this skill's defaults.

---

## 5. Before / after example

**Before:**
We're absolutely thrilled to announce the launch of Tidy, a groundbreaking app that serves as a pivotal tool in the evolving landscape of home organization! Tidy boasts a vibrant, intuitive and robust interface, not just helping you declutter but also fostering a calmer lifestyle. Stay tuned for exciting updates! 🚀

**After:**
Tidy is a home organization app. It helps you declutter. Updates are coming.

**What changed:** cut the "thrilled to announce" opener and the words groundbreaking, pivotal, evolving landscape, boasts, vibrant and robust. Cut the "serves as" copula, the "not just X but also Y" parallelism, the rule-of-three adjectives, the vague "calmer lifestyle" claim and the emoji. No facts were added.

---

## 6. Guardrails

- This pass rewrites style only. It never changes meaning, adds claims or makes promises.
- Output is a draft for the author to review and send themselves.
