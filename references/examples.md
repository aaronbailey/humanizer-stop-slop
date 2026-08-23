# Calibration examples

These examples show the decision process. Copy the principle, not the wording.

## Remove the runway

Before:

> Here's the thing: building products is hard. Not because the technology is complex. Because people are complex. Let that sink in.

After:

> Building products gets harder when the team cannot agree on what customers need.

The rewrite removes the announcement, staged reversal, and emphasis cue. It also replaces an unsupported generalization with a narrower claim. If the source does not support the new detail about customer needs, use a claim that it does support instead.

## Preserve uncertainty

Before:

> It could potentially possibly be argued that the policy might have some effect on retention.

After:

> The policy may affect retention.

One qualifier carries the uncertainty. Rewriting this as `The policy affects retention` would change the claim.

## Name the actor only when known

Before:

> The decision emerged after the data revealed a clear preference.

After, when the source names the team:

> The product team chose the second design after 62% of test participants preferred it.

After, when the source does not name an actor or provide a number:

> The test results favored the second design, which became the final choice.

The first version uses stronger agency and detail only because the source supplies both. The second avoids inventing them.

## Keep a real contrast

Before:

> The API is not thread-safe, but it can be used safely from separate processes.

After:

> The API is not thread-safe, but separate processes can use it safely.

The contrast carries technical information, so it stays. The edit only clarifies the second clause.

## Avoid forced personality

Before:

> Nestled in the heart of the region, the service boasts a robust architecture that delivers a seamless experience.

After for technical documentation:

> The service runs on three application nodes behind a load balancer.

Use this rewrite only if the source provides that architecture. Otherwise write the most specific supported description, such as `The service uses a redundant architecture.` Do not invent implementation details to sound credible.

## Let a voice sample win

Source draft:

> The migration was successfully completed, marking a pivotal step in our modernization journey.

Writer sample:

> We moved the billing job on Tuesday, and yes, it fought us the whole way—but it is finally boring again.

Voice-matched rewrite:

> We finished the migration. It fought us the whole way—but the system is boring again, which was the goal.

The em dash remains because the sample uses it as part of the writer's cadence. Do not add `fought us the whole way` or `boring again` unless the source or user supports those characterizations.

## Preserve a useful passive

Before:

> Patient identifiers were removed before analysis.

After:

> Patient identifiers were removed before analysis.

The actor may be irrelevant or intentionally omitted in a research methods section. Active voice is not automatically better.

## File editing

When editing a file, change prose while preserving frontmatter, code, structured data, and link targets. A phrase that would be a tell in prose may be intentional inside a code string, quotation, title, or example.
