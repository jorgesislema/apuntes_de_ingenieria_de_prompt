# Troubleshooting y Diagnóstico de Prompts

## Introducción

Esta guía sistemática para troubleshooting prompts está basada en metodologías de ingeniería de software aplicadas específicamente a prompt engineering. Proporciona frameworks estructurados para diagnosticar, aislar y resolver problemas de prompts en entornos de producción.

---

## Framework de Diagnóstico Sistemático

### Metodología de 5 Layers

**Layer 1: Symptom Analysis (¿Qué está pasando?)**
**Layer 2: Input Validation (¿El problema está en los datos?)**
**Layer 3: Logic Validation (¿El prompt está bien diseñado?)**
**Layer 4: Context Analysis (¿Hay factores externos?)**
**Layer 5: Output Validation (¿El resultado es correcto pero no útil?)**

---

## Layer 1: Symptom Analysis

### Diagnostic Questions Framework

**1.1 Output Quality Issues**

¿Cuál es exactamente el problema con el output?

**Checklist de Síntomas:**
- [ ] **Inconsistencia:** Outputs diferentes para inputs similares
- [ ] **Incompletitud:** Missing información esperada
- [ ] **Irrelevancia:** Output correcto pero no útil para el caso
- [ ] **Incorrectitud:** Facts or logic errors detectables
- [ ] **Formato:** Structure no cumple especificaciones
- [ ] **Tono:** Style inapropiado para el contexto

**Diagnostic Script:**
```
# SYMPTOM CHARACTERIZATION TEMPLATE

## Issue Description
**Primary Symptom:** [Specific description]
**Frequency:** [Always/Sometimes/Rarely] - [X]% of executions
**User Impact:** [Blocks workflow/Requires manual fix/Minor inconvenience]
**Business Impact:** [High/Medium/Low] - [Quantified if possible]

## Variability Analysis
**Consistent across users:** [Yes/No/Partially]
**Consistent across time:** [Yes/No/Patterns observed]
**Consistent across input types:** [Yes/No/Specific types affected]

## Example Cases
### Working Example (if any):
Input: [Exact input]
Expected Output: [What should happen]
Actual Output: [What actually happened]

### Failing Example:
Input: [Exact input]
Expected Output: [What should happen] 
Actual Output: [What actually happened]
Diff Analysis: [Specific differences]
```

**1.2 Performance Issues**

**Speed/Latency Problems:**
- Response time >expected threshold
- Timeouts o hanging responses
- Inconsistent response times

**Resource Usage:**
- Token consumption higher than expected
- Rate limiting triggers
- Cost escalation

**Diagnostic Metrics:**
```
# PERFORMANCE DIAGNOSIS TEMPLATE

## Response Time Analysis
Average: [X] seconds (vs expected [Y] seconds)
P95: [X] seconds
P99: [X] seconds
Timeout rate: [X]%

## Token Usage Analysis  
Average tokens per request: [X] (vs expected [Y])
Input tokens: [X] | Output tokens: [Y]
Cost per request: $[X]

## Error Rate Analysis
Success rate: [X]%
Error types:
- Timeout: [X]%
- Rate limit: [X]%
- Model error: [X]%
- Invalid response: [X]%
```

---

## Layer 2: Input Validation

### 2.1 Data Quality Assessment

**Input Data Checklist:**
```
# INPUT VALIDATION FRAMEWORK

## Completeness Check
- [ ] All required fields present
- [ ] No unexpected null/empty values
- [ ] Data within expected ranges
- [ ] Referential integrity maintained

## Format Validation
- [ ] Data types match specifications
- [ ] Encoding (UTF-8, etc.) correct
- [ ] Delimiters and structure consistent
- [ ] Special characters handled properly

## Content Quality
- [ ] No truncated data
- [ ] Logical consistency within dataset
- [ ] Temporal consistency (dates, sequences)
- [ ] Domain-specific validation rules met
```

