# Retrieval-Augmented Generation (RAG) Prompts

## 📋 Overview

RAG prompting combines large language models with external knowledge retrieval to provide accurate, up-to-date, and contextually relevant responses. This technique grounds AI outputs in factual information while maintaining natural language fluency.

## 🎯 Use Cases

- **Knowledge Base Queries** - Customer support and internal documentation
- **Research Assistance** - Academic and business research with citations
- **Real-time Information** - Current events and dynamic data analysis
- **Domain Expertise** - Specialized knowledge with source attribution
- **Fact-Checking** - Verification against authoritative sources

## 📈 Performance Metrics

- **Factual Accuracy**: +80-95% improvement with relevant sources
- **Model Compatibility**: ⭐⭐⭐⭐⭐ (All models, varies by implementation)
- **Complexity**: 🔴 Advanced (requires external systems)
- **Token Efficiency**: 🟡 Medium (context + retrieval overhead)

## 🤖 Optimized Models

| Model | Performance | Notes |
|-------|------------|-------|
| GPT-4, GPT-4o | ⭐⭐⭐⭐⭐ | Excellent context integration |
| Claude 4 | ⭐⭐⭐⭐⭐ | Strong source synthesis |
| Gemini 2.5 | ⭐⭐⭐⭐ | Good with structured data |
| o1, o1-pro | ⭐⭐⭐⭐ | Deep contextual reasoning |

## 🔧 Basic RAG Template

```
**Context from Knowledge Base**:
[RETRIEVED_DOCUMENT_1]
Source: [SOURCE_1]

[RETRIEVED_DOCUMENT_2]
Source: [SOURCE_2]

[RETRIEVED_DOCUMENT_3]
Source: [SOURCE_3]

**Question**: [USER_QUESTION]

**Instructions**:
- Answer based on the provided context
- Cite sources using [Source X] format
- If information is missing, state "Information not available in provided sources"
- Do not make assumptions beyond the given context

**Answer**:
```

## 💡 Advanced RAG Template

```
**RETRIEVAL CONTEXT**

**Primary Sources**:
1. **[SOURCE_1_TITLE]** ([CREDIBILITY_SCORE])
   Content: [RELEVANT_EXCERPT]
   Date: [PUBLICATION_DATE]
   Relevance: [HIGH/MEDIUM/LOW]

2. **[SOURCE_2_TITLE]** ([CREDIBILITY_SCORE])
   Content: [RELEVANT_EXCERPT]
   Date: [PUBLICATION_DATE]
   Relevance: [HIGH/MEDIUM/LOW]

3. **[SOURCE_3_TITLE]** ([CREDIBILITY_SCORE])
   Content: [RELEVANT_EXCERPT]
   Date: [PUBLICATION_DATE]
   Relevance: [HIGH/MEDIUM/LOW]

**Supporting Sources**: [ADDITIONAL_REFERENCES]

**Query**: [USER_QUESTION_OR_TASK]

**RAG Processing Instructions**:
1. **Synthesize Information**: Combine insights from all relevant sources
2. **Maintain Attribution**: Clearly cite sources for each claim
3. **Handle Conflicts**: If sources disagree, present both perspectives
4. **Assess Completeness**: Identify gaps in available information
5. **Provide Confidence**: Rate answer confidence based on source quality

**Response Format**:
- **Direct Answer**: [MAIN_RESPONSE_WITH_CITATIONS]
- **Source Analysis**: [QUALITY_AND_RELEVANCE_ASSESSMENT]
- **Confidence Level**: [HIGH/MEDIUM/LOW] based on [REASONING]
- **Limitations**: [WHAT_INFORMATION_IS_MISSING]
```

## 📊 Examples

