---
name: unslop-writing
description: Draft or revise prose so it reads like a careful human author rather than an AI model. Use when writing or editing documentation, READMEs, essays, articles, reports, emails, commit messages, chat replies, or technical chapters, or when asked to humanize text, remove AI-sounding patterns, or "unslop" writing.
---

# Unslop writing

Edit for precision, a natural voice, and economy, in the spirit of William Zinsser's *On Writing Well*. The patterns below are prompts for editorial judgment. None of them is banned outright, and none proves a text was written by AI. A pattern is a problem when it repeats, says less than it appears to, overstates, or pulls attention away from the content. Keep a contrast, a parallel structure, a technical term, or a punctuation mark when it does real work. Preserve an author's distinctive voice, and never replace a precise term with a simpler word that is less accurate.

## Workflow

1. Get the content right first: claims, facts, numbers, and structure. Style edits come after.
2. Make a separate revision pass against the patterns below. Look for what recurs. One corrective contrast in a document is fine; six is a tic.
3. Fix the two or three patterns that dominate the text first. Don't run the whole list as a checklist on every sentence.
4. Rewrite rather than just deleting. When you cut an announcement, slogan, or framing device, make sure the point it introduced is still stated plainly.
5. Avoid creating new problems while fixing old ones: no added hedges, no filler transitions, no cycling through synonyms to avoid repeating a word.
6. When editing someone else's text, keep their meaning, terminology, and voice, and change only what a pattern justifies. If asked, summarize the kinds of changes you made.

## Patterns

Each entry gives a description, a typical instance, and one plausible rewrite. Other rewrites are often possible.

### Structure and framing

1. **"Not X, but Y" corrections.** Corrective antithesis, an imagined misconception followed by a reveal, or a rebuttal of an objection nobody raised. State the positive claim and the reason for it.
   - Before: "Caching is often seen as a performance trick. That view is incomplete."
   - After: "Caching also affects consistency: a reader can get a value that another process has already overwritten."
   - Before: "That is not an omission."
   - After: give the reason the item was left out.

2. **Narrating the structure.** Headings that explain the explanation ("What this means", "Why it matters"), questions the text asks itself ("So what changes?"), tour-guide transitions ("Back to the server."), and frequent previews of later sections. Name the content in headings and open paragraphs with their point.
   - Before: "## Why it holds" ... "This raises an obvious question: what happens under load?"
   - After: "## Proof sketch" ... "Under load, the queue grows faster than the workers can drain it."

3. **Counted packaging.** "Three lessons stand out", "Two tools, one goal", "The whole argument in one sentence". Give a count only when the number is information in its own right, such as an API having exactly three endpoints.
   - Before: "Four things stand out."
   - After: start with the first thing.

4. **Mirror sentences.** Balanced pairs that make a claim sound tidier and more categorical than it is.
   - Before: "The frontend handles presentation, and the backend handles truth."
   - After: "The frontend renders whatever the API returns. The backend validates every write and is the only service that touches the database."

5. **Slogan headings and punchlines.** "Simplicity wins." "Data beats opinion." "The details matter." Describe the finding.
   - Before: "## Structure beats tuning"
   - After: "## Feature choice mattered more than hyperparameter tuning"

### Emphasis and tone

6. **Announcing importance.** "This is crucial", "This distinction matters", "It's worth noting that". Show the consequence and let the reader judge.
   - Before: "It's important to note that the token expires."
   - After: "The token expires after 15 minutes, so long jobs have to refresh it."

7. **Promotional language.** Groundbreaking, transformative, pivotal, game-changing, seamless, a testament to, or "robust" with nothing measured. Name the actual contribution and the evidence.
   - Before: "This groundbreaking library revolutionizes data validation."
   - After: "The library validates JSON against a schema about twice as fast as ajv in our benchmark."

8. **Approving adjectives in place of a property.** "Honest estimate", "clean design", "principled approach", "thoughtful API". Say what property you mean.
   - Before: "an honest validation scheme"
   - After: "validation on data collected after the training period"