**Diagnostic Process:**
```
# STEP 1: Isolate Input Variables
Test with:
1. Minimal viable input (simplest case that should work)
2. Known good input (previously working example)
3. Systematic variation (change one element at a time)

# STEP 2: Input Boundary Testing
- Maximum size inputs
- Minimum size inputs  
- Edge cases (empty strings, special characters)
- International characters and languages

# STEP 3: Data Lineage Verification
- Trace data source and transformations
- Verify no corruption in pipeline
- Validate preprocessing steps
- Check for recent changes in upstream systems
```

### 2.2 Context Loading Issues

**Context Validation:**
```
# CONTEXT COMPLETENESS AUDIT

## Essential Context Elements
- [ ] User role/persona clearly defined
- [ ] Business objective explicit
- [ ] Constraints and limitations specified
- [ ] Success criteria established
- [ ] Domain knowledge provided

## Context Quality Checks
- [ ] Information is current and relevant
- [ ] No conflicting information
- [ ] Appropriate level of detail
- [ ] Cultural/linguistic context included
- [ ] Historical context when relevant

## Context Size Analysis
Total context tokens: [X]
Context window utilization: [X]%
Critical info placement: [Beginning/Middle/End]
Information density: [High/Medium/Low]
```

---

## Layer 3: Logic Validation

### 3.1 Prompt Structure Analysis

**Logic Flow Evaluation:**
```
# PROMPT LOGIC AUDIT TEMPLATE

## Role Definition Analysis
**Clarity Score (1-10):** [X]
- Is the role specific enough? [Yes/No]
- Does it match the task complexity? [Yes/No]
- Are expertise requirements realistic? [Yes/No]

## Instruction Sequence Analysis
**Logical Flow Score (1-10):** [X]
Step-by-step evaluation:
1. [Instruction] → Logic check: [Valid/Invalid/Ambiguous]
2. [Instruction] → Logic check: [Valid/Invalid/Ambiguous]
3. [Instruction] → Dependencies: [Previous step/Independent]

## Constraint Analysis
**Constraint Completeness (1-10):** [X]
- Technical constraints properly specified
- Business constraints included
- Resource limitations acknowledged
- Quality requirements defined

## Output Specification Analysis
**Specificity Score (1-10):** [X]
- Format requirements clear
- Content expectations specific
- Success criteria measurable
- Examples provided when needed
```

### 3.2 Chain of Reasoning Validation

**For Complex Multi-Step Prompts:**
```
# REASONING CHAIN DIAGNOSIS

## Step Dependency Analysis
Map each logical step:
Step 1: [Description] → Depends on: [Input/Assumption]
Step 2: [Description] → Depends on: [Step 1 output/Additional input]
Step N: [Description] → Depends on: [Previous steps/External factors]

## Logical Gap Identification
- Missing steps in reasoning chain
- Unsupported leaps in logic
- Circular dependencies
- Impossible or contradictory requirements

## Alternative Path Analysis
- What if Step X fails?
- Are there fallback reasoning paths?
- How robust is the logic to variations?
```

---

## Layer 4: Context Analysis

### 4.1 Environmental Factors

**External Variables Assessment:**
```
# ENVIRONMENTAL CONTEXT AUDIT

## Model-Specific Factors
Model version: [Specific version]
Recent model updates: [Date of last update]
Known model limitations: [Documented issues]
Model-specific best practices: [Compliance check]

## API and Infrastructure
API endpoint: [URL/Version]
Rate limiting status: [Current limits and usage]
Service health: [Any known issues]
Regional differences: [If using different endpoints]

## Temporal Factors
Time of day: [Peak/Off-peak usage periods]
Day of week: [Patterns in model performance]
Recent changes: [Any system/prompt changes in last 30 days]
Seasonal considerations: [If relevant to content]
```

### 4.2 User and Context Variability

**User Behavior Analysis:**
```
# USER CONTEXT DIAGNOSIS

## User Expertise Level
Domain knowledge: [Expert/Intermediate/Novice]
AI familiarity: [High/Medium/Low]
Expected interaction style: [Technical/Business/Casual]

## Use Case Variance
Primary use case: [As designed]
Actual use case: [How actually being used]
Use case drift: [Evolution over time]
Edge case frequency: [How often unusual requests]

## Organizational Context
Industry specifics: [Relevant regulations/standards]
Company culture: [Formal/Informal communication]
Stakeholder expectations: [Technical depth, timeline, format]
Integration requirements: [How output will be used]
```

