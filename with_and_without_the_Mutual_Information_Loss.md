#### with/without path-enforcing module
As shown in Table 1, we observed a noticeable drop in path explanation performance when the path-enforcing module was removed. This is as expected since there is no strengthening of the impact of paths when explanations are generated without path-enforcing. We expect the gap to be more significant for denser graphs.

##### FB15K-237
| Model               | Fidelity+ | Fidelity- | Avg Sparsity | Hit ΔRank: 1 Path | Hit ΔRank: 3 Paths | Hit ΔRank: 5 Paths |
|---------------------|-----------|-----------|--------------|-------------------|--------------------|--------------------|
| WGCN-DistMult-PS    | 0.013     | 0.021     | 0.938        | 0.168             | 0.220              | 0.238              |
| *WGCN-DistMult      | **0.646** | **0.294** | **0.672**    | **0.629**         | **0.772**          | **0.836**          |
Table 1: Ablation study on the path-enforcing module. -MI indicates the model can only be explained with mutual information loss. The asterisk * indicates the original results from our paper.