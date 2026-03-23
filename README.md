# Brand Voice Architect (BVA)
A Claude skill that reverse-engineers brand voice from raw copy and turns it into a deployable system.

## What it does
- **`/analyze`** — Runs a linguistic audit on any corpus: lexical density, avg sentence length, cadence variance, emotional temperature, top keywords
- **`/synthesize`** — Builds 3 voice pillars + This/Not That logic gates + LLM-ready system prompt
- **`/review`** — Claude-assisted qualitative checklist to assess whether content aligns with established voice pillars
- **`/pivot`** — Adapts voice for specific platforms (LinkedIn, blog, Instagram, etc.) while preserving DNA

> **Note:** Prohibited word replacement is enforced at the prompt level — the generated system prompt instructs the LLM to swap prohibited words for preferred equivalents. Enforcement depends on the model following the system prompt.

## Files
```
brand-voice-architect/
├── SKILL.md                        # Main skill instructions
├── scripts/
│   ├── voice_analyzer.py           # Linguistic metrics engine
│   └── prompt_synthesizer.py       # LLM system prompt generator
└── references/
    └── methodology.md              # 4-Pillar Framework, Cadence Analysis, Semantic Salience
```

## Installation
1. Download `brand-voice-architect.skill`
2. Go to Claude.ai → Settings → Skills
3. Upload the `.skill` file

## Usage
Once installed, trigger with phrases like:
- "analyze this website's brand voice"
- "build a voice guide for [brand]"
- "review this blog post against our brand voice"
- "adapt this copy for LinkedIn"

## Example output
Running `/analyze` on a website returns:
- Lexical density: 62.3%
- Avg sentence length: 13.5 words
- Cadence variance (σ): 8.1
- Emotional temperature: 0.33 / 1.0
- Top keywords + prohibited/preferred lexicon

Running `/synthesize` produces:
- 3 core voice pillars with This/Not That logic gates
- Deployable LLM system prompt with corpus-derived metrics
- Platform pivots for LinkedIn, blog, email, and more

## Built with
[Claude Skills](https://claude.ai) · Python · Anthropic API
