# Automated Mathematics Grading Research

A comprehensive collection of research on automated assessment and error diagnosis in handwritten mathematics, with focus on linear algebra applications.

## Table of Contents

### 📊 [Benchmarks and Datasets](docs/benchmarks.md)
Comprehensive overview of evaluation benchmarks for automated mathematics grading systems:
- **Fermat Benchmark** - 2,200 handwritten solutions across four error dimensions
- **CHECK-MAT** - Russian national exam handwritten solutions with expert grades
- **MathCCS** - Real problems with expert-annotated error categories
- **FATE-M** - Undergraduate abstract algebra problems in Lean4
- Error classification frameworks and evaluation metrics

### 🛠️ [Existing Tools and Platforms](docs/tools.md)
Analysis of current automated grading tools and their capabilities:
- **OCR Services** - Mathpix Snip and handwritten expression recognition
- **Commercial Platforms** - Graded.Pro, Gradescope, specialized systems
- **CAS-based Systems** - STACK, MapleTA, LON-CAPA
- Technical limitations and success patterns

### 📚 [Research Papers and Studies](docs/research-papers.md)
Curated collection of key research papers with summaries and findings:
- **Vision-Language Models** - GPT-4, Gemini studies on handwritten math
- **Error Diagnosis** - Classification systems and conversational feedback
- **Formal Verification** - Lean proof assistants and theorem proving
- **Educational Applications** - Case studies and pilot programs

## Research Focus Areas

### Current Challenges
- **Handwriting Recognition**: OCR struggles with complex mathematical notation
- **Reasoning Assessment**: Most systems focus on final answers vs. solution processes  
- **Error Classification**: State-of-the-art models achieve <30% accuracy
- **Autoformalization**: Converting informal reasoning to formal representations

### Promising Approaches
- **Hybrid Systems**: Combining OCR, error classification, and formal verification
- **Human-AI Collaboration**: Maintaining teacher oversight and verification
- **Specialized Domains**: Success in well-defined mathematical contexts
- **Conversational Feedback**: Multi-round dialogue systems for error correction

## Key Findings

1. **Handwriting remains a major bottleneck** - VLMs perform significantly better with printed vs. handwritten input
2. **Context matters** - Systems work well for elementary arithmetic but struggle with advanced proofs
3. **Process vs. product** - Understanding reasoning steps is more challenging than checking final answers
4. **Human expertise required** - Even sophisticated AI systems need significant oversight

## Future Directions

Research priorities for building robust linear algebra grading systems:
- Better OCR for two-dimensional mathematical notation
- Datasets of real handwritten linear algebra proofs with expert annotations
- Integration of formal theorem provers with LLM-based autoformalization
- Hybrid approaches combining multiple verification methods

