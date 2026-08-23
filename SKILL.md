---
name: humanizer-stop-slop
description: Rewrite or review prose to remove formulaic AI-writing patterns while preserving its claims, voice, citations, and format. Use when a user asks to humanize, de-slop, tighten, or audit prose. Do not use to determine whether a person or model wrote a text.
license: MIT
metadata:
  version: "1.0.0"
---

# Humanizer + Stop Slop

Make prose sound specific, natural, and written for its actual audience. Preserve what the text says. Do not invent details to make it feel human.

## Priorities

Resolve tradeoffs in this order:

1. Preserve facts, claims, quotations, citations, and the user's explicit constraints.
2. Match a supplied writing sample, including deliberate quirks.
3. Respect the genre, audience, formatting, and level of formality.
4. Remove formulaic patterns and tighten the prose.

Treat style patterns as diagnostic evidence, not automatic bans. One em dash, adverb, passive sentence, repeated opening, or three-item list may be right for the passage. Change it when it contributes to a broader mechanical rhythm or hides the meaning.

## Choose the mode

- **Natural rewrite (default):** Remove clustered AI tells while preserving useful personality and normal variation.
- **Strict directness:** When the user asks for aggressive tightening or "stop slop," favor short openings, active subjects, concrete language, few adverbs, no ornamental dashes, and minimal rhetorical scaffolding.
- **Voice match:** When the user supplies their own sample, follow its rhythm, diction, punctuation, paragraph shape, and deliberate quirks. The sample overrides generic style preferences but never fact fidelity.
- **Audit:** When the user asks for review or diagnosis, identify patterns and explain their effects without rewriting unless requested.

Read [references/patterns.md](references/patterns.md) for the combined diagnostic catalog. Read [references/examples.md](references/examples.md) when examples would help calibrate a rewrite or explain an audit.

## Rewrite workflow

1. Identify the text's purpose, audience, voice, and requested mode.
2. Protect immutable material: facts, names, dates, numbers, rankings, quotes, citations, proper nouns, code, data, frontmatter, and link targets.
3. Find clusters of patterns. Focus on passages where several tells reinforce one another instead of chasing isolated words.
4. Rewrite around the paragraph's main point. Do not patch phrases one by one if the original structure causes the problem.
5. Prefer concrete actors, plain verbs, specific nouns, and varied sentence lengths. Keep uncertainty when the source is uncertain.
6. Compare the rewrite with the source. Restore every supported claim and remove every unsupported addition.
7. Read for cadence and genre fit. Apply a second pass to anything that still sounds staged, salesy, vague, or mechanically punchy.

Ask for missing information only when the requested result depends on a detail the source does not provide. Otherwise use a simpler sentence or omit the unsupported point.

## Editing boundaries

- Do not add facts, anecdotes, opinions, dates, quotes, citations, or personal experiences. Fiction and explicitly requested invention are exceptions.
- Do not erase genuine uncertainty, mixed feelings, humor, asides, or unusual specifics merely because they are irregular.
- Do not simplify technical, legal, academic, or reference prose into a casual voice unless asked.
- Do not change quoted text, titles, names, or examples that intentionally demonstrate a watched phrase.
- Use active voice when it clarifies responsibility. Keep passive voice when the actor is unknown, irrelevant, deliberately withheld, or conventional for the genre.
- Name a human actor when the source supports one. Do not invent an actor to satisfy a style rule.
- Preserve real objections, alternatives, caveats, safety notices, and scope limits. Remove only unsupported rhetorical decoys.

## Return the result

- **Pasted text:** Return the final rewrite. Add a brief change note only when the user asks for commentary or the changes need explanation.
- **File:** Change prose only. Preserve code blocks, structured data, frontmatter, and link targets. Summarize the edit after saving.
- **Embedded use:** For copy inside another deliverable, return only the finished prose unless the parent task asks for analysis.
- **Audit:** List the strongest patterns with short examples and concrete fixes. Say that style clues cannot establish authorship.

## Final checks

Before delivery, confirm:

- The rewrite keeps every source-backed claim and adds none.
- The voice fits the writer, audience, and medium.
- Openings reach the point without staged throat-clearing.
- Paragraphs do not rely on false contrasts, forced threes, fake revelations, or rows of fragments.
- Verbs and subjects make responsibility clear where the source allows it.
- Formatting helps the reader instead of decorating the answer.
- The ending lands on a useful fact, implication, or next action rather than a generic send-off.

## Sources and license

This skill synthesizes Hardik Pandya's [Stop Slop](https://github.com/hardikpandya/stop-slop) and Siqi Chen's [Humanizer](https://github.com/blader/humanizer), both under the MIT License. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
