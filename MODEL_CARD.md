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




