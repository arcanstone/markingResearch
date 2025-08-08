# Benchmarks and Datasets for Automated Mathematics Grading

This document catalogs the key benchmarks and datasets used to evaluate automated mathematics grading systems, particularly for handwritten solutions.

## Benchmarks Overview

| Dataset/Benchmark | Description & Purpose | Key findings |
|-------------------|----------------------|--------------|
| **Fermat benchmark (2025)** | Contains ~2,200 handwritten solutions with synthetic perturbations across four error dimensions (computational, conceptual, notational, presentation). Designed to test VLMs on error detection, localization and correction. | Nine VLMs were evaluated; the best (Gemini‑1.5‑Pro) corrected only 77% of errors. Models performed significantly better when the handwritten input was replaced with printed text, highlighting difficulties with handwriting. |
| **CHECK‑MAT (2024–25)** | 122 scanned handwritten solutions from Russia's national high‑school math exam with expert grades and a detailed rubric. Evaluates seven VLMs on error identification and alignment with the rubric. | The benchmark emphasises understanding student solutions rather than just checking the final answer. Early automated grading systems using CAS (STACK, LON‑CAPA) verified algebraic equivalence but could not assess reasoning. |
| **MathCCS (Mathematical Classification and Constructive Suggestions) dataset (2025)** | Contains real problems and student solutions with expert‑annotated error categories and longitudinal data. Designed for multi‑agent systems that classify errors and provide tailored feedback. | State‑of‑the‑art models (Qwen2‑VL, LLaVA‑OV, Claude‑3.5‑Sonnet, GPT‑4o) achieved < 30% classification accuracy, and suggestions were low quality. The authors propose sequential error analysis and a multi‑agent framework to improve performance. |
| **Middle‑School Algebra Misconceptions benchmark (2024)** | Captures 55 algebra misconceptions and 220 diagnostic examples. Evaluated with GPT‑4 constrained by topic and teacher feedback. | Achieved precision/recall up to 83.9%, but performance varied across topics. Teachers considered the dataset valuable and emphasised the need for human expertise. |
| **MathLP/MLP (2015)** | Framework that clusters student solutions into correct/partial/incorrect groups using features from the solution. Allows minimal instructor grading and identifies error locations when a multistep solution deviates from the correct cluster. | Demonstrated that data‑driven clustering can reduce instructor workload and provide targeted feedback, but requires typed solutions and cannot handle complex proofs. |
| **FATE‑M (Formal Algebra Theorem Evaluation—Medium) (2025)** | 141 undergraduate‑level abstract‑algebra problems formalised in Lean4, extracted from 12 textbooks. Problems are paired with Lean proofs and natural‑language comments. Used to evaluate formal theorem provers. | Provides the first Lean benchmark targeting college‑level algebra. When evaluated with REAL‑Prover (retrieval‑augmented Lean prover), the best success rate (Pass@64) was 56.7%, surpassing other 7B‑parameter models. |
| **PeanoBench (2025)** | 371 Peano‑arithmetic proofs derived from the Natural Number Game. Each natural‑language proof step is paired with the corresponding Lean tactic. Used to evaluate the LeanTutor system. | LeanTutor's autoformalizer correctly formalised 57% of tactics in correct proofs and identified the incorrect step in 30% of incorrect proofs. |
| **Probability exam dataset for GPT‑4o grading (2024)** | Real handwritten responses from 18 students' probability exams with rubrics. Used to evaluate GPT‑4o's ability to grade using scanned images and rubrics. | When provided the correct answer and rubric, GPT‑4o achieved the best alignment with human grades (mean absolute error 0.0766). However, scores were still off by ~7.7% on average, showing substantial room for improvement. |

## Key Insights from Benchmarks

### Handwriting Recognition Challenges
- **Handwriting is a major challenge for VLMs and LLMs.** The Fermat benchmark shows that VLMs detect and correct errors better with printed text than with handwriting.
- **GPT‑4o's performance** on a probability exam similarly improved when given the rubric and correct answer but still lagged behind human graders.

### Error Analysis Requirements
- **Accurate error diagnosis requires more than answer verification.** Datasets like CHECK‑MAT and MathCCS highlight the importance of analysing the solution process and aligning feedback with a rubric.
- **Simple clustering or CAS equivalence checks** are insufficient for proofs and complex reasoning.

### Formal Reasoning Evaluation
- **Formal‑theorem benchmarks (FATE‑M, PeanoBench)** bridge the gap between human and machine reasoning.
- These datasets formalise problems in Lean and provide proof scripts, enabling evaluation of automated theorem provers and autoformalization pipelines.

## Error Classification Framework

Based on the Fermat benchmark, mathematical errors can be classified into four main dimensions:

1. **Computational errors** - Arithmetic mistakes, calculation errors
2. **Conceptual errors** - Misunderstanding of mathematical concepts
3. **Notational errors** - Incorrect mathematical notation or symbols  
4. **Presentation errors** - Poor structure or unclear reasoning steps

This taxonomy provides a useful framework for training error classification models and improving feedback quality in automated grading systems.