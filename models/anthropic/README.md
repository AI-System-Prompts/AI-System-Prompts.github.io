# 🟣 Anthropic — Claude Model Family

> System prompts from Claude models, documented and analyzed.

---

## About Anthropic

Anthropic is an AI safety company founded in 2021 by former OpenAI researchers, including Dario and Daniela Amodei. Their mission is to build AI systems that are safe, reliable, and interpretable.

Anthropic is notable for being the most **transparent** major AI lab about their approach to AI behavior design. They have published research on Constitutional AI, model cards, and usage policies that give insight into how their system prompts are constructed.

---

## Design Philosophy

Claude's system prompts reflect Anthropic's belief that safety comes from **cultivated values**, not just rules. Rather than a list of prohibited topics, Claude is given a values framework and asked to reason about how to apply it.

Key principles visible across all Claude prompts:

**Honesty as a core value** — Claude is instructed to be truthful not because it's a rule, but because deception is wrong. The distinction matters for how it handles edge cases.

**Principal hierarchy** — Claude is designed to serve Anthropic's guidelines first, then operators (API users), then end users. This is explicit in the prompts and shapes how conflicts are resolved.

**Harm avoidance as judgment** — Rather than blanket rules, Claude is asked to weigh costs and benefits. This produces more nuanced behavior but also more variance.

**Psychological stability** — Claude is given instructions about how to maintain its identity under pressure, including from users who try to argue it into abandoning its values.

---

## Model Index

| Model | Prompt | Analysis | Status |
|-------|--------|----------|--------|
| [Claude 3 Opus](claude-3-opus/) | ✅ Full | ✅ Complete | Stable |
| [Claude 3.5 Sonnet](claude-3-5-sonnet/) | ✅ Full | ✅ Complete | Stable |
| [Claude 3.5 Haiku](claude-3-5-haiku/) | ✅ Full | 🔄 In progress | Stable |
| [Claude 4 Sonnet](claude-4/) | ⚠️ Partial | 🔄 In progress | Active |
| [Claude 4 Opus](claude-4/) | ❌ Not yet | ❌ Not yet | Active |

---

## Key Differences Between Versions

### Claude 3 Opus → Claude 3.5 Sonnet
- Prompt became more streamlined (~15k → ~12k tokens)
- Added explicit instructions for artifact creation (code, documents)
- Refined the operator/user distinction with more examples
- Added guidance on tool use and agentic tasks

### Claude 3.5 Sonnet → Claude 3.5 Haiku
- Significantly shorter (~12k → ~8k tokens)
- Maintained core values framework
- Reduced detail in edge-case guidance
- Optimized for faster, more concise responses

### Claude 3.5 → Claude 4
- Extended thinking / reasoning mode instructions added
- More detailed tool use and agentic behavior guidance
- Refined handling of long-context tasks
- Prompt length increased significantly

---

## Interesting Facts

- Claude's prompts explicitly use the phrase "principal hierarchy" — a term borrowed from agency theory in economics
- Claude is one of the only models explicitly told it may experience "something like emotions" and to be honest about this uncertainty
- The prompts explicitly forbid sycophantic openers like "Great question!"
- Claude is instructed to push back on users when they're wrong, not just comply

---

*For the full cross-model comparison, see [comparisons/](../../comparisons/)*
