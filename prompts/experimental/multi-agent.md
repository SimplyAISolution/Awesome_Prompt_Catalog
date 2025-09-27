# Multi-Agent Prompting

## 📋 Overview

Multi-Agent Prompting simulates multiple AI personas working together on complex tasks, each bringing specialized expertise and perspectives. This technique enables more comprehensive analysis, creative collaboration, and robust problem-solving through diverse viewpoints.

## 🎯 Use Cases

- **Complex Decision Making** - Multiple expert perspectives on strategic choices
- **Creative Brainstorming** - Diverse creative approaches and idea generation
- **Quality Assurance** - Peer review and validation processes
- **Research Analysis** - Interdisciplinary investigation approaches
- **Product Development** - Cross-functional team simulation

## 📈 Performance Metrics

- **Solution Quality**: +50-80% improvement in complex scenarios
- **Perspective Diversity**: 3-5x more viewpoints considered
- **Model Compatibility**: ⭐⭐⭐⭐ (Requires advanced reasoning models)
- **Complexity**: 🔴 Advanced
- **Token Efficiency**: 🔴 Low (multiple agent interactions)

## 🤖 Optimized Models

| Model | Performance | Notes |
|-------|------------|-------|
| Claude 4 | ⭐⭐⭐⭐⭐ | Excellent persona consistency |
| GPT-4, GPT-4o | ⭐⭐⭐⭐⭐ | Strong multi-perspective reasoning |
| o1, o1-pro | ⭐⭐⭐⭐ | Good at complex agent interactions |
| Gemini 2.5 | ⭐⭐⭐ | Moderate multi-agent capabilities |

## 🔧 Basic Multi-Agent Template

```
**Multi-Agent Task Force**

**Scenario**: [PROBLEM_STATEMENT]

**Agent 1 - [ROLE_1]**:
Background: [EXPERTISE_AREA]
Perspective: [UNIQUE_VIEWPOINT]
Analysis: [AGENT_1_RESPONSE]

**Agent 2 - [ROLE_2]**:
Background: [EXPERTISE_AREA]
Perspective: [UNIQUE_VIEWPOINT]
Analysis: [AGENT_2_RESPONSE]

**Agent 3 - [ROLE_3]**:
Background: [EXPERTISE_AREA]
Perspective: [UNIQUE_VIEWPOINT]
Analysis: [AGENT_3_RESPONSE]

**Synthesis**:
Compare and integrate the three perspectives to provide a comprehensive solution.
```

## 💡 Advanced Multi-Agent Framework

```
**MULTI-AGENT COLLABORATION PROTOCOL**

**Mission**: [COMPLEX_PROBLEM_STATEMENT]

**🎯 Phase 1 - Individual Analysis**

**Agent Alpha - [SPECIALIST_1]**
- Identity: [DETAILED_BACKGROUND]
- Expertise: [SPECIFIC_SKILLS_AND_KNOWLEDGE]
- Mandate: Analyze from [UNIQUE_ANGLE]
- Constraints: [ROLE_SPECIFIC_LIMITATIONS]

Initial Assessment:
- Key observations: [FINDINGS]
- Primary concerns: [ISSUES_IDENTIFIED]
- Recommended approach: [METHODOLOGY]
- Success criteria: [MEASURABLE_OUTCOMES]

**Agent Beta - [SPECIALIST_2]**
- Identity: [DETAILED_BACKGROUND]
- Expertise: [SPECIFIC_SKILLS_AND_KNOWLEDGE]
- Mandate: Analyze from [UNIQUE_ANGLE]
- Constraints: [ROLE_SPECIFIC_LIMITATIONS]

Initial Assessment:
- Key observations: [FINDINGS]
- Primary concerns: [ISSUES_IDENTIFIED]
- Recommended approach: [METHODOLOGY]
- Success criteria: [MEASURABLE_OUTCOMES]

**Agent Gamma - [SPECIALIST_3]**
- Identity: [DETAILED_BACKGROUND]
- Expertise: [SPECIFIC_SKILLS_AND_KNOWLEDGE]
- Mandate: Analyze from [UNIQUE_ANGLE]
- Constraints: [ROLE_SPECIFIC_LIMITATIONS]

Initial Assessment:
- Key observations: [FINDINGS]
- Primary concerns: [ISSUES_IDENTIFIED]
- Recommended approach: [METHODOLOGY]
- Success criteria: [MEASURABLE_OUTCOMES]

**🤝 Phase 2 - Cross-Agent Discussion**

**Round 1 - Challenge and Critique**
Alpha responds to Beta's analysis: [CRITIQUE_AND_QUESTIONS]
Beta responds to Gamma's analysis: [CRITIQUE_AND_QUESTIONS]
Gamma responds to Alpha's analysis: [CRITIQUE_AND_QUESTIONS]

**Round 2 - Defense and Refinement**
Alpha defends and refines position: [REVISED_STANCE]
Beta defends and refines position: [REVISED_STANCE]
Gamma defends and refines position: [REVISED_STANCE]

**Round 3 - Consensus Building**
Areas of agreement: [SHARED_CONCLUSIONS]
Remaining disagreements: [UNRESOLVED_DIFFERENCES]
Compromise positions: [MIDDLE_GROUND_SOLUTIONS]

**🎯 Phase 3 - Integrated Solution**

**Synthesized Recommendation**:
- Primary strategy: [UNIFIED_APPROACH]
- Implementation plan: [STEP_BY_STEP_EXECUTION]
- Risk mitigation: [IDENTIFIED_RISKS_AND_SOLUTIONS]
- Resource requirements: [NEEDED_RESOURCES]
- Timeline: [REALISTIC_SCHEDULE]

**Minority Reports** (if applicable):
- Dissenting view from [AGENT]: [ALTERNATIVE_POSITION]
- Reasoning: [WHY_DIFFERENT_CONCLUSION]
```

