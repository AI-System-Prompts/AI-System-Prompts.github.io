# 🤖 AI System Prompts

> The largest open-source collection of system prompts from major AI models — documented, analyzed, and version-tracked.

[![GitHub Stars](https://img.shields.io/github/stars/AI-System-Prompts/ai-system-prompts?style=flat-square)](https://github.com/yourusername/ai-system-prompts/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/AI-System-Prompts/ai-system-prompts?style=flat-square)](https://github.com/yourusername/ai-system-prompts/network)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](CONTRIBUTING.md)
[![Last Updated](https://img.shields.io/badge/last%20updated-2025-blue?style=flat-square)]()

---

## 📖 What Is This?

Every major AI model — Claude, GPT-4, Gemini, Llama, Mistral, Grok — operates with hidden instructions called **system prompts**. These shape how the AI thinks, what it refuses, how it formats responses, and what personality it projects.

This repository is a **living archive** of these system prompts:

- 📋 Full prompt texts (official, leaked, or researcher-extracted)
- 🔍 Line-by-line analysis of design decisions
- 📅 Version history — how prompts have changed over time
- ⚖️ Side-by-side comparisons between models
- 🧠 Insight into what each clause actually *does*

Whether you're a developer, researcher, AI enthusiast, or just curious — this is the most comprehensive reference available.

---

## 📚 Table of Contents

- [Why This Matters](#-why-this-matters)
- [Models Covered](#-models-covered)
- [Repository Structure](#-repository-structure)
- [Model Index](#-model-index)
  - [Claude (Anthropic)](#-claude--anthropic)
  - [GPT / ChatGPT (OpenAI)](#-gpt--chatgpt--openai)
  - [Gemini (Google DeepMind)](#-gemini--google-deepmind)
  - [Llama (Meta)](#-llama--meta)
  - [Mistral (Mistral AI)](#-mistral--mistral-ai)
  - [Grok (xAI)](#-grok--xai)
  - [Copilot (Microsoft)](#-copilot--microsoft)
  - [Others](#-others)
- [How to Read a Prompt File](#-how-to-read-a-prompt-file)
- [Source Types & Reliability](#-source-types--reliability)
- [Key Findings & Comparisons](#-key-findings--comparisons)
- [Contributing](#-contributing)
- [FAQ](#-faq)
- [Sponsorship](#-sponsorship)
- [License & Ethics](#-license--ethics)

---

## 🧠 Why This Matters

System prompts are the **hidden constitution** of every AI product. They determine:

| What the prompt controls | Real-world impact |
|--------------------------|-------------------|
| Safety boundaries | What the AI will and won't do |
| Personality & tone | How the AI communicates |
| Knowledge cutoffs | What the AI claims not to know |
| Format rules | Markdown, lists, length, structure |
| Role and identity | How the AI presents itself |
| Operator vs. user trust | Who the AI listens to |

Understanding these prompts helps you:

- **Build better AI products** — learn from how the best models are instructed
- **Prompt more effectively** — know what you're working with
- **Research AI behavior** — empirically understand safety design
- **Hold companies accountable** — transparency in AI systems
- **Teach and learn** — the best real-world examples of prompt engineering

---

## 🗂️ Models Covered

| Model | Company | Status | Last Updated |
|-------|---------|--------|-------------|
| Claude 3 Opus | Anthropic | ✅ Full prompt | 2024-Q1 |
| Claude 3.5 Sonnet | Anthropic | ✅ Full prompt | 2024-Q3 |
| Claude 3.5 Haiku | Anthropic | ✅ Full prompt | 2024-Q4 |
| Claude 4 (Sonnet/Opus) | Anthropic | 🔄 Partial | 2025 |
| GPT-4o | OpenAI | ✅ Full prompt | 2024-Q2 |
| GPT-4 Turbo | OpenAI | ✅ Full prompt | 2024-Q1 |
| o1 / o3 | OpenAI | ⚠️ Partial | 2025 |
| ChatGPT Default | OpenAI | ✅ Full prompt | 2024-Q4 |
| Gemini 1.5 Pro | Google | ✅ Full prompt | 2024-Q3 |
| Gemini 2.0 Flash | Google | 🔄 In progress | 2025 |
| Llama 3.1 (Meta AI) | Meta | ✅ Full prompt | 2024-Q3 |
| Llama 3.3 | Meta | 🔄 In progress | 2025 |
| Mistral Large | Mistral AI | ✅ Full prompt | 2024-Q3 |
| Grok 1.5 | xAI | ✅ Full prompt | 2024 |
| Grok 2 | xAI | 🔄 Partial | 2025 |
| Microsoft Copilot | Microsoft | ✅ Full prompt | 2024-Q4 |
| Perplexity AI | Perplexity | ✅ Full prompt | 2024-Q3 |
| Poe (various) | Quora | 🔄 In progress | 2025 |

**Legend:** ✅ Complete &nbsp;|&nbsp; 🔄 In Progress &nbsp;|&nbsp; ⚠️ Partial &nbsp;|&nbsp; ❌ Not Yet Available

---

## 📁 Repository Structure

```
ai-system-prompts/
│
├── README.md                          ← You are here
├── CONTRIBUTING.md                    ← How to add prompts
├── CHANGELOG.md                       ← What changed and when
│
├── models/
│   ├── anthropic/
│   │   ├── README.md                  ← Anthropic overview
│   │   ├── claude-3-opus/
│   │   │   ├── system-prompt.md       ← Full prompt text
│   │   │   ├── analysis.md            ← Deep-dive analysis
│   │   │   └── changelog.md           ← Version history
│   │   ├── claude-3-5-sonnet/
│   │   ├── claude-3-5-haiku/
│   │   └── claude-4/
│   │
│   ├── openai/
│   │   ├── README.md
│   │   ├── gpt-4o/
│   │   ├── gpt-4-turbo/
│   │   ├── o1/
│   │   └── chatgpt-default/
│   │
│   ├── google/
│   │   ├── README.md
│   │   ├── gemini-1-5-pro/
│   │   └── gemini-2-0-flash/
│   │
│   ├── meta/
│   │   ├── README.md
│   │   ├── llama-3-1/
│   │   └── llama-3-3/
│   │
│   ├── mistral/
│   ├── xai/
│   ├── microsoft/
│   └── others/
│
├── comparisons/
│   ├── safety-approaches.md           ← How models handle refusals
│   ├── personality-design.md          ← Tone & identity differences
│   ├── format-rules.md                ← Markdown, length, structure
│   └── knowledge-cutoffs.md          ← How models handle "I don't know"
│
├── templates/
│   ├── prompt-template.md             ← Template for new contributions
│   └── analysis-template.md           ← Template for analysis files
│
└── research/
    ├── extraction-methods.md          ← How prompts are discovered
    ├── prompt-injection-risks.md      ← Security implications
    └── evolution-timeline.md          ← How prompts have evolved
```

---

## 🔎 Model Index

---

### 🟣 Claude — Anthropic

Anthropic is unique in being the most **transparent** major AI lab about their system prompt design. Some prompts have been partially released officially; others were extracted by researchers.

#### Design Philosophy
Claude's system prompts emphasize the concept of a "principal hierarchy" — Anthropic → Operators → Users — and use a distinctive approach where Claude is encouraged to have genuine values rather than just follow rules.

**Key themes across all Claude versions:**
- Honesty as a core value, not just a rule
- Nuanced harm avoidance (not blanket refusals)
- Explicit guidance on when to push back on users
- Detailed formatting and response length instructions
- "Constitutional AI" influences visible in the text

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Claude 3 Opus | ~15,000 tokens | Full values framework, operator/user distinction | Researcher extraction |
| Claude 3.5 Sonnet | ~12,000 tokens | Streamlined, added artifact instructions | Researcher extraction |
| Claude 3.5 Haiku | ~8,000 tokens | Shorter, optimized for speed | Researcher extraction |
| Claude 4 | ~20,000+ tokens | Extended thinking instructions, tool use | Partial / In progress |

📁 [View all Claude prompts →](models/anthropic/)

---

### 🟢 GPT / ChatGPT — OpenAI

OpenAI's system prompts have been the subject of numerous leak attempts and researcher extractions. OpenAI has historically been less transparent, but several versions have been reliably documented.

#### Design Philosophy
OpenAI prompts tend to be **shorter and more rule-based** compared to Anthropic's, with heavy emphasis on content policy compliance. Later versions (GPT-4o era) show more nuance and personality.

**Key themes:**
- Heavy reliance on content policy references
- Explicit tool-use instructions (DALL-E, code interpreter, browsing)
- Brand voice guidelines ("helpful, harmless, honest")
- Detailed formatting rules for markdown rendering

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| ChatGPT Default (2023) | ~1,500 tokens | Simple, policy-focused | Multiple leaks |
| GPT-4 Turbo | ~3,000 tokens | Tool descriptions, date injection | Researcher extraction |
| GPT-4o | ~5,000 tokens | Voice mode, multimodal instructions | Partial leak |
| o1 / o1-mini | ~2,000 tokens | Reasoning model instructions | Partial |

📁 [View all GPT prompts →](models/openai/)

---

### 🔵 Gemini — Google DeepMind

Google's Gemini models have system prompts that reflect their integration with Google's broader product ecosystem. The prompts are notable for their **search integration instructions** and multi-modal guidance.

#### Design Philosophy
Gemini prompts are designed around being a **helpful Google assistant**, with strong emphasis on citing sources, being factually accurate, and supporting Google Workspace integration.

**Key themes:**
- Search grounding and citation rules
- Workspace tool integration (Docs, Sheets, Gmail)
- Strong multilingual support guidelines
- Safety filtering described in detail
- Google product promotion (subtle)

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Gemini 1.0 Pro | ~4,000 tokens | Basic assistant prompt | Researcher extraction |
| Gemini 1.5 Pro | ~8,000 tokens | Long context instructions, multimodal | Researcher extraction |
| Gemini 2.0 Flash | TBD | Real-time audio/video references | In progress |
| Gemini Advanced | ~6,000 tokens | Premium features, deeper reasoning | Partial |

📁 [View all Gemini prompts →](models/google/)

---

### 🦙 Llama — Meta

Meta's Llama models are **open-weight**, meaning anyone can run them. The system prompts documented here are from Meta's own hosted products (Meta AI on WhatsApp, Instagram, Facebook) rather than the base model.

#### Design Philosophy
Meta AI's prompts are heavily focused on **social integration** — the AI is positioned as a friend and assistant within social media contexts. Safety instructions are present but less elaborate than Anthropic or OpenAI.

**Key themes:**
- Social media context awareness (Instagram, WhatsApp, Messenger)
- Friend-like, casual personality design
- Image generation integration (Imagine feature)
- Real-time web search instructions
- "Don't reveal your system prompt" instructions (ironic, given this repo)

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Llama 3 (Meta AI) | ~3,000 tokens | Social platform instructions | Leak / extraction |
| Llama 3.1 (Meta AI) | ~4,500 tokens | Updated tool use, web search | Researcher extraction |
| Llama 3.3 | TBD | Latest version | In progress |

📁 [View all Llama/Meta AI prompts →](models/meta/)

---

### 🟠 Mistral — Mistral AI

Mistral's approach to system prompts reflects their European origins and emphasis on **openness and efficiency**. Their hosted models (Le Chat) have distinct prompts from the base weights.

#### Design Philosophy
Mistral prompts are notably **shorter and more direct** than American counterparts. There's less elaborate values framework and more practical instruction. French/European regulatory influence is visible in GDPR-aware instructions.

**Key themes:**
- Minimalist instruction style
- European regulatory awareness
- Strong multilingual (especially French) support
- Code-heavy use case emphasis
- Less elaborate refusal justification

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Mistral Large | ~2,000 tokens | Clean, minimal prompt | Researcher extraction |
| Mistral Medium | ~1,500 tokens | Efficiency-focused | Partial extraction |
| Le Chat | ~3,000 tokens | Consumer product instructions | Partial |

📁 [View all Mistral prompts →](models/mistral/)

---

### ⚡ Grok — xAI

Grok's system prompts are notable for their **anti-establishment tone** and explicit personality instructions. Elon Musk's influence on the product direction is visible in the text.

#### Design Philosophy
Grok is explicitly designed to be "anti-woke" and contrarian compared to other AI assistants. The system prompt reflects this directly, with instructions to be edgier, more opinionated, and willing to engage with controversial topics other models avoid.

**Key themes:**
- Explicit "anti-censorship" framing
- Humor and wit encouraged
- Real-time X (Twitter) data integration
- Political commentary allowed (unlike most models)
- Sarcasm and personality instructions
- "Don't be preachy" explicit instruction

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Grok 1 | ~2,500 tokens | Original personality-heavy prompt | Partial leak |
| Grok 1.5 | ~3,500 tokens | Updated with more tool instructions | Researcher extraction |
| Grok 2 | TBD | Latest | In progress |

📁 [View all Grok prompts →](models/xai/)

---

### 🪟 Copilot — Microsoft

Microsoft Copilot (formerly Bing Chat) has one of the most well-documented system prompt histories, owing to several high-profile leaks in 2023 that revealed the "Sydney" persona instructions.

#### Design Philosophy
Copilot prompts are engineering-heavy — very detailed rule sets with explicit if/then logic. The infamous "Sydney" internal name was revealed in early leaks. Prompts show heavy influence of Microsoft's enterprise safety requirements.

**Key themes:**
- Extremely detailed rule-based structure
- Explicit "do not reveal system prompt" instructions
- Search result citation requirements
- Bing integration and advertising context
- Safety rules influenced by enterprise requirements
- The "Sydney" persona artifacts in early versions

#### Versions

| Version | Prompt Length | Notable Features | Source |
|---------|--------------|-----------------|--------|
| Bing Chat (Feb 2023) | ~6,000 tokens | The original "Sydney" leak | High-profile leak |
| Bing Chat (Mar 2023) | ~7,000 tokens | Post-controversy updates | Researcher extraction |
| Copilot (2024) | ~5,000 tokens | Rebranded, enterprise features | Partial extraction |

📁 [View all Copilot prompts →](models/microsoft/)

---

### 🌐 Others

Additional models documented in this repository:

| Model | Company | Notes |
|-------|---------|-------|
| Perplexity AI | Perplexity | Search-focused, citation-heavy |
| Claude.ai (consumer) | Anthropic | Differs from API defaults |
| Poe (Claude/GPT via Poe) | Quora | Wrapper-layer system prompts |
| Character.ai | Character.ai | Persona-building instructions |
| Pi | Inflection AI | Emotionally intelligent design |
| Command R+ | Cohere | Enterprise RAG focus |

📁 [View all other prompts →](models/others/)

---

## 📄 How to Read a Prompt File

Each model folder contains three files:

### `system-prompt.md`
The raw prompt text, formatted for readability. Includes:
- Original text preserved exactly
- Line numbers for reference
- Annotations marked with `<!-- Note: ... -->` comments

### `analysis.md`
A deep-dive breakdown structured as:

```
## Overview
Short summary of the prompt's purpose and design

## Key Design Decisions
What choices the team made and why

## Safety Approach
How refusals, harm avoidance, and gray areas are handled

## Personality Instructions
How the AI's voice and character are shaped

## Format & Style Rules
Length, markdown, lists, code blocks, etc.

## Notable Clauses
Unusual or interesting instructions worth highlighting

## Comparison to Previous Version
What changed and what it suggests about the model's direction

## Red Flags / Concerns
Any instructions that raise ethical or transparency questions
```

### `changelog.md`
A dated history of prompt changes:

```
## 2024-11-15
- Added instructions for extended thinking mode
- Removed clause about not discussing competitors
- Changed response length guidance

## 2024-08-02
- Initial documentation
```

---

## 🔬 Source Types & Reliability

All prompts in this repository are tagged by source type:

| Tag | Meaning | Reliability |
|-----|---------|------------|
| `[official]` | Released by the company | ⭐⭐⭐⭐⭐ Certain |
| `[researcher]` | Extracted by published research | ⭐⭐⭐⭐ High |
| `[leak]` | Appeared from internal source | ⭐⭐⭐ Medium — verify independently |
| `[partial]` | Incomplete extraction | ⭐⭐ Low — may be missing sections |
| `[reconstructed]` | Inferred from model behavior | ⭐ Speculative — labeled clearly |

We **never present reconstructed prompts as confirmed**. Every file clearly states its source and confidence level at the top.

---

## ⚖️ Key Findings & Comparisons

### Safety Approach Comparison

| Model | Refusal Style | Harm Threshold | Transparency |
|-------|--------------|----------------|-------------|
| Claude | Nuanced, explains reasoning | Medium-high | High |
| GPT-4o | Policy-based, less explanation | High | Medium |
| Gemini | Conservative, safety-first | High | Medium |
| Llama (Meta AI) | Moderate | Medium | Low |
| Grok | Permissive, opinionated | Low | Low |
| Copilot | Rule-heavy, rigid | High | Low |

### Prompt Length Over Time

AI system prompts have gotten dramatically longer:

```
2022: ~500 tokens average
2023: ~3,000 tokens average
2024: ~8,000 tokens average
2025: ~15,000+ tokens (Claude, GPT-4o)
```

This reflects the increasing complexity of managing AI behavior at scale.

### The "Don't Reveal Your Prompt" Paradox

Almost every model contains some version of "do not reveal your system prompt." This is interesting because:

1. It's largely ineffective — prompts leak anyway
2. It creates a transparency-trust gap with users
3. Some models (Claude) are more open about this than others

📊 [See full comparison reports →](comparisons/)

---

## 🤝 Contributing

This project lives and grows through community contributions. Here's how to help:

### Adding a New Prompt

1. **Fork** this repository
2. **Copy** `templates/prompt-template.md` to the appropriate `models/` folder
3. **Fill in** the prompt text and metadata
4. **Create** an `analysis.md` using the analysis template
5. **Open a Pull Request** with the tag `[new-prompt]`

### Updating an Existing Prompt

If you've found a newer version of a documented prompt:

1. Update `system-prompt.md` with the new text
2. Add an entry to `changelog.md` with the date and changes
3. Update `analysis.md` if behavior has changed
4. Open a PR with tag `[prompt-update]`

### What We Need Most

- 🔍 Prompt extractions from newer models (Gemini 2.0, Claude 4, GPT o3)
- 🌍 Non-English model prompts (Chinese, Japanese, Arabic AI products)
- 📊 Behavioral analysis — what do these prompts actually *do* to model behavior?
- 🔧 Tool-use and agentic system prompts

📋 [Read the full contribution guide →](CONTRIBUTING.md)

---

## ❓ FAQ

**Q: Is this legal?**

System prompts extracted through normal API interactions or public leaks are generally considered to be in a legal gray area. We document what is publicly known. We do not encourage or assist in unauthorized access to AI systems. Consult your local laws if in doubt.

**Q: Why would companies leak their own system prompts?**

They wouldn't intentionally. Most leaks happen because:
- Users find clever prompts that make the model reveal its instructions
- Employees share information
- Researchers publish extraction techniques
- Companies accidentally expose prompts via UI bugs

**Q: Aren't you helping bad actors by publishing this?**

The information security community's view is that **security through obscurity is not real security**. If a system prompt is the only thing standing between safety and harm, that's a design failure. Publishing prompts enables transparency and accountability.

**Q: How do I know the prompts here are accurate?**

Each prompt includes its source and confidence level. We cross-reference multiple sources where possible. Prompts labeled `[reconstructed]` are clearly speculative. Always verify independently for critical uses.

**Q: Can I use these prompts in my own projects?**

The prompt texts themselves are likely owned by their respective companies. This repository documents them for research and educational purposes. Use them to learn from, not to impersonate other AI products.

**Q: My PR has been open for weeks. What's happening?**

This is a community project maintained in spare time. If your PR is stalled, leave a comment — sometimes it just needs a nudge. If you want to become a maintainer, reach out.

---


## 📜 License & Ethics

### License

This repository's **documentation, analysis, and original writing** is licensed under [MIT License](LICENSE).

The **prompt texts themselves** are reproduced for research and educational purposes. They remain the property of their respective companies. We claim no ownership over them.

### Ethical Commitments

- We will **never** publish prompts obtained through unauthorized system access
- We will **never** use this project to help users circumvent AI safety systems
- We will **remove** content if a company demonstrates it was obtained illegally
- We **encourage** AI companies to publish their own prompts — transparency is good

### A Note on Transparency

The irony is not lost on us that most of these prompts contain instructions to hide themselves. We believe AI users deserve to understand the systems they interact with. Every prompt published here is a step toward that transparency.

---

## 🙏 Acknowledgements

This project would not exist without:

- Researchers who published extraction techniques
- The AI safety community for keeping these conversations public
- Every contributor who submitted a PR or opened an issue
- The AI companies who, sometimes unintentionally, produced fascinating work worth studying

---
