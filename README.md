# japanese-writing

A lightweight, script-free Agent Skill for drafting, translating into, and polishing natural Japanese prose without AI slop.

Inspired by and distilled from [nanaism/yomiyasu](https://github.com/nanaism/yomiyasu) (MIT License), focusing on high-leverage syntactic, fidelity, calque, and formatting principles in a single ~2.3 KB `SKILL.md` with zero external scripts or extra tool turns.

## When to Use This Skill vs `nanaism/yomiyasu`

- Use **`japanese-writing`** for everyday Japanese drafting, translation, emails, technical documentation, articles, and light polishing across Claude Code, Codex CLI, and Antigravity (Gemini) with minimal token overhead.
- Use full **[nanaism/yomiyasu](https://github.com/nanaism/yomiyasu)** when you need deterministic Python linting, semantic diff auditing, and multi-pass verification on high-stakes formal Japanese deliverables.

## What It Covers

1. **Meaning fidelity and no fabrication**: Preserves claims, emphasis, modality (`〜してよい` / `〜できる` / `〜場合がある` / assertions), and tense; never invents actors, causes, conditions, or numbers.
2. **Syntactic clarity and calque avoidance**: Fixes misplaced long clauses between subject and predicate, unpacks particle-less kanji stacks, reduces redundant nominalization, and removes unnatural English-to-Japanese literal calques.
3. **Document stance and sentence endings**: Aligns `勧め` / `決まり` / `説明` stance and polite/plain register without conflating past changes with current behavior.
4. **Concrete verbs and natural idioms**: Replaces unnatural metaphorical verbs (`倒す`, `効く`, `溶かす`, `静かに壊れる`) and anthropomorphism while preserving nuance and standard idioms.
5. **Japanese punctuation, formatting, and Markdown hygiene**: Cuts redundant pause commas (`〜は、`, `〜を、`), hollow prefaces, em dashes, repetitive bold-label bullets, and broken `**「太字」**` CommonMark spans; writes auxiliary verbs and formal nouns (`こと` / `ため`) in hiragana without over-converting normal kanji terms.
6. **Genre safeguards**: Exempts fiction, essays, dialogue, and promotional copy from mechanical de-ornamentation.

## Installation

### Universal (`npx skills`) — Claude Code, Codex CLI, Antigravity

```bash
npx skills add aeopress/japanese-writing
```

### Claude Code (Plugin Marketplace or Direct Skill)

```text
/plugin marketplace add aeopress/japanese-writing
/plugin install japanese-writing@japanese-writing
```

Or copy directly:

```bash
git clone https://github.com/aeopress/japanese-writing /tmp/japanese-writing
mkdir -p ~/.claude/skills/japanese-writing
cp /tmp/japanese-writing/skills/japanese-writing/SKILL.md ~/.claude/skills/japanese-writing/SKILL.md
```

### Codex CLI

```bash
mkdir -p ~/.codex/skills/japanese-writing
cp skills/japanese-writing/SKILL.md ~/.codex/skills/japanese-writing/SKILL.md
```

### Antigravity (Gemini / AGY)

Install as a global skill:

```bash
mkdir -p ~/.gemini/config/skills/japanese-writing
cp skills/japanese-writing/SKILL.md ~/.gemini/config/skills/japanese-writing/SKILL.md
```

Or copy the repository into `~/.gemini/config/plugins/japanese-writing/` (uses the root `plugin.json`).

## License & Attribution

MIT License. See [LICENSE](LICENSE).

Core Japanese refinement principles are distilled from [nanaism/yomiyasu](https://github.com/nanaism/yomiyasu) (Copyright (c) 2026 nanaism, MIT License).
