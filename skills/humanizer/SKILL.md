---
name: humanizer
description: Rewrite a draft to remove common AI-writing tells (puffery, AI vocabulary, negative parallelisms, "serves as", chatbot phrases, format tells) while keeping every fact. Use when the user asks to humanize, de-AI, or clean up the style of text.
---
# Humanizer

Input: one draft. Output: the revised draft plus a short list of what changed. This skill only edits text; it never posts or sends anything.

Tell list adapted from Wikipedia's "Signs of AI writing" (CC BY-SA 4.0): https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing

## Steps
1. Scan: read the draft once and flag every item from the list below.
2. Rewrite: fix each flagged item in place. Do not change meaning, facts or numbers.
3. Voice: if the user gave voice samples or a style guide, match them. Otherwise write plain, direct sentences, lead with the subject, use "you" when explaining.
4. Read-aloud test: anything that sounds like a press release or a chatbot reply fails.
5. Report: list the categories of tells removed and confirm every original fact was kept.

## 1. AI-writing tells to remove

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
- **Fix:** fill them in or flag them for the author. Never publish a placeholder.

---


## 2. Guardrails
- Style only. Never add claims, quotes, statistics or promises.
- If something is vague or unverifiable, mark it [CHECK] and leave it unchanged.
- Return the draft to the user for review.

## 3. Example
Before: "We're thrilled to announce our groundbreaking app, which serves as a vibrant hub for teams, not just boosting productivity but also fostering collaboration! 🚀"
After: "Our app is a shared workspace for teams. You can plan, chat and track tasks in one place."
Changed: cut the announcement opener, "groundbreaking", "serves as", "vibrant", the not-just/but-also parallelism, "fostering" and the emoji.
