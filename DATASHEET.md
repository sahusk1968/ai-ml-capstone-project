###**Datasheet: BBO Capstone Project Dataset**###

1. **Motivation**
 
**What task does this dataset help to solve?**

This dataset supports a black-box optimisation (BBO) task involving eight unknown objective functions. The purpose of the dataset is to document the full query history and corresponding function evaluations generated across ten optimisation rounds. It enables analysis of optimisation behaviour under strict evaluation constraints and limited feedback.
The dataset supports:

•	Study of exploration–exploitation trade-offs

•	Analysis of convergence behaviour

•	Evaluation of optimisation strategies under budget limits

•	Reproducibility of the capstone optimisation process

**Who created it, and why?**

The dataset was created by the student as part of the BBO capstone project. It was developed to systematically record iterative query submissions and their performance outcomes, enabling structured reflection and transparency in the optimisation process.

**Was it funded or supported by an organisation?**

The dataset was produced for academic purposes within a structured course setting. No external funding was involved.

2. **Composition**

The dataset contains:

•	8 separate unknown objective functions

•	10 query submissions per function

•	A total of 80 evaluated query points

Each data instance includes:

•	Function identifier

•	Round number (1–10)

•	Query vector (2D–8D depending on function)

•	Scalar evaluation score

All query values:

•	Are continuous values in the range [0,1]

•	Are formatted to six decimal places

The dataset represents a **sampled subset** of each function’s search space, not a complete coverage. Later rounds are concentrated around high-performing regions, reflecting exploitation behaviour.
No sensitive personal data, demographic information, or identifiable individuals are included.



