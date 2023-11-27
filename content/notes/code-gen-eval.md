---
Title: Code Generation Eval
---

Evaluating various modern OSS models and fine tunes for code generation based on recent SOTA/near-SOTA research methodologies. Some of the concepts include attention mechanisisms like sliding window attention, as well
as grouped-query attention vs multi-head and multi-query.  Evaluation will be observed from various points including non assistive prompting, explanatory prompting, "fill-in" prompting, analogy prompting, and COT prompting. To briefly introduce these terms,
- Non assistive prompting gives no additional information towards the desired result, ie "Write the code for sliding window attention"
- Explanatory prompting provides some context to the desired result ie "Implement the sliding window attention method, a new attention mechanism that exploits the stacked layers of transformers beyond the window size: A token...."
- "Fill-in" prompting can provide some explanatory details but most importantly provides the larger portion of the desired output and the model merely filles in a praticular section while using the surrounding context
- Analogy prompting provides additional assistance by giving some explanation, as well as an analogous example in which the desired outcome is merely an adjustment of the analogy
- COT is typical chain of thought prompting, providing some explanation and describing some of the process, then allowing the model to take multiple steps to build up to the desired output


Still need to figure out best way to track the evals across model variations.  W&B probably? Write out post about using wandb for LLM variation eval and comparison.  Track prompts and responses