# Existing Tools for Automated Mathematics Grading

This document catalogs the current landscape of tools and platforms for automated mathematics grading, from OCR services to full grading platforms.

## OCR and Digitization Tools

### Mathpix Snip
- **Purpose**: Commercial OCR service that converts handwritten/printed mathematical expressions into LaTeX
- **Use Case**: Widely used to pre‑process student work before feeding it into grading systems
- **Limitations**: 
  - Digitisation tool only – does not grade or locate errors
  - Sequence‑to‑sequence HME‑recognition models struggle with complex two‑dimensional notation
  - Used in GPT‑4 grading studies because other models perform poorly on complex expressions

## Commercial Grading Platforms

### Graded.Pro
- **Target Audience**: Middle‑ and high‑school mathematics
- **Features**:
  - Accepts scanned handwritten or typed work
  - Supports step‑by‑step solutions, equations, graphs and word problems
  - Teachers upload photos, system provides AI‑generated scores and voice/text annotations
  - Teachers can override scores
- **Limitations**:
  - Evidence of accuracy is marketing‑based
  - Does not claim to understand proofs or abstract reasoning
  - Emphasises teacher control over automated analysis

### Gradescope (Turnitin)
- **Target Audience**: Universities and higher education
- **Features**:
  - Upload scanned exams and grade via dynamic rubrics
  - Uses OCR and AI to group similar answers
  - Instructors grade one representative and propagate the score
  - Supports written responses, mathematical equations, diagrams and code
  - Automatic grouping of similar answers, dynamic rubrics and analytics
- **Limitations**:
  - Does not automatically detect logical errors
  - Clusters and scores answers based on similarity rather than understanding
  - Accelerates grading but doesn't assess reasoning process

### ScribeSense / Quick Comments / Conker AI
- **Purpose**: Automated grading of multiple‑choice or short‑answer mathematics homework
- **Features**: Can scan answer sheets and apply grading rules quickly
- **Limitations**: 
  - Public descriptions emphasise time savings but provide few technical details
  - Designed for basic calculations or multiple‑choice formats
  - Not suited for long proofs or complex reasoning

## Specialized Systems

### Recursive AI Grading Assistant
- **Context**: Custom AI grading system developed in Japan (2024)
- **Target**: Elementary‑school mathematics
- **Process**:
  - Students upload photos of workbook pages
  - System recognises handwritten numbers
  - Computes correct answer and applies government scoring guidelines
  - Returns instant scores
- **Success Factors**:
  - Trained on large, labelled dataset
  - Strict adherence to scoring formats
  - Demonstrates feasibility when problems involve basic arithmetic and fixed formats
- **Limitations**: Limited to elementary arithmetic, not extensible to complex reasoning

### Virtual AI Teacher (VATE)
- **Developer**: Squirrel AI
- **Approach**: 
  - Analyses student drafts and maintains an "error pool"
  - Engages in multi‑round dialogue to point out mistakes
  - Suggests corrections through conversational feedback
- **Performance**: 78.3% accuracy in diagnosing elementary‑level mathematical errors
- **Innovation**: Shows that combining error tracking with conversational feedback can improve learning

## Computer Algebra System (CAS) Based Tools

### STACK
- **Type**: Open‑source system for online mathematics assessment
- **Mechanism**: 
  - Evaluates answers by algebraic equivalence using the Maxima CAS
  - Provides specific feedback while separating validation from assessment
- **Strengths**: Effective for algebraic manipulation
- **Limitations**: Cannot grade reasoning or proofs

### Other CAS Systems (MapleTA, LON‑CAPA)
- **Purpose**: Online mathematics assessment
- **Approach**: Verify algebraic equivalence but cannot assess reasoning
- **Historical Context**: Early automated grading systems used CAS to check final answers

## Key Observations

### Current Limitations
1. **OCR remains a bottleneck** for complex mathematical notation
2. **Efficiency over analysis**: Current platforms prioritise grading speed over deep error understanding
3. **Final answer focus**: Most tools check equivalence rather than reasoning process
4. **Limited complexity**: Systems work well for elementary arithmetic but struggle with advanced mathematics

### Success Patterns
1. **Well-defined tasks**: AI grading can be reliable when problems have fixed formats and clear scoring criteria
2. **Human oversight**: Most successful systems maintain teacher control and override capabilities
3. **Hybrid approaches**: Combining automated processing with human verification shows promise

### Technical Challenges
1. **Handwritten expression recognition**: Complex two‑dimensional mathematical notation remains difficult
2. **Reasoning vs. answers**: Understanding solution processes requires more than final answer verification
3. **Scalability**: Extending elementary arithmetic success to advanced mathematics like linear algebra proofs