---

## Layer 5: Output Validation

### 5.1 Response Quality Framework

**Multi-Dimensional Quality Assessment:**
```
# OUTPUT QUALITY SCORECARD

## Accuracy (Weight: 30%)
Factual correctness: [Score 1-10]
- Verifiable facts: [Correct/Incorrect/Unverifiable]
- Logical consistency: [Consistent/Minor issues/Major issues]
- Domain expertise demonstration: [Expert/Competent/Lacking]

## Completeness (Weight: 25%)
Requirements fulfillment: [Score 1-10]
- All requested elements present: [Yes/Partial/No]
- Appropriate depth: [Too shallow/Right/Too deep]
- Missing critical information: [None/Minor/Major]

## Relevance (Weight: 25%)
Task alignment: [Score 1-10]
- Addresses core question: [Directly/Partially/Off-topic]
- Appropriate for audience: [Yes/Somewhat/No]
- Actionable for intended use: [Highly/Moderately/Not]

## Usability (Weight: 20%)
Practical utility: [Score 1-10]
- Format supports intended use: [Perfect/Good/Poor]
- Language clarity: [Crystal clear/Clear/Unclear]
- Implementation guidance: [Detailed/Adequate/Insufficient]
```

### 5.2 Output Consistency Analysis

**Consistency Testing Protocol:**
```
# CONSISTENCY VALIDATION TEMPLATE

## Reproducibility Test
Execution 1: [Date/Time] → Output: [Summary/Hash]
Execution 2: [Date/Time] → Output: [Summary/Hash]
Execution 3: [Date/Time] → Output: [Summary/Hash]

Consistency Score: [X]% similarity
Variance Analysis:
- Content differences: [Significant/Minor/None]
- Format differences: [Significant/Minor/None]
- Quality differences: [Significant/Minor/None]

## Cross-User Consistency
User A (Expert): [Output summary]
User B (Intermediate): [Output summary]  
User C (Novice): [Output summary]

Inter-user consistency: [High/Medium/Low]
Expertise-dependent variations: [Expected/Unexpected]

## Temporal Consistency
Week 1 average quality: [Score]
Week 2 average quality: [Score]
Week 3 average quality: [Score]

Trend: [Improving/Stable/Degrading]
Significant changes: [Date and description]
```

---

## Troubleshooting Playbooks

### Playbook 1: "Inconsistent Output Quality"

**Symptoms:** Same prompt produces variable quality results
**Primary Suspects:** Temperature settings, context loading, input variations

**Diagnostic Steps:**
1. **Isolate Variables**
   ```
   # Test with identical inputs multiple times
   # Document temperature and sampling settings
   # Check for random elements in prompt
   ```

2. **Context Analysis**
   ```
   # Verify context window isn't being truncated
   # Check for dynamic context that changes
   # Validate context relevance and accuracy
   ```

3. **Parameter Optimization**
   ```
   # Test temperature: 0.0 → 0.3 → 0.7 → 1.0
   # Test top_p values: 0.1 → 0.5 → 0.9
   # Document quality vs. creativity trade-offs
   ```

**Solution Framework:**
```
IF inconsistency > 20% quality variance:
  → Lower temperature to 0.2 or below
  → Add more specific constraints
  → Include quality examples in prompt

IF creative variance desired but quality must be maintained:
  → Use temperature 0.5-0.7 with strict format requirements
  → Add quality validation steps in prompt
  → Implement post-processing validation
```

### Playbook 2: "Slow Response Times"

**Symptoms:** Response times significantly above baseline
**Primary Suspects:** Token count, model choice, API issues

**Diagnostic Steps:**
1. **Token Analysis**
   ```
   # Measure input token count
   # Analyze output token requirements
   # Check for unnecessary verbosity in prompt
   ```

2. **Prompt Optimization**
   ```
   # Remove redundant information
   # Compress context without losing meaning
   # Use bullet points vs. paragraphs where possible
   ```

