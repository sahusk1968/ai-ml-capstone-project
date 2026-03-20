**Model Card: Iterative Black-Box Optimisation Strategy (BBO-12R)**

1. **Basic Details**

**Model name:** Iterative BBO Strategy – 11 Round Refinement

**Version:** v1.1

**Type:** Manual sequential optimisation strategy

**Developer:** Santosh Kumar Sahu

**Task:** Black-box function optimisation (maximisation under evaluation constraints)

**License:** Academic use

**Description**
This model describes a thirteen-round sequential optimisation strategy applied to eight unknown objective functions in a constrained evaluation environment. The approach balances exploration and exploitation, progressively refining candidate solutions based on observed function outputs.

The strategy is deterministic in later rounds and informed by previous evaluation feedback.

2. **Intended Uses and Limitations**

**Intended Uses**

This optimisation approach is suitable for:

•	Educational black-box optimisation tasks

•	Low-budget evaluation settings

•	Demonstrating exploration–exploitation trade-offs

•	Studying convergence dynamics in iterative optimisation

•	Analysing clustering behaviour in continuous search spaces

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

The strategy is manual and heuristic-based rather than algorithmically guaranteed. It does not incorporate probabilistic modelling, surrogate modelling, or formal optimisation guarantees.

3. **Training Data (Adapted to Optimisation Context)**

Since this is not a supervised ML model, there is no traditional training dataset.

Instead, the optimisation strategy uses:

•	Historical query points from previous rounds

•	Corresponding scalar function evaluations

•	Observed performance trends

Each round uses prior evaluation results as “feedback data” to guide subsequent sampling decisions.

The total feedback dataset consists of:

•	96 total function evaluations (12 per function)

•	Sequentially dependent query–response pairs

The feedback data is cumulative and path-dependent, meaning later decisions are influenced by earlier sampling behaviour.

4. **Evaluation Metrics**

Performance was evaluated using:

•	Objective function value (primary metric)

•	Relative improvement across rounds

•	Stability of convergence in final iterations

•	Evidence of convergence or plateau behaviour

Observed behaviour:

•	Increasing performance stability from Rounds 7–10

•	Reduced perturbation magnitude in Round 10

•	Round 11 micro-adjustment within dominant high-performing clusters

Round 12 Local exploitation, Micro-step adjustments and Directional continuation which aligns perfectly with the **PCA idea** (reduce randomness while preserving meaningful variation).

•	Clear shift from exploration-dominant to exploitation-dominant strategy

No fairness metrics were applicable, as no demographic or human-related data were involved.

5. **Optimisation Strategy Details**

**Rounds 1–3: Exploration Phase**

•	Broad coverage of the search space

•	Large step-size variation

•	Identification of promising regions

**Rounds 4–7: Region Identification**

•	Movement toward higher-performing areas

•	Reduced variation in weaker dimensions

•	Emerging cluster formation

**Rounds 8–10: Exploitation & Convergence**

•	Fine-grained parameter adjustments

•	Reduced step size

•	Increased density of queries within promising regions

•	Evidence of stabilisation and diminishing variance

**Round 11: Cluster-Based Micro-Refinement**

•	Centroid-oriented adjustments within dominant clusters

•	Minimal perturbations to test local smoothness

•	Convergence-sensitive tuning rather than expansion

•	Reinforcement of density within high-performing basins

**Round 12: micro-perturbations around the same region**

• Local exploitation (All points remain very close to the previous round)

• Micro-step adjustments (reducing overshooting)

• Directional continuation (Parameters that previously trended upward are nudged upward; those trending downward move slightly down)

This aligns perfectly with the **PCA idea** (reduce randomness while preserving meaningful variation).

**Core Principle:**

A deliberate transition from high-variance exploration to density-guided exploitation and convergence refinement.


6. **Assumptions and Limitations**

**Key Assumptions**

.	The objective functions exhibit some degree of local smoothness.

•	High-performing regions remain stable under small perturbations.

•	Observed multi-round trends provide meaningful signal for refinement.

•	Convergence behaviour indicates proximity to a local optimum.

**Significant Limitation**

•	Limited sampling budget (11 points per function).

•	Large portions of the search space remain unexplored.

•	Risk of convergence to local rather than global optima.

•	No uncertainty quantification or probabilistic confidence estimates.

•	Manual, heuristic nature reduces scalability without detailed documentation.

The optimisation path is sequentially dependent and may not be reproducible without identical evaluation feedback.

7. **Ethical Considerations**

Although the model does not involve human data, responsible documentation remains important.

**Transparency**

•	Full query history and reasoning are documented.

•	Strategy evolution is explicitly described.

**Reproducibility**

•	Sequential decisions are traceable to previous round outcomes.

•	Repository version control preserves iteration history.

**Risk Awareness**

•	The model does not claim global optimality.

•	Results are context-specific to this controlled academic setting.

•	No claims are made regarding universal performance.

This documentation promotes responsible reporting and avoids overstating optimisation outcomes.

8. **Distribution**

The model card and supporting dataset are available in the public GitHub repository for the BBO capstone project.

The repository includes:

•	Datasheet (DATASHEET.md)

•	Model card (MODEL_CARD.md)

•	Query history (Query_history_and Results.md)

•	README documentation

