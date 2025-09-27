# Self-Consistency Prompting

## 📋 Overview

Self-consistency prompting generates multiple reasoning paths for the same problem and selects the most consistent answer. This technique significantly improves accuracy on complex reasoning tasks by reducing the impact of random errors.

## 🎯 Use Cases

- **Complex Problem Solving** - Mathematical, logical, and analytical tasks
- **Decision Making** - Multi-criteria evaluation scenarios
- **Quality Assurance** - Verification of critical outputs
- **Research Analysis** - Cross-validation of findings
- **Code Review** - Multiple perspective analysis

## 📈 Performance Metrics

- **Accuracy Improvement**: +15-30% on reasoning tasks
- **Model Compatibility**: ⭐⭐⭐⭐ (Works best with advanced models)
- **Complexity**: 🟡 Intermediate
- **Token Efficiency**: 🔴 Low (multiple generations required)

## 🤖 Optimized Models

| Model | Performance | Notes |
|-------|------------|-------|
| o1, o1-pro | ⭐⭐⭐⭐⭐ | Built-in consistency checking |
| GPT-4, GPT-4o | ⭐⭐⭐⭐⭐ | Excellent reasoning diversity |
| Claude 4 | ⭐⭐⭐⭐ | Strong logical consistency |
| Gemini 2.5 | ⭐⭐⭐⭐ | Good multi-path reasoning |

## 🔧 Basic Template

```
Problem: [PROBLEM_STATEMENT]

Please solve this problem using three different approaches:

**Approach 1**: [METHOD_1_DESCRIPTION]
[Work through the solution]

**Approach 2**: [METHOD_2_DESCRIPTION]
[Work through the solution]

**Approach 3**: [METHOD_3_DESCRIPTION]
[Work through the solution]

**Final Answer**: Compare the three approaches and provide the most consistent solution.
```

## 💡 Advanced Template

```
**Problem**: [DETAILED_PROBLEM_STATEMENT]

**Context**: [BACKGROUND_INFORMATION]

**Multiple Reasoning Paths**:

**Path 1 - [APPROACH_NAME_1]**:
Perspective: [VIEWPOINT_1]
Method: [METHODOLOGY_1]
Reasoning: [STEP_BY_STEP_LOGIC]
Answer: [RESULT_1]
Confidence: [HIGH/MEDIUM/LOW]

**Path 2 - [APPROACH_NAME_2]**:
Perspective: [VIEWPOINT_2]
Method: [METHODOLOGY_2]
Reasoning: [STEP_BY_STEP_LOGIC]
Answer: [RESULT_2]
Confidence: [HIGH/MEDIUM/LOW]

**Path 3 - [APPROACH_NAME_3]**:
Perspective: [VIEWPOINT_3]
Method: [METHODOLOGY_3]
Reasoning: [STEP_BY_STEP_LOGIC]
Answer: [RESULT_3]
Confidence: [HIGH/MEDIUM/LOW]

**Consistency Analysis**:
- Points of agreement: [COMMON_ELEMENTS]
- Points of disagreement: [DIFFERENCES]
- Most reliable approach: [JUSTIFICATION]

**Final Answer**: [MOST_CONSISTENT_SOLUTION]
```

## 📊 Examples

### Example 1: Mathematical Problem
```
Problem: A company's revenue grew by 15% in Q1, decreased by 8% in Q2, grew by 22% in Q3, and decreased by 5% in Q4. If the starting revenue was $1,000,000, what's the final revenue?

**Approach 1 - Sequential Calculation**:
Start: $1,000,000
After Q1: $1,000,000 × 1.15 = $1,150,000
After Q2: $1,150,000 × 0.92 = $1,058,000
After Q3: $1,058,000 × 1.22 = $1,290,760
After Q4: $1,290,760 × 0.95 = $1,226,222
Final: $1,226,222

**Approach 2 - Compound Formula**:
Final = Initial × (1.15) × (0.92) × (1.22) × (0.95)
Final = $1,000,000 × 1.226222
Final = $1,226,222

**Approach 3 - Verification**:
Net multiplier = 1.15 × 0.92 × 1.22 × 0.95 = 1.226222
Final revenue = $1,000,000 × 1.226222 = $1,226,222

**Final Answer**: All three approaches consistently yield $1,226,222
```

