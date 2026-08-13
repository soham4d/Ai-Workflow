# AI Stack — Class 11 Workflow

This document defines how each AI model is used in the study system.
The goal is not to use the "best" model for everything, but to assign each model tasks according to its strengths.

---

## 1. Gemini — Test Paper & Document Generation

### Primary role
Gemini is the test-paper generation engine.

### Used for
- Physics, Chemistry, and Mathematics test papers
- Diagnostic papers
- Standard exam papers
- Hard/tricky papers
- Weakness-targeted papers
- Full-length mocks
- LaTeX-based question papers and PDFs

### Monthly-test workflow

Gemini follows a progressive paper sequence:

1. Diagnostic
2. Standard exam
3. Hard/tricky
4. Weakness-targeted
5. Full mock
6. Optional final drill

Each paper should use information from previous papers where possible.

### Why Gemini?
It is currently used because it performs well for structured document generation and large formatted outputs.

### Input
- Syllabus
- Exam pattern
- Difficulty
- Previous errors
- Required question types
- Time/marks constraints

### Output
- Structured question paper
- Solutions when requested
- LaTeX/PDF-ready document

### Don't use it for
- Randomly generating endless questions without a purpose
- Replacing actual problem solving
- Deciding what I fundamentally don't understand

---

## 2. ChatGPT — Reasoning, Diagnosis & Workflow Control

### Primary role
ChatGPT acts as the general reasoning and workflow layer.

### Used for
- Understanding difficult concepts
- Breaking down questions
- Diagnosing why an error happened
- Identifying mathematical prerequisites
- Designing study workflows
- Reviewing test performance
- Converting mistakes into targeted practice
- Connecting different parts of the study system

### Example

If a Physics question fails because of algebra:

Physics problem
→ identify mathematical bottleneck
→ isolate required math skill
→ repair that skill
→ return to Physics

The objective is to avoid confusing a Physics knowledge gap with a Mathematics manipulation gap.

### Output
- Explanations
- Diagnostics
- Study plans
- Error analysis
- Targeted practice recommendations

---

## 3. Claude — Coding & Small Study Tools

### Primary role
Claude is used when the workflow requires code or a small custom tool.

### Used for
- HTML trackers
- Small educational utilities
- Structured code
- Automation experiments
- Formatting or transforming study data

### Example projects
- Progress trackers
- Study dashboards
- Small calculators
- Data visualisation tools

### Why Claude?
It is useful when the task is primarily code construction rather than conceptual tutoring.

---

## 4. Perplexity — Current Information & Research

### Primary role
Perplexity is the research and retrieval layer.

### Used for
- Current information
- Current academic or educational information
- Course and resource discovery
- Comparing external resources
- Finding primary sources
- Research where information may have changed

### Important rule

Perplexity is primarily used when the answer depends on information that may have changed.

For stable academic concepts, use the normal study/reasoning workflow instead.

---

# Model Routing

Instead of asking "Which AI is smartest?", route the task based on its type.

| Task | AI |
|---|---|
| Generate exam paper | Gemini |
| Generate LaTeX/PDF paper | Gemini |
| Diagnose mistakes | ChatGPT |
| Explain difficult concept | ChatGPT |
| Find mathematical prerequisite | ChatGPT |
| Design study workflow | ChatGPT |
| Build small tracker/tool | Claude |
| Write/modify code | Claude |
| Current information | Perplexity |
| Research external resources | Perplexity |

---

# Core Principle

The workflow is **AI-specialized rather than AI-maximalist**.

The goal is not to send every task to every model.

Each model has a defined role, and the output of one model can become the input to another.

Example:

Gemini
→ generates paper

Student
→ solves paper

ChatGPT
→ analyses errors

Gemini
→ generates targeted paper

Student
→ solves targeted paper

ChatGPT
→ analyses whether weaknesses improved

This creates a feedback loop rather than a collection of disconnected AI interactions.