3. **Infrastructure Check**
   ```
   # Test from different geographic locations
   # Check API status and known issues
   # Monitor for rate limiting
   ```

**Solution Framework:**
```
IF token count > 8K:
  → Compress context and instructions
  → Split into multiple smaller prompts
  → Use summarization for large inputs

IF infrastructure issues:
  → Implement retry logic with exponential backoff
  → Add request queuing for high-traffic periods
  → Consider alternative endpoints or models
```

### Playbook 3: "Wrong or Irrelevant Output"

**Symptoms:** Output is well-formatted but doesn't address the actual need
**Primary Suspects:** Ambiguous instructions, missing context, logic errors

**Diagnostic Steps:**
1. **Instruction Clarity**
   ```
   # Review prompt for ambiguous language
   # Check if task complexity matches instruction detail
   # Verify examples align with expectations
   ```

2. **Context Completeness**
   ```
   # Map required knowledge vs. provided context
   # Check for domain-specific terminology
   # Verify business context is sufficient
   ```

3. **Logic Validation**
   ```
   # Walk through prompt step-by-step
   # Identify assumptions being made
   # Check for logical gaps or jumps
   ```

**Solution Framework:**
```
IF ambiguous instructions:
  → Add specific examples of desired output
  → Use constraint-based specification
  → Break complex tasks into subtasks

IF missing context:
  → Provide domain-specific background
  → Include relevant business constraints
  → Add success criteria and examples

IF logic errors:
  → Simplify reasoning chain
  → Add validation steps within prompt
  → Use chain-of-thought prompting
```

---

## Monitoring and Prevention

### Real-Time Monitoring Framework

**Quality Metrics Dashboard:**
```
# PROMPT HEALTH MONITORING

## Response Quality Trends
- Average quality score (7-day rolling)
- Quality variance (consistency measure)
- User satisfaction ratings
- Task completion rates

## Performance Metrics
- Average response time
- 95th percentile response time
- Error rates by type
- Token usage efficiency

## Usage Patterns
- Request volume trends
- User behavior changes
- Edge case frequency
- Seasonal variations
```

### Automated Quality Assurance

**Quality Gates:**
```
# AUTOMATED QA PIPELINE

## Pre-Production Testing
- Regression test suite (50+ test cases)
- Performance benchmarks
- Cross-model validation
- User acceptance criteria

## Production Monitoring
- Real-time quality scoring
- Anomaly detection for response patterns
- Automatic rollback triggers
- User feedback integration

## Continuous Improvement
- A/B testing framework
- Performance trend analysis
- Usage pattern optimization
- Proactive issue identification
```

---

## Emergency Response Procedures

### Incident Response Framework

**Severity Levels:**

**P0 - Critical:** Complete failure or major quality degradation
- Response time: <15 minutes
- Actions: Immediate rollback, incident commander assigned

**P1 - High:** Significant impact to user experience
- Response time: <1 hour  
- Actions: Hotfix or configuration change

**P2 - Medium:** Moderate impact, workaround available
- Response time: <4 hours
- Actions: Planned fix in next deployment

**P3 - Low:** Minor issues, minimal user impact
- Response time: <24 hours
- Actions: Include in regular maintenance cycle

### Rollback Procedures

**Immediate Rollback Triggers:**
- Quality score drops >30% from baseline
- Error rate exceeds 25%
- User complaints exceed threshold
- Security concerns identified

**Rollback Process:**
1. **Immediate Action (0-5 minutes)**
   - Revert to last known good configuration
   - Notify stakeholders
   - Begin impact assessment

2. **Short-term Stabilization (5-30 minutes)**
   - Validate rollback effectiveness
   - Monitor for cascading issues
   - Prepare communication

3. **Root Cause Analysis (30 minutes - 24 hours)**
   - Document incident timeline
   - Identify contributing factors
   - Develop prevention strategies

---

*Este framework de troubleshooting debe ser personalizado para cada organización y caso de uso específico, pero proporciona una base sólida para el diagnóstico sistemático de problemas de prompts.*
