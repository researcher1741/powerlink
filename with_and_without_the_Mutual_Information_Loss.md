#### with/without path-enforcing module

We test the impact of the mutual information loss(MIL) in Table 2, explaining the WGCN-Distmult model. Without the loss of mutual information, there is a significant drop in the explanation performance. This behaviour is bound to happen since the MIL is the critical component that enables the explanation method to adjust the weighted mask of the KG according to the prediction of the KGC model. Without the MIL, the path-enforcing module only strengthens the edges on the paths between the head and tail nodes without considering their impacts on the model's prediction. In other words, the method is not explained without the MIL.

##### FB15K-237
| Model               | Fidelity+ | Fidelity- | Avg Sparsity | Hit ΔRank: 1 Path | Hit ΔRank: 3 Paths | Hit ΔRank: 5 Paths |
|---------------------|-----------|-----------|--------------|-------------------|--------------------|--------------------|
| WGCN-DistMult-PS    | 0.013     | 0.021     | 0.938        | 0.168             | 0.220              | 0.238              |
| *WGCN-DistMult      | **0.646** | **0.294** | **0.672**    | **0.629**         | **0.772**          | **0.836**          |

Table 3: Ablation study on mutual information loss. -PS indicates that only path-searching loss is used during the explanation(without mutual information loss). The asterisk * indicates the original results from our paper. 