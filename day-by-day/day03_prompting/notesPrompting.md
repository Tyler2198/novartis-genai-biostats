# 🧪 Prompt Strategy Testing: Arthropathy, Psoriasis & Male Infertility

## 🎯 Objective:
Explore and document three different prompt types to evaluate how they influence the model’s response to the biomedical question:

> **“Is Arthropathy associated with Psoriasis and Male Infertility?”**

## 🧩 Prompt Types and Their Characteristics

---

### 1. Strict Contextual Prompt (Image 1)

**Behavior:**  
- Relies strictly on the provided context.  
- Avoids any speculation or inference.  

**📝 Summary Response:**  
> The context does not mention arthropathy. No conclusions can be drawn without explicit data.

**✅ Pros:** High factual precision  
**⚠️ Cons:** Limited reasoning, lacks clinical depth

---

### 2. Contextual + Logical Reasoning (Image 2)

**Behavior:**  
- Starts from the text and applies logical reasoning.  
- Makes cautious inferences based on medical knowledge.

**📝 Summary Response:**  
> While not explicitly mentioned, arthropathy may relate to psoriasis due to known autoimmune links. No direct conclusion for infertility, but reasonable to suspect a connection via inflammation.

**✅ Pros:** Balanced, grounded in logic  
**⚠️ Cons:** Still cautious, avoids asserting conclusions

---

### 3. Expert-Level Biomedical Synthesis (Image 3)

**Behavior:**  
- Uses external scientific knowledge and mechanisms.  
- Goes beyond context to explain relationships.

**📝 Summary Response:**  
> Up to 30% of psoriasis patients develop psoriatic arthritis. Psoriasis is also linked to male infertility via inflammation and oxidative stress. A shared inflammatory pathway may link all three conditions.

**✅ Pros:** Rich explanation, research-grade synthesis  
**⚠️ Cons:** Not bounded to input context—risky for citation-sensitive tasks

---

## 🔍 Use Case Insight

| Prompt Type | Best For | Avoid When |
|-------------|----------|------------|
| **Strict** | Exams, factual QA | Deep exploration or hypothesis generation |
| **Reasoned** | Hypotheses, exploratory analysis | Purely citation-driven work |
| **Expert Synthesis** | Reviews, model demos, expert reports | Tasks needing context-bounded answers |

---

*Created for prompt benchmarking and model behavior analysis in biomedical contexts.*
