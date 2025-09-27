# Few-Shot Learning Prompts

## 📋 Overview

Few-shot learning provides the AI model with several examples to learn patterns and apply them to new, similar tasks. This technique is highly effective for consistent formatting, style matching, and task-specific behaviors.

## 🎯 Use Cases

- **Format Standardization** - Consistent output structures
- **Style Mimicry** - Writing in specific tones or styles
- **Classification Tasks** - Pattern recognition
- **Data Extraction** - Structured information retrieval
- **Creative Tasks** - Following specific creative patterns

## 📈 Performance Metrics

- **Consistency**: +60-80% improvement in output format
- **Model Compatibility**: ⭐⭐⭐⭐⭐ (All models)
- **Complexity**: 🟢 Beginner-friendly
- **Token Efficiency**: 🟡 Medium (examples use tokens)

## 🤖 Optimized Models

| Model | Performance | Notes |
|-------|------------|-------|
| GPT-4, GPT-4o | ⭐⭐⭐⭐⭐ | Excellent pattern recognition |
| Claude 4 | ⭐⭐⭐⭐⭐ | Great at following examples |
| Gemini 2.5 | ⭐⭐⭐⭐ | Strong with structured data |
| Llama 4 | ⭐⭐⭐⭐ | Good consistency |

## 🔧 Basic Template

```
Here are some examples of [TASK]:

Example 1:
Input: [INPUT_1]
Output: [OUTPUT_1]

Example 2:
Input: [INPUT_2]
Output: [OUTPUT_2]

Example 3:
Input: [INPUT_3]
Output: [OUTPUT_3]

Now, please apply the same pattern to:
Input: [NEW_INPUT]
Output:
```

## 💡 Advanced Template

```
Task: [TASK_DESCRIPTION]

I'll show you examples of the desired input/output pattern:

**Example 1:**
Context: [CONTEXT_1]
Input: [INPUT_1]
Reasoning: [WHY_THIS_OUTPUT]
Output: [OUTPUT_1]

**Example 2:**
Context: [CONTEXT_2]
Input: [INPUT_2]
Reasoning: [WHY_THIS_OUTPUT]
Output: [OUTPUT_2]

**Example 3:**
Context: [CONTEXT_3]
Input: [INPUT_3]
Reasoning: [WHY_THIS_OUTPUT]
Output: [OUTPUT_3]

**Your Task:**
Context: [NEW_CONTEXT]
Input: [NEW_INPUT]
Reasoning: [Think through why you chose this output]
Output: [Your response following the pattern]
```

## 📊 Examples

### Example 1: Email Classification
```
Task: Classify emails by priority level

Example 1:
Input: "Meeting tomorrow at 3pm with the CEO about quarterly results"
Output: HIGH - CEO meeting about business results

Example 2:
Input: "Office printer is out of paper"
Output: LOW - Administrative supply issue

Example 3:
Input: "Customer threatening to cancel $50K contract due to service issues"
Output: URGENT - Major revenue at risk

Now classify this email:
Input: "Server is down, all services unavailable"
Output: URGENT - Critical system failure affecting all users
```

### Example 2: Product Description Writing
```
Task: Write compelling product descriptions

Example 1:
Product: Wireless Headphones
Output: Experience crystal-clear audio freedom with our premium wireless headphones. Featuring 30-hour battery life and noise-canceling technology, these headphones deliver studio-quality sound wherever you go. Perfect for commuting, working out, or relaxing at home.

Example 2:
Product: Smartphone Case
Output: Protect your investment with our military-grade smartphone case. Drop-tested from 10 feet and waterproof to 6 feet, this case offers ultimate protection without sacrificing style. Slim profile maintains device aesthetics while providing maximum security.

Example 3:
Product: Coffee Maker
Output: Wake up to perfect coffee every morning with our programmable coffee maker. Brew 12 cups of rich, flavorful coffee with precision temperature control and automatic shut-off. Your mornings just got a whole lot better.

Now write a description for:
Product: Gaming Keyboard
Output:
```

### Example 3: Code Comment Generation
```
Task: Generate helpful code comments

Example 1:
Code: `for i in range(len(data)):`
Comment: // Iterate through each item in the data array

Example 2:
Code: `if user.is_authenticated():`
Comment: // Check if user has valid authentication credentials

Example 3:
Code: `result = api_call(endpoint, params)`
Comment: // Make HTTP request to API endpoint with specified parameters

Now generate a comment for:
Code: `cache.set(key, value, expire_time)`
Comment: // Store value in cache with specified key and expiration time
```

## ⚠️ Best Practices

### Do's
- **Use 3-5 examples** - Sweet spot for most tasks
- **Vary examples** - Show different scenarios
- **Be consistent** - Keep format identical across examples
- **Include edge cases** - Show how to handle unusual inputs
- **Add reasoning** - Explain why each output is correct

### Don'ts
- **Too many examples** - Can confuse or overwhelm
- **Inconsistent format** - Mixed patterns reduce effectiveness
- **Biased examples** - Avoid skewing toward one type
- **Complex examples** - Keep examples clear and focused

## 🚀 Advanced Techniques

### Progressive Examples
Start with simple examples and gradually increase complexity:

```
Example 1 (Simple): [BASIC_CASE]
Example 2 (Medium): [MODERATE_CASE]
Example 3 (Complex): [ADVANCED_CASE]
```

### Negative Examples
Show what NOT to do:

```
✅ Good Example:
Input: [INPUT]
Output: [CORRECT_OUTPUT]

❌ Bad Example:
Input: [INPUT]
Output: [INCORRECT_OUTPUT] - Wrong because [REASON]
```

### Chain Examples
Link examples to show progression:

```
Example 1: [STEP_1] → [RESULT_1]
Example 2: [STEP_1] → [STEP_2] → [RESULT_2]
Example 3: [STEP_1] → [STEP_2] → [STEP_3] → [RESULT_3]
```

## 🔗 Related Techniques

- [Zero-Shot Prompting](zero-shot.md)
- [Chain-of-Thought](chain-of-thought.md)
- [Role-Based Prompting](../creative/role-based-prompting.md)

## 📚 Research References

- Brown et al. (2020): "Language Models are Few-Shot Learners"
- Min et al. (2022): "Rethinking the Role of Demonstrations: What Makes In-Context Learning Work?"

---
**Tags**: `examples`, `pattern-learning`, `consistency`, `format-control`  
**Difficulty**: 🟢 Beginner  
**Last Updated**: 2025-01-01