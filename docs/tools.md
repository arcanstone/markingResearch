# Existing Tools and Platforms

This document catalogs current tools and platforms for automated mathematics grading, with links and analysis of their capabilities and limitations.

*To add a new tool: Include linked title, category subtitle, brief description of capabilities and limitations. Group by tool type.*

## OCR and Digitization Tools

### [Mathpix Snip](https://mathpix.com/)
**Commercial OCR Service**  
Converts handwritten/printed mathematical expressions into LaTeX. Widely used to pre‑process student work before feeding into grading systems. Digitisation tool only – does not grade or locate errors. Used in GPT‑4 grading studies because sequence‑to‑sequence models struggle with complex two‑dimensional notation.

## Commercial Grading Platforms

### [Graded.Pro](https://graded.pro/pages/best-ai-grading-tool-for-math)
**AI Grading Platform for K-12 Mathematics**  
Accepts scanned handwritten or typed work. Supports step‑by‑step solutions, equations, graphs and word problems. Teachers upload photos, system provides AI‑generated scores with voice/text annotations. Evidence of accuracy is marketing‑based; does not claim to understand proofs or abstract reasoning.

### [Gradescope](https://elearning.ufl.edu/supported-services/gradescope/)
**University Grading Platform (Turnitin)**  
Upload scanned exams and grade via dynamic rubrics. Uses OCR and AI to group similar answers so instructors can grade one representative and propagate scores. Supports written responses, equations, diagrams and code. Does not automatically detect logical errors—clusters answers based on similarity rather than understanding.

### ScribeSense / Quick Comments / Conker AI
**Multiple-Choice and Short-Answer Systems**  
Commercial products for automated grading of basic mathematics homework. Can scan answer sheets and apply grading rules quickly. Designed for basic calculations or multiple‑choice formats, not suited for long proofs or complex reasoning.

## Specialized Systems

### [Recursive AI Grading Assistant](https://recursiveai.co.jp/case-studies/enhancing-education-efficiency-with-automated-grading)
**Elementary School Math System, Japan 2024**  
Students upload photos of workbook pages; system recognises handwritten numbers, computes correct answers, and applies government scoring guidelines. Trained on large, labelled dataset for high accuracy with basic arithmetic and fixed formats. Limited to elementary arithmetic, not extensible to complex reasoning.

### [Virtual AI Teacher (VATE)](https://arxiv.org/html/2409.09403v1)
**Squirrel AI Dialogue System**  
Analyses student drafts and maintains an "error pool." Engages in multi‑round dialogue to point out mistakes and suggest corrections. Achieved 78.3% accuracy in diagnosing elementary‑level mathematical errors. Shows that combining error tracking with conversational feedback can improve learning.

## Computer Algebra System (CAS) Based Tools

### [STACK](https://stack-assessment.org/)
**Open-Source Online Mathematics Assessment**  
Evaluates answers by algebraic equivalence using the Maxima CAS. Provides specific feedback while separating validation from assessment. Effective for algebraic manipulation but cannot grade reasoning or proofs.

### MapleTA / LON-CAPA
**Legacy CAS Systems**  
Online mathematics assessment systems that verify algebraic equivalence but cannot assess reasoning. Early automated grading systems used CAS to check final answers only.

## Analysis and Limitations

### Current Technical Challenges
1. **OCR Bottleneck**: Complex two‑dimensional mathematical notation remains difficult for automated recognition
2. **Efficiency Over Understanding**: Platforms prioritise grading speed over deep error analysis
3. **Final Answer Focus**: Most tools check equivalence rather than reasoning process
4. **Limited Scalability**: Success with elementary arithmetic doesn't extend to advanced mathematics

### Success Patterns
1. **Well-Defined Tasks**: AI grading works when problems have fixed formats and clear scoring criteria
2. **Human Oversight**: Successful systems maintain teacher control and override capabilities  
3. **Hybrid Approaches**: Combining automated processing with human verification shows promise

### Research Gaps
1. **Handwritten Expression Recognition**: Complex notation processing remains unsolved
2. **Process vs. Product**: Understanding solution methods requires more than answer verification
3. **Advanced Mathematics**: Extending success from arithmetic to subjects like linear algebra proofs