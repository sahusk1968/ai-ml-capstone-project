# Santosh Sahu
# BBO Capstone Project – Black-Box Optimisation

**Project Overview**

This repository presents my **Black-Box Optimisation (BBO) Capstone Project**, where eight unknown objective functions were optimised over **11 sequential rounds** under strict evaluation constraints.

The optimisation was conducted within a bounded continuous domain **[0,1]^n**, with a limited query budget per function. The project demonstrates structured decision-making under uncertainty and progressive refinement based solely on observed function outputs.

**Core Objectives**

•	Balance exploration and exploitation under limited evaluations

•	Detect and refine high-performing regions

•	Demonstrate convergence behaviour

•	Document optimisation decisions transparently

•	Apply responsible reporting standards (Datasheet + Model Card)

**Optimisation Summary**

**Component	Value**

Objective Functions	8 (unknown black-box functions)

Optimisation Rounds	11

Total Evaluations	88

Search Space	Continuous [0,1]^n

Strategy Type	Manual, sequential, feedback-driven

**Strategy Evolution**

The optimisation process followed a structured progression:

**Rounds 1–3: Exploration**

•	Broad coverage of search space

•	High step-size variation

•	Identification of promising directions

**Rounds 4–7: Region Identification**

•	Movement toward high-performing regions

•	Reduced variation in weak dimensions

•	Emerging performance clustering

**Rounds 8–10: Exploitation & Convergence**

•	Fine-grained parameter adjustments

•	Step-size reduction

•	Density increase near top-performing points

**Round 11: Cluster-Based Micro-Refinement**

•	Centroid-oriented tuning

•	Minimal perturbations to test local smoothness

•	Convergence-sensitive optimisation

Performance improved steadily in mid-to-late rounds, followed by stabilisation and controlled refinement — consistent with convergence behaviour.


**Documentation**

This repository includes:

•	📄 Datasheet → [DATASHEET.md](https://github.com/sahusk1968/AI-ML-capstone-project/blob/main/DATASHEET.md)

Documentation of the query history dataset following Mini-lesson 21.1.

•	📘 Model Card → [MODEL_CARD.md](https://github.com/sahusk1968/AI-ML-capstone-project/blob/main/MODEL_CARD.md)

Documentation of the optimisation strategy following Mini-lesson 21.2.

These documents promote transparency, reproducibility and responsible reporting.

⚖️ Ethical and Transparency Statement

•	All optimisation decisions are documented.

•	No human or demographic data were used.

•	No claims of global optimality are made.

•	The strategy and assumptions are clearly stated.

👤 Author

**Santosh Kumar Sahu**

**BBO Capstone Project**

