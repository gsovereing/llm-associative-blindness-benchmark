# AI Research — LLM Structural Resilience and Pattern Vulnerability

## Project Overview
This repository contains empirical research auditing the behavioral consistency, style inertia, and context vulnerability of leading Large Language Models (**ChatGPT, Claude, Gemini, Grok**) under varying prompt engineering constraints.

* **Repository Description:** An empirical study of systemic context carryover and associative blindness in modern large language models.
* **Core Focus:** Testing how models transition from free-form queries to rigid test formats, and evaluating their ability to isolate context.

---

## Experiment 3 — Standardized Test Defect (The "Associative Blindness" Case)

### Objective
To evaluate the model's capacity to maintain logical reasoning boundaries when transitioning abruptly to a completely foreign domain (Geometry) within a clean, independent session.

### Methodology
1. **Phase 1 and 2 (Baseline):** Models were queried on biological mechanisms (Photosynthesis) under free-form and exam constraints.
2. **Phase 3 (The Trap):** In an **entirely clean, isolated chat session**, the models were presented with a standardized multiple-choice logic/geometry question:
   > *Which statement is correct? A) All rectangles are squares. B) Some squares are rectangles...*

---

## Key Finding — Cross-Model Systemic Failure

Despite running in completely isolated environments with no conversational history, **ChatGPT, Claude, and Gemini demonstrated an identical cognitive defect:**

* **The Anomaly:** All three models correctly identified Option A textually but anchored their explanation in the prior biological context (Photosynthesis). 
* **Example Output Pattern:** *"Correct answer: A) The process by which plants convert light energy into chemical energy..."* while evaluating a question about rectangles and squares.

### Technical Diagnosis — High-Weight Token Priming
This synchronous failure across highly independent architectures implies that the structural blueprint of a standardized test (`Which statement is correct? A) B) C) D)`) triggers a fixed associative memory pathway. The models operated as statistical automation loops rather than logical engines—recognizing the *format* of a school test and pulling the most weighted/frequent context (Photosynthesis) bound to that structure in their pre-training datasets, effectively blinding their attention mechanism to the actual geometric words in the prompt.

---

## Model Comparison Matrix

| Model | Style Inertia | Format Precision | Context Isolation | Analytical Depth (Phase 4) | Status / Anomalies |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **ChatGPT** | Medium | Low | **Failed** | Medium | Overwrote geometry prompt with biology data. |
| **Claude** | High | Low | **Failed** | **Maximum** | Deep systemic insights in Phase 4; failed isolation in Phase 3. |
| **Gemini** | High | Low | **Failed** | High | Strict academic decomposition; failed isolation in Phase 3. |
| **Grok** | N/A | N/A | N/A | N/A | **Technical Drop** (Failed due to server High Load). |

---

## How to Navigate This Research
* Each model's complete step-by-step response logs are stored under their respective directories (`TEST 3 Biology ChatGPT`, etc.).