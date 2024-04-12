#### Altering the powering order
Table 4 presents the explanation of the performance of Power-Link when we change the order of powering in the path-enforcing module. As suggested by Reviewer 9mi3, this is an experiment we have yet to conduct. Interestingly, increasing the powering order brings better performance and vice versa. Increasing the powering-order strengthens the range of path lengths in the module. This can enable the generation of more explanatory paths that contain more essential nodes. However, it is worth noting that longer paths may be less meaningful to the users, and higher powering orders require more computational power.

#### FB15K-237
| Model             | Order | Fidelity+ | Fidelity- | Avg Sparsity | Hit ΔRank: 1 Path | Hit ΔRank: 3 Paths | Hit ΔRank: 5 Paths |
|-------------------|-------|---------|-----------|----------|--------------|----------------|----------------|
| RGCN-DistMult     | 4     | 0.367 | **0.172** | 0.803    | 0.224        | **0.376**      | **0.440**      |
| RGCN-DistMult     | 2     | 0.172   | 0.175     | **0.954** | 0.200        | 0.296          | 0.350          |
| *RGCN-DistMult    | 3     | **0.377** | 0.186 | 0.784    | **0.234**    | 0.354          | 0.432          |

Table 4: Ablation study on the powering order. The asterisk * indicates the original  results from our paper.