### Example 2: Logic Problem
```
Problem: In a group of 100 people, 60 like coffee, 40 like tea, and 25 like both. How many people like neither coffee nor tea?

**Approach 1 - Venn Diagram Logic**:
Coffee only: 60 - 25 = 35
Tea only: 40 - 25 = 15
Both: 25
Total who like at least one: 35 + 15 + 25 = 75
Neither: 100 - 75 = 25

**Approach 2 - Set Theory Formula**:
|Coffee ∪ Tea| = |Coffee| + |Tea| - |Coffee ∩ Tea|
|Coffee ∪ Tea| = 60 + 40 - 25 = 75
Neither = 100 - 75 = 25

**Approach 3 - Systematic Counting**:
People who like coffee: 60
People who like tea: 40
Double-counted (both): 25
Unique people with preferences: 60 + 40 - 25 = 75
People with no preference: 100 - 75 = 25

**Final Answer**: All approaches consistently show 25 people like neither coffee nor tea
```

### Example 3: Business Analysis
```
Problem: Should a company invest $500K in AI automation that will save $200K annually but requires $50K yearly maintenance?

**Approach 1 - Net Present Value (10% discount rate)**:
Annual net savings: $200K - $50K = $150K
NPV = -$500K + $150K/(1.1)¹ + $150K/(1.1)² + ... (10 years)
NPV = -$500K + $150K × 6.145 = $422K
Recommendation: Invest (positive NPV)

**Approach 2 - Payback Period**:
Net annual savings: $150K
Payback period: $500K ÷ $150K = 3.33 years
If project life > 3.33 years, it's profitable
Recommendation: Invest (reasonable payback)

**Approach 3 - IRR Analysis**:
Find rate where NPV = 0
$500K = $150K × (PVIFA for n years)
IRR ≈ 27% (higher than cost of capital)
Recommendation: Invest (high return rate)

**Final Answer**: All three financial approaches consistently recommend investment
```

## 🚀 Advanced Strategies

### Weighted Consistency
```
**Path 1**: [SOLUTION_1] (Confidence: 90%)
**Path 2**: [SOLUTION_2] (Confidence: 70%)
**Path 3**: [SOLUTION_3] (Confidence: 85%)

**Weighted Analysis**: Give more weight to higher-confidence solutions
```

### Consensus Building
```
**Round 1**: Initial three approaches
**Round 2**: Reconcile differences and re-solve
**Round 3**: Final consensus with highest confidence
```

### Error Detection
```
**Path 1**: [SOLUTION_1]
**Path 2**: [SOLUTION_2] ← Potential error detected
**Path 3**: [SOLUTION_3]

**Error Analysis**: Identify and correct the inconsistent path
```

## 🎯 Implementation Patterns

### Single-Prompt Method
Generate all reasoning paths in one prompt (faster, less expensive):

```
Solve this problem using three different methods and compare results:
[PROBLEM]
```

### Multi-Prompt Method
Use separate prompts for each path (more diverse reasoning):

```
Prompt 1: Solve using [METHOD_1]: [PROBLEM]
Prompt 2: Solve using [METHOD_2]: [PROBLEM]
Prompt 3: Solve using [METHOD_3]: [PROBLEM]
Prompt 4: Compare these three solutions: [RESULTS_1_2_3]
```

### Chain Method
Build each path on previous insights:

```
Path 1: [INITIAL_SOLUTION]
Path 2: Considering Path 1, solve differently: [PROBLEM]
Path 3: Considering Paths 1&2, find alternative: [PROBLEM]
```

## ⚠️ Best Practices

### Do's
- **Use 3-5 reasoning paths** - Sweet spot for consistency
- **Vary approaches** - Different methods reveal different insights
- **Check for systematic errors** - Look for common mistakes
- **Weight by confidence** - Trust more confident solutions
- **Document reasoning** - Show work for each path

### Don'ts
- **Accept first answer** - Always generate multiple paths
- **Ignore outliers** - Investigate significantly different results
- **Rush to consensus** - Analyze differences thoroughly
- **Skip verification** - Always check final answer
- **Ignore confidence levels** - Consider solution reliability

## 🔧 Quick Implementation

### 1-Minute Version
```
Solve this three different ways and pick the most consistent answer: [PROBLEM]
```

### 5-Minute Version
```
Problem: [PROBLEM]

Method 1: [APPROACH_1]
Method 2: [APPROACH_2] 
Method 3: [APPROACH_3]

Compare and choose the most reliable solution.
```

### 10-Minute Version
Use the Advanced Template with full analysis.

## 🔗 Related Techniques

- [Chain-of-Thought](chain-of-thought.md)
- [Tree of Thoughts](../experimental/tree-of-thoughts.md)
- [Multi-Agent Reasoning](../experimental/multi-agent.md)

## 📚 Research References

- Wang et al. (2022): "Self-Consistency Improves Chain of Thought Reasoning in Language Models"
- Huang et al. (2022): "Large Language Models Can Self-Improve"

---
**Tags**: `consistency`, `verification`, `multi-path-reasoning`, `accuracy`  
**Difficulty**: 🟡 Intermediate  
**Last Updated**: 2025-01-01