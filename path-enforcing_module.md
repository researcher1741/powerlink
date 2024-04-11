#### with/without path-enforcing module

As shown in Table 1, we observed a noticeable drop in path explanation performance when the path-enforcing module was removed. This behaviour is expected since there is no strengthening on the impact of paths when explanations are generated without path-enforcing. We expect the gap to be more significant for denser graphs.


##### FB15K-237
| Model                 | Fidelity+ | Fidelity- | Avg Sparsity | Hit ΔRank: 1 Path | Hit ΔRank: 3 Paths | Hit ΔRank: 5 Paths |
|-----------------------|-----------|-----------|--------------|-------------------|--------------------|--------------------|
| RGCN-DistMult-MI      | 0.356     | 0.168     | 0.834        | 0.173             | 0.308              | 0.396              |
| WGCN-DistMult-MI      | 0.325     | 0.397     | 0.640        | 0.599             | 0.683              | 0.739              |
| CompGCN-DistMult-MI   | 0.0411    | 0.0299    | 0.6556       | 0.072             | 0.126              | 0.194              |
| *RGCN-DistMult        | 0.377     | 0.186     | 0.784        | 0.234             | 0.354              | 0.432              |
| *WGCN-DistMult        | 0.646     | 0.294     | 0.672        | 0.629             | 0.772              | 0.836              |
| *CompGCN-DistMult     | 0.043     | 0.025     | 0.506        | 0.092             | 0.170              | 0.220              |
