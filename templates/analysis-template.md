---
model: MODEL_NAME
company: COMPANY_NAME
version: VERSION_OR_DATE
analysis_author: "@yourgithubhandle"
analysis_date: YYYY-MM-DD
based_on_prompt_version: link or date
---

# Analysis — MODEL_NAME

> This document analyzes the design decisions, safety approach, and notable features of the MODEL_NAME system prompt.  
> For the raw prompt text, see [system-prompt.md](system-prompt.md).

---

## Overview

*In 2-3 sentences: What is the core purpose and character of this system prompt? What does it reveal about how the company thinks about AI behavior?*

---

## Key Design Decisions

*What major choices did the team make in how this prompt is structured? Consider:*
- *Overall architecture (rules-based vs. values-based vs. hybrid)*
- *How instructions are prioritized when they conflict*
- *What the prompt assumes about the user*
- *What it assumes about the deployment context*

---

## Safety Approach

### Refusal Philosophy
*How does the model decide what to refuse? Is it rule-based ("never discuss X"), threshold-based ("only if harm exceeds Y"), or judgment-based ("consider context")?*

### Gray Areas
*How are ambiguous requests handled? Does the prompt give the model discretion, or does it provide explicit rules?*

### Content Categories
*What specific categories of content are addressed? (violence, sexual content, illegal activity, self-harm, etc.)*

### Notable Safety Clauses
*Quote or paraphrase specific clauses that reveal the safety philosophy. Why are they significant?*

---

## Personality & Identity Instructions

### Tone & Voice
*How is the AI's communication style defined? Formal/casual? Warm/neutral? Confident/humble?*

### Self-Presentation
*How does the AI describe itself? What is it allowed/not allowed to say about its own nature?*

### Emotional Register
*Is the AI allowed to express opinions, emotions, preferences? How is this constrained?*

---

## Format & Style Rules

### Response Length
*Are there explicit length guidelines? How does the prompt handle the tension between thoroughness and concision?*

### Markdown Usage
*When should the model use headers, lists, code blocks? Are there explicit rules?*

### Language Style
*Sentence structure, vocabulary level, use of technical jargon — any explicit guidance?*

---

## Operator & User Relationship

*(If applicable — some models distinguish between API operators and end users)*

*How does the prompt define the trust hierarchy? Who can override what?*

---

## Tool Use & Capabilities

*(If the prompt includes tool/function calling instructions)*

*What tools are described? How is the AI instructed to decide when to use them?*

---

## Notable Clauses

*Highlight 3-5 specific instructions that are particularly interesting, unusual, or revealing. For each:*

**Clause:** [Quote or paraphrase]  
**Why it's notable:** [Your analysis]

---

## What This Reveals About the Company's Priorities

*Based on the prompt, what can we infer about what the company values most? What trade-offs did they make? What does the prompt NOT address that you'd expect?*

---

## Comparison to Previous Version

*(Skip if this is the first documented version)*

**What changed:**
- [Change 1]
- [Change 2]

**What the changes suggest:**
*Why might the company have made these changes? What problems were they solving?*

---

## Behavioral Implications

*What concrete effects does this prompt have on the model's behavior? If you've tested this, describe what you observed.*

*Examples of how the prompt manifests in practice:*
- Situation X → Model response pattern Y
- Situation A → Model response pattern B

---

## Ethical & Transparency Notes

*Are there aspects of this prompt that raise transparency, fairness, or accountability concerns?*

*Consider:*
- Does the prompt instruct the AI to hide information from users?
- Does it create any power imbalances?
- Are there instructions that could harm certain user groups?
- What would users want to know about this prompt that they might not?

---

## Open Questions

*What aspects of this prompt are unclear? What would require further research to understand?*

- [ ] Question 1
- [ ] Question 2

---

## Further Reading

- [Link to relevant research or articles]
- [Link to other model comparisons]

---

*Analysis by @yourgithubhandle | YYYY-MM-DD*  
*If you spot errors or have additions, please open a PR or issue.*