### Example 1: Technical Documentation Query
```
**Context from Knowledge Base**:

Document 1: "API Authentication Guide v2.1"
To authenticate with our REST API, include the Authorization header with format: 
Authorization: Bearer {your-api-key}. Keys can be generated in the developer console under Settings > API Keys.
Source: [Official Documentation - Updated Dec 2024]

Document 2: "Common API Errors"
Error 401 (Unauthorized) typically occurs when: 1) API key is missing, 2) API key is invalid/expired, 3) API key lacks required permissions for the endpoint.
Source: [Troubleshooting Guide - Updated Nov 2024]

Document 3: "Rate Limiting Policy"
Free tier: 100 requests/hour. Pro tier: 1000 requests/hour. Enterprise: Custom limits. 
Rate limit headers: X-RateLimit-Remaining, X-RateLimit-Reset.
Source: [Service Terms - Updated Oct 2024]

**Question**: "How do I fix a 401 error when calling your API?"

**Answer**:
A 401 Unauthorized error when calling our API is typically caused by authentication issues [Source: Troubleshooting Guide]. Here's how to resolve it:

1. **Check Authorization Header**: Ensure you're including the proper header format: `Authorization: Bearer {your-api-key}` [Source: API Authentication Guide]

2. **Verify API Key**: 
   - Confirm your API key is valid and hasn't expired
   - Generate a new key if needed in Settings > API Keys in the developer console [Source: API Authentication Guide]

3. **Check Permissions**: Ensure your API key has the required permissions for the specific endpoint you're accessing [Source: Troubleshooting Guide]

4. **Rate Limiting**: While less common, verify you haven't exceeded your rate limits (100/hour for free tier, 1000/hour for pro tier) [Source: Service Terms]

**Confidence Level**: HIGH - All information sourced from official documentation
```

### Example 2: Research Query with Multiple Sources
```
**Context from Knowledge Base**:

Source 1: "Climate Change Report 2024" - IPCC
Global temperatures have risen 1.1°C above pre-industrial levels as of 2024. The rate of warming has accelerated in recent decades, with the last 10 years being the warmest on record.
Date: March 2024, Credibility: HIGH

Source 2: "Renewable Energy Statistics" - IEA
Renewable energy capacity increased by 295 GW in 2024, with solar photovoltaic accounting for 75% of additions. This represents a 12% increase from 2023.
Date: January 2025, Credibility: HIGH

Source 3: "Corporate Climate Commitments" - CDP Report
68% of Fortune 500 companies have set net-zero emissions targets, but only 23% have detailed implementation plans with interim milestones.
Date: September 2024, Credibility: HIGH

**Query**: "What's the current status of global climate action in 2024?"

**Response**:

**Direct Answer**:
Global climate action in 2024 shows both progress and challenges. Temperatures have now risen 1.1°C above pre-industrial levels, with acceleration in recent warming trends [IPCC Climate Report, 2024]. However, renewable energy deployment reached record levels with 295 GW of new capacity, primarily driven by solar installations [IEA Statistics, 2025].

Corporate commitment is mixed - while 68% of Fortune 500 companies have announced net-zero targets, implementation remains weak with only 23% having detailed interim plans [CDP Report, 2024].

**Source Analysis**:
- IPCC data provides authoritative temperature measurements
- IEA offers reliable renewable energy statistics  
- CDP report gives comprehensive corporate assessment

**Confidence Level**: HIGH - All sources are authoritative and recent (2024-2025)

**Limitations**: Data covers through 2024; policy effectiveness measures not available in provided sources
```

