# 📊 Prompt Evaluation – Day 3  
**Query:** *"How is Arthropathy related to Psoriasis and Male Infertility?"*  
**Document:** TS3043166.pdf  
**Model:** LLaMA3 via Ollama

---

## 🔍 Prompt Style Comparison

| Prompt Style       | Answer Quality | Factual Accuracy | Depth of Reasoning | Context Grounding | Notes |
|--------------------|----------------|------------------|---------------------|--------------------|-------|
| **Basic Prompt**   | ⚠️ Medium       | ✅ Correct         | ⚠️ Superficial        | ✅ Yes               | Stated that Arthropathy wasn’t mentioned and didn’t elaborate further. |
| **Chain-of-Thought** | ✅ High        | ✅ Accurate        | ✅ Excellent          | ✅ Strong            | Stepped through associations, inferred autoimmune relevance, respected context. |
| **Few-Shot Prompt** | ✅ High        | ✅ Mostly Correct  | ✅ Deep + clinical    | ⚠️ Weak              | Provided compelling reasoning but introduced external facts not grounded in the prompt (e.g., 30% PsA stat). |

---

## 🧠 Sample Outputs

### ✏️ Basic Prompt
> The provided context does not mention Arthropathy as a comorbidity or correlate it with Psoriasis and Male Infertility. [...] Without explicit data or findings related to Arthropathy, we cannot draw a direct correlation.

### 🧠 Chain-of-Thought Prompt
> Based on the provided context, we can reason step by step to answer the question. [...] It is likely that arthropathy would also be associated with psoriasis. [...] There may be a shared inflammatory or comorbidity pathway.

### 📚 Few-Shot Prompt
> Arthropathy, which is inflammation of the joints, has been observed in some individuals with psoriasis. Research suggests that up to 30% of people with psoriasis may develop psoriatic arthritis (PsA) [...] suggesting an underlying inflammatory or oxidative stress pathway.

---

## ✅ Conclusion

| Use Case | Best Prompt Style |
|----------|-------------------|
| Clinical document QA (grounded) | **Chain-of-Thought** |
| Public chatbot, assistant | **Few-Shot** |
| Risk-free factual retrieval | **Basic** |

---

## 🧪 Next Step Ideas

- Test output consistency across additional medical prompts (e.g. obesity, hyperlipidemia)
- Run outputs through automatic hallucination detection (long-term goal)
- Evaluate code-generation prompts next (R with `gtsummary` / `gt`)

---
