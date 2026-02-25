**Datasheet: BBO Capstone Project Dataset**

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

3. **Collection Process**

The dataset was generated sequentially over ten rounds of optimisation.

Sampling strategy evolved as follows:

•	Rounds 1–3: Broader exploration across the search space

•	Rounds 4–7: Identification of promising regions

•	Rounds 8–10: Reduced step-size refinement and local exploitation

Queries were manually selected based on:

•	Observed performance trends

•	Sensitivity of dimensions

•	Convergence patterns in later rounds

The process was deterministic rather than random in later rounds, as decisions were informed by previous evaluation outcomes.
There were no human subjects involved, and no ethical review was required.

4. **Preprocessing / Cleaning / Labelling**

Minimal preprocessing was required.

•	Query values were constrained to [0,1].

•	Values were standardised to six decimal places for submission formatting consistency.

•	No feature engineering or transformation of evaluation scores was applied.

•	Raw query values and returned scores were preserved.

No labelling process was required, as outputs were directly provided by the black-box evaluation system.

5. **Uses**

**Intended Uses**

This dataset is suitable for:

•	Analysing optimisation strategy evolution

•	Studying convergence behaviour in black-box optimisation

•	Demonstrating iterative refinement under evaluation constraints

•	Educational demonstrations of exploration vs exploitation

**Uses to Avoid**

This dataset should not be used:

•	To claim global optimality of the functions

•	As a benchmark dataset for general optimisation algorithms

•	As representative of all black-box optimisation landscapes

Because the dataset is small and sequentially dependent, it may not generalise to broader optimisation contexts.


6. **Distribution**

The dataset is made available via the project’s public GitHub repository.

Format:

•	Markdown documentation and/or CSV files

Access:

•	Public academic access via GitHub

There are no licensing fees. The dataset is shared for academic transparency and reproducibility.

7. **Maintenance**

The dataset is maintained by the project author.

As the project consists of a fixed ten-round process, no further updates are expected. Version control is handled via GitHub.

If corrections are needed, they will be documented through repository version history.
