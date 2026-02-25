**Model Card: Iterative Black-Box Optimisation Strategy (BBO-10R)**

1. **Basic Details**

**Model name:** Iterative BBO Strategy – 10 Round Refinement

**Version:** v1.0

**Type:** Manual sequential optimisation strategy

**Developer:** Santosh Kumar Sahu

**Task:** Black-box function optimisation (maximisation under evaluation constraints)

**License:** Academic use

**Description**
This model describes a ten-round sequential optimisation strategy applied to eight unknown objective functions in a constrained evaluation environment. The approach balances exploration and exploitation, progressively refining candidate solutions based on observed function outputs.

The strategy is deterministic in later rounds and informed by previous evaluation feedback.

2. **Intended Uses and Limitations**

**Intended Uses**

This optimisation approach is suitable for:

•	Educational black-box optimisation tasks

•	Low-budget evaluation settings

•	Demonstrating exploration–exploitation trade-offs

•	Analysing convergence behaviour across rounds

It is appropriate when:

•	The search space is continuous and bounded ([0,1]^n)

•	Evaluation cost is limited

•	Iterative refinement is possible

**Limitations / Scenarios to Avoid**

This approach should not be used:

•	When global optimality guarantees are required

•	In highly multi-modal landscapes without broader sampling

•	In high-dimensional problems with severe local traps

•	In automated large-scale industrial optimisation

The strategy is manual and heuristic-based rather than algorithmically guaranteed.

3. **Training Data (Adapted to Optimisation Context)**

Since this is not a supervised ML model, there is no traditional training dataset.

Instead, the optimisation strategy uses:

•	Historical query points from previous rounds

•	Corresponding scalar function evaluations

•	Observed performance trends

Each round uses prior evaluation results as “feedback data” to guide subsequent sampling decisions.

The total feedback dataset consists of:

•	80 total function evaluations (10 per function)

4. **Evaluation Metrics**

Performance was evaluated using:

•	Objective function value (primary metric)

•	Relative improvement across rounds

•	Stability of convergence in final iterations

Observed behaviour:

•	Steady improvement from rounds 7–9

•	Reduced step size and local refinement in round 10

•	Concentration of queries near high-performing regions

No fairness metrics were applicable, as no demographic or human-related data were involved.



