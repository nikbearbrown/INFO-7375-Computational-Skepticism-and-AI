# Process Document: Extracting Testable Assertions from Biological Papers

## Overview

This document outlines a process for using Large Language Models (LLMs) to extract testable assertions from biological research papers according to Karl Popper's falsifiability framework. The process involves a two-stage LLM pipeline where one model identifies candidate assertions and another evaluates their testability.

## Process Flow

### 1. Preprocessing Stage

1. **Document Preparation**
   - Convert PDFs or other formats to plain text
   - Segment papers into logical sections (Abstract, Methods, Results, Discussion)
   - Normalize scientific terminology and units

2. **Initial Filtering**
   - Prioritize Results and Discussion sections for assertion extraction
   - Identify sentences containing empirical claims, hypotheses, or conclusions
   - Remove purely descriptive or methodological statements

### 2. Assertion Identification Stage

1. **Candidate Assertion Extraction**
   - Apply NLP techniques to identify declarative statements
   - Focus on sentences containing:
     * Causal relationships ("X causes Y", "X leads to Y")
     * Correlational claims ("X is associated with Y")
     * Mechanism proposals ("X functions by Y")
     * Quantitative relationships ("X increases/decreases Y by Z%")

2. **Biological Context Assessment**
   - Identify biological entities (genes, proteins, organisms, pathways)
   - Map relationships between entities
   - Recognize experimental conditions and constraints

3. **Popperian Criteria Application**
   - Evaluate each candidate assertion against:
     * Falsifiability (Can this be proven wrong?)
     * Precision (Are terms clearly defined with measurable parameters?)
     * Scope (Is the domain of application clearly specified?)
     * Independence (Is this testable without numerous auxiliary hypotheses?)

### 3. Testability Scoring and Classification

1. **Testability Classification**
   - High testability: Directly falsifiable with clear experimental conditions
   - Medium testability: Testable with additional clarification or specification
   - Low testability: Requires substantial reformulation to be testable
   - Non-testable: Fundamentally unfalsifiable claims

2. **Output Formatting**
   - Structure extracted assertions with:
     * The assertion in its original form
     * Testability score and classification
     * Required conditions for testing
     * Potential falsification experiments

## Example Prompts for Testing the System

### Prompt 1: Basic Extraction and Classification

```
You are an AI system trained to identify testable scientific assertions according to Karl Popper's philosophy of science. Analyze the following passage from a biological research paper and:

1. Extract all potential scientific assertions
2. Classify each assertion based on testability (High, Medium, Low, Non-testable)
3. For each testable assertion, specify:
   a) The precise conditions under which it would be falsified
   b) A concrete experiment that could potentially falsify it
   c) What would constitute evidence against the assertion

Passage: [INSERT BIOLOGICAL PAPER PASSAGE]
```

### Prompt 2: Focused Mechanistic Assertion Extraction

```
You are analyzing biological research papers to identify testable mechanistic assertions. For the following paper excerpt, identify all claims about biological mechanisms that meet these criteria:

1. The claim proposes a specific mechanism of action
2. The mechanism involves clearly defined biological entities
3. The claim makes predictions that could be experimentally verified
4. The claim is falsifiable through direct experimentation

For each identified assertion:
- Restate it in "If...then..." format
- Specify what observation would falsify this mechanism
- Rate its testability on a scale of 1-10 and explain your rating

Paper excerpt: [INSERT BIOLOGICAL PAPER PASSAGE]
```

### Prompt 3: Comparative Assertion Testing

```
You are evaluating scientific assertions from a biological research paper using Popper's falsifiability criterion. For each of the following statements extracted from the paper:

1. Reformulate it as a testable hypothesis
2. Identify the universal claim being made (if any)
3. Specify what would constitute a critical test of this assertion
4. Determine whether the assertion is:
   a) Directly testable as stated
   b) Testable after reformulation
   c) Not testable even with reformulation

Then rank the assertions from most to least testable according to Popper's framework.

Extracted assertions:
1. [Assertion 1]
2. [Assertion 2]
3. [Assertion 3]
...
```

### Prompt 4: Testing Against Prior Literature

```
You are a scientific assertion analyzer focusing on biological claims. For the following assertion extracted from a recent paper:

"[INSERT BIOLOGICAL ASSERTION]"

1. Determine if this is a testable assertion according to Popperian principles
2. If testable, identify:
   a) The specific predictions it makes
   b) The conditions under which it would be falsified
   c) Whether existing literature already contains evidence that would falsify it
3. Evaluate whether the assertion is novel or reformulates existing knowledge
4. Rate the assertion's potential impact if it survives falsification attempts

Explain your reasoning at each step.
```

### Prompt 5: Extraction from Methods and Results Sections

```
You are extracting testable assertions from a biological research paper, focusing specifically on implicit claims made in the Methods and Results sections. For the following excerpts:

METHODS: [Insert Methods section text]
RESULTS: [Insert Results section text]

1. Identify implicit assumptions and assertions in the Methods section that are testable
2. Extract quantitative claims from the Results section that could be independently verified
3. For each identified assertion:
   a) Reformulate it as an explicit, testable statement
   b) Specify the experimental conditions needed to test it
   c) Describe what would constitute falsification
4. Indicate which assertions are most amenable to independent verification

Focus particularly on assertions about:
- Dose-response relationships
- Causal mechanisms
- Effectiveness of experimental techniques
- Statistical relationships between variables
```

## Example Assertions for Validation Testing

To test if the system is correctly extracting testable assertions, we can use these examples ranging from highly testable to untestable:

### Highly Testable Assertions:
1. "Overexpression of protein X in mouse hepatocytes increases glucose uptake by 45% ± 5% compared to wild-type controls."
2. "Administration of compound Y at concentrations above 5μM induces apoptosis in >80% of MCF-7 breast cancer cells within 24 hours."

### Moderately Testable Assertions:
3. "The signaling pathway involving proteins A, B, and C regulates T-cell differentiation in response to inflammatory cytokines."
4. "Genetic variation in the promoter region correlates with expression levels in liver tissue but not in kidney tissue."

### Minimally Testable Assertions:
5. "Complex interactions between gut microbiota and host metabolism contribute to the development of metabolic syndrome."
6. "Epigenetic mechanisms play an important role in cellular adaptation to environmental stressors."

### Non-Testable Assertions:
7. "A holistic understanding of biological systems requires integration of multiple levels of organization."
8. "Evolution has optimized cellular pathways for energy efficiency."

The system should classify assertions 1-2 as highly testable, 3-4 as moderately testable, 5-6 as requiring substantial reformulation, and 7-8 as fundamentally untestable in their current form.