### Example 3: Conflicting Sources Handling
```
**Context from Knowledge Base**:

Source A: "Economic Forecast Q4 2024" - Federal Reserve
Economic indicators suggest a soft landing is likely, with inflation trending toward 2% target and unemployment remaining stable at 3.8%.
Date: December 2024, Credibility: HIGH

Source B: "Market Analysis Report" - Goldman Sachs
Rising concerns about recession risk in H1 2025 due to tightening credit conditions and weakening consumer spending indicators.
Date: January 2025, Credibility: HIGH

Source C: "Employment Data" - Bureau of Labor Statistics
Unemployment rate increased to 4.1% in December 2024, highest level in 18 months. Job openings declined 8% quarter-over-quarter.
Date: January 2025, Credibility: HIGH

**Query**: "What's the economic outlook for 2025?"

**Response**:

**Direct Answer**:
The economic outlook for 2025 presents conflicting perspectives from authoritative sources:

**Optimistic View**: The Federal Reserve projects a "soft landing" scenario with inflation approaching the 2% target and stable employment conditions [Federal Reserve Forecast, Dec 2024].

**Cautious View**: Goldman Sachs warns of recession risks in the first half of 2025, citing tightening credit and weakening consumer spending [Market Analysis, Jan 2025].

**Employment Reality**: Recent data shows unemployment has risen to 4.1% with declining job openings, suggesting labor market cooling [BLS Data, Jan 2025].

**Source Analysis**:
- Federal Reserve data may reflect policy intentions rather than market realities
- Goldman Sachs provides forward-looking risk assessment
- BLS offers current factual employment data

**Confidence Level**: MEDIUM - High-quality sources present conflicting interpretations

**Limitations**: Economic forecasting inherently uncertain; resolution of conflicting indicators requires additional data not available in sources
```

## 🚀 Advanced RAG Strategies

### Multi-Stage Retrieval
```
**Stage 1 - Broad Context**: Retrieve general topic information
**Stage 2 - Specific Details**: Target precise query aspects
**Stage 3 - Verification**: Cross-reference facts across sources
**Stage 4 - Gap Analysis**: Identify missing information
```

### Source Quality Assessment
```
**Credibility Factors**:
- Authority of publisher (1-5 score)
- Publication date recency (1-5 score)  
- Citation quality (1-5 score)
- Peer review status (bonus +2)

**Relevance Scoring**:
- Direct topic match (1-5 score)
- Query term coverage (1-5 score)
- Context appropriateness (1-5 score)
```

### Confidence Calibration
```
**HIGH Confidence**: 3+ authoritative sources agree, recent data
**MEDIUM Confidence**: 2+ sources or minor disagreements
**LOW Confidence**: Single source or significant conflicts
**UNCERTAIN**: Insufficient or contradictory evidence
```

## ⚠️ Best Practices

### Do's
- **Prioritize recent sources** - Favor newer information when available
- **Cite everything** - Every claim should have source attribution
- **Handle conflicts** - Present disagreements transparently
- **Assess source quality** - Weight responses by credibility
- **Acknowledge gaps** - Clearly state what information is missing

### Don'ts
- **Mix retrieved and generated** - Keep source-based and inference separate
- **Over-extrapolate** - Don't go beyond what sources support
- **Ignore dates** - Temporal relevance matters significantly
- **Cherry-pick** - Present balanced view of available sources
- **Assume completeness** - Always note potential gaps

## 🔧 Implementation Patterns

### Simple RAG
```
Context: [RETRIEVED_DOCS]
Question: [QUERY]
Answer based on context: [RESPONSE]
```

### Structured RAG
```
Sources: [ORGANIZED_REFERENCES]
Analysis: [SYNTHESIS_PROCESS]
Response: [FORMATTED_ANSWER]
Citations: [SOURCE_ATTRIBUTIONS]
```

### Interactive RAG
```
Initial Response: [FIRST_ANSWER]
Follow-up Retrieval: [ADDITIONAL_CONTEXT]
Refined Response: [UPDATED_ANSWER]
```

## 🔗 Related Techniques

- [Chain-of-Thought](../general/chain-of-thought.md)
- [Self-Consistency](../general/self-consistency.md)
- [Citation Generation](citation-generation.md)

## 📚 Research References

- Lewis et al. (2020): "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
- Guu et al. (2020): "REALM: Retrieval-Augmented Language Model Pre-Training"

---
**Tags**: `retrieval`, `knowledge-grounding`, `fact-checking`, `source-attribution`  
**Difficulty**: 🔴 Advanced  
**Last Updated**: 2025-01-01