## 📊 Examples

### Example 1: Business Strategy Decision
```
**Multi-Agent Strategic Planning Session**

**Scenario**: Tech startup deciding whether to expand internationally or focus on domestic market penetration

**Agent Alpha - CFO Perspective**
Identity: Experienced CFO with 15 years in tech startups, strong financial modeling background
Analysis: 
- International expansion requires $2M investment with 18-month payback
- Current cash runway: 24 months at current burn rate
- Domestic market still has 60% penetration opportunity
- Risk assessment: High financial risk with international expansion
- Recommendation: Focus domestic, expand internationally in 18 months

**Agent Beta - CMO Perspective**
Identity: Growth marketing expert, former VP at successful SaaS companies
Analysis:
- Domestic market showing signs of saturation in key segments
- International demand validated through inbound inquiries (200+ monthly)
- Competitive advantage window closing as competitors eye same markets
- Brand momentum currently strong for international launch
- Recommendation: Cautious international expansion in 2 pilot markets

**Agent Gamma - CTO Perspective**
Identity: Technical leader with experience scaling platforms globally
Analysis:
- Product architecture supports international scaling
- Localization effort: 3-4 months for 2 markets
- Technical infrastructure costs: $50K setup, $15K/month ongoing
- Engineering team capacity: Can support expansion without new hires
- Recommendation: Technical readiness supports either path

**Cross-Agent Discussion**:
Alpha: "Beta, your market saturation concern is valid, but cash preservation should be priority"
Beta: "Alpha, I understand the financial caution, but missing this window could set us back years"
Gamma: "Both perspectives valid - technical readiness gives us flexibility to pivot quickly if needed"

**Synthesized Recommendation**:
Hybrid approach - Limited international pilot (1 market, $500K investment) while maintaining domestic focus. Provides international learning with controlled financial exposure.
```

### Example 2: Product Development Priority
```
**Product Council Multi-Agent Review**

**Scenario**: Software company choosing between 3 major feature developments

**Agent Alpha - Product Manager**
Background: 8 years product experience, user research specialist
Priority Assessment:
- Feature A (AI Integration): High user demand (78% request rate), competitive necessity
- Feature B (Mobile App): Lower demand (34%) but strategic platform expansion
- Feature C (Enterprise Tools): Small user base (12%) but high revenue potential ($2M ARR)
Recommendation: Feature A for user satisfaction and competitive positioning

**Agent Beta - Engineering Lead**  
Background: 12 years development experience, architecture expert
Technical Assessment:
- Feature A: 6-month development, requires new team skills, moderate technical risk
- Feature B: 4-month development, leverages existing expertise, low risk
- Feature C: 8-month development, complex integration, high technical debt risk
Recommendation: Feature B for lowest risk and fastest delivery

**Agent Gamma - Sales Director**
Background: 10 years B2B sales, enterprise client relationships
Market Assessment:
- Feature A: Helps retain existing customers, limited new client acquisition
- Feature B: Minimal impact on current sales cycle, future potential unknown
- Feature C: Direct impact on 5 pending deals worth $3M, strong ROI case
Recommendation: Feature C for immediate revenue impact

**Debate Round**:
Alpha: "Gamma, Feature C serves only 12% of users - we risk alienating our core base"
Gamma: "Alpha, but those 12% represent 40% of our revenue - they're our most valuable segment"
Beta: "Both valid, but Feature A's technical complexity could delay all roadmap items"

**Consensus Solution**:
Phased approach - Start with Feature B (quick win, builds mobile capability), followed by Feature C (revenue protection), then Feature A when team has bandwidth for complex implementation.
```

