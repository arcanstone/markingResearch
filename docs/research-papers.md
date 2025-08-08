# Research Papers and Studies

This document contains links to key research papers and studies in automated mathematics grading, with brief explanations of their contributions and findings.

*To add a new paper: Include linked title, author/institution info, brief summary of methods and findings. Organize by research category.*

## Vision and Language Model Based Grading

### [AI-assisted Automated Short Answer Grading of Handwritten University Level Mathematics Exams](https://arxiv.org/html/2408.11728v1)
**ETH Zurich, 2024**  
Used GPT‑4 combined with Mathpix to grade semi‑open responses. Results showed GPT‑4 gave reliable initial grades but still required human verification. Emphasizes that handwritten mathematical expression recognition using WAP/TAP or Mathpix remains challenging.

### [Can Vision-Language Models Evaluate Handwritten Math?](https://arxiv.org/html/2501.07244v2)
**Fermat Benchmark Study, 2025**  
Introduces the Fermat benchmark with ~2,200 handwritten solutions across four error dimensions. Nine VLMs were evaluated; the best (Gemini‑1.5‑Pro) corrected only 77% of errors. Models performed significantly better with printed text than handwriting.

### [CHECK-MAT: Checking Hand-Written Mathematical Answers for the Russian Unified State Exam](https://arxiv.org/html/2507.22958v1)
**2024-25**  
Evaluates seven VLMs on 122 scanned handwritten solutions from Russia's national high‑school math exam. Emphasizes understanding student solutions rather than just checking final answers.

### [Evaluating GPT-4 at Grading Handwritten Solutions in Math Exams](https://arxiv.org/html/2411.05231v1)
**2024**  
Studies GPT‑4o's performance on probability exams. When provided rubric and correct answer, achieved best alignment with human grades (MAE ≈ 0.0766), but scores were still off by ~7.7% on average.

## Error Diagnosis and Classification

### [[2502.13789] From Correctness to Comprehension: AI Agents for Personalized Error Diagnosis in Education](https://arxiv.org/abs/2502.13789)
**MathCCS Dataset, 2025**  
Introduces dataset with real problems and expert‑annotated error categories. State‑of‑the‑art models achieved < 30% classification accuracy. Proposes sequential error analysis and multi‑agent framework.

### [A Benchmark for Math Misconceptions: Bridging Gaps in Middle School Algebra with AI-Supported Instruction](https://arxiv.org/html/2412.03765v1)
**2024**  
Captures 55 algebra misconceptions and 220 diagnostic examples. GPT‑4 achieved up to 83.9% precision/recall when constrained by topic and guided by educator feedback.

### [AI-Driven Virtual Teacher for Enhanced Educational Efficiency: Leveraging Large Pretrain Models for Autonomous Error Analysis and Correction](https://arxiv.org/html/2409.09403v1)
**VATE System**  
Multi‑round dialogue system that maintains an "error pool." Achieved 78.3% accuracy in diagnosing elementary‑level mathematical errors. Shows conversational feedback can complement grading systems.

## Data-Driven Methods and CAS Systems

### [[1501.04346] Mathematical Language Processing: Automatic Grading and Feedback for Open Response Mathematical Questions](https://arxiv.org/abs/1501.04346)
**MathLP/MLP Framework, 2015**  
Framework that clusters student solutions into correct/partial/incorrect groups using solution features. Demonstrated data‑driven clustering can reduce instructor workload, but requires typed solutions.

### [STACK](https://stack-assessment.org/)
**Open-source CAS-based Assessment**  
Evaluates answers by algebraic equivalence using Maxima CAS. Effective for algebraic manipulation but cannot grade reasoning or proofs.

## Formal Proof Verification and Theorem Proving

