# 🟢 OpenAI — GPT Model Family

> System prompts from OpenAI's GPT and ChatGPT models, documented and analyzed.

---

## About OpenAI

OpenAI was founded in 2015 as a nonprofit, later converting to a "capped-profit" structure. They created the modern large language model era with GPT-3 (2020) and triggered the AI mainstream moment with ChatGPT (November 2022).

OpenAI has historically been **less transparent** than Anthropic about their system prompt design, relying more on behavior demonstrations than documentation. However, multiple leaks and researcher extractions have built a detailed picture over time.

---

## Design Philosophy

OpenAI's prompts tend to reflect a **policy compliance model** — the AI is given explicit content categories it must avoid, with less emphasis on underlying values reasoning.

Key characteristics:

**Content policy as authority** — Prompts frequently reference "content policy" as an external document, positioning restrictions as rules rather than values.

**Tool-use integration** — As OpenAI has added capabilities (DALL-E, code interpreter, browsing), their system prompts have become increasingly complex with tool-specific instructions.

**Brand consistency** — Strong emphasis on maintaining the "ChatGPT" brand voice and not impersonating other AI systems.

**Neutrality by default** — Explicit instructions to avoid political opinions and controversial positions, reflecting OpenAI's commercial risk-aversion.

---

## Model Index

| Model | Prompt | Analysis | Status |
|-------|--------|----------|--------|
| [ChatGPT Default (2023)](chatgpt-default/) | ✅ Full | ✅ Complete | Historical |
| [GPT-4 Turbo](gpt-4-turbo/) | ✅ Full | ✅ Complete | Stable |
| [GPT-4o](gpt-4o/) | ✅ Full | ✅ Complete | Current |
| [o1 / o1-mini](o1/) | ⚠️ Partial | 🔄 In progress | Current |
| [o3](o1/) | ❌ Not yet | ❌ Not yet | Active |

---

## Key Differences Between Versions

### ChatGPT Default → GPT-4 Turbo
- System prompt grew significantly longer
- Added extensive tool use instructions
- Date injection became standard (model told current date)
- More nuanced content handling in some areas

### GPT-4 Turbo → GPT-4o
- Multimodal instructions added (vision, voice)
- Voice mode specific behavior guidance
- Refined personality instructions
- More emphasis on response format flexibility

### GPT-4o → o1 Series
- Reasoning model specific instructions
- "Think before responding" explicit guidance
- Different format defaults (longer thinking, shorter output)
- Different tool use approach

---

## The ChatGPT System Prompt Evolution

ChatGPT's default system prompt has evolved dramatically:

**2022 (GPT-3.5 era):** Extremely minimal — just a few sentences about being a helpful assistant

**2023:** Grew to ~1,500 tokens with tool descriptions, content policy references, date injection

**2024:** ~3,000-5,000 tokens with full multimodal, voice, and tool ecosystems described

This growth reflects the increasing complexity of managing a product used by hundreds of millions of people.

---

*For the full cross-model comparison, see [comparisons/](../../comparisons/)*