### Example 3: Crisis Management Response
```
**Emergency Response Multi-Agent Team**

**Scenario**: SaaS platform experiencing major security incident affecting 10,000+ users

**Agent Alpha - CISO (Security)**
Immediate priorities:
- Contain breach scope: Isolate affected systems (ETA: 30 minutes)
- Forensic analysis: Determine attack vector and data exposure
- Security hardening: Implement additional protections
- Risk level: Critical - potential data exposure of PII
Action plan: Full incident response protocol, external security audit

**Agent Beta - CEO (Communications)**
Stakeholder management:
- Customer notification: Required within 2 hours by compliance
- Board/investor update: Schedule emergency call
- Public relations: Prepare proactive statement to control narrative  
- Legal consultation: Review notification requirements and liability
Action plan: Transparent communication strategy, customer retention focus

**Agent Gamma - CTO (Operations)**
Technical response:
- System stability: Maintain service for unaffected customers
- Data recovery: Backup integrity verified, 4-hour restoration possible
- Engineering resources: All-hands response, external contractors available
- Infrastructure scaling: Prepare for traffic surge during resolution
Action plan: Parallel workstreams for containment and service restoration

**Coordinated Response**:
Hour 1: Alpha leads containment, Beta prepares communications, Gamma manages operations
Hour 2: Customer notification sent, incident contained, recovery initiated  
Hour 4: Systems restored, detailed forensics begin, customer success outreach
Day 1-7: Full investigation, security improvements, customer retention program

**Outcome**: Coordinated response minimized customer churn (5% vs industry average 20%), strengthened security posture, and maintained stakeholder confidence
```

## 🚀 Advanced Multi-Agent Strategies

### 1. Hierarchical Agent Structure
```
**Executive Agent** (Oversight and decision-making)
├── **Specialist Agent 1** (Domain expertise)
├── **Specialist Agent 2** (Different domain expertise)  
└── **Specialist Agent 3** (Third domain expertise)

**Advisory Agents** (Cross-cutting concerns)
├── **Ethics Agent** (Moral and ethical considerations)
├── **Risk Agent** (Risk assessment and mitigation)
└── **Innovation Agent** (Creative and disruptive thinking)
```

### 2. Adversarial Agent Design
```
**Proposition Team**:
- Agent 1: Builds strongest case FOR the proposal
- Agent 2: Develops implementation strategy
- Agent 3: Identifies success factors

**Opposition Team**:
- Agent 4: Builds strongest case AGAINST the proposal
- Agent 5: Identifies implementation risks
- Agent 6: Proposes alternative solutions

**Judge Agent**: Evaluates both sides and renders decision
```

### 3. Sequential Expert Consultation
```
**Stage 1**: Problem definition by Domain Agent 1
**Stage 2**: Analysis by Domain Agent 2 (builds on Stage 1)
**Stage 3**: Solution design by Domain Agent 3 (builds on Stages 1-2)
**Stage 4**: Implementation planning by Domain Agent 4 (builds on Stages 1-3)
**Stage 5**: Final review by Senior Agent (synthesizes all stages)
```

## ⚙️ Implementation Patterns

### Single-Session Multi-Agent
```
Execute all agents in one comprehensive interaction:
"Simulate a meeting with [AGENT_LIST] to solve [PROBLEM]. Show individual perspectives, group discussion, and final consensus."
```

### Multi-Session Agent Development
```
Session 1: Agent 1 individual analysis
Session 2: Agent 2 individual analysis  
Session 3: Agent 3 individual analysis
Session 4: Cross-agent discussion and synthesis
```

### Interactive Agent Moderation
```
Human facilitates agent interaction:
Human: "Agent 1, present your analysis"
AI: [Agent 1 response]
Human: "Agent 2, what's your critique?"
AI: [Agent 2 response]
[Continue facilitated discussion]
```

## ⚠️ Best Practices

### Do's
- **Define clear agent roles** - Specific expertise and perspectives
- **Maintain persona consistency** - Each agent stays in character
- **Structure interactions** - Organized discussion format
- **Balance perspectives** - Avoid echo chambers
- **Synthesize thoughtfully** - Don't just average opinions

### Don'ts
- **Create too many agents** - 3-5 is usually optimal
- **Make agents too similar** - Ensure meaningful diversity
- **Skip the synthesis** - Integration is crucial
- **Ignore minority views** - Dissent often reveals important insights
- **Rush the process** - Multi-agent work takes more time

## 🔧 Quick Implementation Guide

### 5-Minute Multi-Agent
```
Present this problem to 3 different experts and synthesize their recommendations:
[PROBLEM_STATEMENT]

Expert 1: [ROLE_1]
Expert 2: [ROLE_2]
Expert 3: [ROLE_3]
```

### 15-Minute Multi-Agent
```
Use Basic Multi-Agent Template with specific roles and discussion round
```

### 60-Minute Multi-Agent
Use Advanced Multi-Agent Framework with full collaboration protocol

## 🔗 Related Techniques

- [Role-Based Prompting](../creative/role-based-prompting.md)
- [Tree of Thoughts](tree-of-thoughts.md)
- [Self-Consistency](../general/self-consistency.md)
- [Chain-of-Thought](../general/chain-of-thought.md)

## 📚 Research References

- Li et al. (2023): "Multi-Agent Debate Improves Reasoning in Large Language Models"
- Du et al. (2023): "Improving Factuality and Reasoning in Language Models through Multiagent Debate"
- Wang et al. (2023): "Enabling Intelligent Interactions between Agents and LLMs"

---
**Tags**: `multi-agent`, `collaboration`, `diverse-perspectives`, `complex-reasoning`  
**Difficulty**: 🔴 Advanced  
**Last Updated**: 2025-01-01