### [[2506.08321] LeanTutor: A Formally-Verified AI Tutor for Mathematical Proofs](https://arxiv.org/abs/2506.08321)
**2025**  
LLM‑based tutoring system that autoformalises proofs in Lean. Autoformalizer correctly formalised 57% of tactics in correct proofs and identified incorrect steps in 30% of incorrect proofs. Accompanies PeanoBench dataset.

### [REAL-Prover: Retrieval Augmented Lean Prover for Mathematical Reasoning](https://arxiv.org/html/2505.20613v1)
**2025**  
Integrates fine‑tuned LLM with retrieval system for theorem selection from mathlib. Achieved 23.7% success rate on ProofNet benchmark and 56.7% on FATE‑M algebra benchmark.

### [DeepSeek-Prover: Advancing Theorem Proving in LLMs through Large-Scale Synthetic Data](https://arxiv.org/html/2405.14333v1)
**2024**  
Generated synthetic dataset of 8 million Lean proofs from competition problems. 7B‑parameter model achieved 46.3% whole‑proof accuracy with 64 samples, compared to GPT‑4's 23.0%.

### [Teaching "Foundations of Mathematics" with the LEAN Theorem Prover](https://arxiv.org/html/2501.03352v2)
**University of Zurich Study**  
Pilot study teaching freshman students logic foundations using Lean. Emphasizes Lean as bridge between automated theorem provers and proof assistants with mathematician‑friendly syntax.

## Educational Applications and Case Studies

### [Automated theorem proving and proof verification | Department of Mathematics](https://math.duke.edu/mathplus/2023/automated-theorem-proving-and-proof-verification)
**Duke University Linear Algebra Game**  
Students write formal proofs in Lean to solve 64 linear‑algebra puzzles. Project contributed new definitions and lemmas to mathlib, including orthogonal complements of subspaces.

### [Enhancing Education Efficiency with Automated Grading](https://recursiveai.co.jp/case-studies/enhancing-education-efficiency-with-automated-grading)
**Recursive AI Case Study, Japan 2024**  
Elementary‑school math grading system. Students upload workbook photos, system recognizes handwritten numbers and applies government scoring guidelines. Demonstrates feasibility for basic arithmetic with fixed formats.

## Platform and Tool Documentation

### [AI Marking and Feedback Platform for Teachers | Graded Pro](https://graded.pro/pages/best-ai-grading-tool-for-math)
Commercial AI grading platform for middle and high‑school mathematics. Advertises support for scanned handwritten work and rubrics, emphasizes teacher control.

### [Gradescope | e-Learning | University of Florida](https://elearning.ufl.edu/supported-services/gradescope/)
University documentation of Gradescope usage. Notes OCR and AI assistance for grouping similar student responses, accelerating grading of free‑response questions and mathematical equations.

## Industry and Technical Resources

### [How the Lean language brings math to coding and coding to math - Amazon Science](https://www.amazon.science/blog/how-the-lean-language-brings-math-to-coding-and-coding-to-math)
Overview of Lean's educational ecosystem including interactive games (Natural Number Game), textbooks, and university courses. Discusses vision of children using Lean as mathematical playground.

### [Feedback Loops Guide AI to Proof Checking – Communications of the ACM](https://cacm.acm.org/news/feedback-loops-guide-ai-to-proof-checking/)
ACM article noting formalization of large proofs like Fermat's Last Theorem via Lean with volunteer communities. Discusses AI assistance through modular proof components and crowdsourced proof data.

## Key Research Gaps and Future Directions

Based on the literature review, several critical challenges remain:

1. **Handwriting Recognition**: Current OCR technology struggles with complex two‑dimensional mathematical notation
2. **Reasoning Assessment**: Most systems focus on final answers rather than solution processes
3. **Error Understanding**: Classification accuracy for mathematical errors remains below 30% for state‑of‑the‑art models  
4. **Autoformalization**: Converting informal mathematical reasoning to formal representations achieves only ~57% accuracy
5. **Human-AI Collaboration**: Successful systems require significant human oversight and verification