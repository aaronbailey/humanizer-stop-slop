# Humanizer + Stop Slop

An agent skill for rewriting or reviewing prose so it sounds natural and direct without changing its facts, citations, voice, or format.

It combines the pattern coverage of [Humanizer](https://github.com/blader/humanizer) with the directness checks from [Stop Slop](https://github.com/hardikpandya/stop-slop). Where their rules conflict, this skill preserves facts, authorial voice, and genre conventions before applying style preferences.

## Modes

- Natural rewrite: removes clustered AI-writing patterns without flattening the writer's voice.
- Strict directness: applies the sharper Stop Slop pass for aggressive tightening.
- Voice match: follows a supplied writing sample's rhythm, diction, and punctuation.
- Audit: identifies patterns and suggests fixes without claiming to determine authorship.

## Install in Codex

Copy or clone this repository to:

```text
~/.codex/skills/humanizer-stop-slop
```

Start a new Codex turn, then invoke `$humanizer-stop-slop` or ask Codex to humanize, tighten, de-slop, or audit prose.

## Structure

```text
humanizer-stop-slop/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── examples.md
│   └── patterns.md
└── THIRD_PARTY_NOTICES.md
```

## License

MIT. The upstream copyright and license notices are retained in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
