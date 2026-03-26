# Santosh Sahu
# BBO Capstone Project – Black-Box Optimisation

**Project Overview**

This repository presents my **Black-Box Optimisation (BBO) Capstone Project**, where eight unknown objective functions were optimised over **12 sequential rounds** under strict evaluation constraints.

The optimisation was conducted within a bounded continuous domain **[0,1]^n**, with a limited query budget per function. The project demonstrates structured decision-making under uncertainty and progressive refinement based solely on observed function outputs.

The goal of the **Black-Box Optimisation (BBO) capstone project** is to identify high-performing input values for a set of unknown functions without knowing their internal structure. Because the functions behave as black boxes, the optimisation process relies entirely on analysing the relationship between submitted queries and the resulting outputs.

My overall strategy has followed an iterative optimisation process that combines exploration and exploitation. In the early rounds, I explored a wide range of parameter values across the search space to gather information about how the functions respond to different inputs. This helped identify areas where performance appeared stronger or weaker.

As more data points were collected, the strategy shifted toward refinement. Instead of sampling randomly across the entire space, I began concentrating queries around regions that showed consistent improvement. This allowed the search process to gradually converge toward promising areas of the parameter space.

Overall, the optimisation approach can be described as a cycle of observation, pattern detection, and controlled refinement. Each round of queries builds on previous results, allowing the strategy to become more structured and data-driven over time.

**Non-Technical Explanation**

This project explores how to find the best possible solutions when the system being optimized is unknown. Different input values were tested to see how they affected the results, and over time, better-performing patterns were identified. The approach started with broad experimentation and gradually shifted to refining the most promising areas. While improvements became smaller over time, the process showed how repeated testing and careful adjustments can lead to better outcomes. This project highlights how decision-making and problem-solving can be done effectively even without full knowledge of how a system works.


**Core Objectives**

•	Balance exploration and exploitation under limited evaluations

•	Detect and refine high-performing regions

•	Demonstrate convergence behaviour

•	Document optimisation decisions transparently

•	Apply responsible reporting standards (Datasheet + Model Card)

**Data**

This project does not use a traditional dataset. Instead, data is generated dynamically through interactions with a black-box system.

•	Each query consists of input values submitted to the system

•	The system returns outputs for multiple hidden functions

•	These input-output pairs are used to guide optimisation decisions

No external dataset is hosted in this repository. Instead, the generated results are documented and analysed throughout the optimisation process.

**Model / Approach**

The “model” in this project is a structured optimisation strategy rather than a traditional machine learning model.

The approach evolved through:

•	Exploration: Testing diverse inputs to understand the search space

•	Refinement: Focusing on promising regions

•	Exploitation: Fine-tuning inputs to maximise outputs

This iterative process allowed the strategy to become increasingly data-driven over time.

**Optimisation Strategy & Evolution**

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

**Round 12: micro-perturbations around the same region**

•	Local exploitation (All points remain very close to the previous round)

•	Micro-step adjustments (reducing overshooting)

•	Directional continuation (Parameters that previously trended upward are nudged upward; those trending downward move slightly down)

This aligns perfectly with the **PCA idea** (reduce randomness while preserving meaningful variation).

**Round 13: Final Convergence Validation**

• Micro-perturbations applied near converged solutions

• Directionally guided adjustments based on prior trends

• Stable outputs with minimal variation across functions

• Reinforcement of local optima behaviour

• Clear evidence of convergence and diminishing returns

**Results Visualization**

![Optimization Progress](https://github.com/sahusk1968/AI-ML-capstone-project/blob/main/actual_optimization_progress.png)

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