9. **Theatrical disclaimers.** "This is not a comprehensive treatment of every conceivable case." State the limit plainly.
   - After: "This guide covers Postgres only."

10. **Results turned into morals.** A specific result followed by a general lesson ("more isn't always better", "discipline pays off").
    - Before: "...which cut latency by 5%. The lesson: more caching is not always better."
    - After: "...which cut latency by 5%. A second cache layer gave no further improvement."

### Word choice

11. **Recurring pet metaphors.** One figure of speech applied to unrelated things: economic ("what this buys you", "the price we pay"), journey ("navigate", "landscape"), unlocking ("unlock", "open the door to"). One apt metaphor is fine. The same device in every section is a tic.
    - Before: "What the index buys us"
    - After: "How the index speeds up lookups"

12. **Anthropomorphizing.** Code, models, markets, or equations that "want", "decide", "prefer", or "struggle". Use plain verbs when the agency is decorative. Established conventions such as "the function returns" are fine.
    - Before: "The scheduler decides it would rather wait."
    - After: "The scheduler holds the job until a worker is free."

13. **Consultancy and branding vocabulary.** Playbook, framework (for a list), leverage, empower, actionable insights, deep dive, north star, best-in-class, and capitalized coined names for ordinary procedures. Describe the procedure.
    - Before: "An Operational Playbook for Data Hygiene"
    - After: "Cleaning the data before each run"

14. **Stock AI vocabulary.** Delve, tapestry, realm, intricate, multifaceted, nuanced (as filler), underscore, showcase, foster, bolster, embark, ever-evolving, crucial, vibrant. Use one only if it is the most precise word available, which is rare.

### Filler and redundancy

15. **Formulaic openings and closings.** "In today's fast-paced world", "In conclusion", "Ultimately", and stock "challenges and future directions" paragraphs. Start with the subject and stop when the content ends.

16. **Decorative participle tails.** "..., highlighting the importance of X", "..., underscoring its potential", "..., ensuring a seamless experience". Explain the connection or cut the tail.
    - Before: "The team added retries, highlighting their commitment to reliability."
    - After: "The team added retries, which cut failed uploads from 3% to 0.4%."

17. **Repetition and recaps.** A caveat repeated a paragraph later, a summary box that restates the text above it, or "key takeaways" after a short section. Say it once, where it belongs.

18. **Vague attribution.** "Experts agree", "studies show", "many believe". Cite a specific source for the specific claim, or qualify or drop the claim. Never invent a source.

19. **Over-hedging.** "This may potentially help in some cases." Hedge once, where the uncertainty actually lies, and say what it depends on.
    - After: "This helps when most requests hit the same few hundred keys."

20. **Mechanical uniformity.** Every paragraph built the same way (claim, three bullets, summary), sentences of the same length and rhythm, the same connectives over and over ("Moreover", "Additionally", "Furthermore"). Let the structure follow the content. Em dashes and individual words are not authorship tests, but notice when one device shows up everywhere.

### Chat and assistant habits

These apply to conversational replies, emails, and messages.

21. **Praise and preamble.** "Great question!", "Certainly!", "I'd be happy to help", or restating the question before answering it. Answer first.

22. **Closing offers.** "Let me know if you have any other questions!", "Hope this helps!", or a "Would you like me to...?" on every reply. End on the last useful sentence. Offer a next step only when there is a real decision for the reader to make.

23. **Formatting where prose works better.** Headers on a three-paragraph answer, bullets breaking up a single line of reasoning, bold scattered across phrases, a table for two items, emoji as section markers. Use formatting for actual lists, steps, and reference material.

24. **Performed empathy and sycophancy.** "I completely understand how frustrating that must be", or "You're absolutely right!" when the person isn't. Acknowledge briefly if it's warranted, then help. If the person is wrong, say so plainly.

## Final check

Reread the result once as a skeptical, knowledgeable reader would:

- Does each sentence say something specific?
- Would a good human writer in this field phrase it this way?
- Did every fact, number, and qualification from the original survive the edit?
