# DSC 180A Methodology Assignment 4

**Name:** Vani Sahjwani

**Email:** vsahjwani@ucsd.edu

**Section:** D04

**Mentor:** Biwei Huang

---

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic was temporal leakage in forecasting evaluation. WorldReset replays historical data so AI forecasting agents can be tested against known outcomes, which only works if every source is time-gated so the agent sees nothing published after the question's open date. `resolves_by` timestamps must match the publisher's exact scheduled UTC time with no buffer. It showed me that building a trustworthy benchmark is as much a research problem as building a good model.

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

I would like to study how to evaluate forecasting models and agents to find a method that evaluates their efficiency and accuracy. Agents in WorldReset have to search large amounts of time-gated data (news, time series, discussions) before they make a prediction. I want to measure the trade-off between how efficiently an agent searches (number of queries, documents retrieved, compute and cost) and how accurate its forecasts are (Brier score, calibration). The goal is to find strategies that reach near-best accuracy with far less search, and to test whether agent rankings stay consistent when we vary the search budget.

**3. What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would read more of the existing research on forecasting benchmarks and question generation and use it to ground design choices that are currently based on judgment. I would also quantify the methods more. Instead of relying on qualitative review, I would measure each pipeline stage (how many questions validation rejects, how many duplicates deduplication removes, how rubric scores are distributed) and report those numbers. That would make it possible to compare design choices with evidence rather than intuition.

**4. What other techniques would you be interested in using in your project?**

I would be interested in several more technical methods:
- Calibration analysis, such as reliability diagrams and Brier score decomposition into calibration and refinement.
- Bootstrapped confidence intervals and paired significance tests, to tell whether differences between agents are real.
- Retrieval methods for efficient search, such as embedding-based retrieval, reranking and query budgeting.
- LLM-as-a-judge scoring for question quality, validated against human ratings with inter-rater agreement (Cohen's kappa).
- Embedding-based deduplication of questions.
- Item response theory, to estimate how difficult and how discriminating each question is.
