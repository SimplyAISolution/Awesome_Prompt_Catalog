# Chain-of-Thought (CoT) Prompting

## 📋 Overview

Chain-of-Thought prompting encourages AI models to break down complex problems into step-by-step reasoning, leading to more accurate and explainable outputs.

## 🎯 Use Cases

- **Mathematical Problem Solving** - Multi-step calculations
- **Logical Reasoning** - Complex decision making
- **Analysis Tasks** - Breaking down information systematically
- **Debugging** - Step-by-step troubleshooting

## 📈 Performance Metrics

- **Accuracy Improvement**: +25-40% on reasoning tasks
- **Model Compatibility**: ⭐⭐⭐⭐⭐ (All models)
- **Complexity**: 🟢 Beginner-friendly
- **Token Efficiency**: 🟡 Medium (longer outputs)

## 🤖 Optimized Models

| Model | Performance | Notes |
|-------|------------|-------|
| GPT-4, GPT-4o | ⭐⭐⭐⭐⭐ | Excellent reasoning |
| Claude 4 | ⭐⭐⭐⭐⭐ | Strong logical flow |
| o1, o1-pro | ⭐⭐⭐⭐⭐ | Built-in CoT reasoning |
| Gemini 2.5 | ⭐⭐⭐⭐ | Good with examples |

## 🔧 Basic Template

```
[Task Description]

Let's think through this step by step:

1. First, I need to...
2. Then, I should...
3. Next, I'll...
4. Finally, I can...

Please show your reasoning for each step.
```

## 💡 Advanced Template

```
You are an expert [DOMAIN] specialist. I need you to solve this problem:

[PROBLEM STATEMENT]

Please approach this systematically:

**Step 1: Understanding**
- What is being asked?
- What information do I have?
- What are the constraints?

**Step 2: Planning**
- What approach should I take?
- What are the key steps?
- Are there any potential issues?

**Step 3: Execution**
- [Work through each step]
- [Show calculations/reasoning]
- [Verify each step]

**Step 4: Verification**
- Does this answer make sense?
- Have I addressed all parts of the question?
- Are there alternative solutions?

**Final Answer:** [Clear, concise conclusion]
```

## 📊 Examples

### Example 1: Mathematical Problem
```
Problem: A store offers a 20% discount on all items, then an additional 10% discount for loyalty members. If an item originally costs $100, what's the final price for a loyalty member?

Let's think through this step by step:

1. First, apply the 20% store discount:
   - 20% of $100 = $20
   - Price after store discount = $100 - $20 = $80

2. Then, apply the 10% loyalty discount to the already discounted price:
   - 10% of $80 = $8
   - Final price = $80 - $8 = $72

Therefore, a loyalty member would pay $72 for the item.
```

### Example 2: Logic Problem
```
Problem: All roses are flowers. Some flowers are red. Some red things are beautiful. Can we conclude that some roses are beautiful?

Let's analyze this step by step:

1. First, let me identify what we know:
   - All roses are flowers (roses ⊆ flowers)
   - Some flowers are red (flowers ∩ red ≠ ∅)
   - Some red things are beautiful (red ∩ beautiful ≠ ∅)

2. Next, let me trace the logical connections:
   - We know roses are flowers
   - We know some flowers are red
   - But we don't know if the roses are among the red flowers

3. Finally, let me check if we can make the conclusion:
   - We cannot definitively conclude that some roses are beautiful
   - The red flowers might not include roses
   - Even if some roses were red, we don't know if those red roses are beautiful

Conclusion: No, we cannot logically conclude that some roses are beautiful based on the given statements.
```

## ⚡ Quick Implementation

For immediate use, simply add this prefix to your prompts:

```
Let's work through this step-by-step:
```

## 🔗 Related Techniques

- [Self-Consistency Prompting](self-consistency.md)
- [Tree of Thoughts](../experimental/tree-of-thoughts.md)
- [Few-Shot Learning](few-shot-learning.md)

## 📚 Research References

- Wei et al. (2022): "Chain-of-Thought Prompting Elicits Reasoning in Large Language Models"
- Kojima et al. (2022): "Large Language Models are Zero-Shot Reasoners"

---
**Tags**: `reasoning`, `problem-solving`, `step-by-step`, `explainable-ai`  
**Difficulty**: 🟢 Beginner  
**Last Updated**: 2025-01-01