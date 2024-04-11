#### Combination methods in the TES scorer
As in Table 2, it can be found that using the Euclidean combination method yields better explanation performance than Concatenation on RGCN-based KGC models. The superiority is more explicit in RGCN-TransE, which uses the energy-based loss function during KGC training. On the contrary, Euclidean downgrades the performance of WGCN-based KGC models. Due to this inconsistent performance, we used Concatenation for TES in the experiments. Nonetheless, we find this phenomenon interesting to explore, and we would like to leave it for future work, e.g. What leads to the variation of explanation performance for different GNN-based KGC models?

#### FB15K-237

| Dataset              | Model                   | Fidelity+ | Fidelity- | Avg Sparsity | Hit ΔRank: 1 Path | Hit ΔRank: 3 Paths | Hit ΔRank: 5 Paths |
|----------------------|-------------------------|----------|-----------|--------------|-------------------|--------------------|--------------------|
| FB15K-237            | RGCN-TransE-euc         |**0.711** | 0.204     |**0.906**     | **0.480**         | **0.640**          | **0.717**          |
| FB15K-237            | RGCN-DistMult-euc      | 0.266     | **0.133** | 0.763        | **0.334**         | **0.455**          | **0.468**          |
| FB15K-237            | RGCN-ConvE-euc         | 0.189    | 0.206     | **0.936**        | **0.444**             | **0.542**              | **0.590**              |
| FB15K-237            | WGCN-TransE-euc        | 0.761    | **0.444**     | 0.648        | **0.382**             | 0.538              | **0.656**              |
| FB15K-237            | WGCN-DistMult-euc      | 0.628    | 0.375     | 0.580        | 0.594             | 0.737              | 0.822              |
| FB15K-237            | WGCN-ConvE-euc         | **0.794**   | 0.377     | 0.581        | 0.416             | **0.650**              | 0.726              |
| FB15K-237            | *RGCN + TransE-concat  | 0.699    | **0.088**     | 0.531        | 0.074             | 0.174              | 0.234              |
| FB15K-237            | *RGCN + DistMult-concat|**0.377**    | 0.186     | **0.784**        | 0.234             | 0.354              | 0.432              |
| FB15K-237            | *RGCN + ConvE-concat   | **0.435**   | **0.111**     | 0.832        | 0.190             | 0.326              | 0.396              |
| FB15K-237            | *WGCN + TransE-concat  | **0.775**   | **0.150**     | **0.753**        | 0.376             | **0.582**              | 0.648              |
| FB15K-237            | *WGCN + DistMult-concat| 0.646    | **0.294**     | **0.672**        | **0.629**             | **0.772**              | **0.836**              |
| FB15K-237            | *WGCN + ConvE-concat   | 0.416    | **0.287**     | **0.720**        | **0.474**             | 0.646              | **0.762**              |
