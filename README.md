# The-Perplexity-Permutation-Puzzle

## Objective
The "Santa 2024 - The Perplexity Permutation Puzzle" is a Kaggle competition designed to challenge participants with a unique optimization task involving large language models (LLMs). The objective of the competition is to minimize the perplexity of word sequences by rearranging the words into an optimal order. The better your model predicts the word sequence, the lower the perplexity score. This serves as a proxy for determining the fluency and naturalness of the text.

## Key Challenges
* Optimization Complexity: The factorial growth of permutations makes brute force infeasible, requiring innovative optimization techniques such as simulated annealing, genetic algorithms, or heuristic methods.
* Perplexity Evaluation: Understanding how LLMs calculate perplexity and effectively integrating this metric into your optimization pipeline.
* Resource Constraints: Balancing computational efficiency with the need to evaluate a large number of permutations.
  
## Simulated Annealing Approach
Starting with a high temperature, the formula math.exp(-delta/temp) encourages the algorithm to explore more adventurous possibilities, even accepting word arrangements that are up to 20% worse than the current best. As the temperature decreases, the algorithm becomes exponentially more selective, balancing exploration with a focused search to escape local minima and progressively identify better sequences.
When invalid arrangements (NaN scores) are encountered, they are skipped, and the algorithm continues testing other word swaps. This iterative process refines the sequence, guided by the language model’s perplexity scores, to uncover increasingly natural and fluent word combinations.
